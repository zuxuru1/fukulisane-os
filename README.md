# FUKULISANE MALL OS

## AI-Powered Digital Mall Operating System

### 3-Pillar Ecosystem
- **Pillar 1: Storefront** - Public Digital Mall (Customer Face)
- **Pillar 2: StoreBrain** - Store Business Operating System
- **Pillar 3: MallBrain** - Mall Operating System

## 15-Phase Build Roadmap

```
1. ✅ Authentication (Phase 1)
2. ✅ Storefront (Phase 2)
3. ✅ Store Leasing (Phase 3)
4. ✅ StoreBrain (Phase 4)
5. ✅ Wallet Layer (Phase 5)
6. ⏳ Communication Layer (Phase 6)
7. ⏳ Localization Layer (Phase 7)
8. ⏳ MallBrain (Phase 8)
9. ⏳ Connector Vault (Phase 9)
10. ⏳ AI Layer (Phase 10)
11. ⏳ Marketing Layer (Phase 11)
12. ⏳ Media Layer (Phase 12)
13. ⏳ Analytics Layer (Phase 13)
14. ⏳ Security Layer (Phase 14)
15. ⏳ Production Deployment (Phase 15)
```

## Tech Stack

- **Frontend**: Next.js 14, React, TypeScript, Tailwind CSS
- **Backend**: Node.js, Express, TypeScript
- **Database**: PostgreSQL, Redis
- **Message Bus**: Bull, RabbitMQ
- **Search**: Meilisearch, Qdrant
- **Storage**: AWS S3, Supabase
- **Auth**: JWT, OTP (WhatsApp-style)
- **Deployment**: Docker, Railway/Render

## Getting Started

### Prerequisites
- Node.js 18+
- Docker & Docker Compose
- PostgreSQL 15+
- Redis 7+

### Quick Start

```bash
# Clone repository
git clone https://github.com/zuxuru1/fukulisane-os.git
cd fukulisane-os

# Start with Docker Compose
docker-compose up -d

# Backend setup
cd backend
npm install
npm run db:migrate
npm run dev

# Frontend setup (in another terminal)
cd frontend
npm install
npm run dev
```

### Access Application

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000
- **API Docs**: http://localhost:5000/api/docs
- **Database**: localhost:5432
- **Redis**: localhost:6379

## Project Structure

```
fukulisane-os/
├── backend/
│   ├── src/
│   │   ├── index.ts              # Entry point
│   │   ├── types/
│   │   ├── middleware/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── database/
│   │   └── utils/
│   ├── package.json
│   ├── tsconfig.json
│   └── Dockerfile
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── lib/
│   │   └── hooks/
│   ├── package.json
│   └── Dockerfile
├── database/
├── docs/
├── docker-compose.yml
├── .env.example
└── .gitignore
```

## Key Features

### Phase 1: Authentication ✅
- WhatsApp-style OTP login
- Role-based access (CUSTOMER, STORE_OWNER, ADMIN)
- JWT token management
- Phone number verification

### Phase 2: Storefront ✅
- Nearby stores discovery
- Product search with AI ranking
- Category browsing
- AI recommendations
- Multi-language support

### Phase 3/4: StoreBrain ✅
- Store management dashboard
- Product management
- Order tracking
- Store analytics

### Phase 5: Wallet Layer ✅
- Multi-wallet support (MALL, STORE, BYSEI)
- Escrow payment management
- Transaction history
- Fund transfers

## API Endpoints

```
POST   /api/v1/auth/send-otp          - Send OTP
POST   /api/v1/auth/verify-otp        - Verify OTP & login
GET    /api/v1/auth/me                - Get current user

GET    /api/v1/storefront/nearby      - Get nearby stores
GET    /api/v1/storefront/search      - Search products
GET    /api/v1/storefront/categories  - Get categories
GET    /api/v1/storefront/recommendations - AI recommendations

POST   /api/v1/stores                 - Create store
GET    /api/v1/stores/:storeId        - Get store details
POST   /api/v1/stores/:storeId/products - Add product
GET    /api/v1/stores/:storeId/orders - Get orders

GET    /api/v1/wallet                 - Get wallet
GET    /api/v1/wallet/transactions    - Transaction history
POST   /api/v1/wallet/transfer        - Transfer funds
```

## Environment Variables

```
DATABASE_URL=postgresql://user:password@localhost:5432/fukulisane
REDIS_URL=redis://localhost:6379
JWT_SECRET=your_jwt_secret_key_here
BACKEND_PORT=5000
NODE_ENV=development
NEXT_PUBLIC_API_URL=http://localhost:5000
```

## Development

```bash
# Run tests
npm test

# Run linter
npm run lint

# Database migrations
npm run db:migrate
npm run db:seed
```

## Docker

```bash
# Start all services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

## License

Proprietary - FUKULISANE

---

Built with ❤️ by the FUKULISANE team
