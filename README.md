# Everest Sustainability Foundation (ESF) - Official Website

A modern, responsive website for the Everest Sustainability Foundation, built with Next.js 14, TypeScript, and Tailwind CSS. The website showcases ESF's mission to advance carbon resilience and sustainability initiatives in Nepal and globally.

## 🌟 Features

- **Modern Design**: Clean, professional interface with dark/light mode support
- **Responsive Layout**: Optimized for all devices (mobile, tablet, desktop)
- **Multilingual Support**: Internationalization with i18next
- **Contact Forms**: Web3Forms integration for reliable email delivery
- **Interactive Components**: Animated sections with Framer Motion
- **SEO Optimized**: Built-in SEO features with Next.js
- **Performance**: Optimized images and lazy loading

## 🚀 Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Forms**: Web3Forms API
- **Deployment**: Vercel (recommended)

## 📁 Project Structure

```
ESF/
├── .env.local                    # Environment variables (create this)
├── public/                       # Static assets
│   ├── logo/
│   ├── photos/
│   └── videos/
├── src/
│   ├── app/                      # Next.js app router
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── how-we-work/
│   ├── components/               # React components
│   │   ├── ui/                   # Reusable UI components
│   │   ├── about-section.tsx
│   │   ├── contact-section.tsx   # Web3Forms integration
│   │   ├── hero-section.tsx
│   │   └── ...
│   ├── data/                     # Static data files
│   └── lib/                      # Utility functions
├── components.json               # shadcn/ui configuration
├── tailwind.config.ts
├── tsconfig.json
└── package.json
```

## 🛠️ Installation & Setup

### Prerequisites

- Node.js 18+
- npm or yarn
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ESF.git
cd ESF
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Environment Configuration

Create a `.env.local` file in the project root:

```env
# Web3Forms Configuration - Dual Access Keys
NEXT_PUBLIC_WEB3FORMS_INQUIRY_ACCESS_KEY=your_inquiry_access_key_here
NEXT_PUBLIC_WEB3FORMS_QUOTATION_ACCESS_KEY=your_quotation_access_key_here
```

**Get your Web3Forms access keys:**

1. Visit [Web3Forms.com](https://web3forms.com/)
2. Create two access keys:
   - One for `info@everestsustainability.com` (General Inquiries)
   - One for `nishchalbaniya@everestsustainability.com` (Quotation Requests)

### 4. Run Development Server

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🌐 Deployment

### Vercel (Recommended)

1. **Connect Repository:**

   - Visit [Vercel.com](https://vercel.com/)
   - Import your GitHub repository
   - Vercel will auto-detect Next.js settings

2. **Configure Environment Variables:**

   - Go to Project Settings → Environment Variables
   - Add your Web3Forms access keys:
     ```
     NEXT_PUBLIC_WEB3FORMS_INQUIRY_ACCESS_KEY=your_inquiry_key
     NEXT_PUBLIC_WEB3FORMS_QUOTATION_ACCESS_KEY=your_quotation_key
     ```

3. **Deploy:**
   - Click "Deploy" - Vercel handles the rest!
   - Your site will be live at `https://your-project.vercel.app`

### Netlify

1. **Build Command:**

   ```bash
   npm run build
   ```

2. **Publish Directory:**

   ```
   .next
   ```

3. **Environment Variables:**
   Add the same environment variables as above in Netlify dashboard.

### Other Platforms

The project can be deployed to any platform that supports Next.js:

- **Railway**: Connect GitHub repo, add env vars, deploy
- **Render**: Connect GitHub repo, add env vars, deploy
- **DigitalOcean App Platform**: Connect GitHub repo, add env vars, deploy

## 📧 Contact Form Setup

The website includes two contact forms with Web3Forms integration:

- **General Inquiry Form**: Sends to `info@everestsustainability.com`
- **Quotation Request Form**: Sends to `nishchalbaniya@everestsustainability.com`

Each form uses a separate Web3Forms access key for proper email routing.

## 🎨 Customization

### Colors & Branding

Update colors in `tailwind.config.ts`:

```typescript
colors: {
  'esf-primary': '#your-primary-color',
  'esf-primary-light': '#your-light-color',
  'esf-primary-dark': '#your-dark-color',
}
```

### Content

- **Hero Section**: Edit `src/components/hero-section.tsx`
- **About Section**: Edit `src/components/about-section.tsx`
- **Contact Info**: Edit `src/components/contact-section.tsx`
- **Static Data**: Update files in `src/data/`

### Internationalization

Add new languages in `src/lib/i18n.ts` and create corresponding translation files.

## 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript checks
```

## 📱 Features Overview

### Homepage Sections

- **Hero Section**: Video background with call-to-action
- **About Section**: Mission, vision, and key focus areas
- **What We Do**: Services and programs
- **Our Work**: Projects and achievements
- **Contact**: Forms and office locations

### How We Work Page

- **Organization Structure**: Team and governance
- **Project Cycle**: Process overview
- **Thematic Programs**: Focus areas
- **Compliance**: Standards and certifications

## 🐛 Troubleshooting

### Common Issues

1. **Forms not sending emails:**

   - Check Web3Forms access keys in `.env.local`
   - Verify keys are correctly configured on Web3Forms.com

2. **Build errors:**

   - Run `npm run type-check` to identify TypeScript issues
   - Ensure all dependencies are installed

3. **Styling issues:**
   - Check Tailwind CSS classes
   - Verify `tailwind.config.ts` configuration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature/new-feature`
5. Submit a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support or questions:

- Email: info@everestsustainability.com
- Website: [Everest Sustainability Foundation](https://your-domain.com)

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Icons by [Lucide](https://lucide.dev/)
- Form handling by [Web3Forms](https://web3forms.com/)

---

**Everest Sustainability Foundation** - Advancing carbon resilience and sustainability for a better future.
