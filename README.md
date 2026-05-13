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

A stacked bar plot showing mean percent cover of the 3–5 dominant salt marsh plant species across survey years. Year would be on the x-axis, mean percent cover would be on the y-axis, and fill color would represent plant species. 

This figure is relevant because it directly shows which species contribute the most cover in salt marsh habitat through time. It will help us identify whether salt marsh vegetation is consistently characterized by the same dominant species or whether dominant species shift across years.

**Potential figure 2:**

A stacked bar plot showing the relative contribution of native and non-native vegetation cover in salt marsh habitat across survey years. Year would be on the x-axis, percent cover would be on the y-axis, and fill color would represent native or non-native cover category.

This figure is relevant because it shows whether salt marsh habitat is mostly characterized by native vegetation, non-native vegetation, or a changing mixture of both through time. This helps connect species composition to broader questions about restoration, habitat condition, and vegetation community change at NCOS.


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

[delete this line and enter your own text here]

**Elective timeline (what you will have completed each week):**

Week 7: enter your own text here

Week 8 (timeline check in): enter your own text here

Week 9: enter your own text here

Week 10: enter your own text here

Finals week: enter your own text here







