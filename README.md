# CareerPilot-AI-Powered-Job-Preparation-Platform

A full-stack Gen AI web application that helps users prepare for job applications by analyzing their resume against a job description, identifying skill gaps, generating role-specific interview questions, and creating an ATS-optimized resume PDF.

Features

Upload a resume in PDF format

Add a job description for analysis

AI-based skill gap analysis

Identify matched and missing skills

Generate role-specific interview questions and answers

Generate an ATS-optimized resume

Download the generated resume as a PDF

Secure user authentication with JWT

Backend token blacklisting for logout

Protected routes for authenticated users

Tech Stack

Frontend

React.js

Vite

SCSS

React Router

Axios

Context API

Custom Hooks

Backend

Node.js

Express.js

MongoDB Atlas

Mongoose

JWT

bcrypt

AI & Processing

Gemini API

Zod

Multer

pdf-parse

Puppeteer

How It Works

Resume PDF + Job Description
            ↓
      PDF Text Extraction
            ↓
       Gemini AI Analysis
            ↓
 ┌──────────┼───────────┐
 ↓          ↓           ↓
Matched   Skill Gaps   Interview
Skills                Questions
            ↓
    ATS-Optimized Resume
            ↓
       PDF Generation

AI Analysis

The backend sends the extracted resume text and job description to the Gemini API.

The AI generates structured information including:

Matched skills

Missing skills / skill gaps

Role-specific interview questions and answers

ATS-optimized resume content

ATS score

Zod is used to validate the AI response against a predefined schema before the result is used by the application.

Resume Processing & PDF Generation

User uploads a resume PDF.

Multer handles the file upload.

pdf-parse extracts the resume text.

Resume text and job description are sent to Gemini.

Gemini generates an ATS-optimized resume in HTML format.

Puppeteer renders the HTML using headless Chrome.

The generated resume is exported as an A4 PDF for download.

