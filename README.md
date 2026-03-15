# FieldConnex Diagnóstico — PWA

App de diagnóstico de campo para o DM-AM · FOUNDATION Fieldbus & PROFIBUS PA · Pepperl+Fuchs.

---

## 📁 Estrutura de arquivos

```
fieldconnex-app/
├── index.html       ← App completo (guia, calculadora, ocorrências, termos)
├── manifest.json    ← Configura o app (nome, ícone, cor, tela cheia)
├── sw.js            ← Service Worker (offline + instalável)
├── icons/
│   ├── icon-192.png ← Ícone do app (tela inicial Android)
│   └── icon-512.png ← Ícone maior (splash screen)
└── README.md        ← Este arquivo
```

---

## 🚀 Como publicar no GitHub Pages (passo a passo)

### 1. Criar conta no GitHub
Acesse https://github.com e crie uma conta gratuita se ainda não tiver.

### 2. Criar um repositório novo
- Clicar em **"New repository"** (botão verde)
- Nome sugerido: `fieldconnex-app`
- Deixar como **Public**
- Clicar em **"Create repository"**

### 3. Fazer upload dos arquivos
- Na página do repositório, clicar em **"uploading an existing file"**
- Arrastar TODOS os arquivos desta pasta (index.html, manifest.json, sw.js)
- Arrastar também a pasta **icons** com os dois ícones
- Clicar em **"Commit changes"**

### 4. Ativar o GitHub Pages
- Ir em **Settings** (engrenagem no topo do repositório)
- No menu lateral, clicar em **Pages**
- Em "Source", selecionar **Deploy from a branch**
- Em "Branch", selecionar **main** e pasta **/ (root)**
- Clicar em **Save**

### 5. Aguardar ~2 minutos
O GitHub vai gerar a URL do seu app automaticamente. Aparecerá algo como:

```
https://SEU-USUARIO.github.io/fieldconnex-app/
```

---

## 📲 Como o técnico instala no celular

### Android (Chrome)
1. Abrir a URL no Chrome
2. Chrome exibe banner automático: **"Instalar FieldConnex"**
3. Tocar em **Instalar**
4. O ícone aparece na tela inicial — funciona como app nativo

### iPhone (Safari)
1. Abrir a URL no Safari
2. Tocar no ícone de **Compartilhar** (quadrado com seta para cima)
3. Rolar e tocar em **"Adicionar à Tela de Início"**
4. Confirmar o nome e tocar em **Adicionar**

---

## 🔄 Como atualizar o app

1. Editar o arquivo `index.html` com as novas informações
2. No repositório do GitHub, clicar no arquivo → ícone de lápis (editar)
3. Fazer as alterações e clicar em **"Commit changes"**
4. Aguardar ~1 minuto — o app atualiza automaticamente para todos os técnicos

Para forçar atualização do cache offline, incrementar o número de versão no `sw.js`:
```js
const CACHE_NAME = 'fieldconnex-v2'; // ← mudar de v1 para v2
```

---

## ✅ Funcionalidades offline

Após a primeira abertura com internet, o app funciona completamente sem conexão:
- ✅ Guia de diagnóstico completo
- ✅ Calculadora de segmento
- ✅ Registro de ocorrências com foto (salvas no dispositivo)
- ✅ Glossário de termos técnicos

---

## 📞 Suporte

Dúvidas sobre o app: consultar o técnico responsável pelo projeto.
Dúvidas sobre o DM-AM: suporte Pepperl+Fuchs.
