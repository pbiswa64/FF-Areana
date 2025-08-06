# Overview

This is a full-stack Free Fire tournament management application built with React (frontend) and Express.js (backend). The application allows players to register for tournaments, track match results, view leaderboards, and provides administrative features for tournament management. It features a gaming-themed UI with dark mode aesthetics and neon effects that match the Free Fire gaming experience.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Framework**: Radix UI components with shadcn/ui design system
- **Styling**: Tailwind CSS with custom gaming theme colors and CSS variables
- **Form Handling**: React Hook Form with Zod validation for type-safe form management

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Validation**: Zod schemas shared between frontend and backend for consistent data validation
- **File Uploads**: Multer middleware for handling screenshot uploads with file type validation
- **Development**: TypeScript with tsx for development server hot reloading

## Data Storage
- **Database**: PostgreSQL with Neon serverless driver for cloud deployment
- **Schema Design**: 
  - Users table for player registration (supports both solo and squad registrations)
  - Tournaments table for tournament management with status tracking
  - Matches table for individual tournament rounds with room credentials
  - Match results table for storing player performance data
  - Leaderboard table for aggregated tournament statistics
  - Admins table for administrative access control
- **Migrations**: Drizzle Kit for database schema migrations and management

## Authentication & Authorization
- **Admin System**: Username-based admin authentication for tournament management
- **User Registration**: Self-registration system with Free Fire UID validation
- **Session Management**: Connect-pg-simple for PostgreSQL session storage

## External Dependencies
- **Database**: Neon PostgreSQL serverless database
- **File Storage**: Local filesystem storage for screenshot uploads (configurable for cloud storage)
- **UI Components**: Radix UI primitives for accessible component foundation
- **Development Tools**: Replit integration with cartographer plugin and runtime error overlay
- **Fonts**: Orbitron font family for gaming aesthetic headings