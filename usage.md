# Usage

## Users

### Basic User
Basic Users can't view anything that haven't been explicitly added to their User account. They also do not have the ability to create any Findings, Engagements, Products, and Product Types. All "edit hamburgers" are disabled/missing from the UI. They do not have permission to close or edit findings as well, they can only add notes. 

The only main pages they have access to are:

1. Product List (this is essentially their home page). It lists products they have access to view.
2. Reports (report builder and a way to view reports built for their products)
3. Metrics (this is restricted to only the products they have permission to view).

### Staff
The Staff user has more write access and can view all products. They have access to /admin but their unable to to anything on that page by default.

The Staff user has access to the following pages by default:

1. Dashboard (By default, as staff, this only shows metrics for Engagements where the staff user is assigned, not org-wide metrics).
2. Products
3. Engagements
4. Findings
5. Endpoints 
6. Reports
7. Metrics
8. Users
9. Calendar (displays engagements)
10. Settings, but only:
    1. Credential Manager
    2. Tool Configuration
    3. Tool Types
    4. Notifications (can only edit personal notifications, not org-wide defaults)
    5. Rules Framework
    6. JIRA
    7. Surveys

Anything within the platform can be edited/created as a Staff user, no matter what they are assigned. Full write-access, with the exception of editing a User, only SuperUsers can edit users.
There have also been some known limitations with the API, adding Engagements and Tests have thrown permission errors as Staff, even though you can create them in the UI without issues. Upgrading to SuperUser fixes this. I would consider this a bug in the platform.

### SuperUser
The SuperUser is essentially Staff with a few extras:

1. They can edit users.
2. They can access/edit things in /admin
    1. You can edit very specific rules for users in this panel. This might be how we create read-only org-wide users.
3. The following Settings are now available for modification:
    1. System Settings 
    2. Note Types
    3. Google Sheet SYnc
    4. Login Banner
    5. As well the Notifications page allows you to set org-wide defaults on notificaitons.
