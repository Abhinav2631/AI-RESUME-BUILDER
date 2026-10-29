# AI Resume Builder

A React/Vite application for generating job-application content with Gemini. It can draft cover letters, suggest resume improvements, identify keywords from a job description, estimate an ATS-style match score, and export generated content to PDF.

## Features in the application

- Draft role-specific cover letters using company and job details.
- Suggest improvements to resume content.
- Identify relevant keywords from a job description.
- Produce an estimated ATS-style match score with explanatory feedback.
- Export generated content to PDF.
- Review and edit generated text before using it.

## Technology stack

- **Frontend:** React, Vite, Bootstrap 5, custom CSS
- **AI:** Gemini API
- **PDF export:** jsPDF and html2canvas

## Run locally

1. Install a current Node.js LTS release and npm.
2. Run `npm install` from the repository root.
3. Copy `.env.example` to `.env`.
4. Set `VITE_GEMINI_API_KEY` to your Gemini API key.
5. Restart the dev server after changing environment variables and run `npm run dev`.

If the Gemini key is missing, the app displays a setup message rather than silently trying to call the API.

## Configuration and security

The client reads the Gemini key from `VITE_GEMINI_API_KEY` and provides feedback when it is not configured. This improves local setup over placing a key directly in source code, but it does **not** make the key secret: Vite `VITE_*` variables are exposed in the browser bundle. For a public production deployment, call Gemini through a backend service and apply appropriate access controls and usage limits.

## Repository-specific changes

- Replaced the inline Gemini API-key placeholder with `import.meta.env.VITE_GEMINI_API_KEY`.
- Added a clear message when the key is not configured.
- Added an `.env.example` file and local configuration guidance.

These changes improve configuration and local usability; they do not make the entire existing application an independently written project.

## Attribution and reuse

This repository is an authorised learning/adaptation copy of [AI-RESUME-BUILDER by Naresh Chary](https://github.com/NareshChary0430/AI-RESUME-BUILDER). The upstream project and its original implementation remain credited to the original creator. This copy is for personal learning and portfolio practice.
