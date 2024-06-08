# NewsPolyML: Multi-lingual European News Fake Assessment Dataset

The NewsPolyML dataset is a comprehensive collection of over 32,000 fact-checked news articles from 5 reputable European fact-checking agencies: AFP, Newtral, Full Fact, Correctiv, and Pagella Politica. The dataset covers articles in 5 languages: English, German, French, Spanish, and Italian.

## Data Collection and Normalization

The data collection process focused on gathering fact-checked articles from the selected European [IFCN signatories](https://ifcncodeofprinciples.poynter.org/signatories) that use [ClaimReview markup](https://developers.google.com/search/docs/appearance/structured-data/factcheck). The dataset was normalized to focus on textual components.

## Key Features

- Wide array of metadata fields, including article descriptions, referenced links, claim reviews, publications and claim dates, and ratings
- Sentiment scores and Language labels for claims and full articles
- Structured and consistent data collection process using the ClaimReview schema

## Dataset Statistics

- **Total number of articles:** 32,508
- **Number of unique claims:** 32,082
- **Average claim length (in characters):** 286.08
- **Average title length (in characters):** 88.18
- **Average article length (in characters):** 3,688.87

## Language Distribution

| Language | Count  | Percentage |
| -------- | ------ | ---------- |
| English  | 12,459 | 38%        |
| German   | 3,431  | 11%        |
| French   | 2,899  | 9%         |
| Spanish  | 10,077 | 31%        |
| Italian  | 3,642  | 11%        |

## Source Distribution

| Source              | Language | Counts |
| ------------------- | -------- | ------ |
| correctiv.org       | German   | 2,442  |
| factcheck.afp.com   | English  | 9,212  |
| factual.afp.com     | Spanish  | 5,793  |
| factuel.afp.com     | French   | 2,899  |
| faktencheck.afp.com | German   | 989    |
| fullfact.org        | English  | 3,247  |
| pagellapolitica.it  | Italian  | 3,642  |
| newtral.es          | Spanish  | 4,284  |

## Label Normalization

Due to the diverse rating systems employed by different fact-checking organizations, we have standardized the truthfulness ratings of the claims using the [Mixtral model](https://arxiv.org/abs/2401.04088) to generate a standardized label for each claim.

The common labeling scheme adopted in this dataset is inspired by the normalization approach outlined in [ClaimsKG](https://data.gesis.org/claimskg/). The various ratings have been consolidated into four broad categories:

- **TRUE**: Claims verified as accurate.
- **FALSE**: Claims proven to be incorrect.
- **MIXTURE**: Claims containing elements of both truth and falsehood or those that could not be fully classified as either true or false.
- **OTHER**: Claims that do not fit into the above categories, including but not limited to opinions, predictions, or unverifiable statements.

## Label Distribution

| Normalized Label | Count  | Percentage |
| ---------------- | ------ | ---------- |
| True             | 2,497  | 7.7%       |
| Other            | 256    | 0.8%       |
| Mixture          | 6,221  | 19.1%      |
| False            | 23,218 | 71.4%      |
| Mislabeled       | 316    | 1.0%       |

## Accessing Dataset

**Paper:** TBD

**Dataset:** [Download NewsPolyML](https://drive.proton.me/urls/P816K00J64#CjS1s5m1xryG)
