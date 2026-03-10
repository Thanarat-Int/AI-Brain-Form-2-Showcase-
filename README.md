<div align="center">

# 🧠 AI BRAIN Forms

**ระบบ AI อัตโนมัติสำหรับกรอก Google Forms**
*Automated Google Forms Intelligence System*

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

> ⚠️ **Private Project** — Source code is not publicly available.
> This repository is for showcase purposes only.

</div>

---

## What is AI BRAIN Forms?

AI BRAIN Forms คือระบบ AI ที่ออกแบบมาเพื่อทำการกรอก Google Forms แบบอัตโนมัติ โดยใช้ Large Language Model (LLM) ในการสร้างคำตอบที่สมจริงตามบริบทของแต่ละคำถาม รองรับฟอร์มที่มีเงื่อนไขซับซ้อน (Conditional Branching) และสามารถรันหลายงานพร้อมกันได้สูงสุด **10 งาน** แบบอิสระจากกัน

---

## Key Features

### 🤖 AI-Powered Answer Engine
ใช้ LLM วิเคราะห์คำถามและสร้างคำตอบที่สมเหตุสมผลตาม context ของฟอร์ม รองรับคำถามหลายรูปแบบ ได้แก่ Multiple Choice, Checkbox, Short Answer, Paragraph, Linear Scale, Dropdown และ Date/Time

### ⚡ Multi-Job System
รันฟอร์มได้พร้อมกันสูงสุด **10 งาน** แบบ Parallel โดยแต่ละงานมี config, status, logs และ results แยกอิสระจากกัน สลับดูผลแต่ละงานได้ real-time

### 🔀 Conditional Branching Support
รองรับฟอร์มที่มีการแยกหน้าตามเงื่อนไข (Skip Logic) ระบบติดตาม page history ได้อย่างถูกต้อง ป้องกัน submission error จาก Google Forms

### 🎭 Multi-Profile / Persona Mode
กำหนด persona ของผู้ตอบได้หลายรูปแบบ ระบบสลับ persona แต่ละรอบเพื่อให้คำตอบมีความหลากหลายและดูเป็นธรรมชาติ

### 📋 Rule Editor
กำหนด rule การตอบแต่ละคำถามได้เอง:
- **Fixed Values** — กำหนดคำตอบตายตัวหรือสุ่มจาก options ที่เลือก
- **Keyword Weights** — ถ่วงน้ำหนักคำตอบให้เอียงไปทิศทางที่ต้องการ
- **Skip Trigger** — สั่งให้ตอบค่าที่กำหนดแล้วตัดจบฟอร์มทันที

### 📊 Cronbach's Alpha Analysis
วิเคราะห์ความเที่ยงตรงภายใน (Internal Consistency) ของชุดคำตอบหลังรันเสร็จ เพื่อตรวจสอบคุณภาพข้อมูล

### 💾 Config Save / Load
บันทึก rule configuration ของแต่ละฟอร์มไว้ใช้ซ้ำได้ ไม่ต้องตั้งค่าใหม่ทุกครั้ง

### 👥 User Management
ระบบ login พร้อมจัดการสิทธิ์ผู้ใช้ รองรับการใช้งานหลายคนบน server เดียว

---

## Tech Stack

| Category | Technologies |
|----------|-------------|
| **Frontend** | Next.js 16, React, TypeScript, TailwindCSS |
| **Backend** | Python 3.12, FastAPI, Threading |
| **AI / LLM** | LLM API Integration (configurable provider) |
| **Infrastructure** | Docker, Docker Compose |
| **Communication** | REST API, Server-Sent Events (real-time logs) |

---

## System Architecture

```
┌─────────────────────────────────────────┐
│           Next.js Frontend              │
│  (Dashboard · Rule Editor · Job Bar)    │
└──────────────────┬──────────────────────┘
                   │ REST API
┌──────────────────▼──────────────────────┐
│           FastAPI Backend               │
│  ┌─────────────────────────────────┐   │
│  │         Job Manager             │   │
│  │  Job 1 │ Job 2 │ ... │ Job 10   │   │
│  └────┬────────────────────────────┘   │
│       │                                 │
│  ┌────▼──────────┐  ┌───────────────┐  │
│  │ Answer Engine │  │ Form Submitter│  │
│  │   (LLM API)   │  │(Google Forms) │  │
│  └───────────────┘  └───────────────┘  │
└─────────────────────────────────────────┘
```

---

## UI Design

ออกแบบ UI ในธีม **Techno-Mage** — ผสมผสานความเป็น Dark Mode กับโทนสี Indigo-Navy และ Arcane Blue เพื่อให้รู้สึกเหมือนระบบ AI ขั้นสูง

- Dark / Light mode toggle
- TH / EN language support (i18n)
- Animated splash screen เมื่อ login
- Real-time log streaming ขณะรัน
- Job status chips แสดง progress แต่ละงาน

---

## Deployment

ระบบ deploy ด้วย Docker Compose บน local network server รองรับ:
- Raspberry Pi / Home Server
- NAS Device
- Any Linux server

---

<div align="center">

**Developed by Thanarat C.**
*Private Project — All Rights Reserved*

</div>
