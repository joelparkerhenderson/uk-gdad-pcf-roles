# Senior machine learning engineer - upskill resources

This page focuses on learning and growth resources for the work role of senior machine learning engineer.

- The resources include links to online courses, blogs, research articles, videos, and books.

- These help with job upskilling, work training, professional development, and career advancement.

- These are intended to be good starting points, not a comprehensive catalogue.

At this role level you build, deploy and operate machine learning systems in production, taking responsibility for their reliability, monitoring and lifecycle. The resources below emphasise MLOps, production practice, model evaluation and technical debt.

We welcome constructive feedback to improve this page and these lists.

- GitHub issues and/or pull requests are welcome.

- The resources are found via AI searches then go through human-in-the-loop proofing.

- For more contact Joel Henderson <joel@joelparkerhenderson.com>

## Coursera courses

- [Machine Learning in Production](https://www.coursera.org/learn/introduction-to-machine-learning-in-production): From DeepLearning.AI, covering the design of a production machine learning system end to end, including project scoping, data needs, modelling strategy and deployment patterns.

- [MLOps: Machine Learning Operations (Duke University)](https://www.coursera.org/specializations/mlops-machine-learning-duke): Covers MLOps principles and data management for building and deploying models in production, across AWS SageMaker, Azure, MLflow and Hugging Face, with pipeline and API development.

- [Machine Learning Operations (MLOps): Getting Started](https://www.coursera.org/learn/mlops-fundamentals): From Google Cloud, introducing tools and best practice for deploying, evaluating, monitoring and operating production machine learning systems.

## Udemy courses

- [Deployment of Machine Learning Models](https://www.udemy.com/course/deployment-of-machine-learning-models/): A focused course on taking a trained model into a served, reproducible deployment rather than a notebook.

- [MLOps Zero to Hero](https://www.udemy.com/course/mlops-zero-to-hero/): Addresses the real problems that arise after a model is trained, including versioning data with DVC, tracking experiments with MLflow, containerisation with Docker, and deployment on Kubernetes with KServe.

- [Ultimate DevOps to MLOps Bootcamp: Build ML CI/CD Pipelines](https://www.udemy.com/course/devops-to-mlops-bootcamp/): Takes a regression use case from data processing to production deployment on Kubernetes, covering model serving, monitoring with Prometheus and Grafana, and GitOps continuous delivery.

## Skillsoft courses

- [Courses for Data Scientist: Machine Learning Specialist](https://www.skillsoft.com/journey/data-scientist-machine-learning-ec124151-3477-44a5-b819-914e25079c6f): A career path covering data literacy, SQL, Python fundamentals, pandas, exploratory data analysis, statistics fundamentals and visualisation, then machine learning fundamentals, supervised and unsupervised learning and deep learning.

- [Courses for Data Science Foundations](https://www.skillsoft.com/journey/data-science-foundations-6cd9e7e0-0ed6-4bd3-9ca9-9b96d735ed19): Teaches cleaning, analysing and visualising data with industry-standard Python libraries including pandas and seaborn, with real-world projects.

- [Courses for Fundamental Mathematics for Data Science](https://www.skillsoft.com/journey/fundamental-mathematics-for-data-science-8803a1be-4e33-4069-b80d-4de06358ac14): Covers probability, statistics, linear algebra and calculus as applied to real data analysis, filling the gaps that limit many practitioners.

## edX courses

- [Statistics and Data Science MicroMasters (MITx)](https://www.edx.org/micromasters/mitx-statistics-and-data-science): Four courses and a proctored exam covering the fundamentals of probability and statistics alongside implementing and experimenting with data analysis techniques and machine learning algorithms.

- [Data Science: Probability (HarvardX)](https://www.edx.org/learn/probability/harvard-university-data-science-probability): Teaches probability theory through a case study on the financial crisis of 2007 to 2008, part of the Harvard data science professional certificate.

- [Probability and Statistics in Data Science using Python (UCSanDiegoX)](https://www.edx.org/learn/statistics/the-university-of-california-san-diego-probability-and-statistics-in-data-science-using-python): Teaches statistical and probabilistic approaches to understanding data, implemented in Python.

## MIT OpenCourseWare courses

- [15.097 Prediction: Machine Learning and Statistics](https://ocw.mit.edu/courses/15-097-prediction-machine-learning-and-statistics-spring-2012/): Starts with machine learning algorithms, then covers the statistical learning theory that provides their mathematical foundation, before moving into Bayesian analysis.

- [15.075J Statistical Thinking and Data Analysis](https://ocw.mit.edu/courses/15-075j-statistical-thinking-and-data-analysis-fall-2011/): Covers applied probability, sampling, estimation, hypothesis testing, linear regression, analysis of variance, categorical data analysis and nonparametric statistics.

- [18.065 Matrix Methods in Data Analysis, Signal Processing, and Machine Learning](https://ocw.mit.edu/courses/18-065-matrix-methods-in-data-analysis-signal-processing-and-machine-learning-spring-2018/): Reviews linear algebra with applications to probability, statistics and optimisation, including a full explanation of deep learning.

## Blog posts

- [How to Detect Model Drift in MLOps Monitoring](https://towardsdatascience.com/how-to-detect-model-drift-in-mlops-monitoring-7a039c22eaf9/): A practical treatment of detecting drift, including the difference between data drift and concept drift and how to test for each.

- [What is model drift? Best practices for dealing with model drift](https://encord.com/blog/model-drift-best-practices/): Covers monitoring model performance to detect concept drift early and triggering retraining workflows.

- [Identifying drift in ML models: best practices for consistent, reliable responses](https://techcommunity.microsoft.com/blog/fasttrackforazureblog/identifying-drift-in-ml-models-best-practices-for-generating-consistent-reliable/4040531): Microsoft engineering guidance on drift detection in deployed models.

- [Managing Tech Debt within AI and Machine Learning Systems](https://audacia.co.uk/technical-blog/technical-debt-in-ai-and-machine-learning): Covers the specific forms technical debt takes in machine learning systems and how MLOps practice reduces it.

- [The Invisible Debt Collector: Technical Debt in Machine Learning](https://medium.com/@dataninsight/the-invisible-debt-collector-technical-debt-in-machine-learning-89ba6e546dfb): A practitioner treatment of how ML-specific debt accumulates and why it is hard to see.

- [Data Debt in Production ML Pipelines: Detection and Remediation at Scale](https://hackernoon.com/data-debt-in-production-ml-pipelines-detection-and-remediation-at-scale): Focuses on the data side of ML debt, which is usually where the largest problems sit.

- [MLOps Production Lessons: CI/CD, Drift, Observability](https://hjlabs.in/AIML/blog/post/mlops-production-lessons.html): Sets out the minimum monitoring for day one, including latency percentiles, error rate, request volume, prediction logging and per-feature drift checks.

- [Technical Debt, from Machine Learning in Production: From Models to Products](https://mlip-cmu.github.io/book/22-technical-debt.html): The technical debt chapter of the Carnegie Mellon open textbook on production machine learning.

- [Reproducible data science](https://domino.ai/blog/reproducible-data-science): Explains why every aspect of a model must be documented for transparency, justification and validation, which is a hard requirement in regulated settings.

- [Data Ethics on the Data in Government blog](https://dataingovernment.blog.gov.uk/category/data-ethics/): Covers the ethical questions that attach to automated decisions in UK public services.

## Research articles

- [Hidden Technical Debt in Machine Learning Systems](https://papers.neurips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf): Sculley and colleagues at NeurIPS, the paper that framed ML technical debt and became the motivating text for the MLOps movement. Essential reading.

- [Hidden technical debt in Machine learning systems (ACM)](https://dl.acm.org/doi/10.5555/2969442.2969519): The ACM record of the same paper, covering the ML-specific risk factors that produce ongoing maintenance cost.

- [Leakage and the reproducibility crisis in machine-learning-based science](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10499856/): Documents leakage across 17 fields and 294 papers, and proposes model info sheets as a preventive measure.

- [Pitfalls in Machine Learning Research: Reexamining the Development Cycle](https://arxiv.org/pdf/2011.02832): Argues that applied machine learning is hindered by ad hoc design, poor data hygiene and weak statistical rigour in evaluation.

- [Generalizability of Machine Learning Models: Quantitative Evaluation of Three Methodological Pitfalls](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9885377/): Quantifies how three common methodological errors damage generalisation beyond training data.

- [Reproducibility in machine-learning-based research: Overview, barriers, and drivers](https://onlinelibrary.wiley.com/doi/10.1002/aaai.70002): Reviews what blocks reproducibility in practice and what actually improves it.

- [Assessing the Quality of Computational Notebooks for a Frictionless Transition from Exploration to Production](https://arxiv.org/pdf/2205.11941): Examines the notebook-to-production gap, which is where most machine learning engineering effort is actually spent.

- [Verification and Validation for Trustworthy Scientific Machine Learning](https://arxiv.org/pdf/2502.15496): Covers what verification and validation mean for machine learning systems, where conventional software testing is insufficient.

- [Data pipeline quality: Influencing factors, root causes of data-related issues, and processing problem areas for developers](https://www.sciencedirect.com/science/article/pii/S0164121223002509): A taxonomy of 41 factors influencing pipeline quality, validated with expert interviews.

- [Cross-Validation, Risk Estimation, and Model Selection](https://arxiv.org/pdf/1909.11696): A rigorous treatment of what cross-validation actually estimates and when it misleads, which matters when promoting a model to production.

## Videos

- [A Gentle Introduction to Machine Learning](https://www.youtube.com/watch?v=Gv9_4yMHFhI): Josh Starmer's clear introduction to what machine learning is doing and why, a good grounding before any specific algorithm.

- [StatQuest: Random Forests Part 1, Building, Using and Evaluating](https://www.youtube.com/watch?v=J4Wdy0Wc_xQ): Explains how random forests are built from decision trees and why they avoid the accuracy problems of single trees.

- [StatQuest: Random Forests Part 2, Missing data and clustering](https://www.youtube.com/watch?v=mIlw5j3WyVk): Covers handling missing data and using proximity for clustering, both frequently needed with real administrative data.

- [Gradient Boost Part 4: Classification Details](https://www.youtube.com/watch?v=StWY5QWMXCw): Works through the mathematics of gradient boosting for classification in detail rather than by analogy.

- [XGBoost Part 2: Classification](https://www.youtube.com/watch?v=8b1JEDvenQU): Explains how XGBoost differs from plain gradient boosting and why those differences matter in practice.

- [XGBoost in Python from Start to Finish](https://www.youtube.com/watch?v=GrJP9FLV3FE): A complete worked example including data preparation, tuning and evaluation.

- [Statistical Learning: Cross Validation the wrong and right way](https://www.youtube.com/watch?v=jgoa28FR__Y): From the authors of An Introduction to Statistical Learning, showing the common cross-validation error that inflates reported performance.

- [Statistical Learning: Validation and cross validation](https://www.youtube.com/watch?v=mzb5Xs58bb0): Covers the validation set approach and k-fold cross-validation with their trade-offs.

- [The StatQuest Introduction to PyTorch](https://www.youtube.com/watch?v=FHdlXe1bSe4): A gentle entry into building neural networks in PyTorch for people who already understand the statistics.

- [Master Statistics for Data Science and Machine Learning, full course](https://www.youtube.com/watch?v=8AsZY4WgtJc): A long-form course covering the statistical foundations that data science work depends on.

## Books on Amazon

- [Python Data Science Handbook: Essential Tools for Working with Data](https://www.amazon.com/Python-Data-Science-Handbook-Essential/dp/1098121228): By Jake VanderPlas. Covers IPython, NumPy, pandas, Matplotlib and scikit-learn for manipulating, transforming, cleaning and visualising data and building models.

- [Data Science from Scratch: First Principles with Python](https://www.amazon.com/Data-Science-Scratch-Principles-Python/dp/149190142X): By Joel Grus. Teaches how the fundamental tools and algorithms work by implementing them from scratch, which builds real understanding of the underlying mathematics.

- [The DAMA Guide to the Data Management Body of Knowledge](https://www.skillsoft.com/book/the-dama-guide-to-the-data-management-body-of-knowledge-dama-dmbok-guide-first-edition-cc095fa0-f038-11e6-87f4-0242c0a80606): The reference across data management knowledge areas, useful for understanding the governance environment analysis happens within.

- [Data Storytelling: Learn AI, Data Science and Python for Beginners](https://www.amazon.com/dp/B09D949DGM): A beginner-friendly treatment of communicating analytical findings, an area many technically strong analysts neglect.

- [Learn Data Analytics and Data Storytelling for Beginners](https://us.amazon.com/dp/B0FNCPLRFG): A practical guide with worked examples and Python exercises focused on turning analysis into a narrative that changes decisions.

- [The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling](https://www.amazon.com/Data-Warehouse-Toolkit-Definitive-Dimensional-ebook/dp/B00DRZX6XS): Kimball and Ross. Useful for understanding how the analytical data you consume is structured and why.

- [Building the Data Lakehouse](https://www.amazon.com/Building-Data-Lakehouse-Bill-Inmon-ebook/dp/B09GRZ9KP3): Inmon, Levins and Srivastava on the lakehouse pattern, increasingly the environment data scientists actually work in.

- [The Chief Data Officer's Playbook](https://www.amazon.com/Chief-Data-Officers-Playbook/dp/1783302577): Carruthers and Jackson. Useful context on how data functions are organised and funded, and where analysis fits.

- [Business Model Generation: A Handbook for Visionaries, Game Changers, and Challengers](https://www.amazon.com/Business-Model-Generation-Visionaries-Challengers-ebook/dp/B06X426D4F): Osterwalder and Pigneur. A fast way to frame the organisational context that analysis is meant to serve.

- [Driving Digital: The Leader's Guide to Business Transformation Through Technology](https://www.amazon.com/Driving-Digital-Business-Transformation-Technology-ebook/dp/B01N10Y94E): Isaac Sacolick on enabling data-driven organisations, useful for understanding what senior stakeholders are trying to achieve.

## Professional development tips

- Treat the model as one component of a system, since most failures are systems failures rather than modelling failures
- Build monitoring and drift detection before you need them, not after the first incident
- Version data, code and models together, since reproducing a result later depends on all three
- Learn the software engineering practices your organisation uses and apply them to machine learning work
- Read the hidden technical debt paper carefully, since it names the traps you are most likely to fall into
- Work closely with data engineers, because model quality is bounded by data quality
- Design for the model being wrong, including a human route of appeal where decisions affect people
