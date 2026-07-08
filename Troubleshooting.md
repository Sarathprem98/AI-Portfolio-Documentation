# 🛠 Troubleshooting Guide

This guide covers the most common issues you may encounter while setting up, customizing, and deploying the portfolio.

---

# Chatbot Issues

## Chatbot says "API Key is not configured"

### Cause

The required environment variable is missing.

### Solution

1. Create a `.env.local` file in the project root.
2. Add your API key.

Example (Groq):

```env
GROQ_API_KEY=your_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

Restart the development server after making changes.

---

## Chatbot returns 400 Bad Request

### Cause

- Invalid request
- Incorrect model name
- Missing request body

### Solution

- Verify the model name.
- Check `app/api/chat/route.ts`.
- Ensure your frontend is sending the correct payload.

---

## Chatbot returns 401 Unauthorized

### Cause

Invalid API Key.

### Solution

- Generate a new API Key.
- Update `.env.local`.
- Restart the server.

---

## Chatbot returns 429 Too Many Requests

### Cause

Free API limit exceeded.

### Solution

- Wait until your quota resets.
- Upgrade your API plan.
- Switch to another AI provider.

---

## Chatbot does not answer correctly

### Cause

The system prompt is not configured properly.

### Solution

Update the system prompt to restrict responses to:

- About
- Skills
- Experience
- Projects
- Certifications
- Resume
- Contact Information

---

# Resume Issues

## Resume is opening instead of downloading

Use the `download` attribute.

```tsx
<a href="/resume.pdf" download>
  Download Resume
</a>
```

---

## Resume not found (404)

Ensure the file exists inside:

```text
public/resume.pdf
```

---

# Images Not Loading

## Profile image missing

Check:

```text
public/images/
```

Verify the file name and path.

---

## Skills Logo Wall icons missing

Possible causes:

- Incorrect icon import
- Invalid icon name
- Missing package

Install required packages if necessary.

```bash
npm install react-icons
```

or

```bash
npm install simple-icons
```

---

# React Errors

## React does not recognize the `asChild` prop

### Cause

The component library being used does not support `asChild`.

### Solution

Replace:

```tsx
<Button asChild>
  <a href="#">Link</a>
</Button>
```

with:

```tsx
<a href="#">
  <Button>
    Link
  </Button>
</a>
```

or use the component library's recommended approach.

---

# Build Issues

## npm install fails

Delete:

```text
node_modules
package-lock.json
```

Reinstall:

```bash
npm install
```

---

## pnpm lockfile mismatch

Run:

```bash
pnpm install --no-frozen-lockfile
```

Commit the updated `pnpm-lock.yaml` file and push again.

---

## Vercel build failed

Before deploying, verify:

```bash
npm run build
```

Resolve any errors shown during the build.

---

# GitHub Issues

## Push rejected due to API key

### Cause

A secret (API key) was committed.

### Solution

- Remove `.env.local` from Git.
- Add `.env.local` to `.gitignore`.
- Remove the secret from Git history if necessary.
- Generate a new API key if it was exposed.

---

## Wrong GitHub username shown in commits

Configure Git with your correct details.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

# Deployment Issues

## Environment variables not working on Vercel

1. Open your Vercel project.
2. Go to **Settings → Environment Variables**.
3. Add the required variables.
4. Redeploy the project.

---

## Website not updating after push

Try:

- Confirm the latest commit reached GitHub.
- Trigger a redeploy in Vercel.
- Clear browser cache.

---

# Mobile Issues

## Layout looks broken on mobile

Check responsive Tailwind classes.

Test using:

- Chrome DevTools
- Edge DevTools
- Firefox Responsive Design Mode

---

## Skills Logo Wall loads slowly

Possible improvements:

- Use SVG icons instead of large PNGs.
- Lazy load non-critical components.
- Optimize icon rendering.
- Reduce unnecessary animations.

---

# Performance Tips

- Use Next.js Image component.
- Optimize images before uploading.
- Remove unused dependencies.
- Enable lazy loading where appropriate.
- Keep bundle size small.

---

# Need More Help?

If you're still facing issues:

- Review the project configuration.
- Verify environment variables.
- Check the browser console.
- Check the terminal output.
- Search the issue on GitHub or Stack Overflow.

---

## Before Creating an Issue

Please include:

- Operating System
- Node.js version
- Package manager (npm/pnpm)
- Error message
- Screenshot (if applicable)
- Steps to reproduce the issue

This information helps identify and resolve problems more quickly.

---

Happy Coding! 🚀
