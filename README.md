<h1 style="text-align:center;">easy Projects Management System</h1>

English | <a href="README_zh.md">简体中文</a><br><br>
**easy Projects Management System** is a multifunctional web management platform designed to simplify project management, file sharing, and collaboration processes. It integrates features such as innovation project management, online document generation, code hosting, and provides user management, system settings, log viewing, and other backend management capabilities.

## ✨ Features

*   **Unified Management Platform:**
    *   **Project Management Center (`program_manage.php`):** Centralized access to various project management modules.
    *   **Home Page (`home.php`):** System overview, announcements, quick access, and recent activities.
*   **Innovation Project Paper Interaction System:**
    *   Create, manage, and delete innovation projects (`dachuang_mange.php`, `add_dachuang_project.php`).
    *   File categorization and upload based on project tags (`dachuang.php`, `upload.php`).
*   **Online Document Generation System:**
    *   Create, manage, and delete online document projects (`onlinefile_manage.php`, `add_onlinefile_project.php`).
    *   Dynamically define table structures (headers).
    *   Fill in form data online (`onlinefile.php`).
    *   Save and export (`save_form_data.php`, `admin_download.php`) or generate XLSX templates (`generate_xlsx.php`).
*   **Code Hosting System:**
    *   Create, view, edit, and delete code repositories (`code_repository.php`, `repo_edit.php`, `repo_delete.php`).
    *   View repository file lists and file contents (supports text, images, Markdown, and basic Office document preview) (`repo_detail.php`, `get_file.php`, `get_file_list.php`).
    *   Upload and delete repository files (`code_upload.php`, `delete_codefile.php`).
    *   (Basic) Commit files (`commit_file.php`).
*   **File Management:**
    *   Centrally view, download, and delete various uploaded files (`file_manager.php`, `delete_file.php`).
    *   Control file public or private status (`toggle_visibility.php`).
*   **User & Permission Management:**
    *   User login, registration, and logout (`login.html`, `register.html`, `logout.php`).
    *   Administrators (`root`) can manage all users (add, view, delete) (`user_management.php`, `add_new_user.php`, `delete_user.php`).
*   **System Management (Admin):**
    *   **System Settings (`settings.php`):**
        *   Publish and update system announcements.
        *   Configure contact information.
        *   Set system access time periods.
        *   Enable/disable user registration.
        *   Change system background image.
        *   Update copyright information.
    *   **Log Viewing (`view_logs.php`):** View user operation logs, support clearing (`clear_logs.php`).
*   **Interaction & Help:**
    *   **Site Search (`search.php`):** Cross-module search for projects, documents, repositories, and help content.
    *   **Help Center (`help.php`):** Provides FAQs and contact information.
*   **Responsive Design:** Basic responsive layout for different screen sizes.

## 📸 Feature Preview

Below are screenshots of some features of the easy Management System:

**Core Interfaces**

![Login Page](img/登录界面.png)
*Login Page*

![Registration Page](img/注册界面.png)
*User Registration Page*

![Home Page](img/首页1.png)
*System Home Overview (Top)*

![Home Page](img/首页2.png)
*System Home Overview (Bottom)*

**Project Management**

![Project Management Entry](img/项目管理界面.png)
*Project Management Entry Page*

![Innovation Project Details](img/大创项目交互系统.png)
*Innovation Project Details and File Upload Page*

![Online Document Filling](img/在线文档交互系统.png)
*Online Document Filling Page*

![Code Repository List](img/代码仓库管理系统1.png)
*Code Repository List and Creation Page*

![Code Repository File List](img/代码仓库管理系统2.png)
*Code Repository File List*

![Code Viewing](img/代码仓库页.png)
*Code File Viewing and Editing Interface*

**File & User Management**

![File Download](img/文件下载界面.png)
*File Download and Management Page*

![User Management](img/人员管理界面.png)
*User Management Page (Admin)*

**System Functions**

![System Settings](img/系统设置界面1.png)
*System Settings Page (Announcements, Contact Info)*

![System Settings](img/系统设置界面2.png)
*System Settings Page (Access Time, Registration Switch, Background Image)*

![Interaction Entry](img/互动功能界面.png)
*Interaction Entry (Log Viewing)*

![System Logs](img/系统日志界面.png)
*System Operation Log Viewing Page (Admin)*

![Help Center](img/帮助中心界面.png)
*Help Center Page*

![Site Search](img/站内搜索功能.png)
*Site Search Popup and Result Display*

## 🛠️ Tech Stack

*   **Backend:** PHP (>= 7.x recommended)
*   **Database:** MySQL / MariaDB
*   **Frontend:** HTML, CSS, JavaScript
*   **Libraries & Frameworks:**
    *   Bootstrap (CSS framework)
    *   Font Awesome (icon library)
    *   jQuery (JavaScript library)
    *   Monaco Editor (code viewer)
    *   PHP Office (for Office document handling):
        *   PhpSpreadsheet
        *   PhpWord
        *   PHPPresentation
    *   Parsedown (Markdown parser)
    *   Composer (PHP dependency management)

## 🚀 Server Installation & Deployment

1.  **Environment Requirements:**
    *   Web server (e.g., IIS, Nginx, Apache)
    *   PHP >= 8.x (8.3 or higher recommended, with `pdo_mysql`, `gd`, `mbstring`, `fileinfo`, `xml`, `zip` extensions enabled)
    *   MySQL database
    *   Composer

2.  **Get the Code:**
    *   Download the latest deployment package from the "Releases" section on the right.

3.  **Database Setup:**
    *   Create a new database (e.g., `project_management`), charset recommended as `utf8mb4`.
    *   Import the `script.sql` file into the created database to create the required tables.
    *   Edit the `config.php` file and fill in the correct database host (`DB_HOST`), username (`DB_USER`), password (`DB_PASS`), and database name (`DB_NAME`).

4.  **Install PHP Dependencies:**
    *   Make sure Composer is installed.
    *   Open a terminal or command line in the project root directory and run `composer install` to install required PHP libraries (such as PhpOffice).

5.  **Server Configuration & Directory Permissions:**
    *   See the original README.md for detailed steps for Windows, Linux, macOS, and local development environments.

6.  **Initial User:**
    *   The database script (`script.sql`) usually does not include an initial user. You need to register a user manually or insert a `root` user record directly into the `users` table (password must be generated using PHP's `password_hash()` function). The first registered user usually has no special privileges; admin must promote or create a `root` user directly.
    *   **Important:** The built-in `root` user has the highest privileges. Please set a strong password.

## 💡 Usage Instructions

1.  **Access:** Visit your configured server address, domain, or local address (e.g., `http://localhost/easyPMS`) in your browser.
2.  **Login/Register:**
    *   Use `login.html` to log in.
    *   If registration is enabled (configurable in system settings), use `register.html` to register a new user.
3.  **Navigation:** Use the left sidebar to switch between different modules.
4.  **Administrator (`root`):**
    *   Can access "User Management", "System Settings", and "Interaction Functions" (logs) menus.
    *   Has permissions to delete projects, manage users, modify system settings, etc.
5.  **Regular Users:**
    *   Can access "Project Management", "File Download", and "Help Center".
    *   Can only manage projects/repositories they created or access content set as public.

## 📁 Directory Structure

```
.
├── css/                 # CSS files (Bootstrap, FontAwesome, custom)
├── js/                  # JavaScript files (jQuery, Bootstrap, Monaco Editor)
├── uploads/             # User-uploaded files
│   └── code/            # Subdirectory for code repository uploads
├── requests/            # Online document request data (JSON)
├── file/                # System files, e.g., background images
├── logs/                # PHP error logs (optional)
├── vendor/              # Composer dependencies
├── add_dachuang_project.php # Add innovation project page
├── add_new_user.php     # Add new user page
├── add_onlinefile_project.php # Add online document project page
├── code_repository.php  # Code repository management home
├── config.php           # Database and basic config
├── Database.php         # Database operation class
├── dachuang_mange.php   # Innovation project management home
├── file_manager.php     # File download/management page
├── home.php             # System home page
├── help.php             # Help center page
├── login.html           # Login page
├── login.php            # Login logic
├── logout.php           # Logout logic
├── onlinefile_manage.php # Online document management home
├── program_manage.php   # Project management aggregation page
├── register.html        # Registration page
├── register.php         # Registration logic
├── repo_detail.php      # Code repository detail page
├── search.php           # Search logic
├── settings.php         # System settings page
├── sidebar_template.php # Sidebar template
├── user_management.php  # User management page
├── composer.json        # Composer dependencies
├── script.sql           # Database structure file
└── README_EN.md         # This file
```

## ☎️ Contact
- Email: 2358155969@qq.com
- For questions, you can also submit issue.

## 🙏 Acknowledgements

*   [Bootstrap](https://getbootstrap.com/)
*   [Font Awesome](https://fontawesome.com/)
*   [jQuery](https://jquery.com/)
*   [Monaco Editor](https://microsoft.github.io/monaco-editor/) 
