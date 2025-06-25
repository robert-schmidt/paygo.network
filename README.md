# PayGo.Network 🚀

> Affordable AI chat and image generation services with a pay-as-you-go credit system. No subscriptions, just pay for what you use.

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Web3](https://img.shields.io/badge/Web3-3C3C3D?style=for-the-badge&logo=web3.js&logoColor=white)

## 🌟 Features

### AI Chat & Completion
- **Multiple AI Providers** - OpenAI GPT, Anthropic Claude, Google Gemini, xAI Grok, and HuggingFace models
- **Real-time Streaming** - Watch AI responses generate in real-time
- **Secure Conversations** - Server-side AES-256-CBC encryption for all messages
- **Chat Sharing** - Share conversations via unique links

### Image Generation
- **DALL-E Integration** - Generate images with DALL-E 2 and DALL-E 3
- **Text-to-Image** - Create images from natural language descriptions
- **Image Editing** - Modify existing images with AI
- **Image Variations** - Generate variations of uploaded images

### Payment & Credits
- **Pay-As-You-Go Model** - No subscriptions, purchase credits as needed
- **Multiple Payment Methods**:
  - Credit/debit cards via Stripe
  - Cryptocurrency (SOL and USDC) via Solana blockchain
- **Transparent Pricing** - Real-time credit usage tracking

### Security & Authentication
- **Web3 Authentication** - Login with email or crypto wallets via Privy.io
- **Server-Side Encryption** - All data encrypted with user-specific keys
- **Rate Limiting** - Built-in protection against abuse
- **ReCaptcha Integration** - Bot protection with v2/v3 support

### Administration
- **Admin Dashboard** - Comprehensive panel built with Filament v3
- **Dynamic Configuration** - Toggle services on/off without code changes
- **API Key Management** - Centralized management for all external services

## 🛠️ Tech Stack

### Backend
- **Framework**: Laravel 12
- **Language**: PHP 8.4+
- **Database**: MySQL 8.0
- **Cache**: Redis
- **Queue**: Laravel Queue with Redis driver
- **Admin Panel**: Filament v3

### Frontend
- **Framework**: Alpine.js
- **Styling**: TailwindCSS
- **Build Tool**: Vite
- **Icons**: Heroicons

### Infrastructure
- **Containerization**: Docker & Docker Compose
- **Web Server**: Nginx

### AI & ML APIs
- **OpenAI** - GPT-4, GPT-4 Turbo, GPT-3.5 Turbo, DALL-E 2, DALL-E 3
- **Anthropic** - Claude 3 models (Opus, Sonnet, Haiku)
- **Google AI** - Gemini models
- **xAI** - Grok models
- **HuggingFace** - Open-source models via Inference API

### Payment & Blockchain APIs
- **Stripe** - Credit card payment processing
- **Solana Blockchain** - Cryptocurrency payments (SOL and USDC)
- **Helius RPC** - Solana blockchain access
- **CoinGecko** - Real-time cryptocurrency price data

### Authentication & Security
- **Privy.io** - Web3 wallet and email authentication
- **Google ReCaptcha** - Bot protection (v2/v3)
- **Firebase JWT** - Token verification

### Communication & Analytics
- **Email Providers** - SMTP, Amazon SES, Postmark, Resend
- **Google Analytics 4** - Usage tracking and analytics

## 🏗️ Architecture

### Core Components

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Web Server    │────▶│  Laravel App    │────▶│    Database     │
│    (Nginx)      │     │                 │     │    (MySQL)      │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   External APIs     │
                    ├─────────────────────┤
                    │  • AI/ML Services   │
                    │  • Payment Gateways │
                    │  • Blockchain RPC   │
                    │  • Authentication   │
                    └─────────────────────┘
```

### Key Services

- **AI Integration Services**
  - OpenAI Service - GPT models and DALL-E image generation
  - AnthropicHandler - Claude model integration
  - GeminiHandler - Google AI integration
  - GrokHandler - xAI integration
  - HuggingFaceHandler - Open-source model access

- **Payment Services**
  - StripeService - Credit card processing
  - SolanaService - Blockchain payments and verification
  - CreditService - Balance management and tracking

- **Core Services**
  - EncryptionService - AES-256-CBC message encryption
  - SettingService - Dynamic configuration management
  - AuthService - Privy.io Web3 authentication
  - ImageService - DALL-E integration for image generation

## 🔐 Security Features

- **Server-Side Encryption**: All chat messages are encrypted before storage
- **User-Specific Keys**: Each user has their own encryption key
- **Rate Limiting**: Configurable throttling for API endpoints
- **CSRF Protection**: Laravel's built-in CSRF token validation
- **XSS Protection**: Automatic output escaping
- **SQL Injection Protection**: Eloquent ORM with parameter binding

## 💰 Supported Payment Methods

### Traditional Payments
- **Stripe Integration**
  - Credit/debit card processing
  - Secure PCI-compliant transactions
  - Support for multiple currencies

### Cryptocurrency Payments
- **Solana Blockchain**
  - Native SOL payments
  - USDC stablecoin support
  - Real-time price conversion via CoinGecko
  - Instant transaction verification via Helius RPC

## 📊 Credit System

PayGo.Network uses a transparent credit-based pricing model:

- Users purchase credits upfront
- Each AI response deducts credits based on token usage
- Different models have different rates
- Real-time balance tracking
- Detailed transaction history

## 🎨 Image Generation Capabilities

### DALL-E 2 Features
- Text-to-image generation (256x256, 512x512, 1024x1024)
- Image editing with masks
- Image variations from uploads
- Batch generation support

### DALL-E 3 Features
- Advanced text-to-image with better prompt adherence
- Higher quality outputs (1024x1024, 1792x1024, 1024x1792)
- Built-in safety filters
- Style customization options

## 🔧 Dynamic Configuration

All services can be configured through the admin panel:
- Enable/disable AI providers
- Manage API keys securely
- Toggle payment methods
- Configure rate limits
- Set pricing for each model
- Customize email providers

## 🤖 Supported AI Models

### Text Generation
- **OpenAI**: GPT-4, GPT-4 Turbo, GPT-3.5 Turbo
- **Anthropic**: Claude 3 Opus, Claude 3 Sonnet, Claude 3 Haiku
- **Google**: Gemini Pro, Gemini Ultra
- **xAI**: Grok-1, Grok-2
- **HuggingFace**: Llama, Mistral, and other open models

### Image Generation
- **DALL-E 2**: Classic image generation
- **DALL-E 3**: Advanced generation with better prompt understanding

---

<div align="center">
Made with ❤️ by me
</div>
