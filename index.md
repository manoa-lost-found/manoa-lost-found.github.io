<!-- Hero / Title -->
<h1 align="center">Manoa Lost &amp; Found</h1>
<p align="center"><em>A UH Manoa community app to report, browse, and recover lost items — built by students for students.</em></p>

<p align="center">
  <a href="https://manoa-lost-found.github.io"><b>Live Site</b></a> ·
  <a href="https://github.com/orgs/manoa-lost-found/repositories"><b>View on GitHub</b></a> ·
  <a href="https://github.com/manoa-lost-found/manoa-lost-and-found/issues"><b>Open an Issue</b></a> ·
  <a href="https://docs.google.com/document/d/1SYR9UNlJHreSRPiQces7M1lXAMndSw5lAGJjuAcbBvU/edit?usp=sharing"><b>Team Contract</b></a>
</p>

<p align="center">
  <img alt="Milestone" src="https://img.shields.io/badge/Milestone-M2-blue" />
  <img alt="GitHub Pages" src="https://img.shields.io/badge/GitHub%20Pages-live-brightgreen" />
  <img alt="Status" src="https://img.shields.io/badge/Status-Proposal%20%2F%20Mockups-orange" />
</p>

**Proposers:** Jermaine Bruno • Michael Lau • Brandon Nguyen • Edward Uzueta • Justin Lai  
**Date:** December 2, 2025

---

## Table of Contents
- [Overview](#overview)
- [Roles & Capabilities](#roles--capabilities)
- [App Features (M1 Scope)](#app-features-m1-scope)
- [App Features (M2 Scope)](#app-features-m2-scope)
- [User Guide (Mockup Walkthrough)](#user-guide-mockup-walkthrough)
- [User Guide (Walkthrough)](#user-guide-walkthrough)
- [Deployment](#deployment)
- [Risks & Mitigations](#risks--mitigations)
- [Potential Enhancements](#potential-enhancements)
- [Team](#team)
- [Developers Guide](#developers-guide)

---

## Overview

### The Problem
Each semester, UH Manoa students lose countless items — IDs, water bottles, textbooks, AirPods, and other valuables. While the university technically has a Lost & Found system, it’s inefficient and fragmented. The current process involves emailing departments, calling offices, or physically visiting locations like Campus Center or the Library. There’s no centralized platform for checking updates, leaving students unsure if their lost items will ever be found.

### The Solution
**Manoa Lost & Found** is a centralized digital platform that unifies reporting and recovering lost items across UH Manoa. Students and staff can:
- Post **Lost** or **Found** items with descriptions, images, and locations.
- Receive **notifications** when potential matches are found.
- Use **UH authentication** for security and campus-only access.
- Route physical returns through **official UH offices** for verified recovery.

> All item exchanges are handled through official UH offices — no private handoffs.

---

## Roles & Capabilities

### Users (Students & Staff)
- Create **Lost Item** reports including photo, category, description, and last-seen location/time.
- Set **alerts/preferences** (keywords, buildings, or item types).
- Access a **personal dashboard** showing “My Lost Items,” “My Found Items,” and “Matches & Alerts.”

### Finders (Any Authenticated User)
- Post **Found Item** reports (photo, where/when found, where turned in).
- Use an in-app **“How to Turn In Items”** page listing official drop-off offices and instructions.
- Notify the rightful owner securely via UH email without direct contact.

### Admins (Campus Center / Library Staff)
- **Verify** items received at official drop-off points.
- Update item status (Received → Ready for Pickup → Recovered).
- **Flag duplicates**, moderate posts, and manage user roles.
- Configure **drop-off locations**, contact info, and office hours.

---

## App Features (M1 Scope)

<a href="https://github.com/orgs/manoa-lost-found/projects/1/views/7"><b>M1 Project Page</b></a>

- UH-authenticated access (campus-only)
- Tabs for **Lost** and **Found** item feeds
- Advanced filters: category, date, building, keyword
- Create/Edit/Delete posts with photo uploads

> M1 focuses on **design and functionality**

---

## App Features (M2 Scope)

<a href="https://github.com/orgs/manoa-lost-found/projects/2/views/1"><b>M2 Project Page</b></a>

- User Dashboard  
- Item detail pages  
- Admin functions  
- Recovery instructions pages  
- Turn-in instructions  
- Locations directory  

> M2 focuses on **implementing user features and admin workflows**

---

## Future Features
- AI-based match notifications  
- Admin verification dashboard  
- “How to Turn In Items” process pages  
- Campus map with markers for lost/found areas  
- Auto-archiving inactive posts  

---

## User Guide (Mockup Walkthrough)

1. **Landing → Login (UH SSO)** → Dashboard  
2. **Report Lost Item**  
3. Your lost item appears in the feed  
4. Finder submits Found item  
5. Admin verifies item  
6. Owner picks up item  

---

## User Guide (Walkthrough)

### Landing Page
![Landing Page](public/landing.png)  
![Sign In Page](public/user-signin.png)

### Lost/Found Feed  
![Items Feed Page](public/item-feed.png)

### User Dashboard  
![Dashboard Page](public/user-dashboard.png)

### Post Lost Item Form  
![Post Lost Item Page](public/post-lost.png)

### Post Found Item Form  
![Post Found Item Page](public/post-found.png)

### Item Details  
![Item Details Page](public/item-details.png)

### Recovery Instructions  
<img src="public/item-detail.png" width="700" />  
<img src="public/locations.png" width="700" />  
<img src="public/staff-verify.png" width="700" />

### Locations Directory  
![Map Locations Page](public/map-locations.png)

---

## Deployment

- **Live Site:** https://manoa-lost-and-found.vercel.app  
- **Repository:** https://github.com/manoa-lost-found/manoa-lost-and-found  

---

## Risks & Mitigations

| Risk | Mitigation |
|------|------------|
| UH authentication complexity | Start with mock login; add SSO later |
| Duplicate posts | Admin merge tools |
| Matching accuracy | Add AI/fuzzy matching |
| Safety | Require official office pickup |

---

## Potential Enhancements

- AI synonym search  
- QR poster generator  
- Map integration  
- Auto-archiving  
- Statistics dashboard  

---

## Team

| Name | Focus |
|------|-------|
| **Jermaine Bruno** | Admin workflows |
| **Michael Lau** | Matching system |
| **Brandon Nguyen** | UI/UX & Mockups |
| **Edward Uzueta** | Locations & Data |
| **Justin Lai** | Frontend Integration |

---

## Developers Guide

This is the **Manoa Lost & Found Developers Guide**.

---

### System Requirements
- Node.js v18+  
- npm  
- Git  
- VS Code  
- Vercel Postgres (Neon)  
- Playwright (auto-installed)  

---

### Downloading the Project

```bash
git clone https://github.com/manoa-lost-found/manoa-lost-and-found.git
cd manoa-lost-and-found
```

---

### Environment Setup

Create a `.env` file:

```env
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-here"

POSTGRES_DATABASE="verceldb"
POSTGRES_HOST="***"
POSTGRES_PASSWORD="***"
POSTGRES_USER="default"

POSTGRES_PRISMA_URL="postgres://..."
POSTGRES_URL_NON_POOLING="postgres://..."
POSTGRES_URL_NO_SSL="postgres://..."

DATABASE_URL="${POSTGRES_PRISMA_URL}"
```

---

### Installing Dependencies

```bash
npm install
```

---

### Database Setup (Prisma)

```bash
npx prisma generate
npx prisma db push
npx prisma db seed
```

---

### Running the Application

```bash
npm run dev
```

---

### Project Structure

```txt
app/
  api/
  dashboard/
  list/
  report/
  item/[id]/
components/
lib/
prisma/
public/
tests/
styles/
```

---

### Modifying the System

#### Updating the Navbar

File:

```
components/Navbar.tsx
```

#### Adding New Pages

```
app/campus-map/page.tsx
```

#### Updating the Database Schema

```bash
npx prisma db push
npx prisma generate
```

#### Creating API Routes

```
app/api/<route>/route.ts
```

#### Updating Authentication

```
lib/authOptions.ts
```

---

## Testing

Run Playwright:

```bash
npx playwright test
```

Headed mode:

```bash
npx playwright test --headed
```

---

## Continuous Integration

GitHub Actions automatically checks:

- ESLint  
- Playwright  
- Build success  

---

## Deployment

1. Push to GitHub  
2. Connect to Vercel  
3. Add environment variables  
4. Deploy  

---

## Contributing Workflow

```bash
git checkout -b issue-XX-description
git commit -m "issue-XX: implemented feature"
git push -u origin issue-XX-description
```

Open PR → Link Issue → Move card → Review → Merge.

---

<p align="center"><sub>Made with ❤️ by UH Manoa students — inspired by Bowfolios/Techfolios.</sub></p>

<p align="center">
  <a href="https://github.com/manoa-lost-found/manoa-lost-found/edit/Project-page/docs/index.md">✏️ Edit this page on GitHub</a>
</p>
