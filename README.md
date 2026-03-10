<p align="center">
  <img src="https://raw.githubusercontent.com/Omarsalama2001/Omarsalama2001/main/Logoooo.png"
       width="300" 
       alt="PPS Logo"/>
</p>

<h1 align="center">Platform Petroleum Services</h1>
<p align="center">
  A Flutter Web CRM system for managing and issuing employee certificates with QR-based access, built with Firebase & Clean Architecture.
</p>

<p align="center">
  <a href="https://dashboard-pps.web.app/">
    <img src="https://img.shields.io/badge/Live%20Demo-Visit%20Now-brightgreen?style=for-the-badge"/>
  </a>
  <img src="https://img.shields.io/badge/Flutter-Web-02569B?style=for-the-badge&logo=flutter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black"/>
</p>

---

## ✨ Features

<table>
  <tr>
    <td align="center" width="50%">
      <h3>🔐 Authentication</h3>
      <p>Secure admin login system powered by <strong>Firebase Authentication</strong></p>
    </td>
    <td align="center" width="50%">
      <h3>📄 Certificate Management</h3>
      <p>Full CRUD operations for managing and issuing certificates with ease</p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <h3>👥 Customer Management</h3>
      <p>Add and manage customers with full profile information</p>
    </td>
    <td align="center" width="50%">
      <h3>📱 QR-Based Access</h3>
      <p>Customers can access their certificates via <strong>QR Code</strong> on mobile</p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <h3>📤 Export PDF & Excel</h3>
      <p>Export certificates as <strong>PDF or Excel</strong> files with one click</p>
    </td>
    <td align="center" width="50%">
      <h3>☁️ Cloud Sync</h3>
      <p>Real-time data management powered by <strong>Firebase Firestore</strong></p>
    </td>
  </tr>
</table>

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white"/>
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black"/>
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flutter_Bloc-02569B?style=for-the-badge&logo=flutter&logoColor=white"/>
</p>

---

### 📦 Key Packages

<details>
<summary>🔍 View All Packages</summary>

<br/>

#### 🔐 Authentication & Storage
| Package | Description |
|---------|-------------|
| `firebase_auth` | Admin authentication |
| `firebase_core` | Firebase core setup |
| `cloud_firestore` | Real-time database |
| `firebase_storage` | Cloud file storage |
| `supabase_flutter` | Certificate image storage |
| `shared_preferences` | Local data caching |

---

#### 📊 Data Grid & Export
| Package | Description |
|---------|-------------|
| `syncfusion_flutter_datagrid` | Advanced data grid |
| `syncfusion_flutter_datagrid_export` | Export to PDF & Excel |
| `syncfusion_flutter_datepicker` | Date picker |
| `qr_flutter` | QR code generation |

---

#### 🎨 UI & UX
| Package | Description |
|---------|-------------|
| `flutter_screenutil` | Responsive UI |
| `google_fonts` | Custom fonts |
| `lottie` | Animations |
| `flutter_animate` | UI animations |
| `easy_sidemenu` | Side navigation menu |
| `cached_network_image` | Image caching |
| `photo_view` | Image zoom viewer |
| `awesome_dialog` | Beautiful dialogs |
| `top_snackbar_flutter` | Custom snackbars |

---

#### 🔧 Utilities
| Package | Description |
|---------|-------------|
| `go_router` | Navigation & routing |
| `get_it` | Dependency injection |
| `dartz` | Functional programming |
| `equatable` | Value equality |
| `uuid` | Unique ID generation |
| `file_picker` | File selection |
| `url_launcher` | URL launching |
| `intl` | Date formatting |

</details>

---

## 🏗️ Architecture

This app is built using **Clean Architecture** pattern:

| Layer | Responsibility |
|-------|---------------|
| 📊 **Data** | Remote data sources, Models, Repository implementations |
| 🧠 **Domain** | Entities, Repository interfaces, Use cases |
| 🎨 **Presentation** | UI Screens, Widgets, Bloc/Cubit State Management |

<details>
<summary>📂 View Full Project Structure</summary>

```
📦 lib
 ├── 📄 bloc_observer.dart
 ├── 📄 injectionContainer.dart
 ├── 📄 main.dart
 ├── 📄 main_demo.dart
 ├── 📄 main_production.dart
 │
 ├── 📂 core
 │   ├── 📄 router.dart
 │   ├── 📂 constants
 │   │   └── 📄 cache_keys.dart
 │   ├── 📂 error
 │   │   ├── 📄 exeptions.dart
 │   │   └── 📄 faliure.dart
 │   ├── 📂 extensions
 │   │   ├── 📄 media_query_extension.dart
 │   │   └── 📄 translation_extension.dart
 │   ├── 📂 network
 │   │   ├── 📄 network_info.dart
 │   │   └── 📂 connection
 │   │       └── 📂 bloc
 │   │           ├── 📄 connection_bloc.dart
 │   │           ├── 📄 connection_event.dart
 │   │           └── 📄 connection_states.dart
 │   ├── 📂 services
 │   │   ├── 📄 certificates_services.dart
 │   │   ├── 📄 customers_services.dart
 │   │   ├── 📄 general_services.dart
 │   │   └── 📂 cubit
 │   │       ├── 📄 customer_services_cubit.dart
 │   │       └── 📄 customer_services_state.dart
 │   ├── 📂 utils
 │   │   ├── 📄 app_colors.dart
 │   │   ├── 📄 size_config.dart
 │   │   ├── 📂 styles
 │   │   │   └── 📄 text_styles.dart
 │   │   └── 📂 theme
 │   │       ├── 📄 app_theme.dart
 │   │       └── 📂 cubit
 │   │           ├── 📄 theme_cubit.dart
 │   │           └── 📄 theme_state.dart
 │   └── 📂 widgets
 │       ├── 📄 defult_app_bar.dart
 │       ├── 📄 defult_elevated_button.dart
 │       ├── 📄 defult_text_feild.dart
 │       ├── 📄 loading_animation_widget.dart
 │       └── 📄 top_snack_bar.dart
 │
 └── 📂 features
     ├── 📂 auth
     │   ├── 📂 data
     │   ├── 📂 domain
     │   └── 📂 presentation
     │       ├── 📂 blocs
     │       │   └── 📂 cubit
     │       │       ├── 📄 auth_cubit.dart
     │       │       └── 📄 auth_state.dart
     │       ├── 📂 pages
     │       │   └── 📄 Login_page.dart
     │       └── 📂 widgets
     │
     ├── 📂 certificates
     │   ├── 📂 data
     │   │   ├── 📂 data_sources
     │   │   ├── 📂 models
     │   │   │   ├── 📄 certificate_model.dart
     │   │   │   └── 📄 certificate_image_model.dart
     │   │   └── 📂 repositories_impl
     │   ├── 📂 domain
     │   │   ├── 📂 entities
     │   │   ├── 📂 repositories
     │   │   └── 📂 use_cases
     │   │       ├── 📄 add_new_certificate_usecase.dart
     │   │       ├── 📄 delete_certificate_usecase.dart
     │   │       ├── 📄 get_all_certificates_usecase.dart
     │   │       ├── 📄 get_certificate_by_id_usecase.dart
     │   │       └── 📄 update_certificate_usecase.dart
     │   └── 📂 presentation
     │       ├── 📂 blocs
     │       ├── 📂 pages
     │       │   ├── 📄 add_cerfificate_page.dart
     │       │   ├── 📄 all_certificates_page.dart
     │       │   └── 📄 certificate_details.dart
     │       └── 📂 widgets
     │
     ├── 📂 customers
     │   ├── 📂 data
     │   ├── 📂 domain
     │   │   └── 📂 use_cases
     │   │       ├── 📄 add_new_customer_usecase.dart
     │   │       ├── 📄 delete_customer_usecase.dart
     │   │       ├── 📄 get_all_customers_usecase.dart
     │   │       └── 📄 update_customer_usecase.dart
     │   └── 📂 presentation
     │       ├── 📂 blocs
     │       ├── 📂 pages
     │       │   ├── 📄 add_customer_page.dart
     │       │   └── 📄 all_customers_page.dart
     │       └── 📂 widgets
     │
     └── 📂 home
         └── 📂 presentation
             ├── 📂 pages
             │   └── 📄 home_page.dart
             └── 📂 widgets
                 ├── 📄 side_menu.dart
                 └── 📄 side_menu_footer.dart
```

</details>

---

## 📸 Screenshots

### 🔐 Login
<p align="center">
  <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/login_image.jpg.png" width="700"/>
</p>

---

### 📄 Certificates
<table>
  <tr>
    <td align="center">
      <strong>All Certificates</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/all_certificates_image.jpg.png" width="500"/>
    </td>
    <td align="center">
      <strong>Certificate Details</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/certificate_details_image.jpg.png" width="500"/>
    </td>
  </tr>
</table>

---

### ➕ Add Data
<table>
  <tr>
    <td align="center">
      <strong>Add Certificate</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/add_certificate_image.jpg.png" width="500"/>
    </td>
    <td align="center">
      <strong>Add Customer</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/add_custm_image.jpg.png" width="500"/>
    </td>
  </tr>
</table>

---

### 👥 Customers
<p align="center">
  <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/all_custm_image.jpg.png" width="700"/>
</p>

---

### 📤 Export PDF & Excel
<p align="center">
  <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/export_image.jpg.png" width="700"/>
</p>

---

### 📱 QR Code & Mobile View
<table>
  <tr>
    <td align="center">
      <strong>QR Code</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/qr-code_image.jpg.png" width="500"/>
    </td>
    <td align="center">
      <strong>Mobile Certificate View</strong><br/><br/>
      <img src="https://raw.githubusercontent.com/Omarsalama2001/platform-pps-demo/main/cr_mobile-portrait.png" width="250"/>
    </td>
  </tr>
</table>

---

## 🔒 Source Code

> 🔒 Source code is private.
> Feel free to [contact me](mailto:omarrsalama90111@gmail.com) for more details.

---

## 📬 Contact

<p align="left">
  <a href="mailto:omarrsalama90111@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://www.linkedin.com/in/0marsalama">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://github.com/Omarsalama2001">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</p>
