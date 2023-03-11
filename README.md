# Leveraging-Adversarial-Samples-for-Enhanced-Classification-of-Malicious-and-Evasive-PDF-Files

Full Paper available at: https://www.mdpi.com/2076-3417/13/6/3472

### Abstract:
The Portable Document Format (PDF) is considered one of the most popular formats due to its flexibility and portability across platforms. Although people have used machine learning techniques to detect malware in PDF files, the problem with these models is their weak resistance against evasion attacks, which constitutes a major security threat. The goal of this study is to introduce three machine learning-based systems that enhance malware detection in the presence of evasion attacks by substantially relying on evasive data to train malware and evasion detection models. To evaluate the robustness of the proposed systems, we used two testing datasets, a real dataset containing around 100 k PDF samples and an evasive dataset containing 500 k samples that we generated. We compared the results of the proposed systems to a baseline model that was not adversarially trained. When tested against the evasive dataset, the proposed systems provided an increase of around 80% in the f1-score compared to the baseline. This proves the value of the proposed approaches towards the ability to deal with evasive attacks

### Methodology:
In this study, we propose the idea of leveraging PDF samples that are known
to be evasive and to perform adversarial learning, where we
train the malware classifier on data containing evasive and non-evasive samples. More-
over, instead of relying on the certainty of the malware classifier’s predictions to detect
evasion, we propose the idea of using this mix of evasive and non-evasive data to build
standalone models that detect evasion. These two missing pieces are the focus of this study,
and accordingly, we propose three approaches:
1. Building a robust malware classifier by performing the training on a mix of evasive and non-evasive data.
2. Building a hierarchical system that first classifies if a PDF is evasive or not, and then, checks for malware by forwarding the PDF to a model that deals exclusively with evasive data or another model that deals only with non-evasive data.
3. Building a multi-label classifier that detects evasion and maliciousness simultaneously and independently instead of relying on two dependent models as in the second approach. This classifier is also trained on a combination of evasive and non-evasive data.

<img src="https://user-images.githubusercontent.com/79650267/222168753-cacefd62-1aab-4890-8fcd-1920af802ac1.png" width=80%>

To implement these approaches, we collected training data from various sources,
and they fall under two categories: evasive and non-evasive. The training for the components of each system is shown in the figure below.

<img src="https://user-images.githubusercontent.com/79650267/222169479-764fbb0d-715c-4ab5-952a-e95f98bece39.png" width=80%>

### Some Results
We test each of the systems against 2 datasets: 
1. One real dataset (100 k samples) collected from monitoring the network of a university campus.
2. An Evasive dataset (500 k samples) that we generated based on the data that we collected.

We compare the performance of the proposed systems with a baseline that was not adversarially trained to compare.
When testing against the first dataset, all systems perform similarly, which proves that the proposed systems still perform well on classic datasets that are not evasive.

<img src="https://user-images.githubusercontent.com/79650267/222174284-e5639acd-46db-4fab-9c95-8ee173504d0a.png" width=50%>

When testing against the second dataset, we can see the superiority of the proposed approaches compared to the baseline that performs worse than random guessing. 

<img src="https://user-images.githubusercontent.com/79650267/222173674-7517d344-aef2-4570-bfaf-a5b285df792a.png" width=50%>


These results highlight the importance of the suggested approaches and their ability to be resilient against PDF evasion attacks. 

### Citation

Any work that uses the data or code provided should cite the following paper:

***F. Trad, A. Hussein, and A. Chehab, “Leveraging Adversarial Samples for Enhanced Classification of Malicious and Evasive PDF Files,” Applied Sciences, vol. 13, no. 6, p. 3472, Mar. 2023, doi: 10.3390/app13063472.2***
