# OpenInfer

Decentralized open-weight LLM inference on Nosana's decentralized GPU network — a solo project for the Decentralize AI Hackathon by HackerNoon.

## The problem

Indie developers depend on expensive, centralized inference APIs: single points of failure, opaque pricing, and user data flowing to big providers.

## The solution

OpenInfer is a web app that routes open-weight LLM inference to Nosana's decentralized GPU network instead of centralized APIs:

- **Chat UI** (Next.js) where users submit prompts and stream results back.
- **Job runner** (FastAPI) that schedules containerized inference jobs — vLLM serving Llama 3.x-class open-weight models — on Nosana GPU markets.
- **Verifiable records**: prompt/output pairs can optionally be pinned to Arweave for permanent, tamper-proof logs.

## Why decentralized infrastructure

1. **Compute layer** — Nosana's permissionless GPU marketplace removes hyperscaler lock-in and lowers cost for students and indie builders.
2. **Storage layer** — Arweave gives tamper-proof, permanent logs of AI outputs for auditability.

## Hackathon milestones

- Working Nosana deployment config + inference job runner
- Streaming chat UI
- Arweave archiving toggle
- Public demo

## Workload plan (Nosana)

- Model: Llama 3.1 8B-class open-weight model served with vLLM in a container.
- Hardware: single consumer GPU (e.g., RTX 3090/4090-class, ~24 GB VRAM) from Nosana GPU markets.
- Runtime: Simple deployment strategy, 1 replica, container timeout set per session (a few hours at a time) to stretch the $70 credits efficiently.
- Workload: interactive chat inference plus small batch evaluation prompts.

Built solo by Yash Gupta (B.Tech CSE, NIET Noida) — also my learning path into DePIN and open-weight model serving.
