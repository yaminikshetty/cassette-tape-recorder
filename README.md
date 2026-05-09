# Cassette — Voice Memos

A modern, high-fidelity voice memo and archive application built with React, Vite, and Express.

## Features

- 🎙️ **Voice Recording**: High-quality audio recording directly from the browser.
- 📁 **Archive Management**: Organize and manage your voice memos.
- ☁️ **Cloud Storage**: Integrated with object storage for reliable data persistence.
- 🔐 **Authentication**: Secure user access powered by Clerk.
- 🎨 **Modern UI**: Sleek, responsive design built with Tailwind CSS and Radix UI.

## Project Structure

This is a **pnpm monorepo** structured as follows:

- `artifacts/cassette`: React + Vite frontend application.
- `artifacts/api-server`: Express.js backend server.
- `lib/api-spec`: OpenAPI specifications and Orval configuration.
- `lib/api-zod`: Generated Zod schemas for API validation.
- `lib/api-client-react`: Generated React Query hooks for API interaction.
- `lib/db`: Database schema and Drizzle ORM configuration.

## Getting Started

### Prerequisites

- Node.js (v20+)
- pnpm

### Installation

```bash
pnpm install
```

### Development

1. **Codegen**: Generate API clients and schemas.
   ```bash
   cd lib/api-spec
   pnpm run codegen
   ```

2. **Frontend**: Start the Vite dev server.
   ```bash
   cd artifacts/cassette
   export PORT=5173
   export BASE_PATH='/'
   pnpm run dev
   ```

3. **Backend**: Start the Express server.
   ```bash
   cd artifacts/api-server
   pnpm run dev
   ```

## License

MIT
