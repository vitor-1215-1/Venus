# 🎯 Guia Completo: Como Criar SUA Loja Online

## 👋 Bem-vindo(a)!

Este guia vai te ajudar a criar sua própria loja online em **menos de 30 minutos**, completamente **GRÁTIS**!

---

## ✅ O Que Você Vai Ter

- 🛍️ Loja online profissional
- 📱 Design responsivo (funciona no celular)
- 🛒 Carrinho de compras
- 💰 Pagamento via PIX
- 📊 Painel administrativo
- 🔐 Login com Google/Facebook
- 🗄️ Banco de dados gratuito
- 🌐 Link próprio: `seu-nome.github.io/sua-loja`

**Tudo 100% GRATUITO! Sem mensalidades!**

---

## 📋 Pré-requisitos

Você vai precisar:
- [ ] Email (Gmail recomendado)
- [ ] 30 minutos de tempo
- [ ] Chave PIX (CPF, email ou celular)
- [ ] Fotos dos seus produtos (opcional para começar)

**Não precisa saber programar!**

---

## 🚀 Passo a Passo

### **ETAPA 1: Criar Conta no GitHub** (5 minutos)

1. Acesse: **https://github.com/signup**
2. Preencha:
   - **Email:** seu melhor email
   - **Password:** crie uma senha forte
   - **Username:** escolha um nome (ex: `mariamodas`)
3. Verifique seu email
4. Faça login no GitHub

---

### **ETAPA 2: Copiar o Template** (2 minutos)

1. Acesse o repositório template:
   ```
   github.com/[NOME-DO-CRIADOR]/ecommerce-template
   ```
   *(O criador do sistema vai fornecer este link)*

2. Clique no botão **Fork** (canto superior direito)

3. Configure seu fork:
   - **Repository name:** Escolha o nome da sua loja
     - Exemplos: `minha-boutique`, `loja-artesanato`, `modas-maria`
   - **Description:** "Minha loja online"
   - Deixe marcado: **Public**

4. Clique em **Create fork**

**Pronto! Você copiou o sistema para sua conta!**

---

### **ETAPA 3: Ativar Sua Loja** (3 minutos)

1. No SEU repositório (agora em `github.com/seu-usuario/nome-loja`)
2. Clique em **Settings** (configurações)
3. No menu esquerdo, clique em **Pages**
4. Em **Source**, selecione:
   - **Branch:** main
   - **Folder:** / (root)
5. Clique em **Save**
6. **Aguarde 2-3 minutos**
7. Recarregue a página
8. Você verá: "Your site is live at..."

**Anote seus links:**

📝 **Sua Loja:**
```
https://seu-usuario.github.io/nome-loja/store/
```

📝 **Seu Painel Admin:**
```
https://seu-usuario.github.io/nome-loja/admin/
```

---

### **ETAPA 4: Configurar Banco de Dados** (15 minutos)

Seu banco de dados será no **Firebase** (Google) - totalmente gratuito!

#### 4.1 - Criar Projeto Firebase

1. Acesse: **https://console.firebase.google.com**
2. Faça login com sua conta Google
3. Clique em **Add project** (Adicionar projeto)
4. Nome: `minha-loja` (ou outro)
5. Desative Google Analytics (não precisa)
6. Clique em **Create project**
7. Aguarde 30 segundos
8. Clique em **Continue**

#### 4.2 - Criar Banco de Dados

1. No menu esquerdo, clique em **Firestore Database**
2. Clique em **Create database**
3. Selecione: **Start in production mode**
4. **Location:** southamerica-east1 (São Paulo)
5. Clique em **Enable**
6. Aguarde 1-2 minutos

#### 4.3 - Configurar Segurança

1. Na aba **Rules**, cole este código:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /products/{productId} {
      allow read: if true;
      allow write: if request.auth != null;
    }
    match /orders/{orderId} {
      allow read, write: if request.auth != null;
    }
    match /notifications/{notificationId} {
      allow read, write: if request.auth != null;
    }
    match /settings/{settingId} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}
```

2. Clique em **Publish**

#### 4.4 - Ativar Login com Google

1. No menu esquerdo, clique em **Authentication**
2. Clique em **Get started**
3. Clique em **Google**
4. Ative o botão
5. **Support email:** seu email
6. Clique em **Save**

#### 4.5 - Pegar Suas Credenciais

1. Na página inicial do Firebase, clique no ícone **</>** (Web)
2. **App nickname:** "Minha Loja"
3. Clique em **Register app**
4. **COPIE** todo o código `firebaseConfig`:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyC...",
  authDomain: "minha-loja.firebaseapp.com",
  projectId: "minha-loja-12345",
  storageBucket: "minha-loja.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```

**GUARDE ESTE CÓDIGO!** Você vai precisar dele no próximo passo.

---

### **ETAPA 5: Colar as Credenciais** (5 minutos)

Agora você vai colar suas credenciais do Firebase no código:

#### 5.1 - Editar admin-script.js

1. No seu repositório GitHub, navegue até: `admin/admin-script.js`
2. Clique no arquivo
3. Clique no ícone de **lápis** (Edit this file)
4. **Encontre estas linhas** (no início do arquivo):

```javascript
const firebaseConfig = {
    apiKey: "SUA_API_KEY_AQUI",
    authDomain: "seu-projeto.firebaseapp.com",
    // ...
};
```

5. **SUBSTITUA** pelo código que você copiou do Firebase
6. Role até o final da página
7. Em "Commit changes", escreva: `Configurar Firebase`
8. Clique em **Commit changes**

#### 5.2 - Editar store-script.js

**REPITA O MESMO PROCESSO** para o arquivo: `store/store-script.js`

1. Navegue até `store/store-script.js`
2. Clique em editar (lápis)
3. Substitua as credenciais
4. Commit changes

**Aguarde 2 minutos para as mudanças subirem para o site.**

---

### **ETAPA 6: Configurar Sua Loja** (5 minutos)

Agora vamos configurar as informações da sua loja!

1. Acesse seu **painel admin**:
   ```
   https://seu-usuario.github.io/nome-loja/admin/
   ```

2. Clique em **Entrar com Google**

3. Vá na aba **Configurações** (menu lateral)

4. Preencha TUDO:
   - **Nome da Loja:** O nome que aparecerá no site
   - **Logo:** Clique para fazer upload (ou cole URL de imagem)
   - **Descrição:** Descreva sua loja
   - **Email:** Seu email de contato
   - **Telefone/WhatsApp:** Seu número com DDD
   - **Chave PIX:** Sua chave PIX (pode ser CPF, email ou celular)
   - **Nome do Titular PIX:** Seu nome completo

5. Clique em **Salvar Configurações**

**Parabéns! Sua loja está configurada!**

---

### **ETAPA 7: Adicionar Produtos** (Quanto tempo quiser)

1. No painel admin, clique em **Produtos**
2. Clique em **+ Adicionar Produto**
3. Preencha:
   - **Nome:** Nome do produto
   - **Categoria:** Feminino, Masculino ou Acessórios
   - **Preço:** Valor em reais
   - **Descrição:** Descreva o produto
   - **Badge:** (opcional) Ex: "Novo", "Promoção"
   - **Status:** Ativo (para aparecer na loja)
   - **URL da Imagem:** Cole o link da foto do produto*
   
4. Clique em **Salvar**

**Como conseguir URL da imagem:**
- Opção 1: Use ImgBB (https://imgbb.com) - gratuito
- Opção 2: Use Google Photos (botão direito → Copiar endereço da imagem)
- Opção 3: Use qualquer host de imagens

**Adicione quantos produtos quiser!**

---

## 🎉 Pronto! Sua Loja Está no Ar!

Acesse sua loja pública:
```
https://seu-usuario.github.io/nome-loja/store/
```

**Compartilhe este link com seus clientes!**

---

## 📱 Como Compartilhar

### WhatsApp Status
```
🛍️ Minha loja online está no ar!
Confira: [seu-link]
```

### Instagram Bio
```
🛒 Loja online
👇 Link abaixo
[seu-link]
```

### Facebook
Crie uma página e fixe o link no topo!

---

## 💡 Dicas Importantes

### ✅ FAÇA:
- Adicione fotos reais dos produtos
- Escreva descrições detalhadas
- Responda rápido no WhatsApp
- Atualize o estoque regularmente
- Teste fazer um pedido completo

### ❌ NÃO FAÇA:
- Não coloque produtos sem foto
- Não esqueça de configurar o PIX
- Não deixe produtos "inativos" aparecendo
- Não ignore as notificações de pedidos

---

## 🔄 Como Atualizar

### Mudar Preços/Adicionar Produtos:
1. Entre no painel admin
2. Faça as alterações
3. Salvar

**Atualização é instantânea!**

### Mudar Cores/Layout:
Você vai precisar editar os arquivos no GitHub (mais avançado).
Contrate um desenvolvedor ou peça ajuda na comunidade.

---

## 💰 Custos

### GRATUITO (Até 500 visitas/dia):
- ✅ GitHub Pages: Grátis
- ✅ Firebase Spark: Grátis
- ✅ Tudo funciona 100%

### Se Crescer Muito:
- Firebase Blaze: Paga só o que usar (~R$50-100/mês)
- Domínio próprio: ~R$40/ano (opcional)

**Mas para começar: R$ 0,00!**

---

## 🆘 Problemas Comuns

### "Não consigo fazer login"
- Use uma conta Google
- Permita pop-ups no navegador
- Limpe o cache: Ctrl + Shift + Del

### "Firebase não está conectado"
- Verifique se colou as credenciais corretas
- Verifique se as regras de segurança foram salvas
- Aguarde 5 minutos após fazer mudanças

### "Produtos não aparecem"
- Verifique se o status está "Ativo"
- Recarregue a página (Ctrl + F5)
- Verifique o console (F12) por erros

### "PIX não aparece no checkout"
- Verifique se configurou a chave PIX
- Salve as configurações novamente
- Limpe o cache do navegador

---

## 🎓 Próximos Passos

Depois que sua loja estiver funcionando:

1. ✅ Divulgue nas redes sociais
2. ✅ Crie conteúdo (fotos, vídeos)
3. ✅ Considere anúncios pagos (Instagram/Facebook)
4. ✅ Ofereça promoções
5. ✅ Peça avaliações dos clientes
6. ✅ Considere um domínio próprio (minhaloja.com.br)

---

## 🤝 Comunidade

Entre no grupo para tirar dúvidas e trocar experiências:

- **Telegram:** [link-do-grupo]
- **WhatsApp:** [link-do-grupo]
- **Discord:** [https://discord.gg/UyDmyVUKKx]

---

## 🌟 Sucesso!

Sua loja está pronta! Agora é só divulgar e vender!

**Boa sorte com seu negócio! 🚀💰**

---

*Dúvidas? Abra uma issue no GitHub ou entre em contato!*