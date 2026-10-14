# Página responsiva PIX

## Arquivos
- `index.html`: interface e estilos responsivos.
- `config.js`: campos editáveis (valor exibido, nome, endereço e código PIX).
- `README.md`: instruções.

## Ajustar dados
Edite `config.js`. O QR Code é gerado a partir do código PIX informado. O valor visual não modifica uma cobrança PIX emitida pelo banco/provedor; use sempre o código original da cobrança correspondente.

## Publicação na Render
Use um Static Site conectado ao repositório GitHub. Build command vazio e Publish Directory `.`.

## Observações
A interface adapta as larguras dos elementos à largura útil do aparelho. A ausência total de rolagem depende também da altura da tela, das fontes e das barras do navegador; em aparelhos pequenos, priorize não cortar conteúdo. O site não verifica recebimentos bancários.

O campo `pixCode` contém a sequência PIX recebida e o QR Code é gerado com esse texto integral, não com o link Markdown. Confirme a cobrança no app bancário antes de usar em produção.
