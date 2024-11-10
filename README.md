# Sahamati--hackathon-nominee-ninja-
This is a project that i worked with my team as part of the Hackthon hosted by Shamati&lt;>dev folio
This is a Next.js project bootstrapped with create-next-app. Scope of the project:

We are aiming to use the Account Aggregator framework, coupled with the government APIs(AP SETU) of user details, in order to build a one stop view of all your financial assets that are secured for your loved ones.
By monitoring your accounts which are missing their Nominee details, and by buildign your family tree to help you seamlessly choose and add nominee details. Further, we are also plannign to integrate with the onboarding forms of all financial institutions, and fintehc apps, so that customers will simply need to click on "Fill with IceBreaker" in roder to ensure all mandatory fields have been completely filled up, leaving no vulnerabilities int eh accounts.

Getting Started
First, run the development server:

npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
Open http://localhost:3000 with your browser to see the result.

You can start editing the page by modifying app/page.tsx. The page auto-updates as you edit the file.

This project uses next/font to automatically optimize and load Geist, a new font family for Vercel.

Learn More
To learn more about Next.js, take a look at the following resources:

Next.js Documentation - learn about Next.js features and API.
Learn Next.js - an interactive Next.js tutorial.
You can check out the Next.js GitHub repository - your feedback and contributions are welcome!

Table of Contents Technical Scope Project Architecture User Flows API Integration Dependencies Setup and Installation Environment Variables

Technical Scope Frontend Next.js 13+ with App Router React Server Components TypeScript for type safety Tailwind CSS for styling shadcn/ui component library Client-side state management with React hooks

Backend Node.js Express server PostgreSQL database Sequelize ORM RESTful API architecture Cron jobs for scheduled tasks JWT authentication Integration Points Account Aggregator Framework CBSE Certificate Verification API RBI Unclaimed Deposits Portal Government ID Verification APIs

Project Architecture Database Schema Users (Personal Information) Family Members Financial Accounts Nominees Consent Requests API Responses Data Request Sessions Auth Tokens API Services Authentication Service

Token generation and management User authentication Consent Management Service

Consent request handling Status tracking Data fetch management Account Management Service

Financial account tracking Nominee management Family tree management Document Verification Service

CBSE certificate verification Government ID verification User Flows New User Journey User signs up with basic information Redirected to landing page Prompted for Account Aggregator consent Consent flow initiated Financial accounts fetched and displayed Option to add nominees for accounts Existing User Journey User logs in Views dashboard with financial accounts Can manage nominees for accounts Access to family tree management Can check unclaimed accounts Nominee Management Flow View accounts without nominees Select accounts for nominee assignment Choose nominees from family tree Set allocation percentages Confirm nominee assignments API Integration Account Aggregator Framework

Token Generation (24-hour refresh) POST https://api.sandbox.sahamati.org.in/iam/v1/user/token/generate

Consent Request POST {{service_base_url}}/v2/consents/request

Consent Status Check POST {{service_base_url}}/v2/consents/fetch

Data Request POST {{service_base_url}}/v2/data/request

Data Fetch POST {{service_base_url}}/v2/data/fetch

Deploy on Vercel
The easiest way to deploy your Next.js app is to use the Vercel Platform from the creators of Next.js.

Check out our Next.js deployment documentation for more details.
