
# arXivBytes

This repository provides daily, TL;DR summaries of recent research papers published on
[arXiv](https://arxiv.org/) which are easy to read. By default, it focuses on the following specific arXiv categories:
- `gr-qc` for General Relativity and Quantum Cosmology
- `hep-th` for High-Energy Physics (Theory)
- `math-ph` for Mathematical Physics

Each day, it automatically:
1. Fetches the most recent papers from the previous day in the above arXiv categories
2. Uses a transformer-based summarization model to produce readable, condensed summaries
3. Commits and pushes a new Markdown file with the latest summaries to this repository at 08:00 CET (07:00 UTC)

<hr>

## How It Works

- **Data Source**:  
  Papers are fetched using the [arXiv API](https://arxiv.org/help/api/) based on specified categories
  
- **Summarization Model**:  
  Summaries are generated using [Hugging Face’s](https://huggingface.co/) `transformers` library and the 
[facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn) model developed by Meta AI

- **Automation**:  
  A workflow runs every day at a fixed time and pushes the resulting `.md` file to this repository

<hr>

## Viewing the Summaries

- **Latest Summary**:  
  The most recent summary files will be placed in the root directory of this repository and are named something like `arXivBytes_{category}_recent.md`, where `{category}` corresponds to the arXiv category.
  
- **Previous Summaries**:  
  All previously generated `.md` files remain in the repository’s commit history and are also available in each arXiv category folder. You can view older summaries by 
browsing past commits or searching through the desired arXiv category folder in the repository. The summaries are saved as `arXivBytes_{category}_summaries_{date}.md` where `{date}` corresponds to the date it was generated.

<hr>

## Attribution and Credits

- **arXiv**:  
  The research papers come from [arXiv](https://arxiv.org/), a free distribution service and an open-access archive 
for scholarly articles.
  
- **Summarization Model**:  
  The summaries are generated using [facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn), a 
model provided by Facebook (Meta) and hosted on [Hugging Face](https://huggingface.co/). Credit goes to the developers and maintainers of the model.
  
- **Tooling**:  
  - [Hugging Face Transformers](https://github.com/huggingface/transformers) for model inference and pipelines.
  - [Feedparser](https://pypi.org/project/feedparser/) and [Requests](https://pypi.org/project/requests/) for 
  fetching and parsing arXiv data.

<hr>

## License

The arXiv paper abstracts are subject to arXiv’s terms of use and the original authors’ copyright. 
The `facebook/bart-large-cnn` model is provided under its respective license on Hugging Face.
This project is strictly non-commercial.