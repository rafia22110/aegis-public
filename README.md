# Aegis Mirror - Digital Sovereignty Shield (Public Repository)

Aegis Mirror is a digital sovereignty and network virtualization framework designed to secure personal telemetry, mask identities, and prevent background device tracking.

This is the **Public Shield** repository, a functional mirror replica for community auditability and cryptographic trust. Server configurations, Docker configs, and local SQLite data files have been stripped for security.

## Features

1. **Embedded Data Architecture (SQLite-vec)**: 15 relational tables managing users, active policies, sandboxing profiles, location/contact virtualization, and sync queues.
2. **Deterministic Routing Hooks (PocketBase)**: Real-time route verification, instant emergency whitelisting (zero-latency bypass), and packet log translation into narrative alerts.
3. **Fail-Closed VPN Subsystem (Kotlin)**: Custom VpnService loopback routing with absolute packet drop on daemon crashes to protect against DNS leakages.
4. **Stitched User Interface (Tailwind + Alpine.js + HTMX)**: Responsive, accessible single-page interface with real-time status control, mock alias redirectors, and vigilance logs.

---

## Directory Structure

```
.
├── pb_hooks/main.pb.js            # PocketBase policy checking and form hooks
├── pb_public/                     # Statically built PWA interface files
│   ├── index.html                 # Unified single-page web app
│   ├── manifest.json              # PWA manifest configurations
│   ├── sw.js                      # Service worker caching files
│   ├── logo.png                   # Brand asset
│   └── medusa-core.png            # Holographic medallion visual asset
└── src/
    ├── database/
    │   └── schema.sql             # On-device SQLite schema
    └── android/
        ├── MirrorVpnService.kt    # Android Kotlin VPN service
        └── AndroidManifest.xml    # Android VPN permissions configuration
```

---

## Auditability

By auditing `src/android/MirrorVpnService.kt` and `pb_hooks/main.pb.js`, the community can verify that Aegis Mirror virtualizes device sensors (microphone, location) and intercepts tracking payloads without leaking any sensitive communications.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
