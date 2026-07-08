# 🚀 AI Portfolio Template

A modern, AI-powered portfolio template built with **Next.js 15**, **React**, **TypeScript**, **Tailwind CSS**, **Motion**, and an **AI Chatbot**.

This repository is designed for developers, SDETs, QA Engineers, DevOps Engineers, Cloud Engineers, and students who want to build a professional portfolio quickly.

Simply clone the repository, replace the sample data with your own, configure your AI provider, and deploy.

---

## ✨ Features

- 🎨 Modern & Responsive UI
- 🌙 Dark / Light Theme
- 🤖 AI Portfolio Chatbot
- 💼 Experience Timeline
- 🚀 Featured Projects
- 🛠 Skills Logo Wall
- 📜 Certifications Section
- 📄 Resume Download
- 📱 Mobile Responsive
- ⚡ Fast Performance
- 🔍 SEO Optimized
- 🚀 One-Click Vercel Deployment

---

# 🖥 Live Demo
```
https://sarathprem.vercel.app
```

---
# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Framework | Next.js 15 |
| Language | TypeScript |
| Styling | Tailwind CSS |
| UI Components | shadcn/ui |
| Animation | Motion |
| Icons | Lucide React |
| AI Provider | Groq / OpenAI / Gemini |
| Deployment | Vercel |
| Version Control | Git & GitHub |

---

# 📂 Project Structure

```
app/
components/
lib/
public/
docs/

README.md
package.json
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/Sarathprem98/Sarath-Portfolio.git
```

Go to the project folder

```bash
cd your-repository
```

---

## 2. Install Dependencies

```bash
npm install
```

or

```bash
pnpm install
```

---

## 3. Run the Project

```bash
npm run dev
```

Open your browser

```
http://localhost:3000
```

---

# ⚙ Environment Variables

Create a file named

```
.env.local
```

Example

```env
GROQ_API_KEY=your_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

If you're using another AI provider, replace the variables accordingly.

Restart the development server after making changes.

---

# 🤖 AI Providers

This template supports multiple AI providers.

- Groq
- OpenAI
- Gemini

The API route can be updated to use your preferred provider.

Refer to:

```
docs/AI-Chatbot.md
```

---

# 📄 Customize Your Portfolio

Most personal information is stored in:

```
lib/data.ts
```

Update the following sections:

| Section | Update |
|----------|--------|
| Name | ✅ |
| Job Title | ✅ |
| About Me | ✅ |
| Skills | ✅ |
| Experience | ✅ |
| Projects | ✅ |
| Certifications | ✅ |
| Contact Details | ✅ |
| Social Links | ✅ |

---

# 🖼 Profile Picture

Replace your profile image inside

```
public/images/
```

Update the image path if necessary.

---

# 📄 Resume

Replace

```
public/resume.pdf
```

with your own resume.

If you change the filename, update the path in

```
lib/data.ts
```

---

# 💼 Projects

Open

```
lib/data.ts
```

Update each project:

- Title
- Description
- Technologies
- GitHub Link
- Live Demo
- Image

---

# 🛠 Skills

Update your skills inside

```
lib/data.ts
```

You can:

- Add new technologies
- Remove existing skills
- Change categories
- Update icons

The Skills Logo Wall will automatically update.

---

# 🌐 Social Links

Update

- GitHub
- LinkedIn
- Email
- Phone
- Location

inside

```
lib/data.ts
```
---

# 🤖 AI Chatbot

This portfolio includes an AI-powered chatbot that answers questions about your profile, experience, projects, and skills.

### Supported AI Providers

- Groq (Recommended)
- OpenAI
- Gemini

Update the API route located at:

```text
app/api/chat/route.ts
```

Configure your API key in:

```text
.env.local
```

Example:

```env
GROQ_API_KEY=your_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

Restart the development server after making changes.

For more details, see:

```text
docs/AI-Chatbot.md
```

---

# 🚀 Deployment

## Deploy to GitHub

Initialize Git if you haven't already:

```bash
git init
git add .
git commit -m "Initial commit"
```

Create a new GitHub repository and connect it:

```bash
git remote add origin https://github.com/<your-username>/<repository-name>.git
git branch -M main
git push -u origin main
```

---

## Deploy to Vercel

1. Sign in to Vercel.
2. Click **Add New → Project**.
3. Import your GitHub repository.
4. Add the required Environment Variables.
5. Click **Deploy**.

Every push to the `main` branch will automatically trigger a new deployment.

---

## Required Environment Variables

| Variable | Description |
|----------|-------------|
| GROQ_API_KEY | Your Groq API Key |
| GROQ_MODEL | AI model name |

If you're using another AI provider, replace these with the corresponding variables.

---

# 🌐 Custom Domain

After deployment, you can assign your own custom domain.

Example:

```
https://yourname.com
```

or

```
https://portfolio.yourname.com
```

---

# 📱 Mobile Responsive

The portfolio is optimized for:

- Desktop
- Laptop
- Tablet
- Mobile Devices

If you customize components, verify the layout on different screen sizes before deploying.

---

# 🔍 SEO

Update the metadata with your own information.

Recommended updates:

- Website Title
- Description
- Keywords
- Open Graph Image
- Favicon
- Social Preview Image

---

# 📦 Build for Production

Run:

```bash
npm run build
```

Preview the production build:

```bash
npm run start
```

---

# 🛠 Common Issues

### Chatbot not responding

- Verify your API key.
- Ensure `.env.local` exists.
- Restart the development server.

---

### Resume not downloading

- Place `resume.pdf` inside the `public` folder.
- Update the resume path if you rename the file.

---

### Build failed on Vercel

Try:

```bash
npm install
npm run build
```

Commit the changes and push again.

---

### Environment variables not working

- Check the variable names.
- Restart the server after changes.
- Add the same variables in your Vercel project settings.

---

# 📚 Documentation

Additional guides are available in the `docs` folder:

| File | Description |
|------|-------------|
| `AI-Chatbot.md` | Configure the AI chatbot |
| `Deployment.md` | GitHub and Vercel deployment |
| `Troubleshooting.md` | Common issues and fixes |

---

# 🤝 Contributing

Contributions are welcome.

If you'd like to improve this project:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit and push.
5. Open a Pull Request.

---

# 📄 License

This project is licensed under the **MIT License**.

Feel free to use, modify, and distribute it for personal or commercial projects.

---

# 🙌 Acknowledgements

This project was built using:

- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Motion
- Lucide React
- Groq AI / OpenAI / Gemini
- GitHub Copilot
- Vercel

Special thanks to the open-source community for providing amazing tools and libraries.

---

# ⭐ Support

If you found this project helpful:

- ⭐ Star this repository
- 🍴 Fork it
- 🐛 Report issues
- 💡 Suggest improvements

Happy Coding! 🚀
