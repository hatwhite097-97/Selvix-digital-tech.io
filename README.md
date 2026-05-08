<div align="center">
  <img src="https://cdn.phototourl.com/free/2026-05-06-6076f61f-5cc5-4589-aa3b-9b732dbbc0b8.png" alt="Selvix Logo" width="250" />

  # 🛡️ SELVIX DIGITAL TECH
  **A Modern, Secure & High-Performance Single-File Web Application**

  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
  [![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)]()
  [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)]()
  [![Appwrite](https://img.shields.io/badge/Appwrite-F02E65?style=for-the-badge&logo=appwrite&logoColor=white)]()
  [![Security](https://img.shields.io/badge/Security-2FA_Secured-4ade80?style=for-the-badge&logo=spring-security&logoColor=white)]()
</div>

---

## 📝 Kuhusu Mradi (About Project)
**Selvix Digital Tech** ni application ya kisasa yenye muonekano wa "Mobile App" iliyotengenezwa ndani ya file moja (`Single HTML`). Imetumia nguvu ya **Tailwind CSS** kutoa muonekano wa kipekee wa *Glassmorphism* na **Vanilla JS** kwa logic zote. Mradi huu umeundwa kwa misingi ya ulinzi wa hali ya juu (Cybersecurity patterns) huku ukitunza data kupitia LocalStorage Sync na Appwrite Backend.

## ✨ Vipengele Vikuu (Key Features)
- 🔐 **Secure Authentication:** Mfumo salama wa kujisajili na kuingia.
- 🛡️ **2FA Admin Security:** Ulinzi thabiti wa QR Code (Google Authenticator) kwa paneli ya Admin.
- 📡 **Cyber-Level Data Flow:** Miundombinu inayochuja taarifa kabla ya kuingia kwenye database.
- 🎁 **Scratch Cards (Kukwangua Vocha):** Mfumo wa kukwangua vocha ukitumia kidole/mouse (Canvas API).
- 👁️ **Unique View Counter:** Hesabu za 'Views' zisizojirudia, inatambua IP/Session ya mtumiaji.
- 🔗 **URL Auto-Linkify:** Inatambua URLs kiotomatiki na kuzibadilisha kuwa links salama (Clickable).
- 💬 **Encrypted Live Chat:** Tawk.to integrated (inafunguka tu baada ya user kuingia).

---

## 🌊 System Architecture & Data Flow (Cybersecurity Vibe)
Mchoro huu chini unaonyesha jinsi data inavyosafiri *(Automatic Data Flow)* kuanzia kwa mtumiaji, inapopita kwenye wigo wa ulinzi (Gateway), hadi kufika kwenye Database na kwa Admin. 

*(GitHub itachora mchoro huu kiotomatiki uki-save faili hili)*

```mermaid
graph TD
    classDef secure fill:#0f172a,stroke:#38bdf8,stroke-width:2px,color:#fff;
    classDef alert fill:#450a0a,stroke:#ef4444,stroke-width:2px,color:#fff;
    classDef database fill:#14532d,stroke:#22c55e,stroke-width:2px,color:#fff;

    Client((📱 User Device)):::secure -->|Encrypted Session TLS| Gateway{🔐 Security Gateway & Auth}:::secure
    Gateway -->|Invalid Credentials| Denied[🚫 Access Blocked / Lockdown]:::alert
    Gateway -->|Token Validated| DB[(🗄️ Core Data / Appwrite Sync)]:::database
    
    DB <-->|Read / Feed Sync| UI[🖥️ User Dashboard Interface]:::secure
    DB <-->|Write / Admin Override| Admin[🛠️ Secure Admin Panel]:::secure

    Admin -->|Require Verification| 2FA{🛡️ 2FA Authenticator}:::secure
    2FA -->|Verified OTP| AdminDashboard[🔓 Full Admin Control]:::database
    2FA -->|Failed OTP| Block[🚫 Alert: Unauthorized Breach]:::alert
