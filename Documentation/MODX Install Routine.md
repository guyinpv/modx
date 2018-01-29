# Installation Routine

1) During install, change database to utf8 and utf8_general_ci.
2) After installation, rename .htaccess in both root folder and in /core. This will allow for FURLs and remove the insecure core message in the dashboard.
3) Edit menus and move the "Preview Site" link to its own top level space to make it quicker to open the front end.
4) Go in System Settings to the FURL section and turn on "Use Friendly URLs".
5) Go to Content->Content Types, edit the HTML type and remove the '.html' extension. Do this by double-clicking the .html extension, it will turn into a textbox, erase the extension and click elsewhere to save.
6) Edit the base template and clear out anything unneeded. Leave a few variables for convenience and some of the header tags like base href.
7) Edit Home resource to clear out unneeded content.
8) Go in package management and install "TinyMCE Rich Text Editor" by jako, and "Ace" by bezumkin2.
9) Create a folder in the assets folder called "css" and create a file in there called "style.css" or whatever sounds good. Now edit the template to add the css to it such as `<link rel="stylesheet" href="[[++assets_url]]css/style.css" />`.
