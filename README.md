# Lauren

**A IA que resolve, em vez de explicar.**

Seu site caiu às duas da manhã. Você não quer ler sobre `journalctl` — quer o
serviço no ar. A Lauren entra no servidor, lê o log, descobre o que quebrou e
sobe de novo, pedindo sua autorização antes de cada comando.

Fala português, entende o seu ambiente e trabalha onde você trabalha: no
navegador, no celular, no seu Windows e dentro do VS Code.

Começa de graça, sem cartão. 👉 **[ialauren.com](https://ialauren.com)**

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
| **VS Code** | extensão que trabalha no projeto aberto, com os arquivos à mão |

A conversa é a mesma nos quatro: o que você começa no computador continua no
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
revisa e manda.

No Chrome e no Edge quem transcreve é o próprio navegador: não sai nada daqui e
não gasta um pingo da sua cota. Nos outros e no aplicativo, o áudio vem para
nós — e aí consome um pouquinho, bem menos que uma pergunta.

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

## Está fora do ar?

**[ialauren.com/status](https://ialauren.com/status)** mostra o estado de cada
parte agora e o histórico dos últimos dias. Se o problema for nosso, está lá —
e você não perde tempo procurando erro do seu lado.

---

## Suporte

Abra uma [issue](https://github.com/LinkjohnDEV/lauren/issues) ou fale com o
suporte pelo próprio site.

<sub>Lauren é um produto <a href="https://linkjohn.com">LinkJohn</a>.</sub>
