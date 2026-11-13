# Site do Clube de Vantagens — FJ Beach Tennis

Site estático publicado pelo GitHub Pages em https://fjbeachtenis.com.br (arquivo `CNAME`).
Tudo que entra na branch `main` vai para o ar em 1 a 2 minutos. Não há build.

## Estrutura

- `index.html`: página única (HTML, CSS e JS juntos). Lê os dados da pasta `dados/` com fetch.
- `dados/parceiros.json`: `{ "parceiros": [ { nome, categoria, descricao, beneficio, responsavel, whatsapp: [ "..." ], link, ativo } ] }`
  - `categoria` = `id` de uma categoria em `dados/categorias.json`.
  - `beneficio`: texto curto, ex. `"10%"`; vazio = "condição a combinar".
  - `whatsapp`: lista de textos, ex. `["(47) 99101-1123"]`. O site acrescenta o 55 e monta o link do WhatsApp.
  - `ativo: false` esconde o parceiro sem apagar.
- `dados/categorias.json`: `{ "categorias": [ { id, nome, icone } ] }`. `icone` é o `d` de um path SVG 24x24 (opcional).
- `dados/galeria.json`: `{ "fotos": [ { src, legenda } ] }`. Fotos novas vão em `assets/img/uploads/`.
- `admin/`: painel Sveltia CMS (`admin/config.yml`). Se mudar campos nos JSON, atualize o config também.
- `assets/`: imagens e vídeo do topo.

## Regras

- Escreva textos do site em português do Brasil.
- Para incluir, alterar ou remover parceiros, edite só `dados/parceiros.json`. Mantenha o JSON válido e com 2 espaços.
- Telefones de celular com 9 dígitos, ex.: (47) 99101-1123. Não invente números; se não foram informados, deixe a lista vazia.
- Antes de mudar o visual, teste a página localmente (`python3 -m http.server`) e confira se não há erros no console.
- Use caminhos relativos (sem `/` no início) para arquivos do site.
