# Perguntas frequentes

## A Lauren tem acesso ao meu servidor?

Só se você instalar ela lá. Na conversa do site ela não tem acesso nenhum: ela
te diz o comando, quem roda é você.

Se instalar na VPS, aí sim ela trabalha lá dentro — **pedindo autorização antes
de cada comando**. Você vê o comando inteiro antes de dizer sim.

## Por que ela instala com poder de administrador?

Porque sem isso ela não resolve nada: lê o log e te devolve "reinicie o serviço",
em vez de reiniciar. A responsabilidade de manter a ordem é de quem usa — e por
isso cada comando passa pela sua autorização.

Prefere o contrário? Instale com `--sem-root`. Ela lê, mas não mexe.

## Como tiro ela do servidor?

```bash
sudo systemctl stop lauren-conector
sudo systemctl disable lauren-conector
```

E remova a máquina na aba **Code**, nos três pontinhos ao lado do nome dela.

## Alguém vê a minha VPS?

Não. Sua máquina só aparece na sua conta, e mesmo aí só depois de você pedir:
digitando `/rc` no terminal da VPS, ou clicando em "conectar este computador"
no programa de Windows. Sem isso, ela não é listada em lugar nenhum.

A conexão é o servidor que liga para nós, não o contrário: você não abre porta,
não configura firewall e não precisa de IP fixo.

## O que acontece com o que eu mando?

Suas conversas ficam na sua conta, e você apaga quando quiser — uma conversa ou
todas, em **Configurações → Privacidade**. Print e arquivo enviados ficam
presos à mensagem e somem junto com ela.

## Ela funciona em qual sistema?

Ubuntu, Debian, Rocky e Alma. A conversa pelo site e pelo app funciona em
qualquer lugar.

## Ela inventa comando?

Ela é instruída a não inventar caminho, comando nem configuração, e a dizer que
não sabe quando não souber. Mas ela é uma IA, e IA erra. **Antes de rodar algo
que apaga ou sobrescreve, leia o comando.** É para isso que a autorização existe.

## Esqueci minha senha

Fale com o suporte pelo site. A recuperação automática por e-mail está a caminho.

## Posso usar em mais de uma VPS?

Pode, com a mesma chave, quantas quiser. Cada máquina aparece com o nome dela.

## Ela trabalha em qual pasta?

Na pasta em que você abriu ela. Dê `cd` para o seu projeto antes de chamar
`lauren` e é ali que ela lê e mexe, sem ficar pedindo autorização a cada
arquivo. Fora dessa pasta, ela pede.

**Cada pasta guarda as conversas dela**: o `/resume` mostra o que você
conversou naquele projeto, não a mistura de todos.

## Que arquivos eu posso mandar para ela?

Arraste na conversa ou toque no clipe:

| Formato | O que ela faz |
|---|---|
| **Print e foto** (`png`, `jpg`, `webp`) | ela *vê* a tela de erro, o gráfico, o painel |
| **PDF** | lê o texto, a tabela e o layout — inclusive PDF escaneado |
| **Excel** (`.xlsx`) e **CSV** | lê as células, soma coluna, acha a linha |
| **Word** (`.docx`) e **PowerPoint** (`.pptx`) | lê o conteúdo |
| **Áudio** | escuta você explicando o problema |
| `.txt`, `.log`, `.json`, `.yml` | lê inteiro |

O arquivo continua valendo nas perguntas seguintes: mande a planilha uma vez e
continue perguntando sobre ela.

Word e Excel **antigos** (`.doc`, `.xls`, do Office 95) não abrem. Salve como
`.docx`, `.xlsx` ou PDF.

## Como funciona o ditado?

Clique no microfone na caixa de escrever e fale. Não precisa segurar: um clique
começa, outro clique para. O texto aparece escrito, você revisa e manda.

Se tiver mais de um microfone no computador, a setinha ao lado escolhe qual.

No Chrome e no Edge quem transcreve é o próprio navegador: não sai nada daqui e
não gasta um pingo da sua cota. Nos outros navegadores e no aplicativo, o áudio
vem para nós — e aí consome um pouquinho, bem menos que uma pergunta.

## Não achei minha pergunta

Abra uma [issue](https://github.com/LinkjohnDEV/lauren/issues) ou fale com o
suporte pelo site.
