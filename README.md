# Carmilla Encryption System - Minimal Binary

A comprehensive, plug-and-play OpenSSL encryption system with in-memory patching capabilities.

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ 
- OpenSSL (usually pre-installed on Linux/macOS)

### Installation
```bash
npm install
npm run build
npm start
```

### Usage
```bash
# Server will start on http://localhost:3000
# API Health: http://localhost:3000/api/health
```

## 🔧 Features

- **Native OpenSSL Encryption** - AES-256-CBC with unique salt/IV per operation
- **Car(); Patch System** - In-memory code injection via `Car();` markers
- **Selective Encryption** - Point-and-click encryption for specific areas
- **Anti-Reverse Engineering** - Fake encryption calls to confuse analysis
- **REST API** - Full HTTP interface for all operations
- **Zero Dependencies** - Uses only Node.js built-ins and OpenSSL

## 📡 API Endpoints

- `POST /api/encrypt` - Encrypt data
- `POST /api/decrypt` - Decrypt data
- `POST /api/encrypt-selective` - Selective area encryption
- `POST /api/patch/apply` - Apply Car(); patches
- `GET /api/health` - Health check

## 🧪 Quick Test

```bash
# Test encryption
curl -X POST http://localhost:3000/api/encrypt \
  -H "Content-Type: application/json" \
  -d '{"data": "Hello World", "passphrase": "test123"}'

# Test health
curl http://localhost:3000/api/health
```

## 📁 Project Structure

```
src/
├── crypto/carmilla.ts      # Core encryption module
├── patch/carPatcher.ts     # Car(); patch system
├── api/encryption.ts       # REST API endpoints
├── components/EncryptionUI.tsx # Web UI
└── server.ts               # Express server

docs/                       # Documentation
examples/                   # Usage examples
```

## 🔐 Security Features

- **Per-Run Isolation**: Every encryption uses unique salt/IV
- **No Fallback**: Failed encryption returns error, no substitution
- **Explicit API**: No automatic execution, all operations manual
- **Anti-RE**: Fake calls and patches to confuse reverse engineering

## 📖 Documentation

See `docs/` folder for:
- Complete API reference
- Usage examples
- Security considerations

## 🛠️ Development

```bash
npm run dev    # Development mode
npm run build  # Build TypeScript
npm test       # Run tests
```

## 📄 License

MIT License - See LICENSE file for details

---

**Ready to use in production with zero external dependencies!**