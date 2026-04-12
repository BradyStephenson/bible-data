# BibleData

**Structured data from the Holy Bible** — turning millennia of Scripture into clean, queryable, machine-readable datasets.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

© 2021–2026 Brady Stephenson  
These datasets are also available on [data.world](https://data.world/bradys).

**How to cite this work:**

Brady Stephenson. (2026). *BibleData: Structured Datasets from the Holy Bible* (Version 1.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.19539956

---

## Why BibleData?

For thousands of years the Bible has been the most translated, most widely published, and most examined text in human history.  
Yet the information inside it has largely remained unstructured — difficult to parse, analyze, or enrich with modern tools.

BibleData addresses this need by providing carefully structured datasets drawn from Scripture.

Whether you wish to trace every descendant of Aaron, count the generations between Adam and King David, calculate the years between the Flood and Solomon’s Temple, or identify every event associated with a specific location, these datasets make such inquiries straightforward.

## Table of Contents
- [Datasets](#datasets)
- [How to Use the Data](#how-to-use-the-data)
- [Contributing](#contributing)
- [License](#license)

## Datasets

### ✅ Completed
- **The Alamo Polyglot** — A single parallel view of Scripture texts including:  
  World English Bible (WEB), King James Version (KJV), Leningrad Codex (BHS), Jewish Publication Society (JPS 1917), Codex Alexandrinus, Brenton's English Translation of Alexandrinus (BET), Samaritan Pentateuch (SP), Samaritan Pentateuch in English (SPE), Targum Onkelos, and Targum Onkelos in English (TOE).
- BibleData-Commandments — The traditionally enumerated 613 commandments given in Scripture
- BibleData-Person — Every named individual in the Bible
- BibleData-PersonLabel — Names and titles with Hebrew or Greek originals, related Strong’s numbers, and meanings
- BibleData-PersonRelationship — Family and other relationships (father, mother, son, daughter, killer, concubine, and more)
- BibleData-PersonVerse — Every person mentioned in every verse of the Bible
- BibleData-PersonVerseApostolic — Person-verse data for the New Testament (Apostolic Writings)
- BibleData-PersonVerseTanakh — Person-verse data for the Old Testament (Tanakh)
- BibleData-Reference — Every book, chapter, and verse reference
- HebrewStrongs — Strong’s Hebrew Concordance as structured data
- Hitchcock’s Bible Names Dictionary
- Naves Topical Dictionary
- Ussher’s Annals of the World

### 🚧 In Progress
- BibleData-Book — Books of the Bible, including number of chapters and verses, traditional authorship, location, and date
- BibleData-Epoch — Time periods such as lifetimes of individuals and reigns of kings
- BibleData-Event — Discrete events recorded in Scripture
- BibleData-Place — Every location mentioned in the Bible
- BibleData-PlaceLabel — Place names and titles with Hebrew or Greek originals, related Strong’s numbers, and meanings
- BibleData-PlaceVerse — Every place mentioned in every verse of the Bible

### 📅 Planned
- BibleData-Thing — Significant objects and items mentioned in Scripture (Solomon’s Temple, the Ark of the Covenant, and others)

## How to Use the Data

All files are provided as CSV format for broad compatibility.

```python
import pandas as pd

# Example: Load people data
df = pd.read_csv('BibleData-Person.csv')

# Quick example query
descendants_of_aaron = df[df['related_to'].str.contains('Aaron', na=False)]
print(len(descendants_of_aaron))
```

The datasets can be loaded into spreadsheets, relational databases, graph databases, or any analysis environment of your choosing.  

## Contributing

Contributions of any kind are warmly welcomed — whether corrections, new entries, removal of duplicates, additional fields, or improved documentation.

> **How to contribute:**
> 1. Fork the repository or open an issue describing your suggestion
> 2. Make your changes
> 3. Add your name to the contributors list below (with the file(s) and date)

**Contributors** (with sincere thanks):

- Brady Stephenson — BibleData-Reference.csv, BibleData-Commandments.csv, HebrewStrongs.csv, BibleData-Book.csv, BibleData-Person.csv, BibleData-PersonLabel.csv, BibleData-PersonRelationship.csv, BibleData-PersonVerse.csv, BibleData-Place.csv, BibleData-PlaceLabel.csv, BibleData-PlaceVerse.csv, BibleData-Event.csv, BibleData-Epoch.csv, NavesTopicalDictionary.csv, HitchcocksBibleNamesDictionary.csv, The Alamo Polyglot.csv, BibleData-PersonVerseApostolic.csv, BibleData-PersonVerseTanakh.csv, Ussher-AnnalsOfTheWorld.csv (various dates 2021–2025)
- Dan Raby — BibleData-PersonalLabel.csv
- Fernando Falci — BibleData-PersonRelationship.csv

## License

This project is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt the data for non-commercial purposes, provided appropriate credit is given and any adaptations are released under the same license.

---

Prepared with care for students, scholars, researchers, and all who approach the Scriptures with curiosity and respect.  

Questions or suggestions are always welcome. Please open an issue or reach out via [data.world](https://data.world/bradys).

Last updated: April 2026
