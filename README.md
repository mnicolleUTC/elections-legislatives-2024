# Election Results Analysis

## Data Sources

The data used in this analysis is sourced from the following locations:

- **Geographical boundaries of constituencies**: [Contours géographiques des circonscriptions législatives](https://www.data.gouv.fr/fr/datasets/contours-geographiques-des-circonscriptions-legislatives/)
- **Legislative election results**: [Résultats du 1er tour des élections législatives 2024 par circonscription](https://www.data.gouv.fr/fr/datasets/resultats-du-1er-tour-des-elections-legislatives-2024-par-circonscription/)

## Methodology

1. **Loading Data**: The notebook begins by importing necessary packages such as `pandas`, `geopandas`, and `matplotlib`. The election results data is loaded from a CSV file using `pandas`.

2. **Data Cleaning and Preparation**:
   - The dataset is filtered to exclude constituencies where the election was decided in the first round. This is achieved by identifying constituencies with candidates who were elected in the first round and excluding them from further analysis.
   - This table explains labels from CodNuaCand column :

    | Label orientation politique | Parti politique                     |
    |-----------------------------|-------------------------------------|
    | EXG                         | Extrême gauche                      |
    | RN                          | Rassemblement National              |
    | LR                          | Les Républicains                    |
    | UG                          | Union de la Gauche                  |
    | DSV                         | Divers                              |
    | ENS                         | Ensemble                            |
    | EXD                         | Reconquête                          |
    | DIV                         | Divers                              |
    | ECO                         | Divers écologistes                  |
    | DVD                         | Divers droite                       |
    | REC                         | Reconquête                          |
    | UXD                         | RN + Républicain                    |
    | DVG                         | Divers gauche                       |
    | UDI                         | Droite écolo                        |
    | REG                         | Vote nul candidat avec 0%           |
    | DVC                         | Vote minoritaire pas RN             |
    | HOR                         | Horizon - ensemble                  |
    | COM                         | Autres pas RN                       |
    | VEC                         | Autres gauches                      |
    | FI                          | Associé front populaire             |
    | SOC                         | DOM TOM                             |
    | RDG                         | Autres gauches                      |

   Each of those labels is classified as follows:
   - **RN**: 'RN', 'EXD', 'REC', 'UXD'
   - **Not RN**: All other labels
   - Constituencies are filtered to identify those where the RN party is participating in the second round of voting

3. **Visualization**: 
   - The notebook employs `matplotlib` to visualize the geographical distribution of election results.
   - Maps are generated where constituencies are color-coded to reflect the Difference in votes between the total of "L'arc républicain" and the RN, expressed as a percentage of the number of registered voters.
   - Constituencies where a candidate was elected in the first round are highlighted in black.
   - The map is divided into regions based on the geographical data from Geographical boundaries of constituencies source.

## Usage

To run the notebook, ensure you have the required packages installed. You can install them using `pip`:

```bash
pip install -r requirements.txt
```
Then, open the notebook in Jupyter and run the cells to reproduce the analysis.

## License
This project is licensed under the MIT License.

