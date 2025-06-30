# replit.md

## Overview

This is a full-stack web application built for "Lagoku" - a professional logo design and brand services platform in Indonesia. The application provides logo design services, AI-powered logo analysis, brand guidelines creation, and trademark registration assistance. It features a modern React frontend with a Node.js/Express backend, using PostgreSQL with Drizzle ORM for data persistence.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **UI Framework**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Pattern**: RESTful API design
- **Session Management**: Express sessions with PostgreSQL store
- **File Handling**: Multer for file uploads with validation

### Database Architecture
- **Database**: PostgreSQL (Replit Database)
- **ORM**: Drizzle ORM with TypeScript schema definitions
- **Migrations**: Drizzle Kit for schema management
- **Storage**: DatabaseStorage class implementing IStorage interface

## Key Components

### Database Schema
The application uses four main entities:
- **Users**: Basic user authentication system
- **Portfolio Items**: Showcase of completed logo designs with categories
- **Contact Submissions**: Customer inquiry and project request forms
- **Logo Analysis**: AI-powered logo quality assessment results

### Frontend Components
- **Navigation**: Fixed navigation with smooth scrolling
- **Hero Section**: Landing page with call-to-action buttons
- **Services Section**: Overview of offered services (logo design, brand guidelines, trademark registration)
- **Logo Analysis Tool**: File upload interface for AI logo analysis
- **Portfolio Gallery**: Filterable gallery of completed work
- **Contact Section**: Comprehensive contact form with service selection
- **Process Section**: Step-by-step workflow visualization

### API Endpoints
- `GET /api/portfolio` - Retrieve portfolio items with optional category filtering
- `POST /api/contact` - Submit contact form data
- `POST /api/analyze-logo` - Upload and analyze logo files

## Data Flow

1. **Client Requests**: Frontend makes API calls using TanStack Query
2. **Server Processing**: Express routes handle requests with validation
3. **Data Layer**: Drizzle ORM manages database operations
4. **Response**: JSON responses sent back to client
5. **State Updates**: React Query caches and updates UI state

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL connection for serverless environments
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **zod**: Runtime type validation
- **multer**: File upload handling

### Development Tools
- **Vite**: Build tool and dev server
- **TypeScript**: Static type checking
- **Tailwind CSS**: Utility-first CSS framework
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay

## Deployment Strategy

### Development
- Vite dev server with HMR for frontend
- tsx for TypeScript execution in development
- Express middleware integration with Vite

### Production Build
- Frontend: Vite builds optimized static assets
- Backend: esbuild bundles server code for Node.js
- Static files served from Express in production

### Environment Configuration
- Database connection via `DATABASE_URL` environment variable
- Drizzle configuration for PostgreSQL dialect
- File uploads stored in local `uploads/` directory

## Changelog

```
Changelog:
- June 29, 2025. Initial setup with MemStorage
- June 29, 2025. Added PostgreSQL database integration with DatabaseStorage
- June 29, 2025. Updated color scheme to #00A69C (teal/tosca) and white
- June 29, 2025. Added admin authentication system with username/password login
- June 29, 2025. Created admin panel with dashboard, portfolio management, contact submissions, and logo analyses
- June 29, 2025. Removed admin button from public navigation - access via /auth or /admin URLs only
- June 29, 2025. Implemented complete portfolio management (add, edit, delete) with form modal
- June 29, 2025. Added expert consultation button that redirects to contact form with "Konsultasi Expert - Rp 300K" pre-selected
- June 29, 2025. Updated contact information: WhatsApp +6285398932001, email makassarlagoku@gmail.com, office location Makassar, Sulawesi Selatan
- June 29, 2025. Added Lagoku logo to navigation bar in top-left corner
- June 29, 2025. Removed expert consultation section from hero area
- June 29, 2025. Changed contact form header text from "Kirim Pesan" to "Isi Form untuk Konsultasi"
- June 29, 2025. Updated logo analysis results consultation text to "Konsultasikan Segera" and button to "Mulai Konsultasi"
- June 29, 2025. Updated "Follow Kami" social media icons to proper Facebook, Instagram, Threads, and TikTok icons
- June 29, 2025. Added functionality to eye icon in admin panel for viewing detailed logo analysis results in modal dialog
- June 29, 2025. Enhanced admin panel to display uploaded logo images in analysis modal, added file serving endpoint
- June 29, 2025. Added delete action for logo analysis in admin panel with confirmation dialog
- June 29, 2025. Added password change functionality for admin in settings tab with secure validation
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```