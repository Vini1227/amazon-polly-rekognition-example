# 🎤 VisionVoice - Node.js + AWS

Aplicação Node.js que usa **AWS Rekognition** para analisar imagens e **AWS Polly** para gerar áudio narrado em português.

## ✨ Solução Limpa

- ✅ **Backend Node.js**: Toda lógica no servidor
- ✅ **Tradução automática**: Usa biblioteca Google Translate
- ✅ **Código simples**: Sem dicionários gigantes
- ✅ **Seguro**: Credenciais no servidor

---

## 🚀 Como Usar

### 1. Instalar dependências

```bash
npm install
```

### 2. Configurar credenciais AWS

Edite o arquivo `.env`:

```env
AWS_ACCESS_KEY_ID=AKIA...
AWS_SECRET_ACCESS_KEY=abc123...
AWS_REGION=us-east-1
PORT=3000
```

### 3. Iniciar o servidor

```bash
npm start
```

Ou com auto-reload:
```bash
npm run dev
```

### 4. Acessar a aplicação

Abra o navegador em: **http://localhost:3000**

---

## 📁 Estrutura

```
projeto/
├── server.js              # Backend Node.js
├── package.json           # Dependências
├── .env                   # Credenciais AWS
└── public/
    ├── index.html         # Frontend
    ├── styles.css         # Design
    └── script.js          # Lógica do cliente
```

---

## 🔧 Como Funciona

### Backend (`server.js`):
1. Recebe imagem do frontend
2. Chama AWS Rekognition (detecta objetos + rostos)
3. Monta descrição em inglês
4. **Traduz automaticamente** para português (biblioteca Google Translate)
5. Chama AWS Polly para gerar áudio
6. Retorna descrição + áudio para o frontend

### Frontend (`public/script.js`):
- Upload de imagem
- Envia para API `/api/process-image`
- Exibe resultado + player de áudio

---

## 📦 Dependências

- **express**: Servidor web
- **multer**: Upload de arquivos
- **aws-sdk**: AWS Rekognition e Polly
- **@vitalets/google-translate-api**: Tradução automática
- **dotenv**: Variáveis de ambiente
- **cors**: CORS

---

## 🎯 Vantagens

✅ Código muito mais limpo e simples  
✅ Tradução automática (sem dicionários manuais)  
✅ Credenciais seguras no servidor  
✅ Fácil de expandir e manter  
✅ Melhor para apresentação técnica  

---

## 🐛 Troubleshooting

**Erro de tradução:**
- A biblioteca de tradução é gratuita mas pode ter limites
- Se falhar, usa o texto em inglês

**Erro AWS:**
- Verifique credenciais no `.env`
- Confirme permissões IAM para Rekognition e Polly

---

**Pronto para rodar!** 🚀# amazon-polly-rekognition-example
