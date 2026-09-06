# Email Assistant

Welcome to the **Email Assistant** project! 

This repository contains an open-source AI-powered email assistant that helps you manage your inbox efficiently. It is built on top of [Inbox Zero](https://github.com/elie222/inbox-zero), an advanced AI application designed to help you spend less time processing emails.

## 🚀 Features

- **AI Personal Assistant:** Organizes your inbox and pre-drafts replies in your tone and style.
- **AI Rules for Email:** Use plain English rules to automate how your AI should handle incoming emails.
- **Cold Email Blocker:** Automatically identify and block unwanted cold emails.
- **Bulk Unsubscribe & Archive:** Clean up your inbox in seconds by getting rid of old or unread newsletters.
- **Email Analytics:** Visualize your email activity and trends over time.
- **Smart Filing:** Automatically save email attachments to your cloud storage (Google Drive, OneDrive).
- **Slack & Telegram Integration:** Manage your inbox directly from the messaging platforms you already use.

## 🛠️ Tech Stack

This project is built using modern web technologies:
- **Framework:** [Next.js](https://nextjs.org/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) & [shadcn/ui](https://ui.shadcn.com/)
- **Database:** [Prisma](https://www.prisma.io/) (Postgres)
- **Monorepo Management:** [Turborepo](https://turbo.build/)

## 📂 Project Structure

All the core application files are located in the `inbox-zero` directory, which operates as a monorepo containing various packages and applications:
- `inbox-zero/apps/web`: The main Next.js web application.
- `inbox-zero/packages/*`: Shared internal packages for database schemas, transactional emails, AI configurations, etc.

## 💻 Getting Started (Local Development)

To run this project locally, ensure you have **Node.js (v24+)**, **Docker**, and **pnpm (v10+)** installed.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/anjaneyulukampalla04-pixel/Email-Assistant.git
   cd Email-Assistant/inbox-zero
   ```

2. **Start the database and Redis services using Docker:**
   ```bash
   docker compose -f docker-compose.dev.yml up -d
   ```

3. **Install dependencies and setup environment variables:**
   ```bash
   pnpm install
   npm run setup
   ```

4. **Run database migrations:**
   ```bash
   cd apps/web && pnpm prisma migrate dev && cd ../..
   ```

5. **Start the development server:**
   ```bash
   pnpm dev
   ```
   Open `http://localhost:3000` in your browser to view the application.

## 🤝 Contributing

Feel free to fork this project, submit pull requests, or open issues to improve the AI Email Assistant further!