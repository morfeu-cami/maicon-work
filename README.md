# PulsePlay — Dashboard de Música e Streaming

Dashboard responsivo, em português, adaptado do projeto original de vendas para o tema de **músicas e plataformas de streaming**.

## O que está incluído

- Indicadores de reproduções, ouvintes únicos, tempo ouvido e faixa destaque.
- Gráfico de evolução diária de reproduções.
- Distribuição de ouvintes por plataforma: Spotify, YouTube Music, Apple Music e Deezer.
- Ranking das faixas com retenção e variação semanal.
- Área de insights sobre horário de lançamento e localização do público.
- Dados fictícios, prontos para serem substituídos no arquivo `index.html`.
- Layout responsivo para computador, tablet e celular.

## Como abrir localmente

Não é necessário instalar dependências nem usar um framework. Basta abrir o `index.html` no navegador.

Se preferir usar um servidor local:

```bash
python3 -m http.server 8000
```

Depois acesse <http://localhost:8000>.

## Como publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie o arquivo `index.html` e este `README.md` para a raiz do repositório.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`.
6. Salve e aguarde o GitHub gerar o endereço público.

O projeto é uma página estática: não precisa de Node.js, banco de dados ou etapa de build. O gráfico usa Chart.js por CDN.

## Onde alterar os dados

No final do `index.html`, edite estas linhas para trocar os valores do gráfico:

```js
const dias = ['Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sáb', 'Dom'];
const reproducoes = [12400, 15800, 13900, 18600, 22100, 27400, 31100];
```

Os textos dos cartões, das plataformas e das faixas ficam no HTML, com comentários e nomes de classes para facilitar a edição.
