# Histórico de versões

A versão em uso aparece no app, em Configurações, no fim da página.

## 1.2.0 (26/10/2026)

**O que a pessoa preenche manda**
- Quando a pessoa muda um estado, uma descrição ou um ponto de atenção à mão, nenhuma camada do Claude troca esse valor sozinha: nem os lotes seguintes, nem o revisor, nem a correção falada (a não ser que a correção cite o item).
- O revisor do laudo não sugere mais "Não se aplica". As sugestões de estado e de ponto de atenção chegam desmarcadas: é a pessoa que decide.
- O Claude só usa "Não se aplica" quando o item não existe no imóvel. Quando o estado não foi dito, ele deixa em branco e pergunta.

**Conferência do laudo antes do Drive**
- Revisor de fidelidade: lê o texto do PDF pronto e confere, item por item, se o estado de cada item, os nomes, o endereço, a data e as fotos batem com o que está no app.
- Revisor visual: o Claude olha as primeiras páginas do PDF como imagem e aponta problemas de aparência, como logo sem contraste, texto cortado ou foto faltando.
- Se algo não bater, ou se o revisor mudou um estado depois da aprovação, o PDF não vai para o Drive antes de a pessoa ver. Dá para desfazer as mudanças do revisor, trocar a capa, voltar para a revisão ou salvar assim mesmo.

**Logo**
- A logo enviada antes da versão 1.1.0 é tratada sozinha ao abrir o app: sai o fundo branco e entra a capa que combina com ela.

## 1.1.0 (25/10/2026)

**Logo e capa**
- O app tira sozinho o fundo branco da logo e recorta as sobras. Dá para voltar à logo original com um toque.
- Há duas capas para o laudo, clara e escura, mostradas lado a lado. O app escolhe a que combina com a logo: capa clara para logo escura, capa escura para logo clara.
- No topo do app, a logo aparece sobre a mesma cor da capa escolhida.

**Laudo**
- O CRECI aparece sempre como "CRECI 0000", mesmo quando só o número é digitado.
- As fotos do laudo ficaram maiores, duas por linha.
- O texto sai como constatação técnica, sem expressões como "conforme relato do vistoriador" ou "não informado".
- O campo de endereço pede o endereço completo, com exemplo.

**Fotos no Google Drive**
- Se o primeiro jeito de enviar falhar, o app tenta o segundo sozinho e passa a usar o jeito que funcionou.
- Quando uma foto não chega ao Drive, o app mostra o motivo e um detalhe técnico para o suporte.
- Novo botão "Reenviar fotos ao Drive", com a contagem de quantas fotos já estão na pasta Imagens.

## 1.0.1 (25/10/2026)

- Instruções de instalação mais seguras: a mensagem só roda no Claude Code, baixa o arquivo pelo terminal e confere se ele veio inteiro.

## 1.0.0 (25/10/2026)

- Primeira versão pública.
- Vistoria de entrada e de saída, com comparação entre as duas.
- Lotes de até 20 fotos com a descrição falada.
- Revisor do laudo antes do PDF.
- Tela de boas-vindas que configura empresa, logo, cores e pasta do Drive.
- Laudo em PDF e cópia de segurança dos dados no Google Drive.
