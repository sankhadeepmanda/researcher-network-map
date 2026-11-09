# IIT Mandi Researcher Network

IIT Mandi Researcher Network is an interactive network visualization tool designed to map, explore, and analyze academic connections, research topic similarities, and collaboration opportunities among researchers at IIT Mandi.

This project is a browser-based web application that visualizes relationships between selected IIT Mandi researchers using topic similarity data. It allows users to explore the academic network, inspect researcher profiles, compare topics, and shortlist promising collaborators.

## Overview

The application presents a dynamic research network where each node represents a researcher and the links represent similarity based on shared research topics and academic interests. The project is built as a static HTML application and is designed to run directly in a browser without requiring a backend service.

## Key Features

- Interactive network map with zoom, pan, and label controls
- Researcher directory with search and filtering
- School-wise and topic-wise grouping views
- Similarity-based edge analysis between researchers
- Shortlist and comparison tools for selected researchers
- Local browser-based cache for faster offline access
- Export of researcher data and shortlist information

## Tech Stack

- Frontend: HTML, CSS, JavaScript
- Visualization: D3.js
- Data sources: OpenAlex author metadata and topic similarity data
- Profile metadata: IIT Mandi faculty directory information

This repository is primarily HTML-based, which matches the current language composition of the project.

## Repository Structure

```text
researcher-network-map/
├── README.md
├── iit-mandi-research-network.html     # Main interactive visualization app
├── iit_mandi_selected_50_researchers.json  # Seed researcher dataset
├── network.zip                          # Archived network dataset
└── ...                                  # Additional local assets/data used by the app
```

## Getting Started

### Prerequisites

- A modern web browser such as Chrome, Firefox, Edge, or Safari
- Python 3.x (optional, only if you want to serve the app locally)

### Run Locally

Option 1: Open the HTML file directly

```bash
open iit-mandi-research-network.html
```

Option 2: Start a local web server

```bash
cd researcher-network-map
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/iit-mandi-research-network.html
```

## How It Works

- The application loads a curated list of IIT Mandi researchers.
- It matches them to OpenAlex author records and retrieves topic information.
- Researchers are placed in a network graph based on topic similarity.
- Users can inspect details such as publications, citations, school affiliation, and research interests.
- The app emphasizes academic similarity rather than formal collaboration or co-authorship.

## Data and Methodology

- Data source: OpenAlex
- Similarity metric: Topic-based similarity across researcher profiles
- Scope: Selected IIT Mandi researchers and their academic network
- Limitation: Topic similarity does not imply direct collaboration or co-authorship

## Project Purpose

The tool is intended to help researchers, academic administrators, and students:

- understand the structure of research communities at IIT Mandi
- find related research areas and potential collaborators
- explore interdisciplinary overlaps and topic clusters

## Author

Sankhadeep Mandal

## Notes

This repository is a static web project and does not require a backend or package installation to run in the browser. It is best suited for local exploration and academic visualization use cases.
