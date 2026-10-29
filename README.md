# AI Web Scraping Benchmark

AIMultiple benchmark of five AI web scraping tools on the same 5,000 URLs, measuring success, completeness, accuracy and completion time of structured data extraction.

> [Read the benchmark on AIMultiple](https://aimultiple.com/ai-web-scraping)

## Workload

The URLs come from 10 of the most visited domains in Semrush's ranking, five e-commerce and five social, with 500 URLs per domain. Every URL went to all five tools, for 25,000 requests.

Each tool received the same prompt per page type: price and currency for e-commerce, post text, likes and author username for social. Bright Data's one-time scraper build per domain is excluded from the timings, and its generated schema was accepted without review. Bright Data, Apify and Firecrawl took 100 URLs per request, Oxylabs and ScrapingBee one.

- Success: share of requests returning at least one requested field.
- Completeness: share of requested fields returned.
- Accuracy: share of checkable values that were correct; missing fields count as wrong. References come from the URL, an independent source or agreement among the other tools, with a 10% tolerance for numbers.

## Benchmark results

Accuracy and completion time, averaged across the 10 domains:

| Tool | Accuracy (%) | Time (s) |
| --- | ---: | ---: |
| Bright Data | 60.1 | 4.61 |
| Oxylabs | 47.8 | 35.15 |
| Firecrawl | 37.5 | 0.37 |
| ScrapingBee | 32.7 | 4.92 |
| Apify | 24.2 | 5.58 |

Bright Data also led on success (85%) and completeness (76%). Even at 60% accuracy, two in five checkable fields came back missing or wrong.

## Scope

Results apply to the tested domains, prompts and API settings. Live pages change, and some sites set prices by the visitor's IP location.

## Ownership

The benchmark implementation was developed for AIMultiple and belongs to AIMultiple. This repository contains a documentation summary. Source code and benchmark datasets are not distributed here.
