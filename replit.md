# Overview

This is a full-stack web application built with a modern TypeScript stack featuring React frontend and Express backend. The project appears to be a landing page or sales funnel with a countdown timer, likely for a digital marketing product targeting Mozambican users. The architecture follows a monorepo structure with shared components between client and server.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript, using Vite as the build tool
- **UI Framework**: shadcn/ui components built on Radix UI primitives with Tailwind CSS for styling
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Styling**: Tailwind CSS with custom CSS variables for theming, includes dark mode support
- **Form Handling**: React Hook Form with Zod validation through hookform/resolvers

## Backend Architecture
- **Runtime**: Node.js with Express framework
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: PostgreSQL-based sessions using connect-pg-simple
- **Development**: Hot reload with tsx and custom Vite middleware integration
- **Production**: Compiled with esbuild for optimal performance

## Data Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema Management**: Shared schema between client and server in `/shared` directory
- **Migrations**: Drizzle Kit for database migrations stored in `/migrations`
- **Type Safety**: Full TypeScript integration with Drizzle for compile-time type checking
- **Validation**: Zod schemas integrated with Drizzle for runtime validation

## Development Workflow
- **Build System**: Vite for frontend bundling with React plugin
- **TypeScript**: Strict mode enabled with path mapping for clean imports
- **Hot Reload**: Development server with HMR for both frontend and backend
- **Code Quality**: ESM modules throughout, consistent import/export patterns

## Project Structure
- `/client` - React frontend application
- `/server` - Express backend with API routes
- `/shared` - Shared types, schemas, and utilities
- Component architecture follows atomic design with UI components in `/client/src/components/ui`

# External Dependencies

## Database & Storage
- **Neon Database**: Serverless PostgreSQL database hosting
- **Drizzle ORM**: Type-safe database toolkit and query builder
- **connect-pg-simple**: PostgreSQL session store for Express sessions

## UI & Styling
- **shadcn/ui**: Pre-built component library based on Radix UI
- **Radix UI**: Headless component primitives for accessibility
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library for consistent iconography
- **class-variance-authority**: Utility for creating variant-based component APIs

## Development Tools
- **Vite**: Fast build tool and development server
- **Replit Plugins**: Integration plugins for Replit development environment
- **TypeScript**: Static type checking and development tooling
- **PostCSS**: CSS processing with Tailwind CSS plugin

## State Management & Data Fetching
- **TanStack Query**: Powerful data fetching and caching library
- **React Hook Form**: Performant form library with minimal re-renders
- **Wouter**: Lightweight routing library for React applications

## Utilities & Helpers
- **date-fns**: Modern date utility library
- **clsx & tailwind-merge**: Utility functions for conditional CSS classes
- **nanoid**: URL-safe unique string ID generator
- **cmdk**: Command palette component for search interfaces