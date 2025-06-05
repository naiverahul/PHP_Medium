# 📰 Medium Clone using Laravel (PHP Framework)

This is a Medium-like blog platform built using the **Laravel** PHP framework.

## ❓ Why Laravel?

Laravel is a modern PHP framework known for:

* Clean and expressive syntax
* Built-in features like routing, authentication, and Eloquent ORM
* A powerful command-line tool (`Artisan`)
* Easy integration with mailing, file storage, and more
* Excellent community and documentation

It provides a robust foundation for building scalable, secure, and maintainable web applications.

---

## ⚙️ Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/naiverahul/PHP_Medium.git
cd PHP_Medium
```

### Step 2: Setup Environment

Create your `.env` file by copying the example:

```bash
cp .env.example .env
```

Edit the following sections:

#### 🔐 App Configuration

Update the section to set your app name, local environment URL, and port:

```env
APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost:8000
```

> You will generate the `APP_KEY` in a later step.

#### 📧 Mail Configuration

To use **Mailpit** for testing email:

```env
MAIL_MAILER=smtp
MAIL_HOST=127.0.0.1
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"
```

> 🔪 Mailpit is a fake SMTP server for testing emails. To use it, simply run `mailpit` in a separate terminal and visit [http://localhost:8025](http://localhost:8025)

If using another email service, replace the credentials and settings above accordingly.

---

### Step 3: Install Dependencies

```bash
composer install
npm install && npm run dev
```

### Step 4: Generate App Key

```bash
php artisan key:generate
```

### Step 5: Set Up Database

Create your database (e.g. using MySQL or SQLite) and update the DB section in `.env`.

Then run:

```bash
php artisan migrate:fresh --seed
```

> This will create all tables and seed the database with sample data.

---

### Step 6: Run the App

```bash
php artisan serve
```

Visit the URL defined in your `.env` (`APP_URL`, typically `http://localhost:8000`)

---

### Step 7: Run Mailpit (Optional)

```bash
mailpit
```

Then visit: [http://localhost:8025](http://localhost:8025) to test email sending (for user verification, etc.)

---

## 🔍 Known Issues

* Posts not visible after login or account creation
* Post images may not display

🚗 You’re welcome to fix these bugs and contribute to improving the UI/UX!

---

## 🤝 Contributions

Feel free to fork this repo, resolve issues, and improve features. Pull requests are welcome!
