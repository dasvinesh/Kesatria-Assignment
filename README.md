# Kesatria-Assignment
Assignment for Kesatria

Project Overview
-This is my submission for the 3D data visualization assignment for the Software Developer role.
-It is a modernized, data-driven web application built on top of the classic Three.js CSS3D Periodic Table example.
-The app dynamically fetches a dataset of user profiles from a Google Sheet (imported from the provided CSV) and renders them in an interactive 3D space.

Authentication and Architecture
-The landing page (index.html) uses Google Identity Services to handle a secure, one-tap OAuth login flow.
-The main visualization (source.html) uses modern async/await JavaScript to fetch and parse the live data via the Google Sheets API.
-I utilized unpkg CDNs for all Three.js dependencies to keep the project lightweight and easily deployable without complex build steps.

Data Handling and Custom Logic
-I replaced the original array logic with dynamic DOM creation and implemented defensive programming to handle the data safely.
-The code uses regex to sanitize currency strings into usable floats to evaluate the Net Worth column and apply the correct background colors to the cards.
-I added image fallback handlers so the UI does not break if a profile photo URL is invalid.
-I retained the original main.css file to keep the core aesthetic but updated the HTML generation to cleanly map the new data fields like Country, Age, and Interest.

3D Layout Calculations
-The vector math was recalculated to arrange the DOM elements into a 20x10 Table.
-It includes a Fibonacci Sphere.
-I mapped coordinates for a custom Double Helix structure.
-It includes a 5x4x10 Grid arrangement.
-All smooth transitions between these geometric states are handled by TWEEN.js.

Running the Project

-Because this application relies on Google Identity Services and the Google Sheets API, it must be served over a local development server (like VS Code Live Server) to avoid CORS and authentication errors.
-It can also be viewed directly via the live deployment URL provided in my submission.
