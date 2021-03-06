# Barch: corpus of bar chart summaries in English :bar_chart:

This repository contains the Barch corpus of human-written bar chart summaries. 

We designed bar charts for a selection of 18 different topics. Each chart is associated with one of four main messages which are signaled in the chart title. For each chart we collected around 20 summaries via crowdsourcing by asking participants to describe the chart as if they were presenting it to an audience. The text in the summaries is labeled (aligned) with the chart data for basic information (axis labels, bar names and heights) as well as analytical information as inferred by humans (relations between bars, height approximations).


| no. topic | no. chart  | no. summary | no. token | no. sentence |
| :--------:|:----------:| :----------:|:---------:| :-----------:|
|         18|          47|        1,063|     57,420|        3,356 |



### Annotation guidelines
The repository also provides the annotation guidelines for aligning summary and chart data.

### NLG
We used the data to train several natural language generation models, namely a baseline LSTM encoder-decoder with attention, Chart2Text ([Obeid and Hoque 2020](https://aclanthology.org/2020.inlg-1.20/)) and KGPT ([Chen et al. 2021](https://aclanthology.org/2020.emnlp-main.697/)).


### Project structure

```
.
├── data                                      # Charts and summaries 
│   ├── chart_summaries.xml                   # Annotated summaries arranged by topic and chart
│   ├── charts                                # Chart images and summaries by topic
│   │   ├── 01
│   │   └── ...
│   └── chartID2plotinto.json                 # Plotting information for each chart
├── splits_nlg                                # Data splits for NLG experiments
│   ├── c2t                                   # Data for the Chart2Text model
│   ├── kgpt                                  # Data for the KGPT model
│   ├── lstm                                  # Data for the LSTM model
│   └── splits_combinations_ids.json        # Summary IDs by data splits
├── Annotation_Guidelines_2.0.pdf           # Annotation guidelines for labeling summaries
└── README.md
```

### Citing
The dataset is described in a paper that was submitted to review for the LREC 2022 conference.


