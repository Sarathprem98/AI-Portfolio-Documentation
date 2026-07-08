# 🚀 Deployment Guide

This guide explains how to deploy your portfolio to GitHub and Vercel.

---

# Prerequisites

Before deploying, make sure you have:

- Git installed
- GitHub account
- Vercel account
- Node.js installed
- Project running successfully using `npm run dev`

---

# Step 1 - Build the Project

Before deploying, ensure the project builds successfully.

```bash
npm run build
```

If the build succeeds without errors, you're ready to deploy.

---

# Step 2 - Create a GitHub Repository

1. Log in to GitHub.
2. Click **New Repository**.
3. Enter a repository name.
4. Choose **Public** or **Private**.
5. Click **Create Repository**.

---

# Step 3 - Push the Project to GitHub

Initialize Git (if not already initialized):

```bash
git init
```

Add all files:

```bash
git add .
```

Commit the changes:

```bash
git commit -m "Initial portfolio commit"
```

Add your GitHub repository as the remote:

```bash
git remote add origin https://github.com/<your-username>/<repository-name>.git
```

Rename the branch:

```bash
git branch -M main
```

Push the code:

```bash
git push -u origin main
```

Your project is now available on GitHub.

---

# Step 4 - Deploy to Vercel

1. Go to https://vercel.com
2. Sign in with GitHub.
3. Click **Add New Project**.
4. Import your repository.
5. Click **Deploy**.

Vercel will automatically detect that the project uses Next.js.

---

# Step 5 - Configure Environment Variables

If your portfolio uses an AI chatbot, add the required environment variables before deploying.

For Groq:

```env
GROQ_API_KEY=your_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

For OpenAI:

```env
OPENAI_API_KEY=your_api_key
OPENAI_MODEL=gpt-5.5
```

For Gemini:

```env
GEMINI_API_KEY=your_api_key
GEMINI_MODEL=gemini-2.5-flash
```

After adding the variables, redeploy the project.

---

# Step 6 - Custom Domain

After deployment:

1. Open your Vercel project.
2. Go to **Settings → Domains**.
3. Add your custom domain.
4. Follow the DNS instructions provided by Vercel.

Example:

```
https://yourname.com
```

or

```
https://portfolio.yourname.com
```

If you don't own a domain, you can continue using the free Vercel domain:

```
https://your-project.vercel.app
```

---

# Step 7 - Automatic Deployments

Every push to the **main** branch automatically triggers a new deployment.

Example workflow:

```bash
git add .
git commit -m "Updated projects section"
git push
```

Vercel will build and publish the latest version automatically.

---

# Updating the Portfolio

Whenever you update:

- About section
- Experience
- Projects
- Skills
- Resume
- Contact details
- Chatbot

Commit and push the changes:

```bash
git add .
git commit -m "Updated portfolio"
git push
```

Within a few minutes, the live site will be updated.

---

# Deployment Checklist

Before deploying, verify the following:

- Project builds successfully (`npm run build`)
- `.env.local` is **not** committed to GitHub
- Environment variables are added in Vercel
- Resume is placed in the `public` folder
- Social links are updated
- Profile image is updated
- Personal information is updated
- AI chatbot is working
- Mobile view is tested

---

# Common Deployment Issues

## Build Failed

Run:

```bash
npm install
npm run build
```

Fix any build errors before deploying again.

---

## Environment Variables Not Working

- Check the variable names.
- Restart the development server.
- Add the same variables in Vercel.
- Redeploy the project.

---

## GitHub Push Rejected

Possible reasons:

- API keys committed to Git
- Branch protection rules
- Authentication issues

Solution:

- Remove secrets from commits.
- Use `.gitignore` for `.env.local`.
- Push again.

---

## Vercel Build Error

Common causes:

- Missing dependencies
- Outdated lockfile
- Incorrect environment variables

Run:

```bash
npm install
npm run build
```

Commit the updated lockfile and push again.

---

# Helpful Resources

- GitHub: https://github.com
- Vercel: https://vercel.com
- Next.js Documentation: https://nextjs.org/docs

---

Congratulations! 🎉

Your portfolio is now live and ready to share with recruiters, hiring managers, and clients.
