# Installation Routine
This is a fairly common routine for setting up a new MODX site.
## Install
1. Change database to utf8 and utf8_general_ci.
## File System
1. After installation, rename .htaccess in both root folder and in /core. This will allow for FURLs and remove the insecure core message in the dashboard.
## Manager
1. Edit menus and move the "Preview Site" link to its own top level space to make it quicker to open the front end.
2. Go to Content->Content Types, edit the HTML type and remove the '.html' extension. Do this by double-clicking the .html extension text.
## System Settings
1. Under "Friendly URL", turn on friendly_urls. Turn on friendly_alias_realtime. Optionally turn on use_alias_path if parent/child linking structures will be used. 
2. Under "Site", set the Site Name.
3. Under "System and Server", disable feed_modx_news_enabled and feed_modx_security_enabled.
4. Under "Backend Manager", disable enable_gravatar.
## Templates and Content
1. Edit the base template and clear out anything unneeded. Leave a few variables for convenience and some of the header tags like base href.
2. Edit Home resource to clear out unneeded content.
3. Create a folder in the assets folder called "css" and create a file in there called "style.css" or whatever sounds good. Now edit the template to add the css to it such as `<link rel="stylesheet" href="[[++assets_url]]css/style.css" />`.
4. Create a new resource called '404' or similar. Create a basic 'page not found' page. Create a matching custom template if needed. Go in System Settings to "Site" and set this resource as the Error Page. Set the page to Published by Hide From Menus.
## Packages
1. Install TinyMCE Rich Text Editor by jako.
2. Install Ace by bezumkin2.
3. Install ModDevTools.
4. Install PDOTools if there will be need for resource listing, menu creating, pagination, field lookups, etc.
5. Updater.
6. Collections.
7. ModDevTools.
8. CssSweet for SCSS based workflow from within Manager.
9. LogPageNotFound for sites where potentially-legit 404 pages might accessed, where you want to create 301s.
10. pThumb.
11. Updater. 
12. Install repositories for ModMore and ModStore if any of these are required:
    1. pdoTools (ModStore free)
    2. ContentBlocks (ModMore paid)
    3. Redactor (ModMore paid)
    4. ClientConfig (ModMore free) to provide clients easy access to customized settings.
## Handy Links
1. Customize LogPageNotFound as a full-width Dashboard widget: https://gist.github.com/sottwell/874cd0edc17d9a714aa9 (by sottwell)
2. Add Error Log Report widget to the Dashboard: https://gist.github.com/sottwell/c8ee468226e3e732602b (by sottwell)
