# 🛠️ Visamate: Product Requirements Document (PRD)

> This file is intended for inclusion in your GitHub project repo at `/docs/VISAMATE_PRD.md`. It outlines implementation phases, app flow, and design system specifications.

**Role:** Head of Product (30+ years experience)  
**Project:** Visamate — A digital advisor and relocation companion for Americans applying for D7/D8 visas to Portugal

---

## 1. 🧭 Step-by-Step Implementation Plan

### Phase 1: Discovery & Planning
- Conduct stakeholder alignment & market review
- Finalize feature list and MVP requirements
- Map the full D7 and D8 visa journeys
- Draft wireframes and sitemap

### Phase 2: Design & Prototyping
- Build high-fidelity Figma prototypes
- Finalize branding and design system (color, type, UI kit)
- Usability testing with early adopters (5–10 digital nomads/expats)

### Phase 3: Core Development
- **Frontend:** Next.js 14, Tailwind CSS, shadcn/UI
- **Backend:** Supabase (auth, DB, file storage)
- **CMS:** Notion for structured content and guides
- Build:
  - Onboarding wizard (visa type recommender)
  - Dynamic checklist dashboard
  - Auth (email/password, Google optional)
  - Chatbot (OpenAI or custom agent)

### Phase 4: Marketplace Integration
- Vet and onboard certified lawyers and real estate agents
- Partner profile pages and intro request forms
- Analytics + event logging for lead generation

### Phase 5: Polish & Deploy
- Add page transitions, animations, hover states
- Ensure mobile responsiveness
- QA, accessibility audit, and testing
- Deploy to Vercel with CI/CD

### Phase 6: Post-Launch
- Set up usage analytics (PostHog, Segment)
- A/B test CTA flows and chatbot performance
- Gather feedback and iterate onboarding/checklists

---

## 2. 🔄 App Flow & User Journey

### Main Navigation:
- Home
- Start (Visa Quiz)
- Checklist
- Chatbot
- Marketplace
- Profile / Account

### User Flow:
1. **Landing Page**
   - Hero CTA: "Start Your Portugal Journey"
   - Feature overview and testimonials

2. **Onboarding Quiz**
   - Questions on income, remote work, purpose
   - Suggests D7 or D8 with rationale

3. **Checklist Generation**
   - Sections: Documents, Financials, Legal, Health
   - Interactive: checkboxes, notes, file upload
   - Login prompt to save progress

4. **Account Creation**
   - Auth via email or Google
   - Sync state to Supabase

5. **Chatbot Advisor**
   - Conversational UX with suggested questions
   - Deep links to checklist items and marketplace

6. **Marketplace Access**
   - Vetted profiles (lawyers, real estate agents)
   - "Request Intro" buttons (referral logged)

7. **Completion Page**
   - Visual checklist progress
   - Optional next steps: schedule consultation, join community

---

## 3. 🎨 Design System for Technical Product Designers

### Typography
- **Font:** Montserrat (Google Font)
- **Fallback:** system-ui, sans-serif
- **Weights:** 400 (body), 600 (UI), 700 (headings)

### Color Palette
- **Primary Blue:** `#0066cc`
- **Accent Cyan:** `#00bcd4`
- **Text:** `#1a1a1a`
- **Backgrounds:**
  - Base: `#ffffff`
  - Section: `#f9f9f9`
  - Borders: `#eaeaea`
- **Status:**
  - Success: `#2ecc71`
  - Warning: `#f39c12`
  - Error: `#e74c3c`

### Layout & Spacing
- **Grid:** 12-col desktop / 4-col mobile
- **Spacing unit:** 8px
- **Page padding:**
  - Mobile: 24px
  - Desktop: 64px

### Components
- **Card:** 16px padding, 12px border-radius, light shadows
- **Button:** Full-rounded, 16px vertical padding, `hover:shadow-md`
- **Modal:** Max-width 640px, centered, with blurred backdrop

### Effects
- Card: `shadow-sm` + border
- Button: `transition-all`, `hover:scale-105`, `duration-200`
- Framer Motion for page/section transitions
- Smooth scrolling for in-page anchors

### Responsive Behavior
- Mobile-first design
- Collapsed nav menu on screens <768px

### Animations
- **Checklist**: Progress bar grows as tasks are checked
- **Chatbot**: Typewriter intro, fading quick replies
- **Hero Section**: Scroll-triggered fade and bounce-in
