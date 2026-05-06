---
layout: post
title: "NCI Imaging Data Commons: a cloud application in cancer imaging"
subtitle: "Using cloud computing to work with biomedical images"
tags: []
comments: true
author: Jan Carreras
---

For this blog post I wanted to look for a real example of cloud computing in biomedicine. I found the **NCI Imaging Data Commons (IDC)**, which is a cloud platform for cancer imaging data.

The main idea is simple. Medical images, such as CT, MRI or PET scans, can be very large. Also, cancer imaging studies usually have many images and a lot of metadata. If every research group has to download everything to a local computer, prepare the data and install all the tools, the process can be slow and difficult.

IDC tries to solve this problem by storing cancer imaging datasets in the cloud. Researchers can search the data, view images, access metadata and use cloud tools to analyse the information. In other words, the data is already close to the computing resources.

## Why is it useful?

I think IDC is a good example of cloud computing because it is not only "data stored online". It is a platform that helps researchers work with large biomedical datasets without having to build all the infrastructure themselves.

For example, a researcher interested in lung cancer images can use the IDC portal to find relevant image collections. Then, they can inspect the images and use tools such as cloud notebooks or metadata queries to start the analysis. This is more practical than downloading huge datasets before even knowing if they are useful.

This connects with several cloud concepts from class:

- the data is stored in remote cloud infrastructure;
- researchers can access it from different places;
- large datasets can be analysed with cloud tools;
- the platform makes sharing and reproducing analyses easier;
- the user does not need to maintain a local server with all the images.

## Benefits and limitations

The main benefit is accessibility. IDC makes cancer imaging data easier to find and use. This can help research groups that do not have a lot of local computing infrastructure.

Another benefit is reproducibility. If different researchers use the same public datasets and similar cloud tools, it is easier to compare results.

However, there are also limitations. Working with cloud platforms still requires some technical knowledge. Researchers need to understand how to access the data, how to use the tools and how to control possible costs. Also, even if the data is de-identified, privacy and ethical use of biomedical data are still very important.

## My opinion

For me, IDC is a clear example of why cloud computing is useful in health data science. Biomedical data is becoming larger and more complex, and local computers are often not enough. A cloud platform can make the first steps of a project faster and can help researchers collaborate better.

At the same time, cloud computing is not a magic solution. The researcher still has to design a good study, check the data quality and interpret the results correctly. The cloud helps with infrastructure, but it does not replace scientific reasoning.

## References

Fedorov, A., Longabaugh, W. J. R., Pot, D., Clunie, D. A., Pieper, S., Aerts, H. J. W. L., et al. (2021). **NCI Imaging Data Commons**. *Cancer Research, 81*(16), 4188-4193. DOI: [10.1158/0008-5472.CAN-21-0950](https://doi.org/10.1158/0008-5472.CAN-21-0950). PubMed: [PMID 34185678](https://pubmed.ncbi.nlm.nih.gov/34185678/).

National Cancer Institute. **Imaging Data Commons (IDC)**. Cancer Research Data Commons. Available at: [https://datacommons.cancer.gov/repository/imaging-data-commons](https://datacommons.cancer.gov/repository/imaging-data-commons).
