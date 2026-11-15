<div align="center">

# 🌱 Agriplanner

### Your field. Your priorities. A clearer next season.

**NASA observations, farmer knowledge and visual crop rotation exploration.**

[![Live demo](https://img.shields.io/badge/OPEN_LIVE_DEMO-Agriplanner-17734F?style=for-the-badge)](https://www.agriplanner.space/)
[![Platform video](https://img.shields.io/badge/WATCH-PLATFORM_DEMO-183A52?style=for-the-badge)](https://youtu.be/bGQB_GMVtp4)

**WIFA Robotics · NASA Space Apps Challenge 2026 · Milano**

*Field Shift: Adapting Farms with NASA Data*

</div>

---

## 🎬 See Agriplanner in action

[![Watch the Agriplanner platform demonstration on YouTube](https://img.youtube.com/vi/bGQB_GMVtp4/hqdefault.jpg)](https://youtu.be/bGQB_GMVtp4)

**[▶ Watch the platform demonstration on YouTube](https://youtu.be/bGQB_GMVtp4)**

Explore the working platform in our demonstration video, then try the [live application](https://www.agriplanner.space/) yourself.

A [downloadable MP4 copy](https://github.com/WIFA-Robotics/Agriplanner/blob/main/Agriplanner.mp4) is also available in this repository.

## The question behind the project

**“What should I grow next on this field?”**

A crop rotation decision connects weather, water, soil, planting windows, equipment and markets. Information is often scattered, and technical data can be difficult to turn into a useful conversation.

Agriplanner brings the farmer’s own field, current rotation, real NASA weather observations and visual comparisons into one approachable workspace.

> **Our mission:** Make Earth observation data easier to understand and useful when farmers explore their next crop rotation.

## 🧭 Mission, vision and goals

| | Our direction |
| --- | --- |
| **Mission** | Help farmers explore rotation choices using clear visuals, accessible environmental information and their own priorities. |
| **Vision** | A future where farmers can connect global observations with local knowledge and make better informed decisions about their land. |
| **Goal today** | Demonstrate a working, transparent journey from selecting a field to inspecting NASA weather and comparing rotation scenarios. |
| **Goal next** | Add verified soil information, measured vegetation observations and regional crop calendars, then validate the approach with farmers and agricultural experts. |

**The farmer stays in control.** Agriplanner supports exploration and expert discussion. It does not replace local agricultural judgment.

## ✨ From a place on the map to a conversation about the next season

| Step | Farmer action | What Agriplanner provides |
| --- | --- | --- |
| **1 · Find your land** | Search for a place or enter coordinates. | An interactive satellite map. |
| **2 · Draw your field** | Trace the boundary with a pencil or tap its corners. | Approximate area, boundary checks and a saved field location. |
| **3 · Tell your crop story** | Select the current crop sequence. | Illustrated crop cards and a clear comparison baseline. |
| **4 · Explore alternatives** | Compare the current rotation with two alternatives. | Adjustable priorities, explanations and tradeoffs. |
| **5 · Inspect the conditions** | Open Insights and choose a date range. | Real NASA POWER observations, charts and source evidence. |

The bottom navigation keeps the main tasks close: **Map · Rotations · Explore · Insights**.

## 🛰️ Real NASA data with evidence you can inspect

Our current integration uses the public **NASA POWER Daily API** for the saved field’s location.

| Observation | Purpose in the MVP |
| --- | --- |
| Air temperature, minimum and maximum | Explore historical temperature conditions. |
| Precipitation | Inspect daily rainfall and totals over available observations. |
| Relative humidity | Add atmospheric context. |
| Solar radiation and wind | Provide additional weather information when available. |

**No API key is required for the endpoint we use.**

The profile and Insights views expose the requested coordinates, exact API URL, request timing, connection status and latest available weather date. Users can inspect daily values and download the original JSON response.

The default view shows the latest seven available complete weather dates from a recent request. Other date ranges are available. Missing values remain missing, and cached responses are labeled.

**POWER is regional gridded historical data. It is not a sensor installed on the field or a weather forecast.**

## 🌾 Three strategies, one field

Agriplanner compares:

1. **The current rotation:** the farmer’s saved sequence.
2. **Alternative A:** an illustrative sequence introducing a legume.
3. **Alternative B:** an illustrative approach exploring longer seasonal soil cover.

Farmers adjust the relative importance of **water compatibility, soil cover and crop family diversity**. Each scenario includes an explanation and points that need local review.

A cover crop also uses water. Planting windows, termination timing, disease history, equipment and markets can change whether an idea is practical.

## 🔎 What is real, and what is illustrative?

Transparency is part of the product.

| Component | Current status |
| --- | --- |
| NASA POWER weather | **Real API observations** for the saved field centre. |
| Satellite basemap | **Real Esri World Imagery**, with acquisition dates varying by location. |
| Ocean and lake exclusion | **Mapped Natural Earth polygons**, with generalized geographic detail. |
| Current crop rotation | **Farmer input**, retained as the comparison baseline. |
| Crop family diversity | **A simple calculation** from known crop families. |
| Water compatibility and soil cover indicators | **Prototype assumptions**, not measured outcomes or validated predictions. |
| Vegetation, thermal, soil moisture and rainfall map overlays | **Illustrative layers**, not analytical satellite raster products. |
| Country crop collections | **Examples**, not annual production rankings or field suitability results. |
| Botanical artwork and optional 3D crops | **Illustrations**, not observations of the selected field. |

**NASA weather currently provides context alongside the comparisons. It does not calculate or validate the rotation scores.** We do not claim measured water savings, improved soil health, yield forecasts or profit estimates.

## 🎯 A quick route for the jury

**Try the live MVP in three minutes:**

* **First minute:** find a location, draw a field on land and choose the current rotation.
* **Second minute:** compare the baseline with two alternatives and move a priority slider.
* **Third minute:** open Insights, inspect real NASA observation dates and show the connection evidence in the profile.

Optional: draw an offshore boundary. A detected overlap with mapped water turns the boundary **red**, shows **“Land unavailable”** and blocks saving. The dataset may miss small ponds, narrow rivers and shoreline details.

## 💬 Questions we want to answer clearly

<details>
<summary><strong>Who is Agriplanner for?</strong></summary>

Farmers and agricultural advisers who want an understandable visual starting point for discussing crop rotations, without needing advanced geospatial skills.

</details>

<details>
<summary><strong>Why use NASA data?</strong></summary>

NASA POWER makes environmental observations accessible through a public API. Agriplanner makes that connection visible and inspectable rather than hiding the source behind an unexplained score.

</details>

<details>
<summary><strong>Are the recommendations ready for real farming decisions?</strong></summary>

The MVP supports exploration. The scenario scores are illustrative and need agronomic validation. Final decisions require local soil information, verified crop requirements, planting calendars and farmer or adviser review.

</details>

<details>
<summary><strong>Does the platform use artificial intelligence?</strong></summary>

The current prototype uses transparent comparison rules. It does not contain a validated AI recommendation model. Future modeling should be explainable, evidence based and tested against expert review.

</details>

<details>
<summary><strong>What happens when NASA data is missing or the connection fails?</strong></summary>

Missing observations remain unavailable. A previous response may be shown only as a labeled cache for the same query. The application does not substitute invented weather values.

</details>

<details>
<summary><strong>Can I select a location other than Pavia?</strong></summary>

Yes. Search for another location, draw and save a field there. The saved place follows the field across the map, field details, profile and Insights. NASA requests use that field’s coordinates.

</details>

<details>
<summary><strong>Are my fields synchronized between devices?</strong></summary>

No. The current MVP saves field settings and rotation information in browser local storage. There is no cloud field account or multiuser field synchronization.

</details>

<details>
<summary><strong>Are Landsat and MODIS/VIIRS already connected?</strong></summary>

Not in this MVP. The current live NASA weather connection is POWER. Measured vegetation observations are part of the next development stage; illustrative overlays must not be presented as downloaded measurements.

</details>

<details>
<summary><strong>How would we measure success?</strong></summary>

First, test whether farmers can complete the workflow and understand the comparisons. Then evaluate future recommendation quality with agricultural experts. Claims about long term soil, water or economic benefits require field evidence.

</details>

## 🚀 Where we go next

| Priority | Next step | Why it matters |
| --- | --- | --- |
| **User testing** | Observe farmers and advisers using the workflow. | Find confusing steps and test understanding. |
| **Local context** | Add suitable soil data, crop requirements and planting calendars. | Connect global observations to practical constraints. |
| **Measured vegetation** | Evaluate appropriate Landsat and MODIS/VIIRS products. | Replace illustrative vegetation layers with quality checked observations. |
| **Model validation** | Develop and test explainable regional comparison rules. | Move from demonstration indicators toward defensible decision support. |
| **Field pilots** | Review suggestions across real growing seasons. | Measure usefulness and investigate outcomes responsibly. |

## 👥 The team

**WIFA Robotics**

| Team member | GitHub |
| --- | --- |
| **William Farokhzad** | [@williamfarokhzad](https://github.com/williamfarokhzad) |
| **Anna Piccinin** | [@annapiccinin](https://github.com/annapiccinin) |

[Space Apps team page](https://www.spaceappschallenge.org/2026/find-a-team/wifa-robotics/) · [Challenge description](https://www.spaceappschallenge.org/2026/challenges/adapting-farms-with-nasa-data/)

## Sources and acknowledgments

* [NASA POWER documentation](https://power.larc.nasa.gov/docs/) and [API tutorial](https://power.larc.nasa.gov/docs/tutorials/api-getting-started/)
* [Esri World Imagery](https://www.esri.com/en-us/arcgis/products/arcgis-data-maps/satellite-imagery)
* [Natural Earth](https://www.naturalearthdata.com/) ocean and lake data
* [Leaflet](https://leafletjs.com/) and [Three.js](https://threejs.org/)
* [OpenStreetMap Nominatim](https://nominatim.org/) place search
* [FAOSTAT](https://www.fao.org/faostat/en/#data/QCL), linked for further exploration of official agricultural statistics

Crop artwork is AI-generated illustration. The optional crop models are procedural. Agriplanner is an independent hackathon project; participation does not imply NASA endorsement.

---

<div align="center">

**Explore the field. Understand the context. Compare the possibilities.**

[**Try Agriplanner →**](https://www.agriplanner.space/) · [**Watch the demonstration →**](https://youtu.be/bGQB_GMVtp4)

</div>
