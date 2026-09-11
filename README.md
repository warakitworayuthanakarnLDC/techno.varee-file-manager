# Techno.Varee Web File Manager Clone

A legacy multi-user PHP file manager cloned from an internal educational deployment used at Varee Chiangmai School. This platform allows students to manage their own sandboxed PHP files, perform file operations, and even manage simple databases all from a web interface.

> 🛡️ Ported and analyzed with permission for ethical and research purposes only.

---

## 🚀 Features

- 🧾 Multi-user directory isolation (`/username/`)
- 🔐 Login system with session tracking
- 📂 File operations (create, edit, rename, delete)
- 🗂️ File viewer for `work1.php` through `work4.php` via iframes
- 🗃️ MySQL table creation wizard
- 📥 File uploads
- 🔧 Password change interface
- ⚙️ Legacy API test endpoint (returns JSON)

---

## 📁 File Structure

| File                | Description                                      |
|---------------------|--------------------------------------------------|
| `index.php`         | Login page frontend                              |
| `check_login.php`   | Handles login logic using MySQL                  |
| `list.php`          | Main file manager dashboard                      |
| `upload.php`        | Handles file uploads                             |
| `deletefile.php`    | Deletes user files                               |
| `editfile.php`      | Loads file for editing                           |
| `updatefile.php`    | Saves edited file                                |
| `rename.php`        | Allows renaming of files                         |
| `createfolder.php`  | Creates folders per user                         |
| `allfile.php`       | Loads multiple file viewers in iframes           |
| `checkfile*.php`    | Displays `work1.php` to `work4.php`              |
| `createdb.php`      | Creates tables using POST-defined structure      |
| `createDbForm.php`  | UI form for table creation                       |
| `changPW.php`       | Password reset via POST                          |
| `composer.php`      | Legacy configuration stub                        |

---

## ⚠️ Legacy Warnings

This project uses **outdated and vulnerable PHP functions**, including:

- `mysql_*` (replaced by `mysqli_*` or PDO in modern PHP)
- No input sanitization
- No password hashing
- Susceptible to session hijacking, RCE, and SQL injection

---

## 🛠️ Setup Instructions

1. Deploy onto a LAMP stack (Linux + Apache + MySQL + PHP ≤ 5.6 recommended)
2. Import the `wow` database manually (you must create the schema)
3. Place all files in `/var/www/html/`
4. Ensure file permissions:
   ```bash
   sudo chown -R www-data:www-data /var/www/html/
   sudo chmod -R 755 /var/www/html/

# Terms of Use

**Last Updated:** April 2025

By using or deploying this project ("Techno.Varee File Manager Clone"), you agree to the following terms:

---

## 1. No Warranty or Guarantee

This software is provided **"as-is"** without any express or implied warranties. The authors and contributors do not guarantee the accuracy, security, or performance of the code in any environment.

---

## 2. Liability Disclaimer

Under no circumstances shall the authors or contributors be held liable for:

- Damage to your server, VPS, hosting infrastructure, or data.
- Security breaches resulting from the use of legacy code or improper configuration.
- Disciplinary or legal consequences if deployed in unauthorized environments.

**You use this software entirely at your own risk.**

---

## 3. Intended Use

This project is intended solely for:

- Educational analysis
- Legacy system study
- Controlled sandbox deployment

**It is not designed for use in production or exposed systems.**

---

## 4. Unauthorized Use

Do **not** use this software to access, replicate, or tamper with servers or systems you do not explicitly own or have permission to interact with. Doing so may constitute a violation of local laws or school policy.

---

## 5. Acknowledgement

By downloading, deploying, or modifying this codebase, you acknowledge that:

- You understand the risks associated with its use.
- You take full responsibility for any consequences of your usage.
- You will not hold the authors liable for any resulting damages, losses, or violations.

---

**Proceed with caution. Use responsibly. Hack ethically.**

