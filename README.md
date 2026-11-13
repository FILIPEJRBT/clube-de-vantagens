# Clube de Vantagens — FJ Beach Tennis

Site: https://fjbeachtenis.com.br  
Painel: https://fjbeachtenis.com.br/admin/

## Como atualizar pelo painel

1. Abra **/admin/** e clique em **Sign In Using Access Token**.
2. Cole o token do GitHub (veja abaixo como criar, só uma vez).
3. Escolha **Parceiros**, **Categorias** ou **Galeria de fotos**, edite e clique em **Save**.
4. O site atualiza sozinho em 1 a 2 minutos.

### Criar o token (uma vez por pessoa)

GitHub → foto do perfil → Settings → Developer settings → Personal access tokens →
**Fine-grained tokens** → Generate new token:

- Repository access: *Only select repositories* → `clube-de-vantagens`
- Permissions → Repository → **Contents: Read and write**
- Guarde o token em local seguro. Não compartilhe.

## Onde ficam os dados

- `dados/parceiros.json` — parceiros (nome, categoria, desconto, WhatsApp, link, ativo)
- `dados/categorias.json` — categorias do filtro
- `dados/galeria.json` — fotos da galeria
- `index.html` — layout e visual da página

WhatsApp: digite com DDD, por exemplo `(47) 99101-1123`. O site monta o link sozinho.
Parceiro com **Aparece no site** desmarcado fica oculto, sem ser apagado.
