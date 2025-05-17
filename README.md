# Multiview Visualisation Systems
> COMPSCI5099 Information Visualisation M - 2024-25

This repository contains the coursework submission for the Information Visualisation course. It involves using a publicly available dataset to build three different multi-view visualisation systems that can perform the same four tasks, and a user evaluation based on the same.

Dataset used from [World Weather Repository (Daily Updated)](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository/data) on Kaggle. (extracted on 2024-02-22)

## Artefacts

- [Multiview Visualisation Systems](https://siddydutta.github.io/Multiview-Visualisation-Systems/)
- [Demo Video | YouTube](https://www.youtube.com/watch?v=PVWMhDoYCgY)

[![Demo Video | YouTube](https://img.youtube.com/vi/PVWMhDoYCgY/0.jpg)](https://www.youtube.com/watch?v=PVWMhDoYCgY)
- [Project Report](/Group%207%20-%20Multiview%20Visualisation%20-%20Report.pdf)

## Development
### Conda Environment
```
conda env create -f environment.yml
conda activate infoviz
jupyter notebook
```

### Data Processing
The `Data Processing.ipynb` notebook involves all the pre processing of the raw data including extracting the file, dropping miscellaneous columns, extrapolating columns and saving the cleaned data as `EU-UK-Weather-Data.csv`.

### Use Data Directly
```
wget https://raw.githubusercontent.com/siddydutta/Multiview-Visualisation-Systems/refs/heads/main/EU-UK-Weather-Data.csv
```

## Team Members
1. Ankit Das - [:email: 2980596D](mailto:2980596D@student.gla.ac.uk)
2. Bhavisha Jatin Dholakia - [:email: 3050100D](mailto:3050100D@student.gla.ac.uk)
3. Dishani Sarkar - [:email: 2979085S](mailto:2979085S@student.gla.ac.uk)
4. Rithik Sah - [:email: 2980356S](mailto:2980356S@student.gla.ac.uk)
5. Siddhartha Pratim Dutta - [:email: 2897074D](mailto:2897074D@student.gla.ac.uk)


## Assessment Feedback (27/30)
### A. Design and implementation (20 marks overall)
- Data (2/2). Good clear description of the original and derived data, using Munzner's taxonomy.
- Tasks (2/2). The tasks chosen here show a good variety across Munzner's task taxonomy, and make sense given the context.
Core systems (4/4). System A, initially at least, has too many colours mapped to cities. Location might distinguish them on the map, but not on the line charts. I suppose you have to just filter quickly. The demo didn't show it, but it seems that it has brushing on the map linked to the two line charts. I'm not sure that selection on the legend counts as brushing, and it doesn't seem like bidirectional (as other controls don't change the legend, I think, e.g. I don't think Valletta ever gets snow). B has brushing on the timeline, linked to the other lat/lon chart. Interesting setup, with a small region around a city's location having the data for that city laid out in a rectangular area. And -- hooray! -- B shows generalised selection, moving up a time hierarchy from a selected city. It seems to have bidirectional linking. Also good to see that C has multi-way linkage between its three charts. Good work here -- very few groups did more than one-way linking, and fewer did GS.
- Generalised selection (4/4). See above. I saw in labs that the most feasible way to do this was via external buttons or toggles, rather than some interaction in the middle of a chart (e.g. shift-click to go up)... but that's fine. The time hierarchy makes sense as a semantic structure, and the traversal policy follows from the semantics (as it should).
- Demo (yes)
- Design comparison (7/8). Good discussion here, although it would have been good to consistently see the best choice argued for, as per the spec. Sometimes the text here just said what each choice was like, but didn't make such a case.
### B. Evaluation (10 marks overall)
- user evaluation comparison (6/8). Good data collection here, with a useful range of data collected. Well done for randomising the order of tasks. Apparently a good amount of qualitative data was collected, but there is almost nothing about the analysis/findings from it in this section. This seems like a gap or loss, although some of this appears in the future work section.
- future work (2/2). All pretty sensible recommendations, well grounded in the evaluation data.
 
2+2+4+4+7+6+2 = **27/30**
