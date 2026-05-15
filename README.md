
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

**Potential figure 3:**

A horizontal bar chart showing mean percent cover for each plant species recorded in salt marsh habitat at NCOS, averaged across all survey years and ranked from highest to lowest. Species will be on the y-axis, mean percent cover on the x-axis, and bars will be colored by cover category (native or non-native) to visually reinforce the native/non-native distinction alongside species identity. Only plant cover categories will be included; bare ground, thatch, and other non-plant categories will be excluded prior to summarizing.

This figure is relevant because it provides a clear, static summary of which species contribute the most cover to salt marsh habitat at NCOS overall, directly answering our first research question.

**Potential figure 4:**

A line chart showing total mean vegetation cover (native + non-native combined) in salt marsh habitat at NCOS across survey years. Year will be on the x-axis, total mean percent cover on the y-axis, and points will be connected by a line to emphasize the temporal trend.

This figure is relevant because it provides context for interpreting figures 1 and 2. Proportional shifts in native vs. non-native cover (figure 2) are better understood when paired with information about whether total vegetation cover is also changing. This figure also helps identify years with unusually high or low total cover that might reflect disturbance, drought, or survey timing differences.

## Data cleaning/wrangling/summarizing plan

Because our project focuses on salt marsh vegetation, we will filter veg.csv to include only records from salt marsh habitat. We will also focus on late summer or early fall surveys by filtering to August and September using the date column, when vegetation cover is expected to be highest and most comparable across years. Before summarizing, we will use complete() to fill implicit NAs with 0, so that species absent from a quadrat in a given year are treated as 0 percent cover rather than missing. We will then join with vp_veg_metadata.csv by year_pool to obtain the number of quadrats (num_quad) surveyed per transect per year, which we will use to calculate mean percent cover as total cover divided by number of quadrats.

For the dominant species figure (figure 1), we will filter to plant cover categories, including native and non-native cover, and remove non-plant categories such as bare ground, thatch, and other cover. We will group the data by year and species to calculate mean percent cover for each species in salt marsh habitat. To keep the figure readable, we will identify the 3–5 dominant species based on mean percent cover averaged across all years, then filter to those species for visualization. Remaining species will be grouped into an "other" category or excluded, and we will document the cutoff clearly in the figure caption.

For the native/non-native figure (figure 2), we will apply the same filtering and implicit NA treatment, then group the data by year and cover category and calculate mean percent cover for native and non-native vegetation separately. We will then calculate proportions within each year using mutate(prop = cover / sum(cover)) so that each bar sums to 1, making it easier to compare the relative contribution of native and non-native vegetation through time even if total sampling effort varies across years.

For the species rank plot (figure 3), we will use the same cleaned and filtered data frame as figure 1. Rather than grouping by year, we will group by species and cover category and calculate mean percent cover averaged across all survey years. We will then arrange species in descending order by mean percent cover using arrange(desc(mean_pc)) to produce a ranked visualization. The cover category column will be retained for color mapping so that native and non-native species are visually distinguished in the plot. This figure will inform and transparently justify the dominant species cutoff applied in figure 1.

For the total vegetation cover figure (figure 4), we will use the same cleaned data frame with implicit NAs filled as 0, filtering to native and non-native plant cover categories only. We will group by year and quadrat, summing cover across all plant species within each quadrat to get total vegetation cover per quadrat per year. We will then summarize across quadrats within each year to calculate mean total cover and standard error, where standard error is calculated as sd(cover) / sqrt(n()). The resulting mean and SE values will be used to plot a line with a shaded ribbon representing ± 1 standard error, providing context for whether total vegetation cover in the salt marsh has changed over the survey period alongside the compositional trends shown in figures 1 and 2.

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







