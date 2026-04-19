# 🌐 Full Stack Web Projects

> Projetos completos de desenvolvimento web utilizando Node.js, PHP, JavaScript e muito mais.

[![Node.js](https://img.shields.io/badge/Node.js-18+-43853D?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![PHP](https://img.shields.io/badge/PHP-8.1+-777BB4?style=flat-square&logo=php&logoColor=white)](https://php.net)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES2023-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org)
[![Author](https://img.shields.io/badge/Author-Josimar%20Pessanha-blueviolet?style=flat-square)](https://github.com/josimarpessanha19-gif)

---

## 🚀 Projetos

### 1. 🔐 API REST com Autenticação JWT
API completa com Node.js + Express + autenticação JWT + banco de dados.

**Stack:** Node.js • Express • JWT • MySQL • Docker

```javascript
// Exemplo de endpoint protegido
app.get('/api/users', authenticateToken, async (req, res) => {
  const users = await UserService.findAll({ active: true });
  res.json({ success: true, data: users, total: users.length });
});
```

**Features:**
- ✅ Autenticação JWT segura
- ✅ CRUD completo de usuários
- ✅ Middleware de validação
- ✅ Rate limiting e segurança
- ✅ Documentação Swagger

---

### 2. 🛒 E-commerce PHP + MySQL
Sistema completo de e-commerce com carrinho, pagamentos e painel admin.

**Stack:** PHP 8 • MySQL • Bootstrap • JavaScript

```php
// Exemplo de controller de produto
class ProductController {
    public function index(): array {
        return Product::query()
            ->active()
            ->with(['category', 'images'])
            ->orderBy('created_at', 'desc')
            ->paginate(12)
            ->toArray();
    }
}
```

**Features:**
- ✅ Catálogo de produtos
- ✅ Carrinho de compras
- ✅ Integração com gateways de pagamento
- ✅ Painel administrativo
- ✅ Responsivo (mobile-first)

---

### 3. 💬 Chat em Tempo Real
Aplicação de chat com WebSockets, salas e histórico de mensagens.

**Stack:** Node.js • Socket.IO • React • MongoDB

```javascript
// Servidor WebSocket
io.on('connection', (socket) => {
  socket.on('join-room', (roomId) => {
    socket.join(roomId);
    socket.to(roomId).emit('user-joined', { id: socket.id });
  });
  
  socket.on('send-message', async ({ roomId, message }) => {
    await Message.create({ roomId, content: message, userId: socket.userId });
    io.to(roomId).emit('new-message', { message, timestamp: new Date() });
  });
});
```

---

### 4. 📊 Dashboard Analytics
Dashboard interativo com gráficos, filtros e exportação de dados.

**Stack:** JavaScript • Chart.js • Node.js • PostgreSQL

---

## 🛠️ Tecnologias Utilizadas

### Backend
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-404D59?style=flat-square&logo=express&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)

### Frontend
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

### Banco de Dados
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)

### DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)

---

## 🚀 Como Rodar

```bash
# Clone
git clone https://github.com/josimarpessanha19-gif/fullstack-web-projects.git
cd fullstack-web-projects

# Escolha um projeto e entre na pasta
cd api-rest-jwt

# Instale dependências
npm install

# Configure o ambiente
cp .env.example .env

# Inicie com Docker
docker-compose up -d

# Ou diretamente
npm run dev
```

---

## 👨‍💻 Autor

**Josimar Pessanha de Aguiar** — Full Stack Developer

📧 josimarpessanha19@gmail.com | 💼 [LinkedIn](https://www.linkedin.com/in/josimar-pessanha-de-aguiar-7a99a9356/) | 🐙 [GitHub](https://github.com/josimarpessanha19-gif)

⭐ Se gostou, deixe uma estrela!
