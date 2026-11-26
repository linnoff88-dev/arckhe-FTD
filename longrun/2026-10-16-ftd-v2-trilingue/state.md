# State (16/10/2026) — CONCLUÍDO
- PT/EN/ES publicados: https://linnoff88-dev.github.io/ (+ en/, es/). Raiz /FTD/ redireciona para o v2.
- validar.py 0 erros; browser-check OK nos 3 idiomas (93 páginas, desktop+celular); 93/93 HTTP 200 após push (bf36f57).
- sobras.py: 21 ocorrências restantes sêo dados de exemplo brasileiros dentro de código (intencional).
- Pendente (só se o Nei pedir): portal — atualizar descriçêo/entrada id 16 e "Disponível em EN/ES" (skill atualiza-portal).
- Reconstruir: python3 scripts/build.py → localization.py → translate.py → render-locales.py → traduz-js-codex.py --files assets/learn.js.
