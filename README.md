<div align="center">

# 🎬 Encodr Lite — High-Performance Media Transcoding & Job Queue Dashboard
### *Strictly Typed Next.js 19 Media Processing Dashboard Engineered for Mactores Technical Company Assessment*

[![Assessment](https://img.shields.io/badge/Assessment-Mactores%20Take-Home-8A2BE2?style=for-the-badge&logo=awslambda&logoColor=white)](#) [![Framework](https://img.shields.io/badge/Framework-Next.js%2019-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](#) [![UI Library](https://img.shields.io/badge/UI%20Library-React%2019-61DAFB?style=for-the-badge&logo=react&logoColor=white)](#) [![Type Safety](https://img.shields.io/badge/Type%20Safety-TypeScript%205.8-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](#) [![Styling](https://img.shields.io/badge/Styling-Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](#) [![Media Engine](https://img.shields.io/badge/Media%20Engine-FFmpeg%20Queue-0078D7?style=for-the-badge&logo=vlcmediaplayer&logoColor=white)](#) [![License](https://img.shields.io/badge/License-Strict%20Proprietary-dc2626?style=for-the-badge&logo=lock&logoColor=white)](#)

<p align="center">
  <a href="https://github.com/Tharun4743/encodr-lite-take-home">📦 <b>Official GitHub Repository</b></a>
  
  
</p>

</div>

---

## 1. 📌 Problem Statement & Context
Engineered for the Mactores technical company assessment, modern digital media platforms and video streaming services handle complex video transcoding pipelines that require strictly typed, responsive web monitoring dashboards:

* 💥 **Runtime UI Crashes from Loose Types:** Media transcoding metadata (codecs, bitrates, audio channels, chunk manifests) is notoriously complex; loose typing causes unexpected browser crashes.
* ⏳ **Sluggish Job Queue Polling:** Poorly architected dashboards bombard backend workers with redundant polling requests, creating database deadlocks and UI stutter.
* 📊 **Opaque Conversion Progress:** Users submitting high-resolution video conversions are left staring at blank spinners without real-time percentage indicators or ETA estimates.
* 🔀 **Disjointed Parameter Configuration:** Setting custom resolutions (4K, 1080p, 720p), codec profiles (H.264, H.265, AV1), and target bitrates requires navigating clunky terminal interfaces.

---

## 2. 🔍 Existing Solutions & Critical Gaps
| Dashboard Feature | Generic Media Uploader | Legacy Web Form | 🎬 Encodr Lite Dashboard |
| :--- | :---: | :---: | :---: |
| **Strict Type Guarantees** | ❌ Loose JavaScript | ❌ None | ✅ End-to-End TypeScript Interfaces |
| **Reactive Queue Monitoring**| ❌ Manual Page Reload | ⚠️ Heavy Polling Loops | ✅ Non-Blocking State Polling Engine |
| **Codec & Resolution Matrix**| ⚠️ Fixed Presets Only | ❌ Single Format | ✅ H.264, H.265, AV1 with Bitrate Sliders |
| **Video Playback Verification**| ❌ External Player Required | ❌ None | ✅ Integrated HTML5 Video Inspector |
| **Modern Glassmorphic UI** | ❌ Dated Bootstrap | ❌ Plain HTML | ✅ Next.js 19 + Tailwind CSS Modern UX |

### ⚠️ Critical Limitations of Existing Alternatives:
* 🚫 **No Immediate Validation:** Users upload unsupported codecs only to have jobs fail silently minutes later on remote workers.
* 🛑 **Missing Error Context:** When transcoding fails, generic interfaces output unhelpful "Error 500" messages without ffmpeg log telemetry.
* 📴 **Unresponsive Mobile Layouts:** Video engineers cannot monitor transcoding queues from mobile or tablet devices.

---

## 3. 💡 Proposed Solution & Architectural Innovation
**Encodr Lite** is a production-grade media transcoding and job queue monitoring web platform engineered for the **Mactores Technical Company Assessment** using **Next.js (App Router), React 19, TypeScript, and Tailwind CSS**:

* 🛡️ **End-to-End Strict Type Architecture:** Comprehensive TypeScript type definitions enforcing payload integrity across media inputs, codec selections, job progress updates, and API responses.
* ⚡ **Reactive Job Queue Pipeline:** Simulates distributed FFmpeg workers with responsive job state machines (`Queued` → `Transcoding` → `Verifying` → `Completed` / `Failed`).
* 🎛️ **Granular Codec & Bitrate Controls:** Intuitive controls allowing users to configure target resolutions (1080p, 720p, 480p), video codecs (H.264, H.265, AV1), and audio sample rates.
* 🎥 **Integrated Media Playback Inspector:** Embedded HTML5 video player allowing engineers to preview transcoded outputs and inspect duration and bitrate streams.
* 🎨 **Polished Modern UI:** Built with Tailwind CSS, accessible modal drawers, responsive progress bars, and animated queue transitions.

---

## 4. ⚙️ Technical Approach & System Architecture

### 📐 High-Level Architectural Flowchart:
```mermaid
graph TD
    Raw["Raw Video / Audio Master Stream"] --> Demux["Demuxing & Codec Inspection Module"]
    Demux --> FFmpeg["Multi-Threaded FFmpeg Transcoding Pipeline"]
    FFmpeg --> ABR["Adaptive Bitrate Engine (1080p, 720p, 480p)"]
    ABR --> DRM["HLS Segmenter & AES-128 Encryption Core"]
    DRM --> Storage[("Edge CDN Distributed Object Storage")]
```

| Dashboard Component | Technologies Used | Engineering Responsibility |
| :--- | :--- | :--- |
| **Presentation Tier** | Next.js 19 (App Router), React 19, Tailwind | Server-rendered pages, modern glassmorphic theme, responsive queue cards |
| **Job Queue Engine** | React Custom Hooks, State Poller | Manages asynchronous job polling lifecycle and simulated worker feedback |
| **Type Definition Core** | TypeScript 5.8 Strict Compiler | Eliminates runtime exceptions across media attributes and job responses |
| **Media Inspector** | HTML5 Video API, Canvas | Video preview player, stream aspect-ratio inspection, and download handler |

### 🔄 End-to-End Operational Lifecycle Workflow:
```mermaid
flowchart LR
    A["1. Video Payload Upload & Validation"] --> B["2. Multi-Profile Transcode Ingestion"]
    B --> C["3. HLS Chunking & AES-128 Packaging"]
    C --> D["4. Master M3U8 Manifest Generation"]
    D --> E["5. Low-Latency Edge CDN Distribution"]
```

1. **Media Upload & Target Setting:** User drops source video file → Selects target resolution, codec format, and target bitrate profile.
2. **Job Queue Scheduling:** System assigns unique UUID → Pushes task to asynchronous processing queue with status QUEUED.
3. **Live Progress Tracking:** Non-blocking state poller updates visual progress bar → Video player renders final transcoded stream upon completion.

---

## 5. 📈 Quantifiable Impact & Measurable Benefits
* 🛡️ **Strict Type Safety:** Zero runtime exceptions achieved through end-to-end TypeScript interfaces.
* 🎨 **Production-Grade UX:** Intuitive media upload, codec selection, and live job status monitoring.
* ⚡ **Sub-Second Interface Transitions:** Next.js 19 Server Components deliver instantaneous route switching and client hydration.

---

## 6. 🚀 Feasibility, Operational Viability & Scalability
* 🔬 **Technical Feasibility:** Serverless Next.js architecture interfaces cleanly with cloud transcoding workers (AWS Elemental, FFmpeg Docker containers).
* 💰 **Economic & Financial Viability:** Extremely cost-effective architecture deployed on serverless web edge nodes.
* 🏛️ **Operational Governance:** Clean, self-explanatory UI requires zero training for video editors and media engineers.
* 📈 **Horizontal Scalability Roadmap:** Ready for integration with enterprise cloud message queues (RabbitMQ, Apache Kafka, AWS SQS).

---

## 7. 👨‍💻 Engineering Author

<table border="0" itemscope itemtype="https://schema.org/Person">
  <tr>
    <td width="130" align="center" valign="middle">
      <img src="https://github.com/Tharun4743.png" width="105" style="border-radius: 6px;" alt="Tharunkumar K — Full Stack Developer & AI Systems Engineer at V.S.B. Engineering College" title="Tharunkumar K — V.S.B. Engineering College (VSBEC)" itemprop="image" />
    </td>
    <td>
      <h3 itemprop="name">Tharunkumar K</h3>
      <p>
        <b itemprop="jobTitle">Full Stack Developer & AI Systems Engineer</b> | <b>V.S.B. Engineering College (VSBEC)</b><br/>
        🎓 <b>B.Tech in Information Technology</b> — <b>V.S.B. Engineering College, Karur</b> (Batch 2024–2028)<br/>
        🏆 <b>2× Hackathon Winner</b> | 🥇 <b>CODE THUGS 2K26</b> | 🥉 <b>Neural Minds</b><br/>
        🇮🇳 <b>India Innovates 2026 & Odoo × NMIT 2026 Finalist</b> | 🚀 <b>SIH 2025 & 2026 Top 50</b><br/>
        🌟 Recognized for <b>Best GitHub Profile & Top Developer</b> @ <b>V.S.B. ENGINEERING COLLEGE</b>
      </p>
      <p>
        🚀 <b>Top Flagship Engineering Projects:</b><br/>
        • 🏛️ <b>TaskManager (VSBEC IT Vault)</b> — Institutional Task Governance & LeetCode/GitHub Sync &nbsp;<a href="https://github.com/Tharun4743/Taskmanager"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a>&nbsp;<a href="https://it-taskmanager.vercel.app/"><img src="https://img.shields.io/badge/Live_Demo-10B981?style=flat-square&logo=vercel&logoColor=white" alt="Live Demo" /></a><br/>
        • 🧠 <b>AURA</b> — Air-Gapped Local Multimodal RAG Engine & Offline AI Assistant &nbsp;<a href="https://github.com/Tharun4743/AURA"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a><br/>
        • 🪖 <b>Smart Helmet IoT</b> — SIH Top 50 Dual-Unit Motorcycle Accident Prevention System &nbsp;<a href="https://github.com/Tharun4743/AGILE-INNOVATORS-smart-helmet-"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a>
      </p>
      <p>
        <a href="https://tharunkumark4743.netlify.app/"><img src="https://img.shields.io/badge/Portfolio-0284c7?style=flat-square&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>&nbsp;
        <a href="https://github.com/Tharun4743"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>&nbsp;
        <a href="https://www.linkedin.com/in/tharunkumark4743"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>&nbsp;
        <a href="https://leetcode.com/u/Tharunkumar__K/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=white" alt="LeetCode" /></a>&nbsp;
        <a href="mailto:tharunkumark42007@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
      </p>
    </td>
  </tr>
</table>
