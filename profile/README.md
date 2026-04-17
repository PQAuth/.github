# PQAuth

**Post-Quantum Secure OAuth 2.0 SDK for Go**

PQAuth is a modular SDK that brings post-quantum cryptographic algorithms to OAuth 2.0 — securing authorization workflows against quantum computing threats while remaining fully compatible with existing standards and drop-in with existing infrastructure.

---

## 🧩 Modules

| Module | Description |
|---|---|
| [`pqauth-core`](https://github.com/PQAuth/pqauth-core) | Cryptographic primitives, JWT sign/verify, JWKS management, key generation, token blacklist |
| [`pqauth-svr-core`](https://github.com/PQAuth/pqauth-svr-core) | Storage and cache abstractions — MongoDB, in-memory, and custom backends |
| [`pqauth-auth-svr`](https://github.com/PQAuth/pqauth-auth-svr) | OAuth 2.0 Authorization Server — all grant types, PKCE, OIDC, algorithm negotiation |
| [`pqauth-resource-svr`](https://github.com/PQAuth/pqauth-resource-svr) | Resource server token validation — local keys, JWKS, and introspection modes |
| [`pqauth-client`](https://github.com/PQAuth/pqauth-client) | OAuth 2.0 client SDK — token acquisition, auto-refresh, server discovery |

---

## ⚡ Key Features

- **🔐 Post-Quantum Security** — ML-DSA (CRYSTALS-Dilithium), SLH-DSA (SPHINCS+), and Falcon signing via NIST FIPS 204/205 standards
- **🔄 Full OAuth 2.0 Compatibility** — Authorization Code, Client Credentials, Device Authorization, JWT Bearer, Token Exchange, PAR, PKCE, OIDC
- **🏗️ Modular Architecture** — Use individual modules or the full stack; swap storage backends via interfaces
- **⚡ Algorithm Negotiation** — Server and client negotiate the best mutually supported algorithm per request
- **🔧 Framework-Agnostic** — Wire to any Go HTTP framework (Fiber, Chi, net/http, Gin)

---

## 🚨 Why Post-Quantum?

Current OAuth 2.0 implementations rely on RSA and ECDSA — algorithms that will be broken by sufficiently powerful quantum computers. Attackers are already harvesting encrypted traffic today for future decryption (**harvest now, decrypt later**). OAuth 2.0 secures billions of authentication flows daily, making it a high-value target.

PQAuth lets you migrate to quantum-resistant signing now, with classical fallback support for gradual rollout.

---

## 🚀 Getting Started

```bash
go get github.com/PQAuth/pqauth-core
go get github.com/PQAuth/pqauth-svr-core
go get github.com/PQAuth/pqauth-auth-svr
go get github.com/PQAuth/pqauth-resource-svr
go get github.com/PQAuth/pqauth-client
```

Full documentation at **[docs.pqauth.dev](https://docs.pqauth.dev)**

---

## 📚 Resources

- 📖 **[Documentation](https://docs.pqauth.dev)** — Setup guides, configuration reference, grant type walkthroughs
- 📊 **[Benchmarks](https://benchmark.pqauth.dev)** — Interactive performance comparison across all algorithms
- 🔐 **[Why PQC?](https://docs.pqauth.dev/pqc/why-pqc)** — The case for post-quantum OAuth 2.0
- 🔄 **[Migration Guide](https://docs.pqauth.dev/security/migration-guide)** — Phased migration from classical to post-quantum

---

## 📜 License

MIT
