# 🔧 Soluções para Problemas de Permissão

## **Principais Ajustes Feitos:**

### **1. Configurações de Segurança:**
- ✅ `signAndEditExecutable: false` - Desabilita assinatura automática
- ✅ `verifyUpdateCodeSignature: false` - Remove verificação de certificado
- ✅ `requestedExecutionLevel: "asInvoker"` - Executa com permissões do usuário
- ✅ `identity: null` - Remove identidade de desenvolvedor (macOS)

### **2. Variáveis de Ambiente:**
- ✅ `CSC_IDENTITY_AUTO_DISCOVERY=false` - Desabilita busca automática de certificado
- ✅ Certificados vazios para evitar erros

### **3. Novos Comandos Disponíveis:**

#### **Comando Principal (Recomendado):**
```bash
npm run dist
```

#### **Apenas Windows:**
```bash
npm run dist-win
```

#### **Versão Portátil (Sem Instalador):**
```bash
npm run dist-portable
```

---

## **🚀 Como Usar:**

### **Opção 1: Executável + Instalador**
```bash
npm run dist
```
- Cria instalador NSIS
- Cria versão portátil
- Ambos na pasta `dist-electron/`

### **Opção 2: Apenas Portátil (Mais Simples)**
```bash
npm run dist-portable
```
- Arquivo único `.exe`
- Não precisa instalar
- Executa direto

---

## **📁 Resultado:**

Após o build, você terá na pasta `dist-electron/`:

- **Instalador:** `Sistema de Seleção de Bombas Setup 1.0.0.exe`
- **Portátil:** `Sistema de Seleção de Bombas 1.0.0.exe`

---

## **⚠️ Se Ainda Der Erro:**

### **Windows PowerShell:**
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### **Executar como Administrador:**
1. Abra PowerShell como Administrador
2. Execute: `npm run dist-portable`

### **Antivírus:**
- Temporariamente desabilite o antivírus
- Adicione a pasta do projeto às exceções

---

## **✅ Teste Rápido:**

Antes de compilar, teste se funciona:
```bash
npm run electron-dev
```

Se abrir o app, então pode compilar com segurança!