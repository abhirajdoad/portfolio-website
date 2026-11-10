# Abhiraj Doad · Data analysis portfolio

Live site: _added after the first deployment_

A single-page portfolio of data analysis projects, each framed as a question answered with data. The site is plain HTML, CSS and JavaScript with no build step or dependencies. Charts are drawn as inline SVG from small summary tables embedded in the page.

## Projects

| # | Project | Repository |
|---|---|---|
| 01 | Vancouver 3-1-1 | [vancouver-sql-analytics](https://github.com/abhirajdoad/vancouver-sql-analytics) |
| 02 | Instacart Grocery Baskets | [instacart-shopping-analysis](https://github.com/abhirajdoad/instacart-shopping-analysis) |
| 03 | The World Cup Effect | [ea-fc-world-cup-analytics](https://github.com/abhirajdoad/ea-fc-world-cup-analytics) |
| 04 | BC Watershed Monitoring | [bc-watershed-gis](https://github.com/abhirajdoad/bc-watershed-gis) |
| 05 | BC Water Quality | [water-quality-analysis](https://github.com/abhirajdoad/water-quality-analysis) |

## Structure

```
index.html     the whole site: styles, markup, chart data and scripts
img/           folder previews and the About photo
favicon.svg
```

## Adding a project

In `index.html`:

1. Add an entry to the `P` array (question, chart title, findings source, limitations, method, tags, repository).
2. Add its takeaways and "Behind the analysis" note to `EXTRA`, keyed by the project's `k`.
3. Add a chart function to `CH` and a small version to `MINI` with the same key, and put any chart data on `DATA`.
4. Add a folder entry to `F` for the "Explore the code" gallery.

Navigation numbers, homepage cards, keyboard shortcuts and section links are generated from `P`, so the order of `P` is the order on the page.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deployment

Deployed on Vercel as a static site. Every push to `main` triggers a new production deployment.

## Data

Charts use summary figures from each project's repository. Source data: City of Vancouver Open Data, Government of BC (BC Freshwater Atlas, hydrometric stations, Environmental Monitoring System), the Instacart Online Grocery Shopping Dataset 2017 (non-commercial use), and SteamDB player counts (summary figures only; raw data is not republished). See each project's repository for full sources and licences.
