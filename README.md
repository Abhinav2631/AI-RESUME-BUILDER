# AI Resume Builder

A React application that calls the Gemini API to draft a tailored cover letter, suggest resume improvements, identify keywords from a job description, and provide an estimated ATS-style match score. It supports PDF export for generated results.

## Features

- Draft cover letters using company, job description, experience level, and tone.
- Suggest resume content improvements and relevant keywords.
- Provide an estimated ATS-style match score with an explanation.
- Export generated content to PDF.

## Tech stack

- React + Vite
- Gemini API
- Bootstrap 5 and custom CSS
- jsPDF and html2canvas

> This repository contains a client-side React app; a separate backend is not included.

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/Abhinav2631/AI-RESUME-BUILDER.git
cd AI-RESUME-BUILDER
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure Gemini

Copy `.env.example` to `.env` and set `VITE_GEMINI_API_KEY` to your own key. Restart the development server after changing environment variables. Never commit `.env` or a real API key.

**Security note:** because this version calls Gemini directly from the browser, a Vite `VITE_*` key is visible to users of the built application. For a public deployment, use a server-side API proxy or a tightly restricted key with suitable quotas and restrictions.

### 4. Start the application

```bash
npm run dev
```

### 5. Build and lint

```bash
npm run build
npm run lint
```

## Usage

Enter the company, job description, experience level, and preferred cover-letter tone. Optionally paste resume content, then request the generated materials. Review all AI-generated content for accuracy before using it in an application.

## Attribution and reuse

This repository is an authorized learning/adaptation copy of [AI-RESUME-BUILDER by Naresh Chary](https://github.com/NareshChary0430/AI-RESUME-BUILDER). The upstream project and its original implementation remain credited to the original creator. This copy has been prepared for personal learning and portfolio practice with permission.
