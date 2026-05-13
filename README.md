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

Erick Morales Oyola, Macey Hartmann, Madison Muhle

## Topic information and question

**Topic:**  

Vegetation: What species characterize major habitats? 

**Question(s):**  

- What plant species characterize the major habitat types at NCOS?
- Which species are most strongly associated with each habitat type?
- Do native and non-native species differ in how they contribute to habitat identity? 

**Response variable(s)**

- Plant species
- Percent cover by species
- Species richness, or number of unique species
- Native/non-native cover category

## Datasets

**Datasets used:**

- veg.csv: vegetation survey data with species identities, percent cover, cover category, habitat type, trasnsect, site, and year. This will be our main dataset for identifying which plant species characterize each major habitat type at NCOS.
- vp_veg_metadata.csv: metadata for vegetation transects, including year, transect name, and number of quadrats. This might help us account for the sampling effort across the different transects.

## Figures

**Potential figure 1:**

[delete this line and enter your figure here]
A stacked bar plot showing mean percent cover of the most common plant species within each major habitat type. Habitat would be on the X-axis, mean percent cover would be on the Y-axis, and fill color would represent plant species. 

This figure would be relevant since it would show which species contribute the most vegetation cover in each habitat, and help us identify the most characteristic plant species for each major habitat type. 

**Potential figure 2:**

[delete this line and enter your figure here; if you don't have one, delete the entire section]
A faceted bar plot showing the top species by mean percent cover within each habitat type. Each panel would represent one habitat instead, species would be on the Y-axis, and mean percent cover would be on the X-axis. 

This figure would be relevant because it would make species-habitat patterns much easier to read than one large, crowded bar plot. Separating habitats into panels would allow us to more clearly compare which species dominate each habitat without making the figure too complicated. 

**Potential figure 3:**

[delete this line and enter your figure here; if you don't have one, delete the entire section]
A boxplot/jitter plot comparing percent cover of native and non-native vegetation across major habitat types. 

This figure would be relevant because it would show whether different habitats are characterized by native vegetation, non-native vvegetation, or a mix of both. This would help us relate species composition to broader ecological patterns and restoration efforts at NCOS.

**Potential figure 4**

[delete this line and enter your figure here; if you don't have one, delete the entire section]
A bar plot showing species richness, or the number of unique plant species, within each major habitat type. Habitat type would be on the X-axis, and species richness would be on the Y-axis. 

This figure would be relevant because it would help compare plant diversity across habitats. Even if one habitat is dominated by a few species, another habitat could support more unique species overall, so richness would give us another way to describe community composition of habitats at NCOS. 

## Data cleaning/wrangling/summarizing plan

We will start by reading in 'veg.csv' and 'vp_veg_metadata.csv' and then cleaning column names so the datasets are easier to work with in R Studio. Our main analysis will use 'veg.csv,' focusing on habitat type, plant species, percent cover, cover category, transect, site, and year. We will filter out non-species cover categories if we decide to focus on only plant species rather than including bare ground, thatch, and other non-plant cover types. We will group the vegetation data by habitat and species to calculate mean percent cover, total percent cover, and frequency for each species within each habitat. 

To keep our figures simple and readable, we will limit some visualizations to the most common or highest-cover species within each habitat. For native and non-native comparison, we will group the data by habitat and cover category, then summarize the percent cover for native and non-native vegetation. If the sampling effort is significantly different across transects or years, we might also use 'vp_veg_metadata.csv' to check the number of quadrats. 

Overall, data cleaning/wrangling will focus on summarizing vegetation composition in a way that makes habitat-level patterns clear and underestandable. 
## Project roles

**Natural history/framing director:**

[delete this line and enter your own text here]

**Stats and visualization director**

Macey Hartmann

**GitHub/code director**

Erick Morales Oyola


## Elective (not required for all groups or group members)

**Group members completing elective:**

[delete this line and enter your own text here]

**Elective idea:**

[delete this line and enter your own text here]

**Elective timeline (what you will have completed each week):**

Week 7: enter your own text here

Week 8 (timeline check in): enter your own text here

Week 9: enter your own text here

Week 10: enter your own text here

Finals week: enter your own text here







