<div align="center">

# 🍎 PureCheck - Food Adulteration Detection

**AI-Powered Food Safety Analysis | Instant Detection | Home Testing Methods**

[![Next.js](https://img.shields.io/badge/Next.js-15.3.3-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Google AI](https://img.shields.io/badge/Google_AI-Gemini-4285F4?style=for-the-badge&logo=google)](https://ai.google.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

[Live Demo](https://food-adultration-.vercel.app) · [Report Bug](https://github.com/rishukumar79/food-adultration-/issues) · [Request Feature](https://github.com/rishukumar79/food-adultration-/issues)

</div>

---

## 📖 Overview

**PureCheck** is a modern web application that helps consumers detect food adulteration using cutting-edge AI technology and practical home testing methods. Built with Next.js 15 and powered by Google's Gemini AI, it provides instant analysis of food items through image recognition and offers step-by-step manual testing procedures.

### ✨ Key Features

- 🤖 **AI-Powered Image Analysis** - Upload food images for instant adulteration detection using Gemini 2.5 Flash
- 🧪 **Manual Testing Guide** - Comprehensive home tests for 6 food categories
- 📊 **Detailed Reports** - Safety ratings, confidence scores, and verification steps
- 🎨 **Modern UI** - Beautiful, responsive interface built with Radix UI and Tailwind CSS
- 📱 **PWA Support** - Works offline with service worker functionality
- ⚡ **Fast Performance** - Optimized with Next.js 15 and Turbopack

---

## 🎯 Use Cases

- **Consumers**: Verify food quality before consumption
- **Small Businesses**: Quick quality checks for sourced ingredients  
- **Educational**: Learn about common adulterants and detection methods
- **Food Safety Awareness**: Understand risks and prevention

---

## 🚀 Tech Stack

### Core Technologies
- **Framework**: Next.js 15.3.3 (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 3.4 + shadcn/ui
- **AI Engine**: Google Genkit + Gemini 2.5 Flash
- **Form Management**: React Hook Form + Zod
- **State Management**: React Hooks

### UI Components
- Radix UI (Accessible primitives)
- Lucide React (Icons)
- Recharts (Data visualization)
- Embla Carousel (Image galleries)

---

## 📁 Project Structure

```
food-adultration-/
├── src/
│   ├── ai/                      # AI integration & flows
│   │   ├── genkit.ts           # Genkit configuration
│   │   └── flows/              # AI detection flows
│   ├── app/                     # Next.js App Router pages
│   │   ├── page.tsx            # Homepage
│   │   ├── detect/             # AI detection page
│   │   └── tests/[category]/   # Manual tests by category
│   ├── components/             
│   │   ├── ui/                 # shadcn/ui components
│   │   ├── header.tsx          # Navigation header
│   │   └── footer.tsx          # Footer component
│   ├── lib/                    # Utilities & data
│   │   ├── categories.ts       # Food categories config
│   │   ├── manual-tests.ts     # Testing procedures
│   │   └── utils.ts            # Helper functions
│   └── hooks/                  # Custom React hooks
├── public/                     # Static assets
│   ├── sw.js                   # Service worker
│   └── manifest.json           # PWA manifest
└── package.json
```

---

## 🛠️ Installation & Setup

### Prerequisites
- Node.js 20+ and npm
- Google AI API Key ([Get one here](https://aistudio.google.com/app/apikey))

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/rishukumar79/food-adultration-.git
   cd food-adultration-
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   # Create .env.local file
   echo "GOOGLE_GENAI_API_KEY=your_api_key_here" > .env.local
   ```

4. **Run development server**
   ```bash
   npm run dev
   ```
   
   Open [http://localhost:9002](http://localhost:9002) in your browser.

### Build for Production

```bash
npm run build
npm start
```

---

## 🌐 Deployment

### Deploy to Vercel (Recommended)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/rishukumar79/food-adultration-)

1. Push your code to GitHub
2. Import project in Vercel
3. Add environment variable:
   - `GOOGLE_GENAI_API_KEY`: Your Google AI API key
4. Deploy!

**📚 Detailed deployment guide**: See [DEPLOYMENT.md](./DEPLOYMENT.md)

---

## 💡 Features Breakdown

### 1️⃣ AI Detection
Upload an image of any food item and get:
- ✅ Adulteration status (Safe/Unsafe)
- 📈 Confidence score (0-100%)
- 🔬 Possible adulterants detected
- 📝 Verification recommendations

### 2️⃣ Food Categories
Explore manual tests for:
- 🍎 Fruits (Apples, Watermelon, etc.)
- 🥕 Vegetables (Green Peas, Potatoes, etc.)
- 🥛 Milk & Dairy
- 🫗 Oils & Fats
- 🌾 Pulses & Grains
- 🌶️ Spices

### 3️⃣ Manual Testing
Each test includes:
- What adulterant to look for
- Step-by-step procedure
- Scientific explanation
- Visual indicators

---

## 📸 Screenshots

<div align="center">

### Homepage
*Clean, modern landing page with category navigation*

### AI Detection
*Upload → Analyze → Get Results in seconds*

### Manual Tests
*Detailed procedures with safety tips*

</div>

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server (port 9002) |
| `npm run build` | Build for production |
| `npm start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | TypeScript type checking |
| `npm run genkit:dev` | Start Genkit development server |

---

## 🔐 Environment Variables

Create a `.env.local` file:

```env
# Required
GOOGLE_GENAI_API_KEY=your_google_ai_api_key

# Optional
NEXT_PUBLIC_APP_URL=http://localhost:9002
```

---

## 🐛 Known Issues

- Service Worker may need manual refresh after deployment
- Large image files (>5MB) may slow AI analysis
- Some older browsers may not support all PWA features

---

## 🗺️ Roadmap

- [ ] Add more food categories (beverages, processed foods)
- [ ] Multi-language support (Hindi, Spanish, etc.)
- [ ] User authentication & history tracking
- [ ] Mobile app (React Native)
- [ ] Barcode scanning integration
- [ ] Community-contributed test methods

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Prince Kumar Prajapati**

- GitHub: [@rishukumar79](https://github.com/rishukumar79)
- Repository: [food-adultration-](https://github.com/rishukumar79/food-adultration-)

---

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React Framework
- [Google AI](https://ai.google.dev/) - Gemini API
- [shadcn/ui](https://ui.shadcn.com/) - UI Components
- [Vercel](https://vercel.com/) - Hosting Platform
- Food safety data from various health organizations

---

## ⚠️ Disclaimer

This application is for educational and informational purposes only. While it uses advanced AI technology, **it should not replace professional food testing or health advice**. Always consult certified laboratories for definitive food safety analysis.

---

<div align="center">

**Made with ❤️ for Food Safety**

⭐ Star this repo if you find it helpful!



</div>