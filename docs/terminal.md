# Lauren no terminal

Aqui ela para de dar conselho e passa a fazer. Ela lê os arquivos do servidor,
roda comando, edita configuração, reinicia serviço — e mostra cada passo.

## Instalar

Abra a aba **Code** no site: o comando aparece pronto, com um convite dentro
dele. Rode no terminal da VPS, como root:

```bash
curl -fsSL https://ialauren.com/instalar.sh | sudo bash -s SEU_CONVITE
```

O convite vale 30 minutos e serve uma vez só. Se vencer, recarregue a página
para pegar outro.

Funciona em Ubuntu, Debian, Rocky e Alma. Leva menos de um minuto.

### Sobre o acesso de administrador

Por padrão ela instala com poder de administrador. É o que faz ela ser útil:
sem isso, ela lê o log e diz "reinicie o nginx", em vez de reiniciar.

Se você prefere o contrário, instale limitada — ela lê, mas não mexe:

```bash
curl -fsSL https://ialauren.com/instalar.sh | bash -s -- SUA_CHAVE --sem-root
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

### Abra ela dentro do projeto

O `cd` que você dá antes vale: a Lauren trabalha na pasta em que foi aberta.

```bash
cd /var/www/meusite
lauren
```

Ela lê e mexe nessa pasta sem pedir nada. Para tocar em coisa de fora dela —
um `/etc/nginx/`, um serviço do sistema — ela pede autorização.

**E cada pasta guarda as conversas dela.** O `/resume` aberto em
`/var/www/meusite` lista o que você conversou ali, não a bagunça das outras.
Trocar de projeto é trocar de pasta.

### Autorizando

Quando ela vai rodar algo, aparece assim:

```
  ⚠  Ela quer executar:
     systemctl restart nginx

     [Enter] deixar   [n] não deixar
```

Enter deixa passar; **n** nega, e ela tenta outro caminho.

Ler arquivo e listar pasta ela faz direto, sem perguntar — o que para para
pedir é o que muda alguma coisa.

### Comandos

Digite `/` e a lista aparece na hora, filtrando conforme você escreve.

| Comando | O que faz |
|---|---|
| `/rc` | liga o controle remoto: esta conversa vai para o site e o celular |
| `/fechar` | desliga o remoto e volta a ser só deste terminal |
| `/resume` | lista as conversas desta pasta e entra numa |
| `/renomear` | dá outro nome para esta conversa |
| `/parar` | interrompe uma rodada que travou |
| `/ajuda` | mostra a lista |
| `/sair` | encerra |

`/remote control` faz o mesmo que `/rc`, para quem prefere escrever por extenso.

### Voltar direto numa conversa

Se você já sabe qual quer, dá para abrir nela sem passar pelo `/resume`:

```bash
lauren --sessao ses_abc123
```

E dá para já chegar perguntando:

```bash
lauren --sessao ses_abc123 "por que o nginx caiu de novo?"
```

Serve também por variável de ambiente, para quem chama a Lauren de dentro de
um script: `LAUREN_SESSAO=ses_abc123 lauren`.

## Print e áudio: o que o terminal não faz

Terminal não recebe imagem. Mas é justamente o print do painel, a foto da tela
de erro ou um áudio explicando que fazem ela entender o problema rápido.

Por isso existe o `/rc`:

1. No terminal, digite `/rc`
2. Abra **[ialauren.com/code](https://ialauren.com/code)** (ou o
   app no celular)
3. A mesma conversa está lá — mande o print por ali
4. A resposta aparece nos dois lugares

Quando terminar, `/fechar`. Enquanto você não pedir `/rc`, sua máquina não
aparece em lugar nenhum.

## Tirar do ar

```bash
sudo systemctl stop lauren-conector
sudo systemctl disable lauren-conector
```

E remova a máquina na aba **Code** do site, nos três pontinhos ao lado do nome dela.

## Quando não funciona

**`lauren` não faz nada / não existe**
Saia e entre no terminal de novo (o `PATH` mudou na instalação).

**"Essa máquina está offline"**
```bash
sudo systemctl status lauren-conector
sudo journalctl -u lauren-conector -n 50
```

**A conversa não aparece no site**
Você precisa digitar `/rc` no terminal primeiro — é assim de propósito: sua
máquina não fica exposta sem você mandar.

**O `/resume` não acha uma conversa antiga**
Ela está na pasta em que você a começou. Dê `cd` para lá e chame de novo.

**"Sua cota acabou"**
Veja [como funciona o consumo](consumo.md).
