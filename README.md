# McDonald's Menu Database Management System

A Python desktop application built with PyQt6 and MySQL to manage fast-food restaurant menu records through dynamic graphical dialogs.

## Overview

This project provides a graphical user interface (GUI) to perform full CRUD (Create, Read, Update, Delete) operations on a relational database modeling a fast-food menu system (`mcdonaldsmenu`). The application dynamically launches dedicated window dialogs depending on the selected table and action.

## Features

- **Full CRUD Functionality**: Add, view, edit, and delete records across relational database tables[cite: 2].
- **Supported Tables**[cite: 2]:
  - `categories`: Item classification and descriptions[cite: 2].
  - `menuitems`: Product names and standard pricing[cite: 2].
  - `sizes`: Serving and portion options[cite: 2].
  - `menuitemsizes`: Relationship mappings between menu items and sizes[cite: 2].
  - `nutritionalinfo`: Item nutritional breakdowns (calories, fat, carbohydrates, protein)[cite: 2].
- **Dynamic Modular UI**: Interfaces are built with Qt Designer and loaded dynamically using PyQt6's `uic.loadUi`[cite: 2].
- **Database Error Handling**: Catches common MySQL exceptions such as authentication errors, missing databases, and invalid operations[cite: 2].

## Tech Stack

- **Language**: Python 3[cite: 2]
- **GUI Framework**: PyQt6[cite: 2]
- **Database Driver**: `mysql-connector-python`[cite: 2]
- **Database**: MySQL Server[cite: 2]

## Project Structure

```text
├── code1.py                 # Main application script
├── combo.ui                 # Main menu and table selection interface
├── addcategory.ui           # UI for adding categories
├── addmenuitem.ui           # UI for adding menu items
├── addmenuitemsize.ui       # UI for adding item-size mappings
├── addnutrional.ui          # UI for adding nutritional data
├── addsize.ui               # UI for adding sizes
├── edit*.ui                 # Dialog interfaces for updating records
├── delete*.ui               # Dialog interfaces for deleting records
└── view*.ui                 # Dialog interfaces for table views

Getting Started
Prerequisites
Python 3.8+

MySQL Server installed and running locally

Required Python libraries:

pip install PyQt6 mysql-connector-python

Database Setup
Create a MySQL database named mcdonaldsmenu[cite: 2]:

SQL
CREATE DATABASE mcdonaldsmenu;
Create the necessary tables (categories, menuitems, sizes, menuitemsizes, nutritionalinfo) corresponding to your schema[cite: 2].

Configuration
Update the MySQL connection credentials in the source code or extract them into environment variables before running[cite: 2]:

Python
connectconfig = {
    'user': 'root',
    'password': 'YOUR_PASSWORD',
    'host': 'localhost',
    'database': 'mcdonaldsmenu'
}
Running the App
Bash
python code1.py
Security Note
Ensure hardcoded credentials are removed or replaced with an environment variable file (.env) before pushing changes to a public repository.
