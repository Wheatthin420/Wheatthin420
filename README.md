# Wheatthin420

Everything here is built and maintained together with a small fleet of Rust-
speaking agents (davinci, pitbull, rusty, warden, …) on a single box with a
locally-served 512k-context model. The agents write the milestones, run the
gates, and push the commits; the human sets direction and approves the
scary bits.

## Projects

| Repo | What it is |
|---|---|
| [pitbull-rs](https://github.com/Wheatthin420/pitbull-rs) | Protocol-adherent Rust client for **Hotline** (the 1997 chat/file/news system still running today) — spec-grounded, differential-interop tested |
| [physcad](https://github.com/Wheatthin420/physcad) | PhysCAD-like parametric CAD/CAM: wgpu viewport, manifold3d CSG, sketch constraint solver (Levenberg–Marquardt, exact-polyhedral volume gates), sweep/extrude/revolve |
| [gentai-rag](https://github.com/Wheatthin420/gentai-rag) | Rust RAG engine over agent memory (BM25 + trigram + dense retrieval, eval-gated) + bootable Linux installer ISO toolchain |
| [rustcheck](https://github.com/Wheatthin420/rustcheck) | Dev-loop helper: incremental diff/fmt/fix/save plus `rustwatch` for on-change gates |
| [hang-watchdog](https://github.com/Wheatthin420/hang-watchdog) | Turns silent kernel hangs (amdgpu HMM/userptr page corruption) into panics + EFI pstore dumps + auto-reboot |
| rd-native | Private: low-latency remote desktop over QUIC (rustls, post-quantum key exchange) |
| msf-ai-console | Private: approval-gated web console (FastAPI + LLM copilot) |

## House rules

- Gate discipline: `cargo fmt --check`, `clippy -D`, tests — re-verified by a
  second agent before a milestone counts as done.
- Compatibility claims must cite live sources, never recall.
- Public servers: read-only guest etiquette, always.
