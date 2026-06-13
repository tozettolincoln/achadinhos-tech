# Segurança Da Landing Page

Esta landing page é estática: não usa JavaScript, formulário, login, banco de dados ou cookies próprios. Isso reduz bastante a superfície de ataque.

## Medidas aplicadas

- `script-src 'none'` na Content Security Policy para bloquear execução de JavaScript.
- `form-action 'none'` porque a página não envia formulários.
- `object-src 'none'` e `frame-src 'none'` para evitar plugins/iframes.
- `referrer` restrito para reduzir vazamento de URL completa ao abrir links externos.
- Links externos com `rel="noreferrer"`.
- Política de privacidade local em `privacy.html`.
- Arquivo `.well-known/security.txt` para contato de segurança.
- Arquivo `_headers` para hosts que suportam cabeçalhos de segurança, como Cloudflare Pages e Netlify.

## Atenção No GitHub Pages

GitHub Pages publica sites estáticos, mas não permite configurar cabeçalhos HTTP customizados por arquivo `_headers`. Por isso, a CSP principal também foi adicionada como `<meta http-equiv="Content-Security-Policy">`.

Se a prioridade for segurança máxima com cabeçalhos HTTP reais, hospede no Cloudflare Pages ou Netlify usando o arquivo `_headers` incluído.

## Checklist Antes De Publicar

- Link oficial do grupo aplicado: `https://chat.whatsapp.com/GmVTplmLx88FddVR1oLpQT`.
- Trocar `contato@example.com` por um e-mail real.
- Quando a URL pública existir, adicionar `canonical`, `og:url` e URLs absolutas para `og:image` e `twitter:image`.
- Não colocar tokens, credenciais, planilhas privadas ou dados de membros no repositório.
- Não adicionar scripts de rastreamento antes de revisar LGPD, consentimento e política de cookies.
- Manter o grupo WhatsApp com entrada voluntária e descrição clara sobre links afiliados.
