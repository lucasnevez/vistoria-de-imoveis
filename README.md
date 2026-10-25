# Vistoria de Imóveis

App de vistoria de entrada e saída de aluguel que roda dentro do Claude.

- As fotos são feitas no celular, em blocos de até 20.
- Você descreve cada bloco falando, e o Claude organiza tudo por cômodo.
- O laudo em PDF sai com a logo e as cores da sua imobiliária e vai para o seu Google Drive.
- Na vistoria de saída, o app compara com a de entrada e aponta desgaste, dano e itens faltando.

Tudo fica na conta de quem instala: as vistorias, as fotos e os laudos.

## O que você precisa

1. Uma conta no Claude com plano Pro ou maior.
2. O aplicativo do Claude no computador (claude.com/download), usado só para instalar.
3. O Google Drive conectado ao Claude: Configurações, depois Conectores, Google Drive e Conectar.

## Como instalar

Abra a aba **Code** no aplicativo do Claude, em qualquer pasta, cole a mensagem abaixo e envie:

```
Instale para mim o app de vistoria de imóveis:
1. Baixe o arquivo https://raw.githubusercontent.com/lucasnevez/vistoria-de-imoveis/main/vistoria-app.html e salve nesta pasta com o nome vistoria-app.html.
2. Publique esse arquivo como artifact, com o ícone "checklist" e exatamente estas capacidades: {"db":{"rules":[{"path":"config","read":"view","write":"owner"}]},"user":{"scopes":["profile"]},"assets":{},"sample":{"images":true},"downloads":true,"mcp":{"servers":[{"server":"Google Drive","tools":["create_file","search_files","get_file_metadata"]}]}}
3. Se o meu conector do Google Drive não se chamar exatamente "Google Drive", troque esse nome nas capacidades e na linha const DRIVE do arquivo antes de publicar.
4. No fim, me dê o link do app.
```

O Claude devolve o link do app. Abra esse link no celular, pelo aplicativo do Claude. Na primeira vez, o próprio app pede o nome da empresa, a cidade e a logo, sugere as cores, cria a pasta no Google Drive e confere se está tudo funcionando.
