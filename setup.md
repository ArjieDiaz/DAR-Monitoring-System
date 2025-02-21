# 🛠️ Setup Guide for Monitoring System  

This guide will help you install and run the **Monitoring System**, a CodeIgniter-based project.  

---

## 📥 1. Download & Extract  
1. Download the project ZIP file: **Monitoring System.zip**  
2. Extract the contents to your local development folder (e.g., `C:\xampp\htdocs\CodeIgniter`).  

---

## 🏗️ 2. XAMPP Installation & Setup  
Ensure you have **XAMPP** installed. If not, download it from [Apache Friends](https://www.apachefriends.org/index.html).  

1. Start **Apache** and **MySQL** from the XAMPP Control Panel.  
2. Open your browser and go to: [`http://localhost/phpmyadmin/`](http://localhost/phpmyadmin/)  

---

## 📂 3. Database Configuration  
1. In **phpMyAdmin**, create a new database:  
   - **Database Name:** `ciblog`  
   - **Collation:** `utf8_general_ci` (Recommended)  
2. Import the provided SQL file:  
   - Go to **Import** → Select `database/ciblog.sql` → Click **Go**.  

---

## ⚙️ 4. Configure CodeIgniter  
Modify the following configuration files:  

### 🔹 **Database Configuration** (`application/config/database.php`)  
Ensure your database settings match your XAMPP setup:  

$active_group = 'default';
$query_builder = TRUE;

$db['default'] = array(
    'dsn'   => '',
    'hostname' => 'localhost',
    'username' => 'root', // Change if necessary
    'password' => '', // Change if necessary
    'database' => 'ciblog',
    'dbdriver' => 'mysqli',
    'dbprefix' => '',
    'pconnect' => FALSE,
    'db_debug' => (ENVIRONMENT !== 'production'),
    'cache_on' => FALSE,
    'cachedir' => '',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    'swap_pre' => '',
    'encrypt' => FALSE,
    'compress' => FALSE,
    'stricton' => FALSE,
    'failover' => array(),
    'save_queries' => TRUE
);

🔹 Base URL Configuration (application/config/config.php)

🚀 5. Run the Project
Open your browser and visit:
http://localhost/CodeIgniter/
You should see the homepage of the Monitoring System.
