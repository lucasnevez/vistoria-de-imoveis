# Vistoria de Imóveis

**Versão atual: 1.3.0** (27/10/2026). O que mudou em cada versão está no [histórico de versões](CHANGELOG.md).

App de vistoria de entrada e saída de aluguel que roda dentro do Claude.

- As fotos são feitas no celular, em blocos de até 20.
- Você descreve cada bloco falando, e o Claude organiza tudo por cômodo.
- O laudo em PDF sai com a logo e as cores da sua imobiliária e vai para o seu Google Drive.
- Na vistoria de saída, o app compara com a de entrada e aponta desgaste, dano e itens faltando.

Tudo fica na conta de quem instala: as vistorias, as fotos e os laudos.

## O que você precisa

1. Uma conta no Claude com plano Pro ou maior.
2. O aplicativo do Claude no computador (claude.com/download), **atualizado** e logado nessa conta. Ele é usado só para instalar.
3. O Google Drive conectado ao Claude: Configurações, depois Conectores, Google Drive e Conectar.

## Como instalar ou atualizar

**Importante:** a mensagem abaixo precisa ser colada na aba **Code** do aplicativo do Claude no computador. Num chat comum do Claude, ou no Cowork, ela não funciona, porque só o Claude Code consegue publicar o app.

1. Abra o aplicativo do Claude no computador e clique em **Code**, no alto da janela.
2. Comece uma conversa nova e escolha uma pasta do seu computador, por exemplo Documentos. Não escolha um ambiente na nuvem.
3. Cole a mensagem abaixo. **Se você já tem o app instalado**, cole o link dele na linha indicada, para atualizar sem perder as vistorias e sem mudar o link. **Se é a primeira instalação**, deixe a linha em branco.
4. Envie.

```
Este pedido é para o Claude Code. Instale ou atualize o meu app de vistoria de imóveis, conforme o caso:

Link do meu app (deixe em branco se for a primeira instalação):

0. Antes de tudo, confira se você tem a ferramenta Artifact, que publica páginas no claude.ai. Se não tiver, pare e me responda só isto: "Este pedido precisa rodar na aba Code do aplicativo do Claude no computador, atualizado e logado na sua conta Pro, numa pasta do seu computador."
1. Baixe o arquivo pelo terminal, por exemplo com: curl -fsSL -o vistoria-app.html https://raw.githubusercontent.com/lucasnevez/vistoria-de-imoveis/main/vistoria-app.html
   Não use busca na web nem leitura de página, porque elas cortam o arquivo. Confira que o arquivo baixado tem mais de 150 KB e que a última linha é </script>. Se o terminal não tiver internet, não tente montar o arquivo: me peça para baixar e colocar nesta pasta.
2. Se o meu conector do Google Drive não se chamar exatamente "Google Drive", troque esse nome na linha const DRIVE do arquivo e, na instalação, também nas capacidades do passo 3.
3. SE EU DEIXEI O LINK EM BRANCO (instalação): publique o arquivo vistoria-app.html como artifact, com o ícone "checklist" e exatamente estas capacidades: {"db":{"rules":[{"path":"config","read":"view","write":"owner"}]},"user":{"scopes":["profile"]},"assets":{},"sample":{"images":true},"downloads":true,"mcp":{"servers":[{"server":"Google Drive","tools":["create_file","search_files","get_file_metadata"]}]}}
   SE EU COLEI O LINK (atualização): leia o meu app atual com a ferramenta Artifact (action "read") nesse link e republique o arquivo baixado no mesmo link, passando a url dele e sem passar capacidades, para manter as atuais e todas as vistorias. Nunca crie um link novo nesse caso.
4. No fim, me dê o link do app e diga qual versão ficou publicada: é o valor de const VERSAO no arquivo.
```

5. O Claude pede permissão para baixar o arquivo e para publicar o app. Clique em permitir.
6. Ele devolve o link do app e a versão. Abra o link no celular, pelo aplicativo do Claude. Na primeira instalação, o próprio app pede o nome da empresa, a cidade e a logo, sugere as cores, cria a pasta no Google Drive e confere se está tudo funcionando.

**Se o Claude pedir o arquivo:** abra https://github.com/lucasnevez/vistoria-de-imoveis/blob/main/vistoria-app.html, clique no botão de download ("Download raw file", o ícone de seta para baixo, à direita) e salve o arquivo na mesma pasta que você escolheu no passo 2. Depois escreva "pronto, o arquivo está na pasta".

A versão em uso aparece no app, em Configurações, no fim da página. A versão mais nova está no topo desta página e no [histórico de versões](CHANGELOG.md).
