## Calculus Connections Explorer

**Updated: 01/05/2026**

This repository contains the source code and data for the **Calculus Connections Explorer**, an interactive tool for exploring how computer science topics connect to core calculus ideas.

The live site is available here:  
[https://boxxelf.github.io/Calculus-Connections-Explorer/](https://boxxelf.github.io/Calculus-Connections-Explorer/)

---

## Overview

The Calculus Connections Explorer is designed to help instructors, curriculum designers, and students:

- Understand **which calculus concepts** are most relevant for specific **computer science topics and courses**.
- See how **multiple CS topics overlap** in their calculus requirements.
- Access **written rationales** that explain *why* each calculus idea matters for a given CS topic.

The interface is entirely client-side (HTML, CSS, and JavaScript) and can be hosted as a static site (for example via GitHub Pages).

---

## How to Explore CS–Calculus Connections

On the live site:

1. **Select CS topics**  
   Use the list under “CS Topics” to choose one or more CS topics or entire CS courses.

2. **Browse connected calculus ideas**  
   The middle panel shows a ranked list of calculus topics that are connected to your CS selections.  
   Darker colors indicate topics with more or stronger connections.

3. **Open details for a calculus topic**  
   Click any colored calculus pill to focus the graph on that topic and its nearby connections.

4. **Read rationales**  
   After you click a pill, the right-hand sidebar shows written explanations (“rationales”) that describe how the selected calculus idea supports the CS topics you chose.  
   These rationales are automatically filtered by your current CS selections.

5. **Full concept map (optional)**  
   Switch to the **“Full concept map”** tab in the middle panel to see the original graph-based visualization and zoom or pan around it.

---

## Project Structure (High Level)

The repository includes:

- `index.html` – Main HTML entry point for the web application.
- `style.css` – Styles and layout for the user interface.
- `app.js` – Core JavaScript logic for:
  - loading data,
  - rendering the interactive views and graph,
  - handling topic selection and filtering,
  - displaying rationales.
- `graph_data.json` – Data describing calculus topics, connections, and relationships.
- `Calculus topic labeling scheme.csv` – Labeling and metadata for calculus topics used in the visualization and lists.
- `ML_Alg_AI_CG_Rationales_081525(Rationales).csv` – Rationales connecting CS topics to calculus ideas.
- `All_Computer_Science_Topics (3).mmd` – Source file describing the CS topic map.
- `deploy.sh` and `DEPLOYMENT.md` – Helper script and notes for deploying to GitHub Pages (or similar static hosting).
- `UPDATE_NOTES1201.md` – Detailed notes about past fixes and improvements.

---

## Running the Project Locally

You can run the explorer locally as a static site:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Boxxelf/Calculus-Concept-Map-Update.git
   cd Calculus-Concept-Map-Update
   ```

2. **Serve the files with any static file server.** For example, using Python:

   ```bash
   python3 -m http.server 8000
   ```

3. **Open the app in your browser:**

   ```text
   http://localhost:8000/index.html
   ```

No backend server or database is required; all data is loaded client-side.

---

## Deployment

This project is intended to be deployed as a static site, for example via **GitHub Pages**.

A typical workflow is:

1. Build or prepare any static assets (if needed).
2. Deploy to the `gh-pages` branch or your configured Pages branch.  
   You may use the existing `deploy.sh` script or follow the steps in `DEPLOYMENT.md`.
3. Confirm that the site is available at your GitHub Pages URL, for example:  
   [https://boxxelf.github.io/Calculus-Connections-Explorer/](https://boxxelf.github.io/Calculus-Connections-Explorer/)

---

## Data Sources and Attribution

The connections between CS topics and calculus ideas, as well as the written rationales, are based on:

- A curated set of **computer science topics and courses** (see `All_Computer_Science_Topics (3).mmd`).
- A labeled hierarchy of **calculus topics** (see `Calculus topic labeling scheme.csv`).
- A set of **rationales** mapping calculus ideas to CS topics (see `ML_Alg_AI_CG_Rationales_081525(Rationales).csv`).

If you use or extend this work, please credit the **Calculus Connections Explorer** project and include a link to the live site:  
[https://boxxelf.github.io/Calculus-Connections-Explorer/](https://boxxelf.github.io/Calculus-Connections-Explorer/)

---

## Contributing

Contributions are welcome, especially in the following areas:

- Improving or refining the **topic mappings** between CS and calculus.
- Enhancing the **user interface or accessibility** of the explorer.
- Adding new **visualizations**, filters, or analytics.
- Extending or clarifying the **rationales** and documentation.

Please open an issue or submit a pull request in this repository to propose changes.

---

## License

Specify the project license here (for example, MIT, CC BY, or another open-source license).  
If no license has been chosen yet, please add one before distributing or reusing this code and data.


