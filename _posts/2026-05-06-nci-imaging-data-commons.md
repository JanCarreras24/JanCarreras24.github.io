---
layout: post
title: "NCI Imaging Data Commons: cloud computing for cancer imaging research"
subtitle: "A biomedical cloud application for sharing and analysing medical images"
tags: [cloud-computing, biomedicine, cancer, medical-imaging]
comments: true
author: Jan Carreras
---

Cloud computing is especially useful when the data is too large, too distributed, or too complex to manage on a normal personal computer. A good example in biomedicine is medical imaging. Cancer imaging studies can contain thousands of CT, MRI, PET or pathology images, and these files can be very large. If every research group has to download all the data, prepare the metadata, install the analysis tools and maintain its own infrastructure, the process becomes slow and difficult to reproduce.

For this reason, I decided to explore the **NCI Imaging Data Commons (IDC)**. IDC is a cloud-based repository created as part of the National Cancer Institute Cancer Research Data Commons. Its goal is to make cancer imaging data easier to access, visualize and analyse using cloud resources.

## The biomedical problem

Medical imaging is central in cancer research. Images can be used to detect tumours, monitor disease progression, evaluate treatment response and train artificial intelligence models. However, imaging research has some practical problems:

- the files are very large;
- the metadata is often complex;
- data can come from different hospitals, scanners and studies;
- researchers need specific tools to visualize and process the images;
- reproducing another group's analysis can be difficult.

These problems are not only medical problems. They are also data management and computing problems.

The article by **Fedorov et al. (2021)** introduces IDC as a cloud-based solution for this situation. Instead of asking researchers to download and maintain everything locally, IDC places curated imaging collections close to cloud computing resources and analysis tools. This is the key cloud idea: the data and computation are placed together.

## What is NCI Imaging Data Commons?

IDC is a public cloud repository focused on cancer imaging. It contains radiology images, pathology images, image annotations, segmentations, measurements and clinical metadata. According to the official IDC page, the platform contains more than 85 TB of data and provides access through both Google Cloud and AWS public buckets.

One important design decision is that IDC harmonizes the data using the **DICOM** standard. DICOM is the standard format used in medical imaging. This makes the data easier to search, compare and reuse.

IDC also provides several ways to work with the data:

- an online portal to explore collections;
- image viewers that work in the browser;
- metadata queries using tools such as BigQuery;
- programmatic access with Python packages;
- integration with cloud-native tools such as Google Colab;
- workflows that support reproducible imaging research.

This means that a researcher can build a cohort, inspect images, access metadata and start an analysis without first building a local imaging infrastructure from zero.

## Why is this a cloud application?

IDC is a clear example of cloud computing because it uses remote infrastructure to store, organize and analyse biomedical data.

In a traditional model, a research group would need to:

1. download large imaging datasets;
2. store them locally;
3. install viewers and analysis software;
4. maintain compute servers;
5. manually organize metadata;
6. share scripts and results with other groups.

With IDC, much of this work is moved to a cloud environment. The data is already hosted in public cloud buckets, the metadata can be queried in the cloud, and analysis can be done near the data.

This is important because moving huge datasets is expensive and slow. In many cases, it is more efficient to move the code to the data instead of moving the data to the computer.

## Relation with cloud computing concepts

IDC connects very well with the concepts studied in class.

| Cloud concept | How it appears in IDC |
|---|---|
| Storage as a service | Cancer imaging data is stored in cloud buckets |
| Scalability | Researchers can use cloud resources for large analyses |
| Public cloud | The data can be accessed through cloud providers such as Google Cloud and AWS |
| Shared responsibility | NCI/IDC manages the public repository, while researchers are responsible for their analysis and correct data use |
| Reproducibility | Data, metadata and tools are closer together, making analyses easier to repeat |
| Interoperability | DICOM harmonization helps different tools understand the same data |

I would not classify IDC as a simple SaaS application like Gmail. It is closer to a **cloud data platform** for biomedical research. It provides data, metadata, tools and access mechanisms that researchers can use to build their own analyses.

## Example use case

Imagine a researcher wants to study lung cancer CT images and train a model to detect suspicious regions.

Using a traditional local workflow, the researcher may need to download many gigabytes or terabytes of images, clean metadata, install viewers, prepare storage and configure compute resources.

Using IDC, the researcher can first search the available collections through the IDC Portal. Then they can define a cohort using metadata, inspect images in the browser and access the data from cloud notebooks or scripts. This makes the first steps of the project much faster.

This does not mean that the scientific part becomes automatic. The researcher still has to design a good study, validate the data, choose methods carefully and interpret the results. But the cloud platform reduces the technical barrier.

## Benefits

The main benefit of IDC is that it makes cancer imaging data more accessible.

It also supports reproducibility. If researchers use public datasets, standard metadata and shared notebooks or workflows, other groups can repeat the analysis more easily.

Another advantage is integration. Cancer research is not only imaging. It can also include genomics, proteomics, clinical data and pathology. IDC is part of a larger Cancer Research Data Commons, so it is designed to connect imaging data with other biomedical data types.

Finally, IDC can help machine learning research. AI models for medical imaging need large and well-curated datasets. Cloud access makes it easier to train, test and compare models using public data.

## Limitations and risks

IDC is powerful, but it does not solve every problem.

First, working in the cloud still requires technical knowledge. Researchers may need to understand cloud costs, notebooks, APIs, metadata queries and data formats.

Second, public cancer imaging data is de-identified, but privacy and ethics are still important. Researchers must respect data use rules and avoid any attempt to re-identify patients.

Third, cloud platforms can create dependency on specific tools or providers. If a workflow depends too much on one cloud service, migrating it later can be difficult.

Finally, data quality is still a scientific issue. A cloud platform can make data easier to access, but it cannot replace careful study design, validation and clinical interpretation.

## Conclusion

NCI Imaging Data Commons is a good example of how cloud computing can be applied in biomedicine. The value is not only storing files online. The real value is putting large imaging datasets, metadata, visualization tools and compute resources in the same environment.

For me, this example shows why cloud computing is useful in health data science. Biomedical data is becoming larger and more complex, and local computers are often not enough. Cloud platforms like IDC can make research faster, more collaborative and more reproducible, as long as researchers also manage privacy, costs and data quality responsibly.

## References

Fedorov, A., Longabaugh, W. J. R., Pot, D., Clunie, D. A., Pieper, S., Aerts, H. J. W. L., et al. (2021). **NCI Imaging Data Commons**. *Cancer Research, 81*(16), 4188-4193. DOI: [10.1158/0008-5472.CAN-21-0950](https://doi.org/10.1158/0008-5472.CAN-21-0950). PubMed: [PMID 34185678](https://pubmed.ncbi.nlm.nih.gov/34185678/).

National Cancer Institute. **Imaging Data Commons (IDC)**. Cancer Research Data Commons. Available at: [https://datacommons.cancer.gov/repository/imaging-data-commons](https://datacommons.cancer.gov/repository/imaging-data-commons).

National Cancer Institute Center for Biomedical Informatics and Information Technology. **Imaging Data Commons Featured in Cancer Research**. Available at: [https://datascience.cancer.gov/news-events/news/imaging-data-commons-featured-cancer-research](https://datascience.cancer.gov/news-events/news/imaging-data-commons-featured-cancer-research).
