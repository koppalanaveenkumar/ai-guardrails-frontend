# AI Guardrails - Frontend

Modern React dashboard for the AI Guardrails API security platform.

## Features

- 🎯 **Interactive Playground** - Test prompts with real-time scanning
- 📊 **Risk Confidence Meter** - Visual risk scoring (0-100%)
- 🔍 **Score Badges** - Color-coded confidence levels in audit logs
- 📄 **Pagination** - Navigate through audit history
- 🗑️ **Clear Logs** - One-click log management
- 📈 **Analytics Dashboard** - Usage stats and metrics
- 🔐 **API Key Management** - Secure authentication

## Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool
- **Lucide Icons** - Icon library
- **Clsx** - Conditional styling

## Setup

### Prerequisites
- Node.js 18+
- Backend API running

### Installation

```bash
npm install
```

### Environment Variables

Create `.env` file:

```env
VITE_API_URL=http://localhost:8000
```

For production:
```env
VITE_API_URL=https://your-api-domain.com
```

### Development

```bash
npm run dev
```

Runs on `http://localhost:5173`

### Build

```bash
npm run build
```

Output: `dist/` folder

## Deployment

### Vercel (Recommended)

1. Push to GitHub
2. Import to Vercel
3. Set `VITE_API_URL` environment variable
4. Deploy

### Manual

```bash
npm run build
# Serve dist/ folder with any static host
```

## Project Structure

```
src/
├── components/
│   ├── Playground.jsx      # Main testing interface
│   ├── AuditTable.jsx      # Log viewer with pagination
│   ├── Dashboard.jsx       # Analytics overview
│   ├── StatsGrid.jsx       # Metrics cards
│   └── RegisterModal.jsx   # Authentication
├── App.jsx                 # Root component
└── main.jsx               # Entry point
```

## API Integration

The frontend communicates with the backend via:

- `POST /api/v1/guard/scan` - Scan prompts
- `GET /api/v1/audit/logs` - Fetch audit logs
- `GET /api/v1/audit/stats` - Get usage statistics
- `DELETE /api/v1/audit/prune` - Clear logs

Authentication: `x-api-key` header

## License

MIT License - see LICENSE file
