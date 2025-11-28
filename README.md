# Chess Move Pattern Analysis

## Project Proposal

This project analyzes my online chess games to uncover patterns in my playing style.

The main research questions include:
- What is my most frequent opening move?
- On average, at which move do I bring my queen into the game?
- How many moves do my games typically last?
- Do I play differently depending on whether I play White or Black?

The goal is to gain personal insight into my gameplay and explore data-driven techniques to understand chess behavior.

---

## Motivation

I play online chess regularly, but I have never analyzed my own habits systematically.  
By collecting and analyzing my own game data, I aim to discover strengths, weaknesses, and playing tendencies that can help me improve as a player.

---

## Data Sources

Primary Source: My personal game history from Chess.com (or Lichess.org). Both platforms provide an API that allows users to export all games in PGN or JSON format.

Metadata fields collected:
- Player color (White / Black)
- Opening name
- ECO code
- Total move count
- Time control
- Game result
- Timestamps of moves

---

## Data Collection

The data was collected by:
- Downloading my full game history using the Chess.com / Lichess API.
- Exporting game files in **PGN** and **JSON** formats.
- Parsing move sequences using the `python-chess` library.
- Extracting structured features such as:
  - Opening name and ECO code  
  - Move number of first queen development  
  - Total game length  
  - Game outcome (Win / Draw / Loss)

The final dataset was stored in **CSV** and **pandas DataFrame** formats.

---

## Methodology

A structured, step-by-step data analysis process was applied:

1. **Data Extraction**  
   Raw PGN game files were imported and combined.

2. **Data Cleaning**  
   Incomplete or corrupted data points were removed. Relevant fields were standardized.

3. **Feature Engineering**  
   New variables were created:
   - Numeric scoring of results (Win = 1, Draw = 0.5, Loss = 0)  
   - Game phase classification (Short / Medium / Long)  
   - Queen development timing  
   - Aggression and mobility metrics  

4. **Exploratory Data Analysis (EDA)**  
   Visual and descriptive analyses were performed.

5. **Hypothesis Evaluation**  
   Relationships between behavior and outcomes were tested using visual and descriptive statistics.

---

## Exploratory Data Analysis (EDA)

Key visualizations included:
- Histograms of total game lengths
- Violin plots of aggression scores by outcome
- Boxplots of queen development timing
- Bar charts of win rates by game phase
- Scatter plots of mobility versus aggression

Key observations:
- Most games occurred between **10–30 moves**
- Short games were more associated with losses
- Longer games showed higher win rates
- Clear visual differences were observed between win and loss patterns

---

## Hypotheses

### Hypothesis 1 – Queen Development Timing
H₀: Early queen development has no effect on game outcome.  
H₁: Early queen development affects game outcome.

### Hypothesis 2 – Performance by Color
H₀: There is no performance difference when playing White or Black.  
H₁: Playing color affects performance.

### Hypothesis 3 – Game Length and Outcome
H₀: Game length and outcome are independent.  
H₁: Game length and outcome are related.

---

## Findings

- My most common openings are based on king’s and queen’s pawn structures.
- Early queen development is strongly associated with poor outcomes.
- Longer games tend to increase the probability of winning.
- Aggressive play style correlates positively with better performance.
- Playing style changes depending on whether I play White or Black.

---

## Tools & Technologies

- Python  
- pandas  
- NumPy  
- python-chess  
- Matplotlib  
- Seaborn  
- Jupyter Notebook / Google Colab  
- GitHub  

---

## Limitations & Future Work

- The analysis is limited to a single player's games.
- Some games may be missing due to privacy or API limitations.
- Future work may include:
  - Comparison with other players  
  - Engine-based accuracy evaluation  
  - Advanced machine learning models  

---


 




