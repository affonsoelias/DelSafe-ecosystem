# 🌌 Aether Ecosystem & Package Hub

Central package hub, registry index, and community libraries repository for the **[Aether](https://github.com/affonsoelias/aether)** programming language (`affonsoelias/aether-ecosystem`).

Unlike the core compiler repository ([`affonsoelias/aether`](https://github.com/affonsoelias/aether)), this repository is dedicated to external libraries, adapters, and package registry metadata that extend Aether without bloating the base compiler toolchain.

---

## 🏛️ Repository Structure

- **`packages/`**: Official, co-official, and community package directories / repositories.
- **`registry/`**: Public package registry catalog:
  - [`registry/index.json`](registry/index.json) — SemVer-indexed metadata mapping short package names (`aetherc pkg search`, `aetherc pkg add`, `aetherc pkg publish`) to verified checksums and package sources.

### Planned Official & Co-Official Packages
- **`aether-horse`**: High-speed adapter and middleware package for Horse (Free Pascal).
- **`aether-mormot`**: Enterprise messaging and persistence integration for Synopse mORMot 2.
- **`aether-sql`**: Unified database drivers (PostgreSQL, SQLite, MySQL) for Aether backends.
- **`aether-jwt`**: Native JSON Web Token signing and verification library.
- **`blaisevue-core`**: Shared modules and integration utilities for [BlaiseVue](https://github.com/affonsoelias/BlaiseVue).

---

## 🔒 Security & Integrity Model

All packages distributed through the Aether ecosystem follow three core safety guarantees:

1. **Cryptographic Lockfile (`aether.lock`)**: Installed dependencies record exact source hashes and verification digests for strictly reproducible builds.
2. **Supply-Chain Auditing (`aetherc audit`)**: Validates installed dependency integrity against SHA-256 digests and flags tampered packages or unencrypted sources.
3. **Static Ownership & Type Safety**: External libraries are checked under Aether's static type system and Borrow Checker guarantees (`borrow`, `mut borrow`, `take`).

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
