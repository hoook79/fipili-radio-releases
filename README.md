# 📻 FiPiLi Radio - Telegram Mini App Walkie-Talkie

Un walkie-talkie digitale per chi viaggia sulla FiPiLi (Firenze-Pisa-Livorno).

## 🛣️ Canali

| Canale | Uso | Max durata |
|--------|-----|------------|
| 🌊 Direzione Mare | Emergenze/segnalazioni | 30s |
| 🏛️ Direzione Firenze | Emergenze/segnalazioni | 30s |
| 🍺 Il Bar | Cazzeggio in coda | 2 min |

## 🚀 Quick Start

### 1. Crea account LiveKit Cloud
Vai su https://cloud.livekit.io e crea un progetto gratuito.

### 2. Crea bot Telegram
Apri @BotFather su Telegram e crea un nuovo bot con `/newbot`.

### 3. Configura variabili ambiente

Copia `backend/.env.example` in `backend/.env` e compila:

```env
LIVEKIT_API_KEY=...       # da LiveKit Cloud
LIVEKIT_API_SECRET=...    # da LiveKit Cloud
LIVEKIT_URL=wss://...     # da LiveKit Cloud

TELEGRAM_BOT_TOKEN=...    # da @BotFather
FRONTEND_URL=https://...  # URL del frontend dopo deploy
```

### 4. Installa dipendenze

```bash
cd backend && npm install
cd ../bot && npm install
```

### 5. Avvia in locale

```bash
# Terminal 1: Backend
cd backend && npm run dev

# Terminal 2: Frontend  
cd frontend && npx serve .

# Terminal 3: Bot
cd bot && npm start
```

### 6. Test Mini App

Apri il bot su Telegram, premi "Apri FiPiLi Radio".

## 📁 Struttura

```
├── backend/      # API server (Express + LiveKit SDK)
├── frontend/     # Mini App (HTML5 + LiveKit Client)
└── bot/          # Telegram bot (Telegraf)
```

## 🌐 Deploy

- **Backend**: Render, Railway, Fly.io
- **Frontend**: Vercel, Cloudflare Pages
- **Bot**: Render (worker), Railway

Dopo il deploy, aggiorna `FRONTEND_URL` nel backend e nel bot.

## 📄 License

MIT
