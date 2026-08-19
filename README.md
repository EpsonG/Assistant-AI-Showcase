# mybudget — Assistant Financier & ERP Intelligent

<p align="center">
  <img src="https://raw.githubusercontent.com/EpsonG/Assistant-AI/main/frontend/public/icon.png" alt="mybudget Logo" width="120" />
</p>

<p align="center">
  <strong>Application moderne de gestion financière, facturation multi-devises et optimisation fiscale alimentée par l'Intelligence Artificielle.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/.NET_9-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET 9" />
  <img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React 19" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/MongoDB_Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB Atlas" />
  <img src="https://img.shields.io/badge/Google_Gemini_AI-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini AI" />
  <img src="https://img.shields.io/badge/Stripe_Billing-635BFF?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
  <img src="https://img.shields.io/badge/Windows_x64-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Desktop" />
</p>

---

## Presentation du Projet

**mybudget** est une solution complete concue pour repondre aux defis financiers des travailleurs autonomes, PME et gestionnaires de budgets familiaux. Combinant une interface web reactive et une application de bureau native Windows ultra-rapide (Kestrel + WebView2), la plateforme integre des modeles d'intelligence artificielle avances pour automatiser la comptabilite et maximiser les deductions fiscales.

---

## Fonctionnalites Cles

### 1. Facturation & Devis Intelligents
- Creation et personnalisation de factures conformes en quelques clics.
- Calcul automatique des taxes de vente canadiennes (**TPS 5%**, **TVQ 9.975%**) et europeennes (**TVA**).
- Suivi en temps reel des statuts de paiement (*Brouillon, Envoyee, Payee, En retard*).
- Generation et telechargement de factures en format PDF haute definition.

### 2. Intelligence Artificielle & Conseiller Fiscal Pro
- **OCR & Vision IA :** Numerisation instantanee des recus et factures papier par simple photo ou glisser-deposer.
- **Importation Bancaire Multi-formats :** Parsing intelligent de releves bancaires (PDF, OFX, QFX, CSV) avec detection automatique des categories et elimination des doublons.
- **Conseiller Fiscal en Temps Reel :** Assistant conversationnel expert alimente par Google Gemini et DeepSeek, fournissant des conseils sur les depenses deductibles et la gestion de tresorerie.

### 3. Collaboration & Espaces Partages
- Synchronisation en direct des transactions et des budgets via **WebSockets**.
- Gestion des roles et des autorisations fines (*Administrateur, Membre, Enfant/Observateur*).
- Repartition equitable des charges communes et suivi des contributions individuelles.

### 4. Passerelle SaaS & Securite Institutionnelle
- Integration complete **Stripe Checkout & Billing Portal** (gestion d'abonnements Freemium, Pro et Business).
- Authentification unifiee **Google OAuth 2.0 & JWT (HMAC-SHA256)**.
- Architecture securisee auditee contre le Top 10 OWASP avec controle d'acces base sur les roles (RBAC).

---

## Architecture Technique

```
┌─────────────────────────────────────────────────────────────┐
│                       Client Layer                          │
│  ┌─────────────────────────────┐ ┌────────────────────────┐ │
│  │   React 19 / Vite / TS      │ │  Windows Desktop App   │ │
│  │   (Tailwind/Design System)  │ │  (WPF + WebView2)      │ │
│  └──────────────┬──────────────┘ └───────────┬────────────┘ │
└─────────────────┼────────────────────────────┼──────────────┘
                  │       HTTPS / WSS          │
┌─────────────────▼────────────────────────────▼──────────────┐
│                    API Gateway (.NET 9)                     │
│  ┌─────────────────────────────┐ ┌────────────────────────┐ │
│  │   REST Controllers (Kestrel)│ │  WebSocket Manager     │ │
│  └──────────────┬──────────────┘ └───────────┬────────────┘ │
│                 │ JWT & Rate Limiting        │              │
│  ┌──────────────▼────────────────────────────▼────────────┐ │
│  │  Services Metier (Auth, Invoices, Expenses, Audit)     │ │
│  └──────────────┬────────────────────────────┬────────────┘ │
└─────────────────┼────────────────────────────┼──────────────┘
                  │                            │
┌─────────────────▼──────────────┐ ┌───────────▼──────────────┐
│       Persistance Cloud        │ │    Integrations Externes │
│  MongoDB Atlas (FreelanceAIDb) │ │  - Google Gemini AI      │
│  - Collections partitionnees   │ │  - DeepSeek Chat         │
│  - Indexation & Caching        │ │  - Stripe Payments API   │
└────────────────────────────────┘ └──────────────────────────┘
```

---

## Stack Technologique

- **Frontend :** React 19, TypeScript, Vite, Lucide Icons, Custom Design System (Inter + IBM Plex Mono).
- **Backend :** .NET 9 (C#), ASP.NET Core Kestrel, Architecture Modulaire & Services Decouples.
- **Desktop :** WPF (.NET 9), Microsoft WebView2 Runtime, Inno Setup Installer.
- **Persistance :** MongoDB Atlas Cloud (Driver officiel .NET).
- **IA & Vision :** Google Gemini 2.0 Flash / Pro API, DeepSeek-V3, UglyToad PdfPig OCR.
- **Paiements :** Stripe .NET SDK (Webhooks, Checkout Sessions, Customer Portal).
- **Deploiement :** Docker Multi-Stage Build, Render Cloud API, Vercel Web Hosting.

---

## Telechargements & Demo

- **Demo Web Live :** [https://www.mybudgett.xyz](https://www.mybudgett.xyz/)
- **Application Windows x64 :** [Telecharger l'installateur Windows (mybusiness.exe)](https://assistant-ai-0fr7.onrender.com/api/download/windows)

---

## Confidentialite & Licence

> **Note de Propriete Intellectuelle :**  
> Ce logiciel est un produit commercial proprietaire.  
> Le code source complet, l'architecture interne et les algorithmes sont heberges sur un depot prive et proteges par les lois sur le droit d'auteur.  
> 
> (c) 2026 mybudget / Assistant AI. Tous droits reserves.
