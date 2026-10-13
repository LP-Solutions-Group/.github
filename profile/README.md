<div align="center">

# LP Solutions Group

**Inteligência competitiva para quem vende em marketplace brasileiro**

[sellerscope.com.br](https://sellerscope.com.br)

</div>

---

## O que fazemos

Transformamos o que os marketplaces já publicam em decisão de compra de estoque: o que vende, por quanto, com que margem e contra quem.

A suíte é um produto só, em três frentes. Cada marketplace tem a sua extensão, e todas falam com a mesma plataforma de conta, assinatura e dados compartilhados.

## Produtos

### SellerScope — Shopee Brasil
Extensão Chrome (Manifest V3) que injeta os painéis na própria página da Shopee: vendas, faturamento, ranking, calculadora de preço e margem, análise por variação e mineração de avaliações. A leitura vem do que a página já carregou.

### SellerScope ML — Mercado Livre
A mesma leitura para o Mercado Livre, com o que é específico dele: taxa exata por categoria e tipo de anúncio, rivais do mesmo produto de catálogo, visitas oficiais, prazo de entrega e estoque declarado por variação.

[Política de privacidade](https://github.com/LP-Solutions-Group/sellerscope-privacidade)

### SellerScope TK — TikTok Shop Brasil
A terceira do conjunto. Além dos painéis, resolve um problema que o TikTok Shop não publica: a data de criação do anúncio, estimada por calibração do próprio identificador contra âncoras de terceiros.

### Plataforma
Site, painel do assinante e backend da suíte: conta, planos, cobrança recorrente, painel administrativo e os dados que as extensões compartilham entre si.

## Stack

| Camada | Tecnologia |
|---|---|
| Extensões | JavaScript, Chrome MV3, webpack, Vitest. Zero dependência de runtime |
| Site e painel | Next.js 16, React 19, Tailwind, hospedado na Render |
| Backend | Supabase (Postgres, Auth, Edge Functions em Deno, pg_cron) |
| Dados compartilhados | Cloudflare Workers com D1 e KV |
| Cobrança | Asaas, com webhook validado por segredo compartilhado |

## Como trabalhamos

Três práticas que sustentam o resto:

**O número tem de dizer de onde veio.** Todo valor na tela carrega procedência: oficial do marketplace, calculado por nós, lido da página ou faixa. Onde não houve medição, a tela mostra traço e explica o motivo. Número errado é pior que ausência de número.

**Teste de regressão só vale depois de falhar.** Todo guardião é conferido reintroduzindo o defeito que ele cobre, e a reprovação tem de vir por asserção. Hoje são mais de 5.600 testes nos três repositórios.

**O que está no ar é a verdade.** Merge não é publicação. A CI confere o artefato servido contra o commit que entrou, porque já aconteceu de um deploy não disparar sem erro nenhum.

Fluxo de branch: trabalho em branch pessoal, integração em `dev`, release em `main`, sempre por pull request com CI verde.

## Equipe

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LeonardoPCavalcanti">
        <img src="https://github.com/LeonardoPCavalcanti.png" width="100px;" alt="Leonardo"/><br />
        <sub><b>Leonardo Cavalcanti</b></sub>
      </a><br />
      <sub>Co-fundador</sub><br />
      <sub>Infraestrutura, backend e segurança</sub>
    </td>
    <td align="center">
      <a href="https://github.com/Pedrolucas888">
        <img src="https://github.com/Pedrolucas888.png" width="100px;" alt="Pedro"/><br />
        <sub><b>Pedro Lucas Sarmento</b></sub>
      </a><br />
      <sub>Co-fundador</sub><br />
      <sub>Produto, interface e publicação</sub>
    </td>
  </tr>
</table>

## Contato

Suporte e parcerias: [suporte@sellerscope.com.br](mailto:suporte@sellerscope.com.br)

Os repositórios de produto são privados. Encontrou uma vulnerabilidade de segurança? Escreva para o endereço acima com o máximo de detalhe que puder, e não abra issue pública.

---

<div align="center">

<sub>LP Solutions Group &copy; 2026</sub>

</div>
