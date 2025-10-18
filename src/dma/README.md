# DSE Score Calculator 🎓

A modern web application to calculate your Hong Kong Diploma of Secondary Education (HKDSE) score and compare it with 2024 statistics.

## Features ✨

- **Best 5 Score Calculation**: Automatically calculates your best 5 subjects
- **Advanced Percentile Ranking**: See exactly where you stand among Hong Kong students
  - Compare against 18,027 day school candidates or 18,850 all candidates who achieved (332A)22+
  - Toggle between day school and all candidates comparison
  - See exact number of students you performed better than
  - View your score range and how many students share it
  - Get personalized performance messages with visual indicators
- **Accurate Statistical Placement**: Based on official 2024 HKDSE table3f data
  - Know your exact percentile (e.g., "94th percentile - Top 6%")
  - See how many students scored above and below you
  - Understand your score range context
- **Visual Analytics**: Interactive charts and graphs showing your performance
- **University Requirements Check**: Verify if you meet common JUPAS requirements (3322+2, 332A, 222A)
- **Subject Comparison**: Detailed breakdown of each subject's performance
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices

## Technology Stack 🛠️

- **Frontend Framework**: React 18 with TypeScript
- **UI Library**: HeroUI (Modern React UI components)
- **Build Tool**: Vite
- **Styling**: TailwindCSS v4
- **Charts**: Recharts

## Getting Started 🚀

### Prerequisites

- Node.js 18+ or Bun
- npm, pnpm, yarn, or bun

### Installation

1. Install dependencies:

```bash
npm install
# or
pnpm install
# or
bun install
```

2. Run the development server:

```bash
npm run dev
# or
pnpm dev
# or
bun dev
```

3. Open [http://localhost:5173](http://localhost:5173) in your browser

### Building for Production

```bash
npm run build
# or
pnpm build
# or
bun build
```

The build output will be in the `dist/` directory.
