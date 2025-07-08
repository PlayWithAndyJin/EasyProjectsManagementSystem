# easy管理系统
<a href"README.md">English</a> | 简体中文 <br><br>
**easy管理系统** 是一个多功能的 Web 管理平台，旨在简化项目管理、文件共享和协作流程。它集成了大创项目管理、在线文档生成、代码托管等多种功能，并提供了用户管理、系统设置、日志查看等后台管理能力。

## ✨ 功能特性

*   **统一管理平台:**
    *   **项目管理中心 (`program_manage.php`):** 集中访问各类项目管理模块。
    *   **首页 (`home.php`):** 提供系统概览、公告、快捷入口和最近活动。
*   **大创论文交互传送系统:**
    *   创建、管理和删除大创项目 (`dachuang_mange.php`, `add_dachuang_project.php`)。
    *   基于项目标签进行文件分类和上传 (`dachuang.php`, `upload.php`)。
*   **在线文档生成系统:**
    *   创建、管理和删除在线文档项目 (`onlinefile_manage.php`, `add_onlinefile_project.php`)。
    *   动态定义表格结构（表头）。
    *   在线填写表单数据 (`onlinefile.php`)。
    *   保存并导出 (`save_form_data.php`, `admin_download.php`) 或生成 XLSX 模板 (`generate_xlsx.php`)。
*   **代码程序托管系统:**
    *   创建、查看、编辑和删除代码仓库 (`code_repository.php`, `repo_edit.php`, `repo_delete.php`)。
    *   查看仓库文件列表和文件内容（支持文本、图片、Markdown 和基本 Office 文档预览） (`repo_detail.php`, `get_file.php`, `get_file_list.php`)。
    *   上传和删除仓库文件 (`code_upload.php`, `delete_codefile.php`)。
    *   （基础）提交文件 (`commit_file.php`)。
*   **文件管理:**
    *   集中查看、下载和删除各类上传的文件 (`file_manager.php`, `delete_file.php`)。
    *   控制文件的公开或私有状态 (`toggle_visibility.php`)。
*   **用户与权限管理:**
    *   用户登录、注册和退出 (`login.html`, `register.html`, `logout.php`)。
    *   管理员 (`root`) 可管理所有用户（添加、查看、删除） (`user_management.php`, `add_new_user.php`, `delete_user.php`)。
*   **系统管理 (管理员):**
    *   **系统设置 (`settings.php`):**
        *   发布和更新系统公告。
        *   配置联系方式。
        *   设置系统访问时间段。
        *   启用/禁用用户注册。
        *   更换系统背景图片。
        *   更新版权信息。
    *   **日志查看 (`view_logs.php`):** 查看用户操作日志，支持清空 (`clear_logs.php`)。
*   **互动与帮助:**
    *   **站内搜索 (`search.php`):** 跨模块搜索项目、文档、仓库和帮助内容。
    *   **帮助中心 (`help.php`):** 提供常见问题解答和联系方式。
*   **响应式设计:** 基础的响应式布局，适应不同屏幕尺寸。

## 📸 功能预览

以下是 easy管理系统 部分功能的界面截图：

**核心界面**

![登录页面](img/登录界面.png)
*登录页面*

![注册页面](img/注册界面.png)
*用户注册页面*

![系统首页](img/首页1.png)
*系统首页概览 (上半部分)*

![系统首页](img/首页2.png)
*系统首页概览 (下半部分)*

**项目管理**

![项目管理入口](img/项目管理界面.png)
*项目管理入口页面*

![大创项目详情](img/大创项目交互系统.png)
*大创项目详情与文件上传页面*

![在线文档填写](img/在线文档交互系统.png)
*在线文档填写页面*

![代码仓库列表](img/代码仓库管理系统1.png)
*代码仓库列表与创建页面*

![代码仓库文件列表](img/代码仓库管理系统2.png)
*代码仓库文件列表*

![代码查看](img/代码仓库页.png)
*代码文件查看与编辑界面*

**文件与用户管理**

![文件下载](img/文件下载界面.png)
*文件下载与管理页面*

![用户管理](img/人员管理界面.png)
*用户管理页面 (管理员)*

**系统功能**

![系统设置](img/系统设置界面1.png)
*系统设置页面 (公告、联系方式)*

![系统设置](img/系统设置界面2.png)
*系统设置页面 (访问时间、注册开关、背景图)*

![互动功能入口](img/互动功能界面.png)
*互动功能入口 (日志查看)*

![系统日志](img/系统日志界面.png)
*系统操作日志查看页面 (管理员)*

![帮助中心](img/帮助中心界面.png)
*帮助中心页面*

![站内搜索](img/站内搜索功能.png)
*站内搜索弹窗及结果展示*

## 🛠️ 技术栈

*   **后端:** PHP (>= 7.x 推荐)
*   **数据库:** MySQL / MariaDB
*   **前端:** HTML, CSS, JavaScript
*   **库与框架:**
    *   Bootstrap (CSS 框架)
    *   Font Awesome (图标库)
    *   jQuery (JavaScript 库)
    *   Monaco Editor (代码查看器)
    *   PHP Office (用于处理 Office 文档):
        *   PhpSpreadsheet
        *   PhpWord
        *   PHPPresentation
    *   Parsedown (Markdown 解析)
    *   Composer (PHP 依赖管理)

## 🚀 服务器安装与部署

1.  **环境要求:**
    *   Web 服务器 (如 IIS, Nginx, Apache)
    *   PHP >= 8.x (建议 8.3 或更高版本，需要启用 `pdo_mysql`, `gd`, `mbstring`, `fileinfo`, `xml`, `zip` 等扩展)
    *   MySQL 数据库
    *   Composer

2.  **获取代码:**
    *   通过该页右边"发行版"处下载最新版本的部署包。

3.  **数据库设置:**
    *   创建一个新的数据库 (例如 `project_management`)，字符集建议使用 `utf8mb4`。
    *   导入 `script.sql` 文件到创建的数据库中，这将创建所需的表结构。
    *   修改 `config.php` 文件，填入正确的数据库主机 (`DB_HOST`)、用户名 (`DB_USER`)、密码 (`DB_PASS`) 和数据库名 (`DB_NAME`)。

4.  **安装 PHP 依赖:**
    *   确保已安装 Composer。
    *   在项目根目录下打开终端或命令行，运行 `composer install` 来安装所需的 PHP 库 (如 PhpOffice)。

5.  **服务器配置与目录权限:**

    ### Windows Server (IIS)

    *   **安装 IIS 和 PHP:**
        *   通过 "服务器管理器" -> "添加角色和功能" 安装 "Web 服务器 (IIS)" 角色。
        *   确保在 IIS 功能中启用了 CGI 或 FastCGI 支持。
        *   下载并安装适用于 Windows 的 PHP 版本 (推荐 Non-Thread Safe 版本配合 FastCGI)。可以使用 [PHP for Windows 官网](https://windows.php.net/download/) 下载。
        *   配置 IIS 以识别 PHP：在 IIS 管理器中，选择服务器节点，打开 "处理程序映射"，添加模块映射，将 `*.php` 请求映射到 `php-cgi.exe` (通常通过 FastCGI)。确保配置 `php.ini` (启用所需扩展，设置 `extension_dir` 等)。
    *   **创建站点:**
        *   在 IIS 管理器中，右键点击 "网站" -> "添加网站"。
        *   设置站点名称，将 "物理路径" 指向项目文件所在的根目录。
        *   配置绑定（IP 地址、端口、主机名）。
    *   **目录权限:**
        *   找到项目中的以下目录：`uploads/`, `requests/`, `logs/` (如果需要文件日志), `file/`。
        *   右键点击每个目录 -> "属性" -> "安全" 选项卡 -> "编辑"。
        *   添加 IIS 应用程序池的标识用户（默认为 `IIS_IUSRS` 或特定应用程序池名称，如 `DefaultAppPool`）并授予其 "修改" 和 "写入" 权限。可能需要先创建这些目录。
        *   对于 `uploads/` 及其子目录，确保写入权限。
    *   **测试:** 访问站点 URL，检查是否能正常显示登录页面。

    ### Linux Server (Apache/Nginx)

    *   **安装 Web 服务器和 PHP:**
        *   **Apache:** `sudo apt update && sudo apt install apache2 php libapache2-mod-php php-mysql php-gd php-mbstring php-xml php-zip php-fileinfo` (Debian/Ubuntu) 或 `sudo yum update && sudo yum install httpd php php-mysqlnd php-gd php-mbstring php-xml php-zip php-pecl-fileinfo` (CentOS/RHEL)。
        *   **Nginx + PHP-FPM:** `sudo apt update && sudo apt install nginx php-fpm php-mysql php-gd php-mbstring php-xml php-zip php-fileinfo` (Debian/Ubuntu) 或 `sudo yum update && sudo yum install nginx php-fpm php-mysqlnd php-gd php-mbstring php-xml php-zip` (CentOS/RHEL)。
        *   确保启用了 PHP 和必要的模块。对于 Apache，可能需要 `sudo a2enmod phpX.Y` (X.Y 是 PHP 版本)。对于 Nginx，需要配置 PHP-FPM。
    *   **配置 Web 服务器:**
        *   **Apache:** 创建或编辑虚拟主机配置文件 (通常在 `/etc/apache2/sites-available/` 或 `/etc/httpd/conf.d/`)。设置 `DocumentRoot` 指向项目根目录，配置 `Directory` 指令允许访问，确保 `AllowOverride All` (如果项目依赖 `.htaccess`，虽然此项目目前看不需要)。重启 Apache (`sudo systemctl restart apache2` 或 `httpd`)。
        *   **Nginx:** 创建或编辑服务器块配置文件 (通常在 `/etc/nginx/sites-available/` 或 `/etc/nginx/conf.d/`)。设置 `root` 指向项目根目录，配置 `location ~ \.php$` 以将 PHP 请求传递给 PHP-FPM (例如 `fastcgi_pass unix:/var/run/php/phpX.Y-fpm.sock;`)。重启 Nginx (`sudo systemctl restart nginx`) 和 PHP-FPM (`sudo systemctl restart phpX.Y-fpm`)。
    *   **目录权限:**
        *   找到项目中的以下目录：`uploads/`, `requests/`, `logs/` (如果需要文件日志), `file/`。如果它们不存在，请先创建 (`mkdir uploads requests logs file`)。
        *   确定 Web 服务器运行的用户（通常是 `www-data` 在 Debian/Ubuntu 上，`apache` 或 `nginx` 在 CentOS/RHEL 上）。
        *   更改这些目录的所有者为 Web 服务器用户：`sudo chown -R www-data:www-data uploads/ requests/ logs/ file/` (将 `www-data:www-data` 替换为实际用户和组)。
        *   设置适当的写入权限，例如：`sudo chmod -R 755 uploads/ requests/ logs/ file/`。对于需要写入的目录（如 `uploads`），有时可能需要 `775` 并确保你的部署用户也在 `www-data` 组中，或者更严格地只给 Web 服务器用户写入权限。
    *   **测试:** 访问配置的域名或 IP 地址，检查是否能正常显示登录页面。

6.  **初始用户:**
    *   数据库脚本 (`script.sql`) 通常不包含初始用户。您需要手动注册一个用户，或者直接在 `users` 表中插入一个 `root` 用户记录（密码需要使用 PHP 的 `password_hash()` 函数生成）。第一个注册的用户通常没有特殊权限，需要管理员手动提升或直接创建 `root` 用户。
    *   **重要:** 系统内置 `root` 用户拥有最高权限，请务必设置一个强密码。

## 本地部署 (开发/测试)

除了服务器部署，您也可以在本地计算机上部署 easy管理系统 进行开发或测试。

### Windows (使用 IIS)

1.  **启用 IIS 和 PHP:**
    *   打开 "控制面板" -> "程序" -> "启用或关闭 Windows 功能"。
    *   勾选 "Internet Information Services" 及其下的 "Web 管理工具" 和 "万维网服务"。
    *   在 "万维网服务" -> "应用程序开发功能" 中，确保勾选了 "CGI"。
    *   下载并安装适用于 Windows 的 PHP 版本 (推荐 Non-Thread Safe 版本)。可以使用 [PHP for Windows 官网](https://windows.php.net/download/) 下载。
    *   解压 PHP 到一个目录，例如 `C:\PHP`。
    *   配置 IIS 以识别 PHP：
        *   打开 "IIS 管理器" (可在 Windows 管理工具中找到)。
        *   选择您的计算机名节点，双击 "处理程序映射"。
        *   在右侧操作窗格中，点击 "添加模块映射"。
        *   请求路径填 `*.php`，模块选择 `FastCgiModule`，可执行文件指向 `C:\PHP\php-cgi.exe` (替换为您的实际路径)，名称可填 `PHP_via_FastCGI`。
        *   编辑 `C:\PHP\php.ini` 文件 (如果不存在，可以将 `php.ini-development` 或 `php.ini-production` 复制并重命名为 `php.ini`)：
            *   取消注释并设置 `extension_dir = "ext"`。
            *   取消注释所需的扩展，如 `extension=pdo_mysql`, `extension=gd`, `extension=mbstring`, `extension=fileinfo`, `extension=openssl` (xml 通常默认启用)。
            *   设置 `cgi.force_redirect = 0`。
2.  **安装 MySQL:**
    *   访问 [MySQL Community Downloads](https://dev.mysql.com/downloads/mysql/) 下载适用于 Windows 的 MySQL Community Server 安装程序。
    *   按照安装向导完成安装，过程中需要设置 root 用户的密码。
    *   确保 MySQL 服务正在运行 (可以在 Windows 服务中检查)。
3.  **安装 Composer:**
    *   访问 [Composer 官网](https://getcomposer.org/) 下载 Windows 安装程序 (`Composer-Setup.exe`) 并运行。
    *   安装过程中，它会要求您指定 `php.exe` 的路径 (例如 `C:\PHP\php.exe`)。
4.  **放置项目文件:**
    *   将 easy管理系统 的所有文件和文件夹复制到 IIS 的默认站点目录 `C:\inetpub\wwwroot\easyPMS` 或您指定的其他本地目录。
5.  **数据库设置:**
    *   可以使用 MySQL 命令行客户端或图形化工具 (如 MySQL Workbench 或 phpMyAdmin - 如果您另外安装了 Apache/Nginx + phpMyAdmin) 连接到本地 MySQL。
    *   登录 MySQL (用户 `root`，密码是您安装时设置的)。
    *   创建一个新的数据库: `CREATE DATABASE project_management CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;`
    *   导入数据: `mysql -u root -p project_management < C:\inetpub\wwwroot\easyPMS\script.sql` (使用 CMD 或 PowerShell，并替换为实际路径)。
    *   编辑项目根目录下的 `config.php` 文件：
        *   `DB_HOST` 通常是 `localhost`。
        *   `DB_USER` 是 `root`。
        *   `DB_PASS` 是您安装 MySQL 时设置的 root 密码。
        *   `DB_NAME` 设置为 `project_management`。
6.  **安装 PHP 依赖:**
    *   打开命令提示符 (CMD) 或 PowerShell。
    *   使用 `cd` 命令切换到项目根目录 (例如 `cd C:\inetpub\wwwroot\easyPMS`)。
    *   运行 `composer install`。
7.  **配置 IIS 站点:**
    *   打开 IIS 管理器。
    *   右键点击 "网站" -> "添加网站" (或者使用默认网站)。
    *   设置站点名称，将 "物理路径" 指向您的项目根目录 (例如 `C:\inetpub\wwwroot\easyPMS`)。
    *   设置绑定 (通常是端口 `80`)。
8.  **目录权限:**
    *   在项目根目录下手动创建 `uploads`, `requests`, `logs`, `file` 目录 (如果不存在)。
    *   右键点击这些目录 -> "属性" -> "安全" -> "编辑"。
    *   添加用户 `IUSR` 和 `IIS_IUSRS`，并授予它们 "修改" 和 "写入" 权限。
9.  **访问系统:**
    *   打开浏览器，访问 `http://localhost/easyPMS` (如果项目在子目录) 或 `http://localhost` (如果配置为根站点)。
10. **初始用户:**
    *   参考服务器部署部分的初始用户说明进行设置。

### macOS (使用 Homebrew)

1.  **安装 Homebrew:** 如果未安装，请访问 [brew.sh](https://brew.sh/) 安装。
2.  **安装 PHP:** `brew install php` (会安装最新稳定版，确保是 8.x)。安装后，按照提示将 PHP 添加到 PATH。
3.  **安装 MySQL:** `brew install mysql`。启动 MySQL 服务: `brew services start mysql`。运行 `mysql_secure_installation` 设置 root 密码等安全选项。
4.  **安装 Web 服务器 (可选，可用 PHP 内建服务器):**
    *   Apache: macOS 内建 Apache，或 `brew install httpd`。
    *   Nginx: `brew install nginx`。
    *   或者，直接使用 PHP 内建服务器进行开发测试。
5.  **安装 Composer:** `brew install composer`。
6.  **放置项目文件:** 将项目文件放置在您选择的目录下 (例如 `~/Sites/easyPMS`)。
7.  **数据库设置:**
    *   使用终端登录 MySQL: `mysql -u root -p` (输入您设置的密码)。
    *   创建数据库: `CREATE DATABASE project_management CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;`
    *   导入数据: `mysql -u root -p project_management < /path/to/your/project/script.sql` (替换为实际路径)。
    *   编辑 `config.php`，填入数据库信息 (用户 `root`，密码是您设置的，数据库名 `project_management`)。
8.  **安装 PHP 依赖:**
    *   在终端中 `cd` 到项目根目录。
    *   运行 `composer install`。
9.  **目录权限:**
    *   `cd` 到项目根目录。
    *   `mkdir uploads requests logs file` (如果不存在)
    *   `chmod -R 777 uploads/ requests/ logs/ file/` (注意：`777` 权限过于宽松，仅建议本地开发使用)。
10. **访问系统:**
    *   **使用 PHP 内建服务器:** 在项目根目录运行 `php -S localhost:8000`。然后在浏览器访问 `http://localhost:8000`。
    *   **使用 Apache/Nginx:** 配置虚拟主机指向项目目录，然后通过配置的地址访问。
11. **初始用户:**
    *   参考服务器部署部分的初始用户说明进行设置。

### Linux (Ubuntu/Debian 示例)

推荐使用系统的包管理器安装 LAMP/LEMP 或单独安装组件。

1.  **安装 LAMP/LEMP 和 MySQL:**
    *   **LAMP (Apache):** `sudo apt update && sudo apt install apache2 php libapache2-mod-php php-mysql php-gd php-mbstring php-xml php-zip php-fileinfo mysql-server composer`。
    *   **LEMP (Nginx):** `sudo apt update && sudo apt install nginx php-fpm php-mysql php-gd php-mbstring php-xml php-zip php-fileinfo mysql-server composer`。
    *   **MySQL 安全设置:** 运行 `sudo mysql_secure_installation` 设置 root 密码等。
2.  **放置项目文件:**
    *   将项目文件复制到 Apache 的默认 Web 根目录 `/var/www/html/easyPMS` 或 Nginx 的相应目录 (可能相同或自定义)。
    *   更改文件所有权，使其属于 Web 服务器用户 (通常是 `www-data`): `sudo chown -R $USER:$USER /var/www/html/easyPMS` (本地开发建议使用当前用户，避免权限复杂化，或者 `sudo chown -R www-data:www-data /var/www/html/easyPMS` 如果坚持用 www-data)。
3.  **数据库设置:**
    *   登录 MySQL: `sudo mysql -u root -p`。
    *   创建数据库: `CREATE DATABASE project_management CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;`
    *   导入数据: `sudo mysql -u root -p project_management < /var/www/html/easyPMS/script.sql`。
    *   编辑 `config.php`，填入数据库信息 (用户 `root`，密码是您设置的，数据库名 `project_management`)。
4.  **安装 PHP 依赖:**
    *   `cd /var/www/html/easyPMS`
    *   运行 `composer install`。
5.  **目录权限:**
    *   `cd /var/www/html/easyPMS`
    *   创建目录 (如果不存在): `mkdir uploads requests logs file`
    *   设置权限: `sudo chown -R $USER:$USER uploads/ requests/ logs/ file/` (如果前面用了当前用户) 或 `sudo chown -R www-data:www-data ...`，然后 `sudo chmod -R 755 uploads/ requests/ logs/ file/`。
6.  **Web 服务器配置 (如果未使用默认目录):**
    *   如果项目放在非默认目录，需要配置 Apache 虚拟主机或 Nginx 服务器块指向项目目录。
7.  **访问系统:**
    *   打开浏览器，访问 `http://localhost/easyPMS`。
8.  **初始用户:**
    *   参考服务器部署部分的初始用户说明进行设置。

---

## 💡 使用说明

1.  **访问:** 通过浏览器访问您配置的服务器地址、域名或本地地址 (如 `http://localhost/easyPMS`)。
2.  **登录/注册:**
    *   使用 `login.html` 页面进行登录。
    *   如果注册功能开启（可在系统设置中配置），使用 `register.html` 注册新用户。
3.  **导航:** 使用左侧边栏在不同的功能模块之间切换。
4.  **管理员 (`root`)**:
    *   可以访问 "人员管理"、"系统设置" 和 "互动功能" (日志) 等特殊菜单。
    *   拥有删除项目、管理用户、修改系统配置等权限。
5.  **普通用户**:
    *   可以访问 "项目管理"、"文件下载" 和 "帮助中心"。
    *   只能管理自己创建的项目/仓库，或访问被设置为公开的内容。

## 📁 目录结构

```
.
├── css/                 # CSS 样式文件 (Bootstrap, FontAwesome, 自定义)
├── js/                  # JavaScript 文件 (jQuery, Bootstrap, Monaco Editor)
├── uploads/             # 用户上传文件的存储目录
│   └── code/            # 代码仓库上传文件的子目录
├── requests/            # 在线文档请求数据的存储目录 (JSON)
├── file/                # 存放系统文件，如背景图
├── logs/                # PHP 错误日志目录 (可选)
├── vendor/              # Composer 安装的依赖库
├── add_dachuang_project.php # 添加大创项目页面
├── add_new_user.php     # 添加新用户页面
├── add_onlinefile_project.php # 添加在线文档项目页面
├── code_repository.php  # 代码仓库管理主页
├── config.php           # 数据库和基本配置
├── Database.php         # 数据库操作类
├── dachuang_mange.php   # 大创项目管理主页
├── file_manager.php     # 文件下载/管理页面
├── home.php             # 系统首页
├── help.php             # 帮助中心页面
├── login.html           # 登录页面
├── login.php            # 登录处理逻辑
├── logout.php           # 退出登录逻辑
├── onlinefile_manage.php # 在线文档管理主页
├── program_manage.php   # 项目管理聚合页面
├── register.html        # 注册页面
├── register.php         # 注册处理逻辑
├── repo_detail.php      # 代码仓库详情页
├── search.php           # 搜索处理逻辑
├── settings.php         # 系统设置页面
├── sidebar_template.php # 左侧导航栏模板
├── user_management.php  # 用户管理页面
├── composer.json        # Composer 依赖定义
├── script.sql           # 数据库结构文件
└── README.md            # 本文件
```

## ☎️ 问题联系
- 邮箱：2358155969@qq.com
- 有问题可以及时提issue

## 🙏 致谢

*   [Bootstrap](https://getbootstrap.com/)
*   [Font Awesome](https://fontawesome.com/)
*   [jQuery](https://jquery.com/)
*   [Monaco Editor](https://microsoft.github.io/monaco-editor/)
