# Job Hunter Telegram Bot

This bot does the following as a daily routine, while it listens to the users requests as well.

1. Scrape job listings from various job portals based on user-defined criteria.
2. Send personalized job alerts to users via Telegram.
3. Allow users to manage their job search preferences through Telegram commands.

## Features

- **Job Scraping**: Automatically scrape job listings from multiple job portals.
- **Personalized Feeds**: Send job feeds based on user image.
- **Feedback System**: Users can provide feedback on his / her image to improve future job recommendations.
- **Requirements Deep Dive**: Analyze job requirements and match them with user profiles. (On Demand)
- **Improvement Plans**: Based on requirements and user image, suggest improvement plans. (On Demand)
- **Telegram Integration**: Seamless interaction through Telegram bot commands.

## Modules

- **Scraper Module**: Handles the scraping of job listings from various job portals. (use brightdata)
- **User Image Module**: Manages user profiles and preferences.
- **Job Listing Module**: Manages job listings and matches them with user profiles.
- **Match Module**: Analyzes job requirements and user profiles for better matching.
- **Analysis Module**: Provides insights and improvement plans based on job requirements and user profiles.
- **Gateway Module**: Manages communication between the bot and Telegram. Manages timed jobs.

## Architecture

Telegram Server <-> Gateway Module 

Gateway Module <-[Search Job Listings]-> Scraper Module
Gateway Module <-[Job Listings]-> Job Listing Module
Gateway Module <-[User Requests]-> User Image Module
Gateway Module <-[Match Requests]-> {Match Module, User Image Module, Job Listing Module}
Gateway Module <-[Analysis Requests]-> {Analysis Module, User Image Module, Job Listing Module}

## Setup Instructions

