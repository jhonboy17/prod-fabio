# Sistema de Login com MongoDB Atlas e Vercel

Sistema completo de autenticação com cadastro e login, utilizando Node.js, Express, MongoDB Atlas e preparado para deploy no Vercel.

## 🚀 Funcionalidades

- ✅ Cadastro de usuários (nome, email, senha)
- ✅ Login de usuários
- ✅ Criptografia de senhas com bcrypt
- ✅ Autenticação JWT
- ✅ Interface responsiva e moderna
- ✅ Integração com MongoDB Atlas
- ✅ Pronto para deploy no Vercel

## 📋 Pré-requisitos

- Node.js instalado (versão 14 ou superior)
- Conta no MongoDB Atlas
- Conta no Vercel (para deploy)

## ⚙️ Configuração do MongoDB Atlas

1. Acesse [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Crie uma conta gratuita (se ainda não tiver)
3. Crie um novo cluster (opção gratuita M0)
4. Clique em "Connect" no seu cluster
5. Escolha "Connect your application"
6. Copie a connection string
7. Substitua `<password>` pela senha do seu usuário do banco

## 🔧 Instalação Local

1. Clone ou baixe este projeto

2. Instale as dependências:
```bash
npm install
```

3. Crie um arquivo `.env` na raiz do projeto:
```env
MONGODB_URI=mongodb+srv://seu_usuario:sua_senha@cluster.mongodb.net/login_db?retryWrites=true&w=majority
JWT_SECRET=sua_chave_secreta_super_segura_aqui
PORT=3000
```

4. Execute o servidor:
```bash
npm start
```

5. Acesse no navegador: `http://localhost:3000`

## 🌐 Deploy no Vercel

### Opção 1: Via CLI do Vercel

1. Instale a CLI do Vercel:
```bash
npm install -g vercel
```

2. Faça login no Vercel:
```bash
vercel login
```

3. Deploy do projeto:
```bash
vercel
```

4. Configure as variáveis de ambiente no Vercel:
   - Acesse o dashboard do Vercel
   - Vá em Settings > Environment Variables
   - Adicione:
     - `MONGODB_URI` = sua connection string do MongoDB
     - `JWT_SECRET` = sua chave secreta JWT

### Opção 2: Via GitHub

1. Crie um repositório no GitHub e faça push do código
2. Acesse [Vercel](https://vercel.com)
3. Clique em "Import Project"
4. Selecione seu repositório
5. Configure as variáveis de ambiente (MONGODB_URI e JWT_SECRET)
6. Faça o deploy!

## 📁 Estrutura do Projeto

```
├── index.html          # Página principal com formulários
├── style.css           # Estilos da aplicação
├── app.js             # JavaScript do frontend
├── server.js          # Servidor Node.js/Express
├── package.json       # Dependências do projeto
├── vercel.json        # Configuração do Vercel
├── .env.example       # Exemplo de variáveis de ambiente
├── .gitignore         # Arquivos ignorados pelo Git
└── README.md          # Este arquivo
```

## 🔒 Segurança

- Senhas são criptografadas com bcrypt
- Autenticação via JWT (JSON Web Tokens)
- Validação de dados no backend
- Proteção contra usuários duplicados

## 🛠️ Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: Node.js, Express
- **Banco de Dados**: MongoDB Atlas
- **Autenticação**: JWT, Bcrypt
- **Deploy**: Vercel

## 📝 Próximos Passos

Após o deploy, você pode adicionar:
- Recuperação de senha
- Verificação de email
- Perfil do usuário
- Dashboard após login
- Logout
- Middlewares de autenticação para rotas protegidas

## 🆘 Problemas Comuns

### Erro de conexão com MongoDB
- Verifique se o IP está liberado no MongoDB Atlas (Network Access)
- Confira se a senha no connection string está correta
- Certifique-se de que o usuário tem permissões

### Erro no Vercel
- Verifique se as variáveis de ambiente estão configuradas
- Confirme que o `vercel.json` está correto
- Veja os logs no dashboard do Vercel

## 📄 Licença

Este projeto é livre para uso pessoal e educacional.
