# 🛍️ Sistema Multi-Loja - E-commerce Open Source

## 🎯 O Que É?

Um sistema **gratuito e open source** para criar lojas online individuais. Cada pessoa pode ter sua própria loja com seu próprio link!

## 🌟 Como Funciona?

### Para VOCÊ (desenvolvedor):
- Disponibiliza o código público no GitHub
- Outras pessoas podem fazer "fork" e criar suas lojas

### Para CADA LOJISTA:
- Faz fork do repositório
- Configura sua loja (nome, produtos, PIX)
- Tem seu próprio link: `usuario.github.io/nome-loja`
- Banco de dados separado (cada um tem o seu)

---

## 🏗️ Estrutura do Sistema

```
Template Base (seu repositório público)
    ↓ fork
Loja do João (joao.github.io/minha-loja)
    ↓ fork  
Loja da Maria (maria.github.io/boutique)
    ↓ fork
Loja do Pedro (pedro.github.io/store)
```

**Cada loja é INDEPENDENTE e tem seus próprios:**
- ✅ Produtos
- ✅ Configurações
- ✅ Banco de dados Firebase
- ✅ Link único
- ✅ Admin próprio

---

## 📁 Arquivos Incluídos

```
ecommerce-template/
├── index.html (página inicial)
├── admin/
│   ├── index.html (painel administrativo)
│   └── admin-script.js
├── store/
│   ├── index.html (loja pública)
│   └── store-script.js
├── docs/
│   ├── SETUP-GUIDE.md (guia de configuração)
│   ├── FIREBASE-CONFIG.md (configurar banco de dados)
│   └── CUSTOMIZE.md (personalizar a loja)
└── README.md (este arquivo)
```

---

## 🚀 Para Lojistas: Como Criar Sua Loja

### Passo 1: Fork do Repositório

1. Acesse: `github.com/SEU-USUARIO/ecommerce-template`
2. Clique em **Fork** (canto superior direito)
3. Escolha um nome para sua loja (ex: `minha-boutique`)
4. Clique em **Create fork**

### Passo 2: Ativar GitHub Pages

1. No SEU fork, vá em **Settings**
2. Clique em **Pages**
3. Source: **main** branch, **/ (root)**
4. Clique em **Save**
5. Aguarde 2 minutos

**Sua loja estará em:**
```
https://seu-usuario.github.io/nome-da-loja/store/
```

**Seu painel admin:**
```
https://seu-usuario.github.io/nome-da-loja/admin/
```

### Passo 3: Configurar Firebase (Seu Banco de Dados)

1. Leia o arquivo `docs/FIREBASE-CONFIG.md`
2. Crie SEU projeto Firebase
3. Cole SUAS credenciais nos arquivos
4. Pronto! Banco de dados funcionando!

### Passo 4: Personalizar Sua Loja

1. Acesse o painel admin
2. Faça login com Google
3. Configure:
   - Nome da loja
   - Logo
   - Descrição
   - Email e WhatsApp
   - **Chave PIX** (obrigatório)
4. Adicione seus produtos
5. Compartilhe o link!

---

## 💡 Para Desenvolvedores: Como Disponibilizar

### Opção 1: Repositório Público (Recomendado)

```bash
# 1. Crie um repositório público
# 2. Nomeie: ecommerce-template (ou outro)
# 3. Suba todos os arquivos
# 4. Adicione um bom README
# 5. Ative GitHub Pages (para demo)
```

**Seu repositório será:**
```
github.com/SEU-USUARIO/ecommerce-template
```

**Demo estará em:**
```
https://seu-usuario.github.io/ecommerce-template/store/
```

### Opção 2: Marketplace GitHub

1. Adicione tag `ecommerce-template`
2. Adicione tag `online-store`
3. Adicione tag `firebase`
4. Adicione licença MIT
5. Pessoas podem descobrir via busca

### Opção 3: Website Próprio

Crie um site explicando:
- O que é o sistema
- Como fazer fork
- Tutorial em vídeo
- Link para o repositório

---

## 🔐 Segurança e Privacidade

### Cada loja tem:
- ✅ Banco de dados Firebase SEPARADO
- ✅ Autenticação própria
- ✅ Dados isolados
- ✅ Configurações independentes

### Você (desenvolvedor) NÃO tem acesso:
- ❌ Aos produtos das lojas
- ❌ Aos pedidos
- ❌ Às configurações
- ❌ Aos dados dos clientes

### Como funciona:
```
Você disponibiliza: CÓDIGO (open source)
Lojista cria: FIREBASE próprio
Resultado: Dados ficam no Firebase DO LOJISTA
```

---

## 📊 Exemplos de Uso

### Loja de Roupas
```
github.com/maria/boutique-maria
→ https://maria.github.io/boutique-maria/store/
```

### Loja de Artesanato
```
github.com/joao/artesanato-joao
→ https://joao.github.io/artesanato-joao/store/
```

### Loja de Cosméticos
```
github.com/ana/cosmeticos-ana
→ https://ana.github.io/cosmeticos-ana/store/
```

**Cada uma TOTALMENTE independente!**

---

## 🎨 Personalização

Os lojistas podem personalizar:
- ✅ Cores (via CSS)
- ✅ Logo
- ✅ Nome da loja
- ✅ Categorias de produtos
- ✅ Layout (editando HTML)
- ✅ Funcionalidades (editando JS)

Leia: `docs/CUSTOMIZE.md`

---

## 💰 Modelo de Negócio

### Gratuito (GitHub Pages + Firebase Spark)
- ✅ Totalmente grátis
- ✅ 50mil leituras/dia
- ✅ Ideal para começar

### Pago (Se lojista crescer)
- Upgrade Firebase (Blaze): paga só o que usar
- Domínio próprio: ~R$40/ano
- Hospedagem premium (opcional)

**Você (desenvolvedor) não precisa pagar nada!**

---

## 📈 Roadmap

### Versão Atual (v1.0)
- ✅ Sistema de produtos
- ✅ Carrinho de compras
- ✅ Checkout com PIX
- ✅ Painel admin
- ✅ Seletor de tamanhos
- ✅ Notificações
- ✅ Firebase integrado

### Próximas Versões
- [ ] Sistema de cupons
- [ ] Frete calculado
- [ ] Múltiplos métodos de pagamento
- [ ] Relatórios de vendas
- [ ] Integração com correios
- [ ] App mobile

---

## 🤝 Como Contribuir

Se você é desenvolvedor e quer melhorar o sistema:

1. Fork este repositório
2. Crie uma branch: `git checkout -b feature/nova-funcionalidade`
3. Commit suas mudanças: `git commit -m 'Adiciona nova funcionalidade'`
4. Push para a branch: `git push origin feature/nova-funcionalidade`
5. Abra um Pull Request

---

## 📄 Licença

MIT License - Livre para uso comercial e pessoal

```
Copyright (c) 2026 [Seu Nome]

É concedida permissão para usar, copiar, modificar e distribuir
este software gratuitamente.
```

---

## 🆘 Suporte

### Para Lojistas:
- Leia: `docs/SETUP-GUIDE.md`
- Issues: Use a aba Issues do GitHub
- Comunidade: Crie um Discord/Telegram

### Para Desenvolvedores:
- Documentação: `docs/`
- API: Comentada nos arquivos .js
- Contribuições: Pull Requests são bem-vindos!

---

## 📞 Links

- **Repositório:** github.com/SEU-USUARIO/ecommerce-template
- **Demo:** seu-usuario.github.io/ecommerce-template/store/
- **Documentação:** github.com/SEU-USUARIO/ecommerce-template/wiki
- **Issues:** github.com/SEU-USUARIO/ecommerce-template/issues

---

## 🎯 Casos de Sucesso

*Adicione aqui lojas que usaram o sistema!*

1. **Boutique da Maria** - 100+ vendas/mês
2. **Artesanato João** - 50+ produtos
3. **Cosméticos Ana** - R$5mil/mês

---

## 🌟 Star o Projeto!

Se você gostou do sistema, dê uma ⭐ no repositório!

Isso ajuda outras pessoas a descobrirem o projeto.

---

## ✨ Agradecimentos

Obrigado a todos que usam e contribuem com o sistema!

---

**Comece agora: Faça fork e crie sua loja em 10 minutos! 🚀**