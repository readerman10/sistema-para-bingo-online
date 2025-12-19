# Sorteio de Bingo Online Grátis

Painel web completo para gerenciar sorteios de bingo com interface moderna e funcionalidades avançadas.

## 🎯 Características

- ✅ **Sorteio Aleatório**: Sorteio completamente aleatório de bolas
- ✅ **Gerenciamento de Participantes**: Cadastro e edição ilimitada de participantes
- ✅ **Gerenciamento de Prêmios**: Controle total sobre prêmios e vencedores
- ✅ **Histórico Completo**: Visualização de todas as bolas sorteadas
- ✅ **Exportação/Importação**: Backup e restauração de dados em JSON
- ✅ **Salvamento Automático**: Dados salvos automaticamente no navegador
- ✅ **Atalhos de Teclado**: Espaço (sortear), Ctrl+Z (desfazer), F (tela cheia)
- ✅ **Interface Responsiva**: Adaptável a diferentes tamanhos de tela
- ✅ **Tema Moderno**: Design profissional com gradientes e animações
- ✅ **100% Gratuito**: Sem custos, sem cadastro, sem limites

## 🚀 Como Usar

1. Abra o arquivo `index.html` no navegador
2. Configure o número máximo de bolas (padrão: 75)
3. Adicione participantes e prêmios na seção "Gerenciar"
4. Use "Sortear bola" para iniciar o sorteio
5. Registre os vencedores conforme as bolas são sorteadas

## 📁 Estrutura de Arquivos

```
Bin/
├── index.html          # Página principal do aplicativo
├── robots.txt          # Instruções para crawlers
├── sitemap.xml         # Mapa do site para SEO
├── .htaccess          # Configurações do servidor (Apache)
├── 404.html           # Página de erro 404
├── 500.html           # Página de erro 500
└── README.md          # Este arquivo
```

## 🔧 Configuração do Servidor

### Apache (.htaccess)

O arquivo `.htaccess` já está configurado com:
- Redirecionamento HTTPS
- Compressão GZIP
- Cache do navegador
- Headers de segurança
- UTF-8 encoding

### Nginx

Se estiver usando Nginx, adicione ao seu `nginx.conf`:

```nginx
# Compressão GZIP
gzip on;
gzip_types text/html text/css application/javascript application/json;

# Cache
location ~* \.(jpg|jpeg|png|gif|ico|css|js|woff|woff2)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
}

# HTTPS redirect
if ($scheme != "https") {
    return 301 https://$host$request_uri;
}
```

## 🔍 SEO

O projeto está otimizado para SEO com:
- Meta tags completas
- Open Graph e Twitter Cards
- Schema.org structured data (JSON-LD)
- Sitemap.xml
- Robots.txt
- Conteúdo otimizado para keywords
- Breadcrumbs estruturados

**Keyword Principal**: Sorteio de bingo online grátis

## 📱 Responsividade

O aplicativo é totalmente responsivo e funciona em:
- Desktop
- Tablets
- Smartphones

## 🎨 Tecnologias

- HTML5
- CSS3 (com variáveis CSS)
- JavaScript Vanilla (sem dependências)
- LocalStorage para persistência

## 📝 Licença

Este projeto é gratuito e de código aberto. Use como desejar.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## 📧 Suporte

Para dúvidas ou sugestões, abra uma issue no repositório.

---

**Desenvolvido com ❤️ para facilitar sorteios de bingo**

