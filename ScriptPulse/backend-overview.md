# Backend (.NET) Overview

## Technology Stack
- **Backend Framework:** .NET
- **Database:** SQLite (database file stored in the `PulseData` folder)
- **AI Integration:** OpenAI or similar service for script processing

## Main Controller
The backend exposes a controller with two primary methods:

### 1. Process Script
- **Input:** Original script text from the user
- **Output:**
  - `title`: Generated title for the script
  - `cleanedScript`: Improved/cleaned version of the script
  - `hookLine`: Catchy hook line
  - `scenes`: List of scenes extracted from the script
- **Logic:** Uses OpenAI (or similar) to process the script and generate the required outputs.

### 2. Save Script & Scenes
- **Input:** Title, cleanedScript, hookLine, scenes (from Angular frontend after user presses save)
- **Output:** Confirmation of successful save
- **Logic:** Saves the provided data to the SQLite database in the `PulseData` folder.

## Data Flow
- **Frontend (Angular):** Sends original script and receives processed results.
- **Backend (.NET):** Processes script, returns results, and saves data to SQLite.
- **AI Service:** Used for generating cleaned script, hook line, and scenes.

---
This file summarizes the backend structure, main controller methods, and data flow. Update as needed as your project evolves.