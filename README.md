# Casinhas Encantadas — Landing Page

Página de vendas estática feita com Vite + Tailwind CSS. O Tailwind é compilado e purgado no build, então só o CSS usado vai para produção (sem o aviso da CDN, carregamento muito mais rápido).

## Rodar localmente

```bash
npm install
npm run dev
```

Abre em `http://localhost:5173`.

## Build de produção

```bash
npm run build
```

Os arquivos finais ficam em `dist/`.

## Subir no Vercel

1. Suba esta pasta para um repositório no GitHub.
2. No Vercel, clique em **Add New > Project** e importe o repositório.
3. O Vercel detecta o Vite sozinho. Confirme:
   - Framework Preset: **Vite**
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Deploy.

## Onde mexer

- **Pixel da Meta:** cole o script dentro do `<head>` do `index.html`, no ponto marcado com o comentário `META PIXEL`.
- **Checkouts:** já estão nos links (VIP, básico e downsell). Procure por `pay.wiapy.com` no `index.html`.
- **Vídeo VSL:** o ID do Vimeo está no `index.html`, procure por `player.vimeo.com/video/`.
- **Prints / imagens:** todas hospedadas externamente (b-cdn, iili.io). Para trocar, é só mudar a URL.
- **Estilos e animações:** `src/style.css`.
- **Lógica (VSL, FAQ, popup de downsell):** `src/main.js`.

## Dica de performance

Para ganhar ainda mais velocidade, suba as imagens em formato WebP no seu CDN (b-cdn.net). Os PNGs atuais funcionam, mas WebP costuma pesar 60-70% menos.
