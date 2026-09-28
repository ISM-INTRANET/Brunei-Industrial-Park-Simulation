# Brunei Industrial Park Sandbox Simulator

A lightweight, local planning prototype. The entire simulator is in [index.html](index.html); it needs no build step, account, server, package install, or network connection.

## Try it locally

1. Download or clone this folder.
2. Open index.html in a current desktop or mobile browser.
3. Choose sectors, land, the brownfield/greenfield split, zoning, utilities, budget, and shared services.
4. Select **Generate Park** to create a layout, then **Run Simulation** to refresh the findings. **Randomize** creates a new scenario; **Reset** restores the balanced starting scenario.

### Edit the park

- The park boundary grows or shrinks with land size. Select **Fit park** to see the whole site; use the zoom buttons or mouse wheel for detail.
- Click a plot to see its sector, tenants, area, and location. Drag the plot to move it; drag the round corner handle to resize it. Drag open land to pan.
- For keyboard control, focus a plot and use the arrow keys to move it or Shift + arrow keys to resize it.
- **Run Simulation** keeps your edits. **Generate Park**, **Randomize**, and **Reset** create fresh plot layouts.

Red plot outlines flag overlaps, main-road crossings, or plots outside the site. Assigned plot area feeds into occupancy and jobs. The map is conceptual, not a surveyed plan. All data stays in the browser tab.

## Put it on GitHub Pages

1. Create a GitHub repository and upload the contents of this folder to its root (index.html and README.md).
2. In the repository, open **Settings → Pages**.
3. Choose **Deploy from a branch**, select your main branch and **/(root)**, then save.
4. Open the Pages URL shown by GitHub after deployment.

You can also keep this folder in a larger repository and select /docs for Pages after copying index.html there.
See [GitHub's publishing-source guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) if your repository uses a different branch.

## What the model does

Tenants are split evenly among selected sectors. Fixed illustrative factors estimate each sector's land, power, water, wastewater, road trips, fibre, and direct jobs. The engine compares demand with installed capacity, editable plot area, developable land, zoning, park services, and an approximate infrastructure budget. The tightest constraint reduces the jobs estimate. It flags shortages, congestion, treatment overload, zoning conflicts, undersized or invalid plots, missing services, low utilization, and capacity built far above demand.

Brownfield refers to previously developed land; greenfield refers to previously undeveloped land. The two shares sum to total park land and are separate from the planned green-area percentage. The brownfield cost allowance is illustrative; it does not imply contamination or replace a site assessment. For general planning terminology, see the [UK government's brownfield definition](https://www.gov.uk/guidance/brownfield-land-registers).

The **Contribution to Brunei** panel is explicitly non-official. Its payroll proxy assumes BND 32,000 per modelled direct job per year. These assumptions are for scenario exploration only; they are not measured Brunei averages, engineering design criteria, an environmental approval, or an official economic forecast.
