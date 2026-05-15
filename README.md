
# Group project proposal

**Spring 2026**

Directions:

- Use your work plan from class to fill in the information below.
- Practice pulling, making changes, staging/committing/pulling/pushing to the same repo.
- **Communicate about who is doing what throughout the entire process.**

What you will submit on Friday the 15th:

- proposal: a link to your forked repository with the completed proposal in the README
- work plan: your paper plan that you completed in class on Monday the 4th

Use your project proposal to:

- refer back to the original plan while you are working
- keep track of high-level changes in structure (e.g. role switching, elective modifications)

Note:

- your project proposal is subject to change after you learn more about your datasets and what is possible - allow yourselves the flexibility to make adjustments as needed
- the more detail you can provide in your proposal, the more thorough your feedback will be

## Group members

Erick Morales Oyola and Macey Hartmann

## Topic information and question

**Topic:**  

Vegetation: What species characterize salt marsh habitats at NCOS? 

**Question(s):**  

- Which dominant plant species characterize salt marsh habitat at NCOS?
- How has the mean percent cover of the dominant salt marsh species changed across survey years? 
- How has the relative contribution of native and non-native vegetation changed across survey years? 

**Response variable(s)**

- Plant species within salt marsh habitat
- Percent cover by species
- Native/non-native cover category

## Datasets

**Datasets used:**

- veg.csv: vegetation survey data with species identities, percent cover, cover category, habitat type, transect, site, and year. This will be our main dataset for identifying which plant species characterize each major habitat type at NCOS.
- vp_veg_metadata.csv: metadata for vegetation transects, including year, transect name, and number of quadrats. This might help us account for the sampling effort across the different transects.

## Figures

**Potential figure 1:**

A stacked bar plot showing mean percent cover of the 3–5 dominant salt marsh plant species across survey years. Year will be on the x-axis, mean percent cover on the y-axis, and fill color will represent plant species. To identify the dominant species, we will calculate mean percent cover for each species across all years and select the top 3–5 contributors. Remaining species will either be excluded or grouped into an "other" category to keep the figure readable. Each bar will represent the summed mean percent cover of the dominant species in a given survey year, allowing us to compare both the absolute cover of individual species and overall vegetation cover through time.

This figure is relevant because it addresses which plant species characterize salt marsh habitat at NCOS and whether that composition has changed across survey years. By visualizing dominant species cover through time, we can identify whether the salt marsh is consistently dominated by the same species or whether shifts in community composition have occurred. These shifts may reflect restoration progress, disturbance, or interannual variability in conditions at NCOS.

**Potential figure 2:**

A proportional stacked bar plot showing the relative contribution of native and non-native vegetation cover in salt marsh habitat across survey years. Year will be on the x-axis, proportion of total vegetation cover on the y-axis (scaled 0 to 1), and fill color will represent native or non-native cover category. Before summarizing, we will filter to only plant cover categories (NATIVE COVER and NON-NATIVE COVER) and exclude non-plant categories such as bare ground, thatch, and other cover. We will then group by year and cover category to calculate total or mean percent cover, and convert to proportions so each bar sums to 1.

This figure is relevant because it addresses how the relative contribution of native and non-native vegetation has changed across survey years at NCOS. By expressing cover as proportions rather than raw values, we can make fair comparisons across years even if total sampling effort or total vegetation cover varies. A shift toward greater native dominance over time may suggest restoration progress.

## Data cleaning/wrangling/summarizing plan

Because our project focuses on salt marsh vegetation, we will filter `veg.csv` to include only records from salt marsh habitat. We will also focus on late summer or early fall surveys, when vegetation cover is expected to be highest and most comparable across years.

For the dominant species figure, we will filter to plant cover categories, including native and non-native cover, and remove non-plant categories such as bare ground, thatch, and other cover. We will group the data by year and species to calculate mean percent cover for each species in salt marsh habitat. To keep the figure readable, we will identify the 3–5 dominant species based on total or mean percent cover across all years, then visualize those species across survey years.

For the native/non-native figure, we will group the data by year and cover category, then summarize percent cover for native and non-native vegetation. We will use a stacked proportional bar plot so each year adds up to 1, making it easier to compare the relative contribution of native and non-native vegetation through time.

## Project roles

**Natural history/framing director:**

Erick Morales Oyola and Macey Hartmann

**Stats and visualization director**

Macey Hartmann

**GitHub/code director**

Erick Morales Oyola


## Elective (not required for all groups or group members)

**Group members completing elective:**

Erick Morales Oyola and Macey Hartmann

**Elective idea:**

For our advanced elective, we will create an educational magazine about the salt marsh plants of the North Campus Open Space (NCOS). Inspired by National Geographic, the magazine will introduce readers to the dominant plant species that characterize salt marsh habitat at NCOS. The magazine will include species spotlight pages profiling the dominant salt marsh plants with illustrated profiles, fun facts, and native/non-native status; a "Meet the Marsh" illustrated map of NCOS showing habitat zones; a data feature communicating our findings;a "Native vs. Non-Native vs. Invasive" explanation page; a salt marsh vocabulary word search; a "What Plant Are You?" personality flowchart; and a how to get involved page describing how to visit and learn more about NCOS  

**Elective timeline (what you will have completed each week):**

Week 7: Finalize magazine structure, section outline, and visual style; identify the 3–5 dominant salt marsh species to feature based on preliminary data exploration

Week 8 (timeline check in): Draft complete for species spotlight pages and "Native vs. Invader" explainer; rough sketch or mockup of the "Meet the Marsh" map and overall layout

Week 9: Complete all remaining sections (data feature, word search, flowchart, ways to help); begin design and layout in Canva or equivalent

Week 10: Finalize and polish full magazine; present elective

Finals week: Deliver completed magazine; give to Mrs. McCarter's fourth grade classroom







