FreeCinema OTT Platform - Full Project Documentation

Overview

FreeCinema is a fully functional, modern OTT (Over-the-Top) movie and TV streaming platform built using Next.js. The UI draws inspiration from Netflix, Amazon Prime Video, Hotstar, and Dribbble shots, featuring a 3D-styled design, rounded corners, blur effects, motion transitions, and responsive layouts. This system is content-rich and supports full auto-fetching from APIs and Telegram storage, offering a premium visual experience and robust performance.


---

1. Project Architecture

Frontend

Framework: Next.js (React-based SSR and SSG)

Styling: Tailwind CSS, Animate.css, Framer Motion

Design Aesthetic: 3D cards, rounded UI, neumorphism, glassmorphism with CSS blur and drop shadows

Device Support: Fully responsive (Desktop, Tablet, Mobile)


Backend

Admin Panel: Built with Next.js and Tailwind

Authentication: Password-protected admin access only (e.g. Admin@9165)

Storage: Telegram Bots & Channels (used as CDN)

Data Fetching: TMDB, OMDB, TVDB, OBDB APIs

Database: Supabase (PostgreSQL based)

Deployment: Vercel for frontend; Cloudflare Workers for CDN and player proxy



---

2. UI Layout Design

Homepage

Hero banner with animated slider (Featured/Trending)

Sections:

Trending in India

Hollywood

Bollywood

South Indian

New Releases

Most Viewed

Top Rated

Popular Web Series


Each card: 3D hover effect, rounded corners, dynamic blur background

Custom RXPlayer embedded with controls


Content Play Page (/play/{id})

Full-width RXPlayer

Movie/Show Info Section:

Title, Release Date, Language, IMDB Rating, Genre

Actor/Director Details with profile avatars


Stream Source Selector: (AutoEmbed, MultiEmbed, Telegram)

Related Movies (carousel)

For Series:

Episode/Season selector below player

Auto-playing next episode option



Live TV Page

Auto-updated IPTV M3U support

Grid-style EPG with time slots

Player with instant tuning and pause/resume


Search Page

Full page search with debounce filtering

Shows results across categories


Category Pages

Each category (Movies, TV, Series) with scrollable sections

Filters by year, genre, language

Country-based recommendations



---

3. Admin Panel (Password Protected)

Login Protection

Single password auth (Admin@9165)


Dashboard Overview

Analytics: Views, Clicks, Search Trends, Top Content

Graphs for last 7/30 days


Content Management

Add Content (Title, TMDB/IMDB ID, Upload to Telegram, Categories, Genres)

Upload System:

Upload local file to Telegram via bot

Save metadata to Supabase

Extract direct Telegram links (for RXPlayer)


Fetch Details Button:

Auto-fetch details from OBDB/TMDB via ID



Manage Content

Edit/Update/Delete content

Manage categories/tags

Assign priority for homepage sections

Toggle visibility (hide/unhide)


Search Integration

Full-text search of all saved content

Result linking to /play/{id}


IPTV Integration

Add new M3U link

KV storage auto-refreshes M3U daily

EPG parser integration

Channel grouping and display customization


User Management

View users via Google OAuth (email list)

Revoke access


Settings

Set site name, logos, colors (theme override)

Change password



---

4. RXPlayer Features

Tech Stack: Hybrid of JW Player and Shaka Player

Supported Formats: M3U, M3U8, MP4, MKV, DASH, HLS

Features:

Multi-audio and quality selection (Auto/Manual)

Resume playback

Skip intro

Next/Previous episode navigation

DRM support (Widevine/Fairplay)

Direct play from Telegram files

Adaptive Bitrate (ABR)




---

5. APIs & Data Sources

TMDB: https://api.themoviedb.org/

OMDB: http://www.omdbapi.com/?apikey=3ccc73c8

TVDB: For series & TV metadata

OBDB: Primary metadata fetcher

Streaming Sources:

AutoEmbed

MultiEmbed

Vidsrc.dev

Telegram CDN




---

6. Deployment Guide

Environment

Node.js v18+

Vercel account

Supabase account with SQL schema

Telegram Bot and Channel set up


Steps

1. Clone repo and configure .env with API keys and secrets


2. Integrate Google OAuth for admin login


3. Deploy to Vercel (automatic CI/CD)


4. Telegram Bot Setup:

Use Telegram Bot API to upload files

Save message/file ID in Supabase



5. KV Setup for IPTV

Use Cloudflare Workers to fetch and refresh M3U data daily



6. Upload Initial Content via Admin Panel




---

7. Security & Optimizations

Obfuscate API keys

Disable right-click, inspect in production

Rate limit API routes

Lazy load components

Image optimization via Next.js

Responsive design using CSS grid/flexbox



---

8. Future Enhancements

Multi-language UI support

Watchlist/favorites

Telegram-based user subscription

Notification system (new content alerts)

Custom domain with SEO metadata

PWA + Offline Support



---

9. Tech Stack Summary


---

10. Credits & Licenses

3D Icons: 3dicons.co

UI Animations: cssanimation.io, animate.style

Content APIs: TMDB, OMDB, TVDB,

Developer: xD MLHK
Developed By ❤️ In India
FreeCinema - Watch Now Free Now

