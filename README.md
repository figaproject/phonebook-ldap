SIP Phonebook Server

SIP Phonebook Server is a lightweight self-hosted phonebook management system for SIP/IP phones. It allows you to store, edit, import, and serve contact lists from an Excel file to IP phones using LDAP and HTTP-based phonebook formats.

The project is designed for small offices, call centers, retail stores, warehouses, hotels, and any environment where multiple SIP phones need access to a shared contact directory.

What is it for?

Many SIP/IP phones support remote phonebooks, but managing contacts manually on every device is inconvenient. This project provides a centralized phonebook server that can be installed on a Windows PC and used as a shared contact source for supported phones.

Contacts can be edited through a simple web admin panel, imported from Excel, and automatically served to phones over the local network.

Main Features
Web-based admin panel for contact management
Login protection for the admin interface
Excel-based contact storage
Import and download contacts in .xlsx format
Built-in LDAP server for SIP/IP phone lookup
HTTP XML/CSV phonebook endpoints
Support for short internal numbers
Improved number matching to avoid false matches inside mobile numbers
Pagination for large contact lists
Tested design for large phonebooks with thousands of contacts
Windows startup scripts for automatic launch after reboot
Configuration through a simple config.json file
Supported Phone Brands

The project includes ready-to-use settings examples for many SIP/IP phone brands, including:

Grandstream
Yealink
Fanvil
Cisco
Snom
Poly / Polycom
Panasonic
Htek
Akuvox
Dinstar
Escene
Flyingvoice
Avaya
Mitel
Alcatel-Lucent
Unify

Most phones that support LDAP or remote XML/CSV phonebooks can be connected with manual configuration.

How it works

The server reads contacts from:

data/contacts.xlsx

The web admin panel is used to manage contacts.

SIP phones can access the same phonebook using LDAP:

ldap://SERVER_IP:389
Base DN: ou=contacts,dc=phonebook,dc=local

HTTP phonebook endpoints are also available for devices that use XML or CSV remote phonebooks.

Typical Use Case
Install the project on a Windows PC.
Import or edit contacts through the web admin panel.
Configure SIP phones to use the server as an LDAP or remote phonebook source.
Phones will search and display names from the shared phonebook during dialing and incoming calls.
Default Admin Login
Username: admin
Password: 1234

The login and password can be changed in config.json.

Windows Autostart

The project includes scripts for automatic startup:

Start when the user logs in
Start after Windows boot using Task Scheduler

This makes the phonebook server available automatically after a PC restart.



