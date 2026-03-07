### *The source code is part of academic coursework and is available upon request for review purposes, subject to university guidelines.*

# User Guide - Web Application

This guide explains how to use the core features of this web application. The application allows users to manage **Gebiete** (topics/areas) and **Themen** (themes/subjects within those areas).



## Getting Started

### 1. Accessing the Application

- **Live Demo:** Visit [web-application-sigma-tawny.vercel.app](https://web-application-sigma-tawny.vercel.app)

### 2. Login

To access protected features, you'll need to log in:

1. Click the **Login** button in the header (top-right corner)
2. Enter your credentials (Campus ID and password)

**Test User 1 – Moriarty**
- CampusID: `459810`
- Password: `123_abc_ABC`

**Test User 2 – Holmes**
- CampusID: `459813`
- Password: `123_abc_ABC`
3. Click **Submit**

> **Note:** Some features like browsing public Gebiete are available without login.

---

## Core Features

### Browsing Gebiete (Topic Areas)

**Available to:** Everyone (including guests)

The home page displays all available Gebiete that you have access to:
- **Public Gebiete:** Visible to all users
- **Private Gebiete:** Only visible to their manager

Each Gebiet card shows:
- Name and description
- Manager name
- Creation date
- Number of themes
- Public/closed status

**To view details:** Click on any Gebiet card to see its full information and associated Themen.

---

### Viewing Themen (Themes)

**Available to:** Everyone who can access the parent Gebiet

When you open a Gebiet, you'll see:
- Complete Gebiet details (description, manager, creation date)
- List of all Themen within that Gebiet
- Each Thema shows its name, description, and other details

**To view a Thema:** Click on any Thema to see its complete information.

---

### Creating a New Gebiet

**Available to:** Logged-in users only

1. Navigate to the home page
2. Click the **"Neues Gebiet"** button (usually in the header or main area)
3. Fill in the required information:
   - **Name:** Title of your Gebiet (3-100 characters)
   - **Description:** Detailed description (1-1000 characters)
   - **Public:** Check if you want it visible to everyone
   - **Closed:** Check if you want to prevent new Themen from being added
4. Click **Save**

You will be automatically set as the manager of the Gebiet you create.

---

### Creating a New Thema

**Available to:** Manager of the Gebiet only

1. Open the Gebiet where you want to add a Thema
2. Click the **"Neues Thema"** button
3. Fill in the required information:
   - **Title:** Name of your Thema
   - **Description:** Detailed description
   - Additional fields as required
4. Click **Save**

> **Note:** You can only create Themen in Gebiete that you manage and that are not closed.

---

### Editing a Gebiet

**Available to:** Manager of the Gebiet only

1. Open the Gebiet you want to edit
2. Click the **"Editieren"** (Edit) button
3. Modify the fields you want to change:
   - Name
   - Description
   - Public status
   - Closed status
4. Click **Save** to apply changes or **Cancel** to discard

---

### Deleting a Gebiet

**Available to:** Manager of the Gebiet only

1. Open the Gebiet you want to delete
2. Click the **"Löschen"** (Delete) button
3. Confirm the deletion

> **Important:** You can only delete a Gebiet if it has no Themen. Remove all Themen first before deleting the Gebiet.

---

### Managing Your Profile

**Available to:** Logged-in users only

#### Admin Page
Access your professor profile:
1. Click **"Admin"** in the header navigation
2. View your profile information
3. Make any necessary changes

#### Preferences Page
Customize your settings:
1. Click **"Prefs"** in the header navigation
2. View and edit your global preferences
3. Update your profile settings

---

## User Permissions

The application has two main permission levels:

### Guest Users (Not Logged In)
- ✅ Browse public Gebiete
- ✅ View public Themen
- ❌ Create Gebiete or Themen
- ❌ Edit or delete content

### Authenticated Users (Logged In)
- ✅ All guest permissions
- ✅ Browse private Gebiete they manage
- ✅ Create new Gebiete
- ✅ Create Themen in Gebiete they manage
- ✅ Edit and delete their own Gebiete
- ✅ Access Admin and Preferences pages

---

## Tips for Hiring Team

### What to Test

1. **Authentication Flow:**
   - Try logging in and out
   - Notice how the available features change

2. **CRUD Operations:**
   - Create a new Gebiet
   - Add Themen to it
   - Edit the Gebiet details
   - Try to delete it (with and without Themen)

3. **Access Control:**
   - Notice that you can only edit Gebiete you created
   - Public vs. private Gebiet visibility

4. **Responsive Design:**
   - Try the application on different screen sizes
   - Test the mobile navigation

5. **Error Handling:**
   - Try submitting forms with invalid data
   - Check how errors are displayed to users

### Technical Highlights

- **Full-Stack Application:** React frontend + Node.js/Express backend
- **RESTful API:** Clean API structure with proper HTTP methods
- **Authentication:** JWT-based authentication system
- **Validation:** Front-end and back-end validation
- **Responsive UI:** Bootstrap-based responsive design
- **Error Boundaries:** Graceful error handling
- **Testing:** Comprehensive test coverage (see coverage/ folders)

---

*Last updated: March 2026*
