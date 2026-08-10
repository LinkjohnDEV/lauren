# Lauren no terminal

Aqui ela para de dar conselho e passa a fazer. Ela lê os arquivos do servidor,
roda comando, edita configuração, reinicia serviço — e mostra cada passo.

Disponível nos planos **PRO** e **MAX**.

## Instalar

Pegue sua chave em **Configurações → Conta** no site e rode:

```bash
curl -fsSL https://lauren.linkjohn.com/instalar.sh | bash -s -- SUA_CHAVE
```

Funciona em Ubuntu, Debian, Rocky e Alma. Leva menos de um minuto.

### Sobre o acesso de administrador

Por padrão ela instala com poder de administrador. É o que faz ela ser útil:
sem isso, ela lê o log e diz "reinicie o nginx", em vez de reiniciar.

Se você prefere o contrário, instale limitada — ela lê, mas não mexe:

```bash
curl -fsSL https://lauren.linkjohn.com/instalar.sh | bash -s -- SUA_CHAVE --sem-root
```

Nos dois modos, **ela pede autorização antes de cada comando**. Você vê o
comando inteiro antes de dizer sim.

## Usar

```bash
lauren
```

Escreva o que precisa, em português:

```
› o site está fora do ar, descubra o porquê
› o disco encheu, veja o que está ocupando
› instale o certbot e coloque HTTPS no meu domínio
› por que o mysql não sobe depois do reboot?
```

### Autorizando

Quando ela vai rodar algo, aparece assim:

```
  A Lauren quer rodar
  systemctl restart nginx

  [s] autorizar   [a] sempre   [n] não
```

- **s** — autoriza esse comando, uma vez
- **a** — autoriza esse tipo de comando pelo resto da conversa
- **n** — nega; ela tenta outro caminho

### Comandos

| Comando | O que faz |
|---|---|
| `/code` | espelha esta conversa no site — é assim que você manda print e áudio |
| `/fechar` | para de espelhar |
| `/resume` | lista as conversas anteriores e volta para uma delas |
| `/parar` | interrompe o que ela está fazendo agora |
| `/ajuda` | mostra os comandos |
| `/sair` | sai |

## Print e áudio: o que o terminal não faz

Terminal não recebe imagem. Mas é justamente o print do painel, a foto da tela
de erro ou um áudio explicando que fazem ela entender o problema rápido.

Por isso existe o `/code`:

1. No terminal, digite `/code`
2. Abra **[lauren.linkjohn.com/code](https://lauren.linkjohn.com/code)** (ou o
   app no celular)
3. A mesma conversa está lá — mande o print por ali
4. A resposta aparece nos dois lugares

Quando terminar, `/fechar`. Enquanto você não pedir `/code`, sua máquina não
aparece em lugar nenhum.

## Tirar do ar

```bash
sudo systemctl stop lauren-conector
sudo systemctl disable lauren-conector
```

E revogue a chave em **Configurações → Conta** no site.

## Quando não funciona

**`lauren` não faz nada / não existe**
Saia e entre no terminal de novo (o `PATH` mudou na instalação).

**"Essa máquina está offline"**
```bash
sudo systemctl status lauren-conector
sudo journalctl -u lauren-conector -n 50
```

**A conversa não aparece no site**
Você precisa digitar `/code` no terminal primeiro — é assim de propósito: sua
máquina não fica exposta sem você mandar.

**"Sua cota acabou"**
Veja [como funciona o consumo](consumo.md).
