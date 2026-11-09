# Atlas - Country Explorer (Task 3: API Integration)

A responsive frontend application that fetches live country information from the public REST Countries API.

## Features
- Fetches country data from `https://restcountries.com/v3.1/all`
- Loading skeletons while data is being fetched
- Error state with retry action if the API or network is unavailable
- Search countries by common name or capital
- Filter countries by region
- Sort by country name or population
- Country details modal with capital, region, population, area, languages, and currencies
- Favorite countries saved in browser localStorage
- Responsive layout for mobile, tablet, and desktop
- Accessible labels, keyboard shortcut `/` to focus search, Escape to close modal, and reduced-motion support

## Run locally
Open `index.html` in a modern browser with an internet connection. The application uses the browser Fetch API and does not require a build step or API key.

## API
This project uses the public REST Countries API:
`https://restcountries.com/v3.1/all?fields=name,flags,cca3,capital,region,population,area,languages,currencies,subregion,maps,car`

The API request runs in the browser. An internet connection is required to load live country data.

## GitHub Pages deployment
1. Create a public GitHub repository, for example `task3-api-integration-country-explorer`.
2. Upload `index.html`, `style.css`, `script.js`, and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the app.

## Implementation notes
- `fetchCountries()` handles the API request, loading state, HTTP errors, and retry.
- `applyFilters()` handles search, region filtering, favorites, sorting, and pagination.
- Favorites are stored locally under `atlas-country-favorites-v1`.
- The country data is live API content and may change over time.
