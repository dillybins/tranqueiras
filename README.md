# ⬡ GARAGE — Biblioteca de Anúncios de Carros

Site privado para salvar e compartilhar anúncios de carros encontrados na OLX, Facebook Marketplace, Webmotors, etc.

---

## 🚀 Como publicar no GitHub Pages

### 1. Crie o repositório
- Vá em [github.com/new](https://github.com/new)
- Dê um nome (ex: `garage-carros` — pode ser qualquer nome)
- Deixe como **Public** (necessário para GitHub Pages gratuito)
- Clique em **Create repository**

### 2. Faça upload dos arquivos
Suba estes 3 arquivos para o repositório:
- `index.html`
- `admin.html`
- `data.json`

Você pode arrastar direto pela interface do GitHub.

### 3. Ative o GitHub Pages
- Vá em **Settings** → **Pages**
- Em "Source", selecione **Deploy from a branch**
- Branch: **main**, pasta: **/ (root)**
- Clique em **Save**

### 4. Acesse o site
Após ~2 minutos, o site estará em:
```
https://SEU_USUARIO.github.io/SEU_REPOSITORIO/
```

O painel admin fica em:
```
https://SEU_USUARIO.github.io/SEU_REPOSITORIO/admin.html
```

---

## ⚙️ Configuração

### Senhas
Edite as senhas direto nos arquivos HTML:

**`index.html`** — linha com `CONFIG`:
```js
const CONFIG = {
  password: 'garage2025',    // ← senha para ver o site
  githubUser: 'SEU_USUARIO',
  githubRepo: 'SEU_REPOSITORIO',
};
```

**`admin.html`** — linha:
```js
const ADMIN_PASSWORD = 'admin2025';  // ← senha do painel admin
```

### Token do GitHub (para o Admin funcionar)
1. Acesse [github.com/settings/tokens](https://github.com/settings/tokens)
2. Clique em **Generate new token (classic)**
3. Dê um nome (ex: "Garage Admin")
4. Marque a permissão **repo** (acesso total a repositórios)
5. Clique em **Generate token** e copie o token
6. No painel admin do site, cole o token na configuração

O token fica salvo só no seu navegador (localStorage) — nunca vai para o GitHub.

---

## 📱 Como usar

### Adicionar um anúncio
1. Abra `seusite.github.io/seurepositorio/admin.html`
2. Digite a senha admin
3. Cole a URL do anúncio
4. Preencha título, preço, ano, km, etc.
5. Clique em **+ Adicionar**
6. Em ~30 segundos o site principal já mostra o novo anúncio

### Compartilhar
- Envie o link `seusite.github.io/seurepositorio/` para seus amigos
- Eles precisarão da senha para ver os anúncios
- A senha fica salva na sessão (não precisa digitar de novo se fechar e abrir a aba)

---

## 🔒 Privacidade

- O repositório é público, mas o conteúdo do site é protegido por senha
- Qualquer pessoa que **souber a URL exata** pode tentar adivinhar a senha
- Para mais segurança, use um nome de repositório aleatório (ex: `garage-xk7m2q`)
- A senha é verificada no cliente (JavaScript) — não é segurança de nível bancário, mas serve para uso pessoal/familiar

---

## 🛠️ Fontes suportadas
- OLX
- Facebook Marketplace
- Webmotors
- iCarros
- Qualquer outro site (categoria "Outro")
