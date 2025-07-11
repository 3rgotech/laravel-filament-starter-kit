# 🚀 Laravel Filament Starter Kit

This is a **Filament v3 Starter Kit** for **Laravel 12**, designed to accelerate the development of Filament-powered applications.

Preview:
![](https://raw.githubusercontent.com/ercogx/laravel-filament-starter-kit/main/preview-white.png)
Dark Mode:
![](https://raw.githubusercontent.com/ercogx/laravel-filament-starter-kit/main/preview.png)

## 📦 Installation

You need the Laravel Installer if it is not yet installed.

```bash
composer global require laravel/installer
```

Now you can create a new project using the Laravel Filament Starter Kit.

```bash
laravel new test-kit --using=3rgotech/laravel-filament-starter-kit
```

## ⚙️ Setup

1️⃣ **Database Configuration**

By default, this starter kit uses **SQLite**. If you’re okay with this, you can skip this step. If you prefer **MySQL**, follow these steps:

- Update your database credentials in `.env`
- Run migrations: `php artisan migrate`
- (Optional) delete the existing database file: ```rm database/database.sqlite```

2️⃣ Create Filament Admin User
```bash
php artisan make:filament-user
```

3️⃣ Assign Super Admin Role
```bash
php artisan shield:super-admin --user=1 --panel=admin
```

4️⃣ Generate Permissions
```bash
php artisan shield:generate --all --ignore-existing-policies --panel=admin
```

5️⃣ Create settings
Update `app/Settings/GeneralSettings.php` and `database/settings/2023_01_01_000000_create_general_settings.php`

## 🄻Laravel Include

- [Spatie Laravel Permissions](https://spatie.be/docs/laravel-permission/) Roles and permissions managements
- [Spatie Laravel Settings](https://github.com/spatie/laravel-settings) Settings management
- [Blade Lucide Icons](https://github.com/PascaleBeier/blade-lucide-icons) [Lucide icons](https://lucide.dev/) for blade

## 🌟Panel Include

- [Breezy](https://filamentphp.com/plugins/jeffgreco-breezy) My Profile page.
- [Themes](https://filamentphp.com/plugins/hasnayeen-themes) Themes for Filament panels. Setup for `user` mode.
- [Shield](https://filamentphp.com/plugins/bezhansalleh-shield) Access management to your Filament Panel's Resources, Pages & Widgets through spatie/laravel-permission.
- [Settings](https://filamentphp.com/plugins/filament-spatie-settings) Integrates Spatie/Laravel-settings into Filament.
- [Logger](https://filamentphp.com/plugins/z3d0x-logger) Extensible activity logger for filament that works out-of-the-box.
- [Laravel Log](https://filamentphp.com/plugins/saade-laravel-log) Log reading plugin for Filament

## 🧑‍💻Development Include

- [barryvdh/laravel-debugbar](https://github.com/barryvdh/laravel-debugbar) The most popular debugging tool for Laravel, providing detailed request and query insights.
- [barryvdh/laravel-ide-helper](https://github.com/barryvdh/laravel-ide-helper) Generates helper files to improve autocompletion and static analysis in IDEs.
- [larastan/larastan](https://github.com/larastan/larastan) A PHPStan extension for Laravel, configured at level 5 for robust static code analysis.
- [larswiegers/laravel-translations-checker](https://github.com/LarsWiegers/laravel-translations-checker) A command to check the availability of all translation in every defined language

This kit includes **Laravel Pint** for automatic PHP code styling and structured PHPDoc generation for your models.
After running migrations, execute the following command to update model documentation:

```bash
php artisan ide-helper:models -W && ./vendor/bin/pint app
```

The `composer check` script runs **tests, PHPStan, Pint, and translation-checker** for code quality assurance:
```bash
composer check
```

## 📜 License

This project is open-source and licensed under the MIT License.

## 💡 Contributing

We welcome contributions! Feel free to open issues, submit PRs, or suggest improvements.


### 🚀 Happy Coding with Laravel & Filament! 🎉
