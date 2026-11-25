# Histórico de versões

A versão em uso aparece no app, em Configurações, no fim da página.

## 1.5.0 (25/11/2026)

**Melhorias pedidas pela equipe**
- O tipo da vistoria (entrada ou saída) pode ser trocado a qualquer momento, inclusive em vistorias antigas. O botão aparece em Dados e no topo de cada lote.
- Fotos extras: dá para adicionar fotos a um lote já enviado ou direto a um item, na Revisão, sem refazer o lote e sem passar de novo pelo Claude. Funciona também depois do laudo.
- Junto com o PDF, o app salva na mesma pasta um arquivo Word (.docx) editável, com o mesmo conteúdo e as fotos. Se o arquivo não couber no envio, ele vai com fotos menores ou só com o texto. Também dá para baixar o Word na tela do laudo.
- Laudo padronizado: página A4 com margens de 2 cm, texto justificado e o mesmo rodapé em todas as páginas (empresa, CRECI, contato, tipo e data do laudo, página X de Y), no PDF e no Word.

**Segurança**
- Só a equipe convidada lê as vistorias. Quem tem acesso só de leitura, ou chega por link público, não vê mais nada.
- Tudo o que vem do banco é conferido antes de ir para a tela: um registro estragado não derruba o app nem insere código.
- Os links do Drive são montados pelo próprio app, e os códigos de pasta são conferidos antes de qualquer envio.
- As bibliotecas externas (PDF) só carregam se forem exatamente as originais.
- Vistoria excluída não volta sozinha, nem neste aparelho nem em outro que estava com ela aberta. O rascunho de um usuário não entra na conta de outro no mesmo aparelho, e rascunhos esquecidos somem em até 7 dias.
- Instalação e atualização baixam só a versão publicada como release, com conferência de que o arquivo é o original.

**Proteção contra texto malicioso em fotos e falas**
- Um lote novo não melhora sozinho o estado de um item que já estava ruim ou regular, nem tira um ponto de atenção: o app pede confirmação.
- A correção falada só remove em massa o que foi citado pelo nome, e a lista do que mudou fica na tela com o botão de desfazer.
- Na comparação entre entrada e saída, os estados vêm do que está guardado no app. Item que o Claude pulou entra como "a avaliar".

**Privacidade**
- O link da pasta do Drive não vai mais no laudo, a não ser que o dono ligue essa opção em Configurações.
- As cópias de segurança saíram da pasta de cada vistoria e foram para a pasta "Cópias de segurança (uso interno)", sem dados técnicos do aparelho.
- O endereço do imóvel não é mais enviado ao Claude. Aviso na tela do lote para não fotografar pessoas nem documentos.
- Aviso "alterada depois do laudo" quando uma vistoria muda depois de o PDF ter sido gerado.
- A tela "Onde ficam os dados" conta tudo: o que o Claude recebe, o que fica no Drive e o que continua lá depois de excluir.

## 1.4.0 (24/11/2026)

**Lotes de 20 fotos mais rápidos**
- As fotos são guardadas no app até três ao mesmo tempo, em vez de uma por vez. A grade mostra miniaturas leves, sem carregar a foto inteira.
- O lote termina assim que o Claude responde. As fotos seguem para o Google Drive em segundo plano, três ao mesmo tempo, e dá para começar o próximo lote sem esperar. A garantia continua igual: cada foto é conferida na pasta, o que falhar volta para a fila, e o laudo só sai depois de tudo enviado e conferido.
- Cada foto é enviada ao Drive uma vez só, no tamanho em que foi guardada. Se a resposta do Drive for duvidosa, o app procura a foto na pasta antes de mandar de novo.
- A cópia de segurança dos dados também vai para o Drive sem prender a tela.
- O app salva menos vezes durante o envio das fotos, o que deixa o celular mais leve. O rascunho no aparelho continua protegendo o que ainda não foi salvo.

**Dá para ver o que está acontecendo**
- Enquanto o Claude trabalha, a tela mostra há quanto tempo ele está olhando as fotos e quantos itens já escreveu.
- Ao sair de uma vistoria com fotos ainda a caminho do Drive, o app avisa que o envio continua quando ela for aberta de novo.
- Um erro antigo do Drive, já resolvido, não volta a aparecer no painel.

**Medição**
- Cada lote guarda quanto tempo levou para guardar as fotos, para o Claude responder e para o Drive receber. O cartão do lote mostra o resumo, e os números ficam na vistoria para o suporte.

## 1.3.1 (27/10/2026)

- O visual padrão é genérico, para qualquer imobiliária. A identidade de cada uma (logo, cores e capa) entra só em Configurações.
- Preparado um lugar discreto para a marca de quem fornece o app (fim das Configurações e rodapé do PDF), vazio por enquanto.

## 1.3.0 (27/10/2026)

**Fotos no Google Drive, agora com garantia**
- Cada foto é enviada e, em seguida, conferida na pasta do Drive. Só conta como enviada depois de conferida.
- Se o envio falhar, o app reduz a foto e tenta de novo, em até quatro tamanhos, e guarda o tamanho que funcionou para as próximas.
- O que não subir fica numa fila: o app tenta de novo sozinho, com intervalos crescentes, enquanto a vistoria está aberta, e também quando a internet volta ou a vistoria é reaberta.
- Painel "Drive: X de Y fotos na pasta Imagens", com o último erro em palavras simples, o detalhe técnico para o suporte e os botões "Sincronizar agora" e "Conferir o Drive".
- Antes do laudo, um revisor do Drive envia o que falta e confere cada foto. Na lista inicial, a vistoria com foto faltando no Drive aparece marcada.
- Cada tentativa fica registrada na própria vistoria, para o suporte conseguir ler.

**Editar e excluir lotes**
- Na lista "Lotes enviados", cada lote tem Editar e Excluir.
- Editar reabre o lote com as fotos e a fala; dá para tirar ou adicionar fotos e mudar a fala. Ao processar de novo, os itens que o lote tinha colocado no relatório são refeitos. O que foi mudado à mão em outros itens continua.
- Excluir tira o lote e as fotos do app. O que já estava no Drive fica lá.

**Revisão agêntica do app inteiro**
- Três revisores independentes leram o app inteiro (fluxo de dados, Drive e sincronização, telas e PDF) e apontaram 58 pontos; os que eram defeitos reais foram corrigidos. Entre eles: itens criados pela correção falada sumiam ao editar um lote; o PDF que não subia ao Drive se perdia ao recarregar; trocar a vistoria de entrada mantinha a comparação antiga; o parecer e a comparação editados à mão eram sobrescritos ao consolidar de novo; uma vistoria apagada podia voltar; sugestões do revisor sobre um mesmo item se perdiam; a conferência do PDF podia confundir um item com a descrição de outro.
- No laudo em PDF: títulos de seção não ficam mais sozinhos no fim da página, nomes longos não passam por baixo do rótulo de estado, a lista de fotos quebra linha, a legenda das fotos tem duas linhas, o rodapé não cruza com o número da página, e acentos digitados de forma decomposta são preservados.
- Textos e telas: um nome só para "pontos de atenção", botões citados pelo nome certo, erros do Drive em português, botão "Parar" ao gerar o laudo, aviso claro quando a vistoria não salva, confirmação de exclusão que volta ao normal, e a pasta do Drive não é mais recriada em silêncio.

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
