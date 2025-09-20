# Overview

This is a full-stack web application built for tracking Vinted sales with a React frontend and Express backend. The application allows users to manage items for sale, track their status through different stages (listed, for-money, sold, delivered), and view sales metrics. It features a dashboard with filtering capabilities, CSV import/export functionality, and responsive design with dark theme support.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for client-side routing with basic dashboard and 404 pages
- **UI Framework**: Shadcn/ui components built on Radix UI primitives with Tailwind CSS
- **State Management**: React hooks with local storage persistence for data and TanStack Query for server state
- **Styling**: Tailwind CSS with CSS variables for theming, supporting dark mode with custom color palette

## Backend Architecture
- **Framework**: Express.js with TypeScript
- **Server Setup**: Custom Vite development server integration with middleware for logging and error handling
- **API Structure**: RESTful endpoints with `/api` prefix (routes currently minimal but structured for expansion)
- **Storage Interface**: Abstracted storage layer with in-memory implementation (MemStorage) that can be extended for database integration

## Data Storage Solutions
- **Database ORM**: Drizzle ORM configured for PostgreSQL with Neon serverless database
- **Schema Management**: Centralized schema definitions in shared directory with Zod validation
- **Session Storage**: PostgreSQL session store configuration with connect-pg-simple
- **Local Persistence**: Browser localStorage for client-side data persistence

## Authentication and Authorization
- **Session Management**: Express sessions with PostgreSQL store (configured but not fully implemented)
- **User Schema**: Basic user model with username/password fields and UUID primary keys
- **Security**: Prepared for session-based authentication with secure cookie configuration

## External Dependencies
- **Database**: Neon PostgreSQL serverless database (@neondatabase/serverless)
- **UI Components**: Radix UI primitives for accessible component foundation
- **Form Handling**: React Hook Form with Hookform resolvers for validation
- **Data Validation**: Zod schema validation integrated with Drizzle
- **Date Handling**: date-fns for date manipulation and formatting
- **Development Tools**: Replit-specific plugins for development environment integration
- **Build Tools**: esbuild for server bundling, Vite for client bundling
- **CSS Framework**: Tailwind CSS with PostCSS for styling pipeline