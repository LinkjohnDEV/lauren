# Lauren

**Uma IA que já vem com a sua VPS.** Você conversa com ela no navegador, e
instala ela no servidor para trabalhar de verdade: ler log, achar por que o
serviço caiu, subir de novo.

Ela fala português, entende o seu ambiente e não te devolve um tutorial de
quatro páginas quando você só quer o comando que resolve.

👉 **[lauren.linkjohn.com](https://lauren.linkjohn.com)**

---

## Começando

Entre em [lauren.linkjohn.com](https://lauren.linkjohn.com), crie a conta com
e-mail ou com o Google, e pergunte. Não precisa instalar nada para conversar.

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

Pegue sua chave em **Configurações → Conta** no site e rode na sua VPS:

```bash
curl -fsSL https://lauren.linkjohn.com/instalar.sh | bash -s -- SUA_CHAVE
```

Ubuntu, Debian, Rocky, Alma. Leva menos de um minuto.

Depois é só chamar:

```bash
lauren
```

📖 **[Manual do terminal →](docs/terminal.md)** — todos os comandos, o que ela
pode fazer, como autorizar e como tirar do ar.

---

## Planos

| | Grátis | PRO | MAX |
|---|---|---|---|
| Conversa no site e no app | ✅ | ✅ | ✅ |
| Ler print, PDF, Word, Excel | ✅ | ✅ | ✅ |
| **Lauren na sua VPS** | — | ✅ | ✅ |
| Modelos mais fortes | — | ✅ | ✅ |
| Uso por mês | pequeno | alto | muito alto |
| | | **R$ 49,90** | **R$ 149,90** |

Pagamento por PIX, sem fidelidade.

📖 **[Como funciona o consumo →](docs/consumo.md)** — as três janelas, por que
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
