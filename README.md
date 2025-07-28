# React + TypeScript + Tailwind + Vite Starter Template

A modern, containerized development environment for React applications with TypeScript, Tailwind CSS, Vite, and Claude Code integration.

## 🚀 Features

- **React 18** - Latest React with modern hooks and features
- **TypeScript** - Type-safe development with full IntelliSense
- **Tailwind CSS** - Utility-first CSS framework for rapid styling
- **Vite** - Lightning-fast build tool with hot module replacement
- **Claude Code** - AI-powered coding assistant built into your terminal
- **DevContainer** - Consistent, isolated development environment
- **Node.js 22 LTS** - Latest long-term support version of Node.js

## 🛠️ What's Included

### Development Tools
- **VS Code Extensions**: Tailwind IntelliSense, Prettier, ESLint, TypeScript support
- **Claude Code CLI**: AI assistant for coding tasks and explanations
- **Auto-formatting**: Code formatting on save with Prettier
- **Live Reload**: Instant updates with Vite's dev server

### Pre-configured Setup
- Port forwarding (5173) with auto-preview
- Optimized VS Code settings
- Node.js 22 LTS runtime
- Git integration ready

## 🚦 Quick Start

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [VS Code](https://code.visualstudio.com/)
- [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Getting Started

1. **Use this template**
   ```bash
   # Option 1: Clone this repository
   git clone https://github.com/yourusername/react-starter-template.git my-project
   cd my-project
   
   # Option 2: Use with DevPod
   # Enter this repo URL as workspace source in DevPod
   ```

2. **Open in VS Code**
   ```bash
   code .
   ```

3. **Start development container**
   - When prompted, click "Reopen in Container"
   - Or use Command Palette: `Ctrl/Cmd + Shift + P` → "Dev Containers: Reopen in Container"

4. **Wait for setup** (first time takes ~2-3 minutes)
   - Container builds automatically
   - Dependencies install via `npm install`
   - Dev server starts on port 5173

5. **Start coding!**
   - Your React app will be available at `http://localhost:5173`
   - Edit files in `src/` and see changes instantly

## 🤖 Using Claude Code

Claude Code is pre-installed and ready to help with your development:

```bash
# First time setup - authenticate with Claude
claude

# Example commands
claude "Create a new React component for a user profile card"
claude "Explain this TypeScript interface"
claude "Add error handling to this function"
claude "Generate unit tests for this component"
```

### Claude Code Features
- **Code Generation**: Create components, functions, and tests
- **Code Explanation**: Understand complex code patterns
- **Debugging Help**: Identify and fix issues
- **Git Integration**: Commit messages, branch management
- **Natural Language**: Just describe what you want in plain English

## 📁 Project Structure

```
my-project/
├── .devcontainer/
│   └── devcontainer.json      # Container configuration
├── src/
│   ├── App.tsx               # Main app component
│   ├── main.tsx              # React entry point
│   └── index.css             # Global styles with Tailwind
├── public/
├── package.json              # Dependencies and scripts
├── vite.config.ts            # Vite configuration
├── tailwind.config.js        # Tailwind configuration
├── tsconfig.json             # TypeScript configuration
└── README.md                 # This file
```

## 🎨 Customization

### Adding Dependencies
```bash
# Inside the container terminal
npm install package-name
# or
npm install -D package-name  # for dev dependencies
```

### VS Code Extensions
Edit `.devcontainer/devcontainer.json` to add more extensions:
```json
"extensions": [
  "bradlc.vscode-tailwindcss",
  "esbenp.prettier-vscode",
  "your-extension-id"
]
```

### Tailwind Configuration
Customize colors, fonts, and utilities in `tailwind.config.js`:
```js
module.exports = {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        primary: '#your-color'
      }
    }
  }
}
```

## 📦 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run format       # Format code with Prettier
```

## 🐳 Container Details

The development container includes:
- **Base Image**: `mcr.microsoft.com/devcontainers/typescript-node:22`
- **Node.js**: Version 22 LTS (latest long-term support)
- **Package Manager**: npm (yarn and pnpm also available)
- **Shell**: Bash with enhanced terminal experience
- **Security**: Isolated environment with no access to host system

## 🔧 Troubleshooting

### Container Won't Start
- Ensure Docker Desktop is running
- Try rebuilding: Command Palette → "Dev Containers: Rebuild Container"

### Port Already in Use
- Change port in `vite.config.ts`:
```ts
export default defineConfig({
  server: {
    port: 3000  // or any other port
  }
})
```

### Claude Code Authentication
- Run `claude` in terminal and follow authentication prompts
- You'll need either Claude Max subscription or Claude API key

### Slow Performance
- Ensure Docker Desktop has sufficient resources (4GB+ RAM recommended)
- On Windows, use WSL2 backend for better performance

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Anthropic** for Claude Code integration
- **Vercel** for Vite and modern tooling
- **Tailwind CSS** team for the utility-first framework
- **Microsoft** for VS Code and DevContainers

---

**Happy coding!** 🎉 If you run into any issues or have suggestions, please open an issue on GitHub.