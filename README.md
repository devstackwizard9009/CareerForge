# CareerForge

**CareerForge** is an AI-powered career development platform that helps professionals build resumes, generate cover letters, prepare for interviews, and stay ahead with real-time industry insights.

## Features

- **AI Resume Builder** — Create polished, industry-tailored resumes
- **Cover Letter Generator** — Generate personalized cover letters for any role
- **Interview Preparation** — Practice with AI-driven mock interviews and track your progress
- **Industry Insights** — Access salary data, in-demand skills, and market trends across 50+ industries
- **Personalized Onboarding** — Get recommendations tailored to your experience and career goals

## Tech Stack

- [Next.js 15](https://nextjs.org) (App Router)
- [React 19](https://react.dev)
- [Tailwind CSS](https://tailwindcss.com)
- [Clerk](https://clerk.com) — Authentication
- [Prisma](https://www.prisma.io) — Database ORM
- [Google Gemini AI](https://ai.google.dev) — AI content generation
- [Inngest](https://www.inngest.com) — Background jobs

## Getting Started

### Prerequisites

- Node.js 18+
- A PostgreSQL database
- API keys for Clerk and Google Gemini

### Installation

1. Clone the repository and install dependencies:

```bash
npm install
```

2. Create a `.env` file in the project root with the following variables:

```env
DATABASE_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

GEMINI_API_KEY=
```

3. Run database migrations:

```bash
npx prisma migrate dev
```

4. Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the app.

## Project Structure

```
app/
  (auth)/          # Sign-in and sign-up pages
  (main)/          # Authenticated routes (dashboard, resume, interview, etc.)
  api/             # API routes
components/        # Shared UI components
data/              # Static content (features, FAQs, industries)
lib/               # Utilities, Prisma client, Inngest setup
actions/           # Server actions
prisma/            # Database schema and migrations
```

## Scripts

| Command         | Description                    |
| --------------- | ------------------------------ |
| `npm run dev`   | Start development server       |
| `npm run build` | Build for production           |
| `npm run start` | Start production server        |
| `npm run lint`  | Run ESLint                     |

## License

This project is private and not licensed for public distribution.
