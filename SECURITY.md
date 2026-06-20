# Segurança da Landing Page

Esta landing page é estática: não usa JavaScript, formulário, login, banco de dados ou cookies próprios.

## Medidas aplicadas

- `script-src 'none'` na Content Security Policy para bloquear execução de JavaScript.
- `form-action 'none'` porque a página não envia formulários.
- `object-src 'none'` e `frame-src 'none'` para evitar plugins e iframes.
- `referrer` restrito para reduzir vazamento de URL completa ao abrir links externos.
- CTAs externos com URL explícita e navegação direta na mesma aba.
- Política de privacidade local em `privacy.html`.
- Arquivo `.well-known/security.txt` para contato de segurança.
- Arquivo `_headers` para hosts que suportam cabeçalhos de segurança, como Cloudflare Pages e Netlify.

## Atenção no GitHub Pages

GitHub Pages publica sites estáticos, mas não permite configurar cabeçalhos HTTP customizados por arquivo `_headers`. Por isso, a CSP principal também foi adicionada como `<meta http-equiv="Content-Security-Policy">`.

Se a prioridade for segurança máxima com cabeçalhos HTTP reais, hospede no Cloudflare Pages ou Netlify usando o arquivo `_headers` incluído.

## Checklist antes de publicar

- Link oficial do grupo aplicado: `https://chat.whatsapp.com/GmVTplmLx88FddVR1oLpQT`.
- Marca pública aplicada: `Achados Tech Tz`.
- Manter `canonical`, `og:url` e URLs absolutas para `og:image` e `twitter:image`.
- Não colocar tokens, credenciais, planilhas privadas ou dados de membros no repositório.
- Não adicionar scripts de rastreamento antes de revisar LGPD, consentimento e política de cookies.
- Manter o grupo WhatsApp com entrada voluntária e descrição clara sobre links afiliados.
