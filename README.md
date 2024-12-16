# Advanced-Coding-Final-Project
This repository contains all my work regarding the final project for AS.410.712.82.FA24 Advanced Coding in Bioinformatics class in my Masters of Bioinformatics course at Johns Hopkins University

# Cytochrome P450 Search Application

## Overview
This application allows users to query the Cytochrome P450 database and view enzyme-related details. Results are displayed in an HTML table.

## Prerequisites
- **Web server** with CGI enabled
- **Python 3** installed
- **MySQL Database** with Cytochrome P450 data

## Setup Instructions
1. **Database Setup**:
   - Import the provided SQL script to create and populate the database:
     ```sql
     mysql -u <username> -p <database_name> < cytochrome_p450.sql
     ```

2. **Edit Database Configuration**:
   - Open the `db_config.txt` file and update with your database credentials:
     ```
     host=localhost
     user=your_username
     password=your_password
     database=your_database
     ```

3. **Deploy the Files**:
   - Place these files in your web server directory:
     - `search_cytochrome.html` (HTML form)
     - `cytochrome_query.cgi` (CGI script)
     - `db_config.txt` (configuration)
   - Ensure the `cytochrome_query.cgi` script has execute permissions:
     ```bash
     chmod +x cytochrome_query.cgi
     ```

4. **Access the Application**:
   - Open the following URL in your browser:
   - http://bfx3.aap.jhu.edu/amulpur1/project01/search_cytochrome.html

## Usage
1. Enter an enzyme name in the search box (e.g., `CYP2`).
2. Click **Search** to view the results.

## Notes
- Credentials are stored in `db_config.txt` for easy updates.
- Ensure correct file permissions and paths.

## Troubleshooting
- **404 Error**: Verify file paths and permissions.
- **Internal Server Error**: Check the shebang line in the CGI script:
- dos2unix command on files
- Renaming cytochrome_query.py to .cgi
- Correcting file permissions
- Setting the action path in HTML
- Placing files in /var/www/html

Credits
Developed by Akhil Mulpuru
