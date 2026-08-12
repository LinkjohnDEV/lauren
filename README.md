# Lauren

**Uma IA que já vem com a sua VPS.** Você conversa com ela no navegador, no
celular ou no computador — e instala ela no servidor para trabalhar de verdade:
ler log, achar por que o serviço caiu, subir de novo.

Ela fala português, entende o seu ambiente e não te devolve um tutorial de
quatro páginas quando você só quer o comando que resolve.

👉 **[ialauren.com](https://ialauren.com)**

---

## Começando

Entre em [ialauren.com](https://ialauren.com), crie a conta com
e-mail ou com o Google, e pergunte. Não precisa instalar nada para conversar.

### Onde ela roda

| | |
|---|---|
| **Navegador** | funciona sem instalar nada, no computador e no celular |
| **iPhone e Android** | aplicativo próprio, com câmera, anexo e ditado |
| **Windows** | programa com janela própria, e a Lauren pode cuidar do seu PC |

A conversa é a mesma nos três: o que você começa no computador continua no
celular. 👉 **[Baixar](https://ialauren.com/app)**

### O que ela lê

Arraste na conversa ou toque no clipe:

| Formato | O que ela faz |
|---|---|
| **Print, foto** (`png`, `jpg`, `webp`) | ela *vê* a tela de erro, o gráfico, o painel |
| **PDF** | lê o texto, a tabela e o layout — inclusive PDF escaneado |
| **Excel** (`.xlsx`) e **CSV** | lê as células, soma coluna, acha a linha |
| **Word** (`.docx`) e **PowerPoint** (`.pptx`) | lê o conteúdo |
| **Áudio** | escuta você explicando o problema |
| `.txt`, `.log`, `.json`, `.yml` | lê inteiro |

O arquivo continua valendo nas perguntas seguintes: mande a planilha uma vez e
continue perguntando sobre ela.

> Word e Excel **antigos** (`.doc`, `.xls`, do Office 95) não abrem. Salve como
> `.docx`, `.xlsx` ou PDF.

### Ditado

Segure o microfone na caixa de escrever e fale. O texto aparece escrito, você
revisa e manda. No navegador isso não gasta nada da sua cota.

---

## Lauren na sua VPS

Aqui ela para de dar conselho e passa a fazer. Ela entra no servidor, lê os
arquivos, roda os comandos, corrige e reinicia o serviço — pedindo autorização
antes de cada coisa que muda alguma coisa.

**Disponível nos planos PRO e MAX.**

### Instalar

Abra a aba **Code** no site: o comando aparece lá, já com um convite dentro
dele. Copie e rode **no terminal da sua VPS**, como root:

```bash
curl -fsSL https://ialauren.com/instalar.sh | sudo bash -s SEU_CONVITE
```

Ubuntu, Debian, Rocky, Alma. Leva menos de um minuto. O convite vale 30 minutos
e funciona uma vez só — se vencer, recarregue a página e pegue outro.

> Esse comando roda **dentro do servidor**, não no seu computador. Se você usa
> Windows, entre nele antes com `ssh root@seu-servidor`.

Depois é só chamar:

```bash
lauren
```

📖 **[Manual do terminal →](docs/terminal.md)** — todos os comandos, o que ela
pode fazer, como autorizar e como tirar do ar.

### E no seu computador

No programa de Windows, a aba **Code** tem um botão "Este computador". Um
clique e ela passa a cuidar da sua máquina: acha o arquivo, resolve o serviço
que não sobe, arruma o que travou — pedindo autorização antes de cada comando,
igual à VPS.

Ler é liberado; mexer pede autorização; formatar disco e mexer no `Windows` são
proibidos de saída.

---

## Planos

| | Grátis | PRO | MAX |
|---|---|---|---|
| Conversa no site, no app e no computador | ✅ | ✅ | ✅ |
| Ler print, PDF, Word, Excel | ✅ | ✅ | ✅ |
| **Lauren na sua VPS e no seu PC** | — | ✅ | ✅ |
| Modelos mais fortes | — | ✅ | ✅ |
| Uso | para tirar dúvida | folgado, para trabalhar todo dia | quase o triplo do PRO |
| | | **R$ 69,90** | **R$ 199,90** |

Pagamento por PIX, sem fidelidade e sem renovação automática.

📖 **[Como funciona o consumo →](docs/consumo.md)** — as duas janelas, por que
sua porcentagem sobe e o que fazer quando ela chega perto de 100%.

---

## Perguntas

📖 **[Perguntas frequentes →](docs/perguntas.md)** — segurança, root, o que ela
faz com os seus dados, o que fazer quando algo não funciona.

---

## Suporte

Abra uma [issue](https://github.com/LinkjohnDEV/lauren/issues) ou fale com o
suporte pelo próprio site.

<sub>Lauren é um produto <a href="https://linkjohn.com">LinkJohn</a>.</sub>
