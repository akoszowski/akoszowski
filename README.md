# Antoni Koszowski

Tech Lead at [vlayer](https://www.vlayer.xyz/) · Founding Engineer at [CarCanny](https://carcanny.co.uk/) · MSc CS, University of Warsaw

I build systems that let people prove things about themselves without handing over their data. Most of my day-to-day code lives in private company repositories, so this page collects what I can show publicly, with links.

[LinkedIn](https://www.linkedin.com/in/akoszowski/) · a2k.koszowski@gmail.com

---

## Projects

### 🔐 Vouch + Social Data Platform · vlayer · 2025 → now

Vouch verifies **private** account data: a user proves facts like their Instagram reach or an exchange balance straight from the source website, using zkTLS. Nobody else sees their password. The Social Data Platform verifies **public** social data with no login at all. Together they cover the full verification process, public and private. Vouch alone handles 3–4k private verification sessions a day.

**My part**
- One of the main developers of the browser extension, now used by 5,000+ people.
  - Moved it into the Vouch codebase.
  - **Led the research on running per-site JS snippets safely under Manifest V3.** I prototyped interpreter and sandbox approaches that shaped how the extension runs site logic, and built the snippet bundling.
  - Built the original release pipeline to the Chrome Web Store.
- **We rewrote in 2 months what had taken 1.5 years to build.** I was one of the main engineers moving Vouch to a React Native SDK and native mobile apps (late May to end of July 2026). My part: native TLSNotary proving orchestration, the iOS module and the `useVouch` API.
- Built much of the mobile end-to-end suite (Maestro on iOS and Android CI) and contributed to the extension's end-to-end tests.
- Tech Lead since 09/2026. I own the architecture and roadmap, plus the GCP infrastructure in Terraform, which includes the AWS-to-GCP migration and alerting.

**Links:** [Chrome Web Store](https://chromewebstore.google.com/detail/jbchhcgphfokabmfacnkafoeeeppjmpl) · [Vouch docs](https://docs.vlayer.xyz/vouch) · [Social Data API docs](https://docs.vlayer.xyz/social-data-api) · [Mobile SDK on npm](https://www.npmjs.com/package/@getvouch/mobile-sdk)

### 🚗 CarCanny · vlayer · 2026 → now

Car-history checks for UK used-car buyers, built on vlayer's verification stack.

**My part:** I set up the project from scratch and built its AI-answers tooling: a daily prompt panel that asks several LLMs (Claude, Gemini, OpenAI, Perplexity) the questions real buyers ask.

**Links:** [carcanny.co.uk](https://carcanny.co.uk/)

### 🏥 WorldCare · ETHGlobal Brussels 2024 · 🥇 Worldcoin (World ID) · 🥈 ENS

Patients own their medical records. They log in anonymously with World ID, records are stored encrypted on IPFS, and doctors see them only on request.

**My part:** the IPFS layer and the encoding and decoding of encrypted records. 4-person team.

**Links:** [ETHGlobal showcase](https://ethglobal.com/showcase/worldcare-9x3z0) · [Code](https://github.com/b-tarczynski/worldcare-new)

### ⚡ SuperElectro · ETHGlobal Amsterdam 2022 · 🥇 Voltz (Most Useful) · 🥇 EPNS (Frontend SDK)

A web app and bot for the Voltz interest-rate-swap protocol. Anyone can liquidate under-margined positions for a reward, and position owners get push alerts in time to top up their margin.

**My part:** the backend's position-tracking engine. It pulls positions from the Voltz subgraph, checks each one's margin requirement on-chain, and keeps a live ranking of the riskiest positions that drives the alerts. TypeScript and ethers.js. 4-person team.

**Links:** [ETHGlobal showcase](https://ethglobal.com/showcase/superelectro-aum84) · [Code](https://github.com/rzadp/eth-amsterdam)

### 🔌 Failure risk in power networks · MSc thesis · 2025–2026

Which nodes of a power grid matter most if someone attacks it? We built an automated pipeline that simulates removing grid nodes under different attack strategies. It compares topological and energy-based centrality measures by how well they predict the damage. The work was used in the NATO R-Grid project.

Co-authored with Aleksandra Makuracka · grade 5.0 · Python

**Links:** [Thesis (PDF)](https://drive.google.com/file/d/1DXN0pdiyW7TuILPqbq35WPJWZIPbRjw4/view)

### 🌐 Distributed session management · BSc thesis · 2022

A self-scaling system of node managers that assigns user sessions to servers, redirects clients to existing sessions and survives component failures. It is built on a modified Chord distributed hash table.

Team of 4 · grade 5.0 · Go

**Links:** [Thesis (PDF)](https://drive.google.com/file/d/1pb7p_6a_MNCHMKwtI8XSxdvB1NlM-ChE/view)
