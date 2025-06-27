# Inventorize

A modern Laravel application for inventory management built with Livewire, Tailwind CSS, and Docker.

## 🚀 Development URLs

When running locally with Laravel Sail, access your application at:

- **Main Application**: http://localhost:8080
- **Laravel Telescope** (Debugging): http://localhost:8080/telescope
- **Mailpit** (Email Testing): http://localhost:8025

## 🛠 Development Setup

### Prerequisites
- Docker & Docker Compose
- Git

### Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Inventorize
   ```

2. **Copy environment file**
   ```bash
   cp .env.example .env
   ```

3. **Start Docker containers**
   ```bash
   ./vendor/bin/sail up -d
   ```
   
   Or use the alias:
   ```bash
   sail up -d
   ```

4. **Generate application key**
   ```bash
   sail artisan key:generate
   ```

5. **Run database migrations**
   ```bash
   sail artisan migrate
   ```

6. **Install frontend dependencies**
   ```bash
   sail npm install
   sail npm run dev
   ```

## 🐳 Docker Services

- **Laravel Application**: Port 8080
- **MySQL Database**: Port 3308 (internally 3306)
- **Mailpit (Email Testing)**: Port 8025 (Dashboard), Port 1025 (SMTP)
- **Vite Dev Server**: Port 5173

## 🔧 Development Tools

### Code Quality
- **Laravel Pint**: Code style formatting
- **PHPStan (Larastan)**: Static analysis
- **Prettier**: Frontend code formatting
- **Husky**: Pre-commit hooks

### Debugging & Monitoring
- **Laravel Telescope**: Application debugging and monitoring
- **Mailpit**: Local email testing and preview

### Useful Commands

```bash
# Start containers
sail up -d

# Stop containers
sail down

# Run tests
sail test

# Code formatting
sail composer pint

# Static analysis
./vendor/bin/phpstan analyse

# Frontend development
sail npm run dev

# Build for production
sail npm run build

# Access container shell
sail shell

# View logs
sail logs

# Database operations
sail artisan migrate
sail artisan migrate:fresh --seed
```

## 📁 Project Structure

- **Frontend**: Livewire components with Tailwind CSS
- **Backend**: Laravel 12 with PHP 8.4
- **Database**: MySQL 8.0
- **Development**: Docker with Laravel Sail

## 🚀 Deployment

The project includes GitHub Actions CI/CD pipeline that:
- Runs tests on push to `main` and `development` branches
- Checks code style with Laravel Pint
- Performs static analysis with PHPStan
- Builds frontend assets

## 📝 Environment Configuration

Key environment variables in `.env`:

```bash
# Application
APP_URL=http://localhost:8080
APP_PORT=8080

# Database
DB_HOST=mysql
DB_DATABASE=inventorize
FORWARD_DB_PORT=3308

# Mail (Mailpit)
MAIL_HOST=mailpit
MAIL_PORT=1025

# Telescope
TELESCOPE_ENABLED=true
```

## 🤝 Contributing

1. Create a feature branch from `development`
2. Make your changes
3. Run tests and code quality checks
4. Submit a pull request

## 📧 Contact

Bumbieru 13
