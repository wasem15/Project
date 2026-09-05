# Python Career & Job Portal

A Django-based web application that presents information about the Python developer profession, including skills, career demand, and geographic trends, with live Python job vacancies retrieved from the HeadHunter API.

## Overview

The project combines career-oriented informational content with live job-market data.

Users can explore:

- Python developer career information
- Required skills
- Job-market demand
- Geographic information
- Recent Python-related vacancies

Vacancy data is retrieved directly from the HeadHunter API and processed before being displayed in the application.

## Features

### Career Information
- Informational pages about the Python developer profession
- Skills and technologies overview
- Job-market demand information
- Geographic career information
- Chart/image-based content managed through Django Admin

### Job Vacancies
- Live vacancy retrieval from the HeadHunter API
- Filtering of Python-related vacancies
- Sorting by publication date
- Vacancy detail retrieval
- Salary information formatting
- Key-skill extraction and formatting

### Content Management
- Django ORM models for application content
- Django Admin for managing text and images
- Local media storage for uploaded images

## Architecture

The project uses a server-rendered Django architecture.

```text
Browser
   │
   ▼
Django Views
   │
   ├── Django ORM ──► SQLite
   │
   ├── Django Templates ──► HTML/CSS
   │
   └── HeadHunter API ──► Job Vacancy Data
