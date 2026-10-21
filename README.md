# Black Friday Unicive — página de VENDA

Página de venda da Black Friday da **Unicive**: leva o visitante direto ao **checkout de matrícula**.
(A página de cadastro/lista VIP é a `../blackFridayUnicive`.)

| | |
|---|---|
| **Oferta** | Matrícula de ~~R$ 399~~ por **R$ 69,90** |
| **Mensalidade** | de R$ 250 por *(a definir — tabela oficial)* |
| **Duração** | 09/11 (00h00) até 20/11, 23h59 |
| **Cursos** | Serviços Jurídicos · Segurança Privada · Gestão de RH · Criminologia · Segurança Pública (só servidores públicos) |

## Antes de publicar

| O quê | Onde |
|---|---|
| Link do checkout de matrícula (já preenchido) | `CONFIG.checkout` no `script.js` |
| Mensalidade de Black Friday (quando sair a tabela) — preenchida, aparece sozinha | `CONFIG.mensalidade` (ex.: `"R$ 129,90"`) |
| `og:image` 1200×630 | `<head>` do `index.html` |

## Fases automáticas

- **antes de 09/11**: cronômetro conta até o início, botões travados ("Oferta liberada em 09/11");
- **09/11 a 20/11**: cronômetro conta até o fim, botões levam ao checkout (com as UTMs da visita);
- **depois de 20/11 23h59**: "Oferta encerrada".

Datas em `CONFIG.inicio` / `CONFIG.fim`. Clique no checkout vai para o dataLayer como `clique_checkout`.

## Deploy

Estático, sem build (`"framework": null`). Imagens em `assets/`, nunca em `public/`.
