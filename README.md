# Kesatria-Assignment
Assignment for Kesatria

# 3D Data Visualization App

This project visualizes a dataset of user profiles in a 3D interactive space, functioning as a modernized, data-driven take on the classic Three.js Periodic Table. It dynamically pulls data from a Google Sheet and requires Google OAuth for access.

## Features & Implementation Details

* **Google Authentication:** Implemented Google Identity Services for a secure, one-tap login flow on the landing page (`index.html`).
* **Dynamic Data Integration:** Integrated the Google Sheets API using modern ES6 `async/await` to fetch and parse live user data (`Data Template.csv`) on the fly.
* **Data Sanitization & Defensive UI:** * Built-in Regex parsing to clean currency strings (e.g., converting "$200,000" to workable floats) for accurate conditional color rendering based on Net Worth.
    * Added image fallback handlers to prevent the UI from breaking if a profile photo URL is dead.
* **Custom 3D Layout Algorithms:** * Calculated exact vector math to arrange the DOM elements into four distinct formations: a 20x10 Table, a Fibonacci Sphere, a custom Double Helix structure, and a 5x4x10 Grid.
* **Animation Engine:** Utilized `TWEEN.js` to calculate smooth interpolation when transitioning between the 3D layouts.

## Architecture & Best Practices

To keep the solution maintainable and scalable:
* **Modular Logic:** Separated network requests (`loadDataset`), DOM creation (`buildScene`), and layout mathematics (`calculateGrid`, etc.) into distinct functions. 
* **CDN Dependencies:** Utilized `unpkg` CDNs for the Three.js libraries to keep the repository lightweight and easily deployable without a complex build step.
* **Responsive:** Bound a resize event listener to automatically update the camera projection matrix and renderer size.

## How to Run

Because this app utilizes Google Identity Services and the Google Sheets API, it must be run on a local development server (like VS Code Live Server) or viewed via the live deployment URL to avoid CORS/Auth restrictions.
