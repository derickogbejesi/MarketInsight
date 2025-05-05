# MarketInsight

A SaaS platform that generates data-driven market plans for businesses.

## Overview

MarketInsight helps businesses make informed decisions by providing sophisticated market analysis and personalized go-to-market strategies. Our platform leverages advanced analytics to deliver actionable insights that drive growth and competitive advantage.

## Features

- **Data-Driven Insights**: Analyze market trends and customer data to inform strategic decisions
- **SWOT Analysis**: Identify strengths, weaknesses, opportunities, and threats
- **Persona & Competitor Mapping**: Understand your target audience and competitive landscape
- **Market Simulation**: Test your strategies in simulated market environments
- **Go-to-Market Planning**: Develop comprehensive plans tailored to your business goals

## Tech Stack

- **Frontend**: Next.js 14+ with TypeScript
- **UI Components**: Custom UI components with shadcn/ui
- **State Management**: React Query
- **Authentication**: Custom auth flow
- **Payment Processing**: Paystack integration

## Getting Started

### Prerequisites

- Node.js 18+
- Bun (or npm/yarn)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/market-insight.git
cd market-insight
```

2. Install dependencies:
```bash
bun install
```

3. Create a `.env.local` file in the root directory with the following variables:
```
NEXT_PUBLIC_API_BASE_URL=http://localhost:8080

NEXT_PUBLIC_PAYSTACK_PLAN_PROFESSIONAL=your_professional_plan_id
NEXT_PUBLIC_PAYSTACK_PLAN_ENTERPRISE=your_enterprise_plan_id

NEXT_PUBLIC_PAYSTACK_PLAN_PROFESSIONAL_PRICE=your_professional_plan_price
NEXT_PUBLIC_PAYSTACK_PLAN_ENTERPRISE_PRICE=your_enterprise_plan_price

NEXT_PUBLIC_PAYSTACK_PUBLIC_KEY=your_paystack_public_key
```

4. Run the development server:
```bash
bun run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Project Structure

```
.
├── public/           # Static assets
├── src/
│   ├── _api/         # API service layer
│   ├── app/          # Next.js app router pages and components
│   │   ├── (auth)/   # Authentication routes (login/signup)
│   │   ├── board/    # Main application dashboard
│   │   └── plans/    # Subscription plans and pricing
│   ├── components/   # Shared UI components
│   ├── hooks/        # Custom React hooks
│   ├── lib/          # Utility libraries
│   └── utils/        # Helper functions
```

## Authentication

The application includes a complete authentication system with login and signup functionality. Users must authenticate before accessing the main board features.

## Subscription Plans

MarketInsight offers tiered subscription plans:
- **Professional**: For growing businesses
- **Enterprise**: For established organizations

Plans can be managed through the `/board/plans` route where users can upgrade, downgrade, or manage their current subscription.

## Deployment

This application is configured for easy deployment on Vercel:

```bash
vercel
```

## Environment Variables

| Variable | Description |
|----------|-------------|
| `NEXT_PUBLIC_API_BASE_URL` | Base URL for the backend API |
| `NEXT_PUBLIC_PAYSTACK_PLAN_PROFESSIONAL` | Paystack ID for the Professional plan |
| `NEXT_PUBLIC_PAYSTACK_PLAN_ENTERPRISE` | Paystack ID for the Enterprise plan |
| `NEXT_PUBLIC_PAYSTACK_PLAN_PROFESSIONAL_PRICE` | Price of the Professional plan |
| `NEXT_PUBLIC_PAYSTACK_PLAN_ENTERPRISE_PRICE` | Price of the Enterprise plan |
| `NEXT_PUBLIC_PAYSTACK_PUBLIC_KEY` | Your Paystack public key |

## License

[MIT](LICENSE)
