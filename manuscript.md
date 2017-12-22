---
author-meta:
- Daniel S. Himmelstein
- Casey S. Greene
date-meta: '2017-12-22'
keywords:
- markdown
- publishing
- manubot
- proposal
lang: en-US
title: Manubot 2018 development proposal
...






<small><em>
This manuscript was automatically generated
from [greenelab/manufund-2018@5d08b30](https://github.com/greenelab/manufund-2018/tree/5d08b30fa2ddd9c9a9ad889b6eb0ebcce1180610)
on December 22, 2017.
</em></small>

## Authors



+ **Daniel S. Himmelstein**<br>
    ![ORCID icon](images/orcid.svg){height="13px" width="13px"}
    [0000-0002-3012-7446](https://orcid.org/0000-0002-3012-7446)
    · ![GitHub icon](images/github.svg){height="13px" width="13px"}
    [dhimmel](https://github.com/dhimmel)
    · ![Twitter icon](images/twitter.svg){height="13px" width="13px"}
    [dhimmel](https://twitter.com/dhimmel)<br>
  <small>
     Department of Systems Pharmacology and Translational Therapeutics, University of Pennsylvania
  </small>

+ **Casey S. Greene**<br>
    ![ORCID icon](images/orcid.svg){height="13px" width="13px"}
    [0000-0001-8713-9213](https://orcid.org/0000-0001-8713-9213)
    · ![GitHub icon](images/github.svg){height="13px" width="13px"}
    [cgreene](https://github.com/cgreene)
    · ![Twitter icon](images/twitter.svg){height="13px" width="13px"}
    [GreeneScientist](https://twitter.com/GreeneScientist)<br>
  <small>
     Department of Systems Pharmacology and Translational Therapeutics, University of Pennsylvania
  </small>



## Proposal {.page_break_before}

Manubot is a system for writing scholarly documents on GitHub.
Manubot aims to **transform publishing** to be transparent & reproducible, immediate & permissionless, versioned & automated, collaborative & open, linked & provenanced, decentralized & hackable, interactive & annotated, and free of charge.

Manubot transfers the lessons from the **open source software movement** to academic writing.
Documents are written in the open, creating an easy path for readers to become contributors.
We recommend following a workflow where anyone can propose changes, which are then reviewed by project members and revised as necessary before being incorporated (for example, [see how](https://github.com/greenelab/manufund-2018/pull/2) this proposal was created).

Manubot is based on a collection of open source **tools and standards**.
Manuscripts are written in markdown, using git for version control and GitHub for collaboration and review.
Users can cite standard persistent identifiers and Manubot retrieves bibliographic details to automatically create a reference list.
Conversion between formats (e.g. from markdown to HTML, PDF, and DOCX) is done using [Pandoc](http://pandoc.org/).
When the manuscript changes, continuous integration automatically rebuilds and deploys it [@Qh7xTLwz; @18w6XKsQO].

Currently, the Manubot consists of two repositories: [`greenelab/manubot-rootstock`](https://github.com/greenelab/manubot-rootstock) (a blank manuscript with the required files) and [`greenelab/manubot`](https://github.com/greenelab/manubot) (a backend Python package).
As of December 2017, [10](https://github.com/greenelab/manubot-rootstock/graphs/contributors) individuals have contributed to the **Manubot codebase**, which has [33](https://github.com/greenelab/manubot-rootstock/stargazers) ⭐s on GitHub.
For more information on the Manubot, see [these slides](http://slides.com/dhimmel/manubot#/) as well as the in-progress [Meta Review](https://greenelab.github.io/meta-review/).

We initially created the Manubot to enable the **Deep Review**, a review paper on deep learning that we collaboratively drafted [on GitHub](https://github.com/greenelab/deep-review).
Over 30 authors contributed to the Deep Review [@tJKvnIaZ], using [issues](https://github.com/greenelab/deep-review/issues?utf8=%E2%9C%93&q=is%3Aissue) to discuss source material and [pull requests](https://github.com/greenelab/deep-review/pulls?utf8=%E2%9C%93&q=is%3Apr) to propose manuscript changes.
The community appreciated the breadth of perspectives on a quickly-developing topic and the Deep Review was the most-viewed _bioRxiv_ preprint from April–June 2017 [@9IrsqXRa].
We've also used the Manubot to write our [Sci-Hub Coverage Study](https://greenelab.github.io/scihub-manuscript/) --- the second [most viewed](http://web.archive.org/web/20171221221858/http://www.prepubmed.org/top_preprints/) _PeerJ Preprint_ ever --- and to reproduce the [Bitcoin Whitepaper](https://dhimmel.github.io/bitcoin-whitepaper/) [@yte07Fnn].
In the Manubot's first year, its collaborative, open, and review-driven _authoring process_ yielded two of the most popular preprints of 2017.

In 2018, we seek to expand Manubot's capabilities by accomplishing four feature-driven specific aims and one outreach aim:

1. JATS is the predominant archival format for scholarly manuscripts that is optimized for machine-readability and interoperability.
We will implement JATS export and incorporate an existing **JATS viewer**, such as [Lens](https://lens.elifesciences.org/about/), into Manubot webpages.

2. Currently all changes to a manuscript's source are tracked using git.
We will implement **rendered diff functionality** to show how a manuscript changed from the reader's perspective and make creating "tracked changes" documents for journal resubmission easy.

3. **End-to-end reproducibility** is when the provenance of every manuscript result can be traced to its source.
We will continue to evaluate and improve the Manubot template variables functionality, which allows users to embed results and method parameters directly from the analyses that created them.

4. The Manubot's **citation metadata** system is a powerful and versatile approach for bibliographic information.
We will continue to expand Manubot's citation-by-persistent-ID capabilities.

5. Currently Manubot requires considerable technical expertise [to setup](https://github.com/greenelab/manubot-rootstock/blob/f165f609f33b11fdf71a0db6435d4dd159f23973/SETUP.md) and some technical expertise [to use](https://github.com/greenelab/manubot-rootstock/blob/f165f609f33b11fdf71a0db6435d4dd159f23973/USAGE.md).
The current userbase consists of researchers or publishers who are using tools like git and continuous integration for other tasks, so we will **improve documentation, develop user stories, and perform outreach activities** at relevant conferences.

Our **long-term vision** is an improved ecosystem of scholarly communication.
Imagine you could click an author to highlight only the text they wrote.
Or highlight all results and figures that descend from source code contributions by the selected author.
Or highlight all results that depend on a selected upstream experiment or database.
Or, if a new version of software used in the manuscript or an updated dataset is released, rebuild the manuscript with the updated version and see the resulting changes...
regardless of whether you're the original authors or a curious third-party!
Manubot forms the foundation for the traceability of all aspects of a scholarly manuscript, which is the key principle that underlies this potential future.

_Now is the time to bring the innovation and ethos of open source software development to the scholarly manuscript.
Join us in powering the next generation of scholarly manuscript._


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
