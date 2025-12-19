# Guia de Configuração - Sorteio de Bingo Online Grátis

## 📋 Checklist de Configuração

### 1. URLs e Domínio

**✅ Domínio configurado**: `https://sistema-para-bingo-online.vercel.app`

Arquivos já configurados com o domínio:

- ✅ `index.html` (meta tags, Open Graph, Twitter Cards, Schema.org)
- ✅ `sitemap.xml` (URLs do sitemap)
- ✅ `robots.txt` (URL do sitemap)

**Como fazer:**
```bash
# Use find/replace no seu editor
# ✅ Já configurado: https://sistema-para-bingo-online.vercel.app
```

### 2. Favicons e Ícones

Crie e adicione os seguintes arquivos na raiz do diretório:

- `favicon.ico` (32x32 ou 16x16)
- `favicon-16x16.png` (16x16)
- `favicon-32x32.png` (32x32)
- `apple-touch-icon.png` (180x180)
- `icon-192x192.png` (192x192) - Para PWA
- `icon-512x512.png` (512x512) - Para PWA

**Ferramentas recomendadas:**
- [Favicon Generator](https://realfavicongenerator.net/)
- [PWA Asset Generator](https://github.com/onderceylan/pwa-asset-generator)

### 3. Imagens para Redes Sociais

Crie e adicione:

- `og-image-bingo.png` (1200x630px) - Para Open Graph
- `twitter-image-bingo.png` (1200x630px) - Para Twitter Cards

**Recomendações:**
- Tamanho: 1200x630 pixels
- Formato: PNG ou JPG
- Peso: Máximo 1MB
- Inclua texto: "Sorteio de Bingo Online Grátis"

### 4. Configuração do Servidor

#### Apache (.htaccess)

O arquivo `.htaccess` já está configurado. Certifique-se de que:

- ✅ Módulo `mod_rewrite` está habilitado
- ✅ Módulo `mod_deflate` está habilitado (compressão GZIP)
- ✅ Módulo `mod_expires` está habilitado (cache)
- ✅ Módulo `mod_headers` está habilitado (headers de segurança)

**Verificar módulos:**
```bash
# No terminal do servidor
apache2ctl -M
# ou
httpd -M
```

#### Nginx

Se estiver usando Nginx, configure conforme o README.md.

### 5. SSL/HTTPS

**Obrigatório para SEO!**

- ✅ Configure certificado SSL (Let's Encrypt é gratuito)
- ✅ O `.htaccess` já força HTTPS
- ✅ Teste: https://www.ssllabs.com/ssltest/

### 6. Google Search Console

1. Acesse: https://search.google.com/search-console
2. Adicione sua propriedade
3. Verifique a propriedade (HTML tag, DNS, ou arquivo)
4. Envie o sitemap: `https://sistema-para-bingo-online.vercel.app/sitemap.xml`

### 7. Google Analytics (Opcional)

Se quiser adicionar Google Analytics, adicione no `index.html` antes do `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### 8. Testes de SEO

Após a publicação, teste:

- ✅ [Google PageSpeed Insights](https://pagespeed.web.dev/)
- ✅ [Google Mobile-Friendly Test](https://search.google.com/test/mobile-friendly)
- ✅ [Schema Markup Validator](https://validator.schema.org/)
- ✅ [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
- ✅ [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### 9. Atualização do Sitemap

Atualize a data no `sitemap.xml` sempre que fizer alterações:

```xml
<lastmod>2024-01-15</lastmod>
```

### 10. Verificação Final

Antes de publicar, verifique:

- [ ] Todas as URLs substituídas
- [ ] Favicons adicionados
- [ ] Imagens OG/Twitter criadas
- [ ] SSL/HTTPS configurado
- [ ] Sitemap.xml atualizado
- [ ] Robots.txt configurado
- [ ] .htaccess funcionando
- [ ] Páginas 404 e 500 funcionando
- [ ] Testes de SEO realizados

## 🚀 Deploy

### Opções de Hospedagem Recomendadas

1. **Netlify** (Grátis)
   - Deploy automático via Git
   - HTTPS automático
   - CDN global

2. **Vercel** (Grátis)
   - Deploy automático
   - HTTPS automático
   - Performance otimizada

3. **GitHub Pages** (Grátis)
   - Hospedagem estática
   - HTTPS automático
   - Integração com Git

4. **Hostinger/Bluehost** (Pago)
   - Hospedagem compartilhada
   - cPanel incluído
   - Suporte completo

## 📊 Monitoramento

Após o deploy, monitore:

- Google Search Console (impressões, cliques, posição)
- Google Analytics (tráfego, comportamento)
- PageSpeed Insights (performance)
- Core Web Vitals (LCP, FID, CLS)

## 🔧 Troubleshooting

### Problema: Redirecionamento HTTPS não funciona
**Solução**: Verifique se o módulo `mod_rewrite` está habilitado no Apache

### Problema: Compressão GZIP não funciona
**Solução**: Verifique se o módulo `mod_deflate` está habilitado

### Problema: Cache não funciona
**Solução**: Verifique se o módulo `mod_expires` está habilitado

### Problema: Erro 500 no servidor
**Solução**: Verifique os logs de erro do Apache/Nginx e permissões dos arquivos

---

**Última atualização**: Janeiro 2024

