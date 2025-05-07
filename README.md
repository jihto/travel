# 🌱 Travel Project Setup

> A step-by-step guide to set up how to run travel theme with a modern WordPress development environment using [Bedrock](https://roots.io/bedrock/) and [Laragon](https://laragon.org/).

---

## 📦 What is Bedrock?

Bedrock is a modern WordPress boilerplate that helps you manage your project using:

- Composer for dependency management
- A better folder structure
- Improved security and configuration management

---

## 🛠️ Requirements

Before you begin, make sure you have:

- ✅ [Laragon](https://laragon.org/download/) installed
- ✅ [Composer](https://getcomposer.org/download/) installed
- ✅ Git installed

---

## 🚀 Create Your Project

### Step 1: Open Laragon Terminal checking

Open the **Terminal**

```bash
composer -v
```

### Step 2: Install Bedrock

Run the following command:

```bash
composer create-project roots/bedrock my-project-name
```

Replace `my-project-name` with your desired folder/project name.

### Step 3: Configure `.env`

Inside your project folder, duplicate the `.env.example` file and rename it to `.env`:

```bash
cp .env.example .env
```

Edit the `.env` file and update these values:

```
DB_NAME=my_project
DB_USER=root
DB_PASSWORD=

WP_HOME=http://my-project-name.test

# Generate your keys here: https://roots.io/salts.html

AUTH_KEY=
SECURE_AUTH_KEY=
LOGGED_IN_KEY=
NONCE_KEY=
AUTH_SALT=
SECURE_AUTH_SALT=
LOGGED_IN_SALT=
NONCE_SALT=

```

> `WP_HOME` should match the domain you'll use in Laragon (e.g., `http://my-project-name.test`).

### Step 4: Create a Database

- Open **Laragon → Menu → Database → phpMyAdmin**
- Create a new database named: `my_project`

---

## 📁 Folder Structure

```
my-project-name/
├── config/         # Environment config
├── web/
│   ├── app/
│   ├─────├── plugins/
│   ├─────├── themes/
│   ├── wp/         # WordPress core
│   └── index.php
├── .env            # Environment variables
└── composer.json   # PHP dependencies
```

---

### Step 5: Git clone theme

```
    cd my-project-name/web/app/themes
```

```
    git clone git@github.com:jihto/travel.git
```

---

### Step 6: Setup Virtual Host in Laragon

Laragon auto-detects folders and assigns domains ending in `.test`. To enable this:

1. Place your project inside `C:\laragon\www\`
2. Restart Laragon
3. Visit `http://my-project.test` in your browser

---

## ✅ Done!

You now have a modern WordPress setup using Bedrock and Laragon!  
Start building your theme or plugin the right way 🎉

---

## 📚 Resources

- [Bedrock Documentation](https://roots.io/docs/bedrock/master/)
- [Laragon Documentation](https://laragon.org/docs/)
- [WordPress CLI](https://developer.wordpress.org/cli/)

---

## 🧩 Optional Tips

- Use Trellis for automated server provisioning
- Use Sage theme for modern frontend development
