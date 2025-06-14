# 🚀 Comandos para Compilar o Executável

## **Opção 1: Electron (Recomendado)**

### **1. Testar em Desenvolvimento:**
```bash
npm run electron-dev
```
*Abre o app em modo desenvolvimento para testar*

### **2. Compilar Executável:**
```bash
npm run dist
```
*Gera o executável final na pasta `dist-electron/`*

### **3. Build Apenas (sem instalador):**
```bash
npm run build-electron
```
*Cria apenas o executável, sem instalador*

---

## **Opção 2: Build Web (para PWA)**

### **Build para Web:**
```bash
npm run build
```
*Gera arquivos otimizados na pasta `dist/` para hospedar online*

### **Preview do Build:**
```bash
npm run preview
```
*Testa o build localmente*

---

## **📁 Onde Encontrar os Arquivos:**

### **Executável Electron:**
- **Pasta:** `dist-electron/`
- **Windows:** `.exe` + instalador
- **Arquivos:** Prontos para distribuir

### **Build Web:**
- **Pasta:** `dist/`
- **Arquivos:** Para hospedar em servidor web

---

## **🎯 Comando Recomendado:**

Para criar o executável desktop:
```bash
npm run dist
```

Este comando vai:
1. ✅ Fazer build da aplicação web
2. ✅ Criar o executável do Electron
3. ✅ Gerar instalador (se configurado)
4. ✅ Colocar tudo na pasta `dist-electron/`

---

## **⚠️ Possíveis Problemas:**

### **Erro de Permissão (Windows):**
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### **Falta de Ícone:**
- Crie pasta `assets/`
- Adicione `icon.ico` (Windows)
- Adicione `icon.png` (Linux)

### **Build Demora Muito:**
- É normal na primeira vez
- Pode demorar 5-10 minutos
- Dependências são baixadas automaticamente

---

## **🔍 Verificar se Funcionou:**

Após `npm run dist`, verifique:
- Pasta `dist-electron/` foi criada
- Contém arquivos `.exe` (Windows)
- Tamanho aproximado: 100-200MB

---

## **🚀 Executar o App:**

Depois de compilado:
1. Vá para `dist-electron/`
2. Execute o arquivo `.exe`
3. O app abre como programa nativo!