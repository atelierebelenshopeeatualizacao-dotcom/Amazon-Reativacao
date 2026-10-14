# Página de pagamento PIX — interface responsiva

## Arquivos
- `index.html`: página e estilos.
- `README.md`: estas instruções.

## Personalização
No fim de `index.html`, edite o objeto `CONFIG`:
- `amount`: valor exibido, por exemplo `"20,00"`.
- `recipient`: nome e cidade exibidos no resumo de entrega (edição somente no código).
- `address`: endereço exibido (edição somente no código; não existe botão de edição na página).
- `pixCode`: sequência PIX copia e cola original.

O QR Code é gerado automaticamente a partir de `pixCode`. O valor mostrado na tela não modifica a cobrança. Use o código original gerado pelo banco/provedor para o mesmo valor. Se for um PIX dinâmico, o valor pode ser determinado pelo sistema do provedor.

## Publicar na Render
Crie um Static Site ligado ao repositório GitHub que contém `index.html`. Deixe o comando de build vazio e defina `.` como Publish Directory.

## Observações importantes
- O QR Code é criado por QRCode.js carregado de CDN, então é necessária conexão à internet.
- Este front-end não confirma recebimentos nem consulta o banco.
- O navegador pode impedir o fechamento automático da aba. Os botões tentam voltar no histórico e, se isso não for permitido, orientam o usuário.
- Para a prévia de logo no WhatsApp, adicione uma imagem de logo hospedada publicamente e configure `og:image` com uma URL absoluta no `<head>`. O WhatsApp pode armazenar a prévia em cache.
