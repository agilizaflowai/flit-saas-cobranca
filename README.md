# 🚀 SaaS Cobrança - Deploy GitHub Pages

Esta pasta contém todos os arquivos necessários para hospedar o SaaS de Cobrança no GitHub Pages.

## 📋 Como usar

### 1. Criar repositório no GitHub
1. Acesse [GitHub](https://github.com) e faça login
2. Clique em "New repository"
3. Nomeie o repositório (ex: `saas-cobranca`)
4. Marque como **público** (obrigatório para GitHub Pages gratuito)
5. Clique em "Create repository"

### 2. Fazer upload dos arquivos
1. **Arraste toda esta pasta** para o repositório criado
2. Ou use o comando git:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```

### 3. Configurar Secrets
No seu repositório GitHub:
1. Vá em **Settings > Secrets and variables > Actions**
2. Clique em **New repository secret**
3. Adicione estas secrets:
   - `VITE_SUPABASE_URL`: Sua URL do Supabase
   - `VITE_SUPABASE_ANON_KEY`: Sua chave anônima do Supabase

### 4. Habilitar GitHub Pages
1. Vá em **Settings > Pages**
2. Em **Source**, selecione **GitHub Actions**
3. O deploy será automático!

### 5. Configurar nome do repositório
Se seu repositório tiver nome diferente de `SAAS-Cobranca-Integrado`:
1. Edite `vite.config.ts`
2. Altere a linha: `base: '/SEU-NOME-DO-REPOSITORIO/'`
3. Edite `package.json`
4. Altere o script `build:github` com o nome correto

## 📁 Arquivos incluídos

- ✅ Código fonte completo (`src/`)
- ✅ Assets públicos (`public/`)
- ✅ Configurações de build
- ✅ Workflow GitHub Actions (`.github/workflows/deploy.yml`)
- ✅ Exemplo de variáveis de ambiente (`.env.example`)

## 🌐 Acesso

Após o deploy, seu site estará em:
`https://SEU-USUARIO.github.io/SEU-REPOSITORIO/`

## 🆘 Suporte

Se tiver problemas:
1. Verifique se as secrets estão configuradas
2. Confirme se o repositório é público
3. Verifique os logs do GitHub Actions
4. Teste o build local com `npm run build`

---

✅ **Pronto para arrastar e hospedar!** 🎉