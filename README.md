# 🌌 DelSafe Ecosystem & Package Hub

Central package hub, registry index, and community libraries repository for the **[DelSafe](https://github.com/affonsoelias/delsafe)** programming language (`affonsoelias/delsafe-ecosystem`).

Unlike the core compiler repository ([`affonsoelias/delsafe`](https://github.com/affonsoelias/delsafe)), this repository is dedicated to external libraries, adapters, and package registry metadata that extend DelSafe without bloating the base compiler toolchain.

---

## 🏛️ Repository Structure

- **`packages/`**: Official, co-official, and community package directories / repositories.
- **`registry/`**: Public package registry catalog:
  - [`registry/index.json`](registry/index.json) — SemVer-indexed metadata mapping short package names (`delsafec pkg search`, `delsafec pkg add`, `delsafec pkg publish`) to verified checksums and package sources.

### Planned Official & Co-Official Packages
- **`delsafe-sql`**: Unified database drivers (SQLite, PostgreSQL, MySQL/MariaDB, Firebird) for DelSafe applications and backends.
- **`delsafe-jwt`**: Native JSON Web Token signing, verification, and authentication helpers.
- **`delsafe-http-client`**: Native HTTP/HTTPS client for consuming external APIs.
- **`delsafe-dotenv`**: Lightweight `.env` configuration loader for servers and CLI tools.
- **`delsafe-log`**: Structured logging utilities for DelSafe services and applications.

---

## 🔒 Security & Integrity Model

All packages distributed through the DelSafe ecosystem follow three core safety guarantees:

1. **Cryptographic Lockfile (`delsafe.lock`)**: Installed dependencies record exact source hashes and verification digests for strictly reproducible builds.
2. **Supply-Chain Auditing (`delsafec audit`)**: Validates installed dependency integrity against SHA-256 digests and flags tampered packages or unencrypted sources.
3. **Static Ownership & Type Safety**: External libraries are checked under DelSafe's static type system and Borrow Checker guarantees (`borrow`, `mut borrow`, `take`).

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
