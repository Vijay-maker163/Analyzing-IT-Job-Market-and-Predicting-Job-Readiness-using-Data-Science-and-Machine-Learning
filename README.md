# Analyzing IT Job Market and Predicting Job Readiness using Data Science and Machine Learning

Thesis project, Metropolia University of Applied Sciences.

## Overview
This repository contains the code and datasets of a thesis that analyses IT job postings in Finland, extracts the skills they request, and builds a model that predicts the role family from a set of skills. A skill-based readiness score and skill gap are calculated for a target role family.

## Files
| File | Description |
|---|---|
| Thesis.ipynb | Analysis notebook (cleaning, skill extraction, charts, models) |
| finland_it_jobs_FINAL_ML_READY.csv | Input dataset (829 postings) |
| finland_it_jobs_CLEANED.csv | Cleaned dataset (466 postings) |
| finland_it_jobs_SKILL_MATRIX.csv | Skill matrix (466 postings x 57 skills, values 0/1), same row order as the cleaned file |

## How to run
1. Open `Thesis.ipynb` in Google Colab.
2. Upload `finland_it_jobs_FINAL_ML_READY.csv` in the Files panel.
3. Run all cells.

Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn.

## Method
Dictionary-based skill extraction, role families, baseline vs Logistic Regression vs Random Forest (80/20 split and 5-fold cross-validation). The readiness score is a defined metric (demand-weighted coverage of the top 10 skills of the target role family) and has not been validated with real users.

## Data
Public job postings, compiled in September 2026 with AI-assisted search from public job boards. The final dataset has 466 postings. Two sources provide most of the data: englishjobs.fi (221) and Glassdoor (164), together about 83%.

| Source | URL | Postings |
|---|---|---|
| englishjobs.fi | https://englishjobs.fi | 221 |
| Glassdoor | https://www.glassdoor.com | 164 |
| Remote Rocketship | https://www.remoterocketship.com | 13 |
| LinkedIn Jobs | https://fi.linkedin.com/jobs | 12 |
| ite wiki | https://www.itewiki.fi | 11 |
| All Odoo Jobs | https://www.allodoojobs.com | 9 |
| Indeed | https://www.indeed.com | 4 |
| Built In | https://builtin.com | 4 |
| FinTech Careers | https://fintechcareers.com | 3 |
| ZipRecruiter | https://www.ziprecruiter.com | 3 |
| Faruse | https://faruse.com | 3 |
| EurSAP | https://eursap.eu | 3 |
| Web3 Career | https://web3.career | 2 |
| EU Digital Skills and Jobs Platform | https://digital-skills-jobs.europa.eu | 2 |
| MeetFrank | https://meetfrank.com | 2 |
| Jobs in Helsinki | https://jobsinhelsinki.com | 2 |
| JobsPortal | https://jobsportal.fi | 1 |
| Jobly | https://www.jobly.fi | 1 |
| Fivr | https://fivr.fi | 1 |
| Unity careers | https://unity.com/careers | 1 |
| Nordea careers | Nordea company careers page | 1 |
| Games Jobs Direct | https://www.gamesjobsdirect.com | 1 |
| Glassdoor / PayScale (salary page) | https://www.payscale.com | 1 |
| SAP Jobs | https://jobs.sap.com | 1 |

Eight records (ZipRecruiter, Faruse, Games Jobs Direct and Glassdoor/PayScale) come from pages where the location or posting date could not be confirmed. They are kept in the dataset and marked in the `Source` column.

A random sample of [X] postings was checked against the original pages. The records have no links saved. No personal data is included.
## Limitations
Small dataset after cleaning, most data from two sources, missing company/city/date in many records, no links saved per record.

## Author
[Vijay]
