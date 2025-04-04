# ERP Vendor Management System

A comprehensive Enterprise Resource Planning (ERP) system for managing vendors, customers, and products with role-based access control.

## Features

### For Administrators
- Dashboard with real-time system status monitoring
- User management for vendors and customers
- Order tracking and management
- System health monitoring
- Activity logs and notifications

### For Vendors
- Product management (Add, Edit, Delete)
- Order management
- Inventory tracking
- Sales analytics
- Revenue monitoring

### For Customers
- Browse and search products
- Shopping cart functionality
- Order placement and tracking
- Order history
- Invoice generation

## Tech Stack

- **Frontend**: React with TypeScript
- **Styling**: Tailwind CSS
- **State Management**: Zustand
- **Database**: Supabase
- **Icons**: Lucide React
- **PDF Generation**: jsPDF
- **Date Handling**: date-fns

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm (v9 or higher)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env` file in the root directory with the following variables:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Start the development server:
```bash
npm run dev
```

## Database Structure

The application uses Supabase with the following tables:

- **users**: Stores user information and roles
- **products**: Product catalog with vendor relationships
- **orders**: Customer order information
- **order_items**: Individual items within orders
- **cart_items**: Shopping cart contents

## Authentication

The system supports three user types:
- Administrator
- Vendor
- Customer

Each user type has specific permissions and access levels managed through Row Level Security (RLS) policies in Supabase.

## Deployment

The application is deployed on Netlify and can be accessed at:
[https://deft-stardust-a58be8.netlify.app](https://deft-stardust-a58be8.netlify.app)

## Development

### Available Scripts

- `npm run dev`: Start development server
- `npm run build`: Build for production
- `npm run preview`: Preview production build
- `npm run lint`: Run ESLint

### Project Structure

```
src/
├── components/        # React components
├── lib/              # Utility functions and configurations
├── store/            # Zustand store
└── types/            # TypeScript type definitions

supabase/
└── migrations/       # Database migrations
```

## Security

- Row Level Security (RLS) enabled for all database tables
- Role-based access control
- Secure authentication flow
- Protected API endpoints

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
