# Lauren

**A IA que entra no seu servidor e conserta.**

São duas da manhã e o site caiu. Você não quer ler sobre `journalctl` — quer o
serviço no ar.

```
você     meu site tá fora do ar

Lauren   Vou olhar agora. Posso rodar isto na sua VPS?

         ›  systemctl status nginx

         [ Autorizar ]   [ Agora não ]

você     ✓ autorizado

Lauren   O nginx caiu às 02:14 por falta de espaço: o log do PHP encheu
         38 GB dos 40. Limpo o log e subo o serviço?
```

Ela lê, decide e executa — **pedindo autorização antes de cada comando que muda
alguma coisa.** Você vê exatamente o que ela vai fazer antes de ela fazer.

**[Conhecer a Lauren →](https://ialauren.com)**

---

## O que ela faz

- **Resolve no servidor.** Entra na sua VPS, lê o log, corrige a configuração,
  reinicia o serviço. E no seu Windows também, com um clique.
- **Enxerga o que você manda.** Print da tela de erro, PDF, planilha, áudio.
  Arraste na conversa e pergunte.
- **Desenha.** Peça um cartaz, um logo, um banner para a sua promoção, e ela
  entrega a imagem pronta na conversa.
- **Fala português.** De verdade — não é tradução de manual gringo.

## Onde ela trabalha

No navegador, no iPhone, no Android, no Windows e dentro do VS Code. **A
conversa é a mesma nos cinco:** o que você começa no computador continua no
celular, com o mesmo histórico.

No celular ela instala na tela inicial e abre como aplicativo, sem passar pela
loja.

**[Baixar →](https://ialauren.com/app)**

---

## Planos

| | PRO | MAX | ULTRA |
|---|:---:|:---:|:---:|
| Conversa, leitura de arquivo e aplicativos | ✅ | ✅ | ✅ |
| **Lauren dentro da sua VPS e do seu PC** | ✅ | ✅ | ✅ |
| Imagens por mês | 50 | 150 | 300 |
| **Lauren 6**, a mais capaz de todas | — | ✅ | ✅ |
| Quanto dá para usar | trabalhar todo dia | 3× o PRO | o dobro do MAX |
| | **R$ 79,90** | **R$ 199,90** | **R$ 399,90** |

Por mês, no PIX. **Sem fidelidade e sem renovação automática** — quando acabar,
acabou, e você renova se quiser.

📖 **[Como funciona o consumo →](docs/consumo.md)**

---

## Instalar na VPS

Abra a aba **Code** no site, copie o comando com o seu convite e rode **dentro
do servidor**, como root:

```bash
curl -fsSL https://ialauren.com/instalar.sh | sudo bash -s SEU_CONVITE
```

Ubuntu, Debian, Rocky e Alma. Leva menos de um minuto. Depois é só chamar:

```bash
lauren
```

📖 **[Manual do terminal →](docs/terminal.md)** · 📖 **[Perguntas frequentes →](docs/perguntas.md)**

---

## Fora do ar?

**[ialauren.com/status](https://ialauren.com/status)** mostra o estado de cada
parte agora, e o histórico. Se o problema for nosso, está lá — e você não perde
tempo procurando erro do seu lado.

Precisa de gente? Abra uma
[issue](https://github.com/LinkjohnDEV/lauren/issues) ou fale pelo próprio site.

<sub>Lauren é um produto <a href="https://linkjohn.com">LinkJohn</a>.</sub>
