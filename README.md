# Advanced Cloud & Weather Simulator

This is a feature-rich, interactive meteorological simulator built with HTML, CSS, and vanilla JavaScript. It renders photo-realistic, dynamic skies, complete with various cloud types, atmospheric optics, and a procedural weather system. It can simulate weather patterns for different global locations and seasons, model the progression of weather fronts, or fetch and visualize live, real-time weather data for any location.

## Features

* **Photo-Realistic Rendering:** Utilizes a multi-layered fractal noise system and a dynamic lighting model to create volumetric, detailed clouds.
* **Dynamic Time of Day:** A slider allows you to control the sun's position, realistically changing the color of the sky, clouds, and ambient light to simulate sunrise, noon, sunset, and night.
* **Three Simulation Modes:**
    * **Location Simulation:** Select from a list of global cities and a season to generate a representative, looping weather pattern.
    * **Weather Front:** Observe the full life-cycle of various meteorological fronts, from the initial high clouds to storms and eventual clearing.
    * **Live Weather:** Fetches and visualizes real-time weather data from a live API for any location in the world.
* **Advanced Atmospheric Optics:**
    * **Crepuscular Rays:** Beautiful "sunbeams" that fan out from behind clouds when the sun is low.
    * **Halos & Sun Dogs:** Scientifically-accurate 22° halos and parhelia (sun dogs) appear when thin, high-altitude cirrostratus clouds are present.
* **Diverse Weather Patterns:** Includes a wide variety of presets for locations (e.g., London, Tokyo, Cape Town) and weather fronts (e.g., Cold Front, Warm Front, Monsoon).
* **Interactive UI:** A collapsible control panel allows for easy adjustment of all parameters and a clean, full-screen viewing experience.

## How to Use

1.  **Select a Simulation Mode:**
    * **Location Simulation:** Choose a city and a season from the dropdowns. The simulation will automatically start and loop through a typical weather pattern for that selection.
    * **Weather Front:** Choose a front type (e.g., "Classic Cold Front") to see its progression over time.
    * **Live Weather:** Enter a location and click "Get Current Weather". The simulator will display the current conditions.

2.  **Adjust Controls:**
    * **Weather Progression Speed:** In "Location" or "Front" mode, this slider acts as a fast-forward or slow-motion control for the weather changes.
    * **Wind Speed:** Manually sets the base wind speed, affecting how fast the clouds drift. In "Live" mode, this is set automatically.
    * **Time of Day:** Controls the position of the sun and all associated lighting effects. In "Live" mode, this is set automatically.
    * **Minimize/Maximize:** Click the `-`/`+` button to collapse or expand the control panel.

### Live Weather API Setup

The "Live Weather" mode requires a free API key from [Visual Crossing](https://www.visualcrossing.com/weather-api).

1.  Sign up for a free account on their website.
2.  Find your API key on your account page.
3.  Open the `index.html` (or the script block) and replace the placeholder value in the `API_KEY` constant with your actual key:

    ```javascript
    const API_KEY = 'YOUR_API_KEY_HERE'; // Replace with your key
    ```

## Technology Stack

* **HTML5/CSS3/JavaScript:** The core of the project.
* **Tailwind CSS:** For modern, utility-first styling of the UI.
* **Simplex Noise:** A fast, high-quality procedural noise algorithm used for generating the base cloud shapes and textures.
* **Visual Crossing Weather API:** Used to fetch real-time weather data.
