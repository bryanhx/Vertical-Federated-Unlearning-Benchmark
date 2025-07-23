# Vertical-Federated-Unlearning-Benchmark

## Introduction
This repository serves as a comprehensive resource for all existing Vertical Federated Unlearning (VFU) studies and is designed to establish foundational benchmarks for the research community. By curating a centralized collection of studies, datasets, and evaluation metrics, the repository aims to standardize methodologies and facilitate consistent comparisons among various approaches.

Additionally, the repository seeks to foster collaboration and innovation by providing researchers and practitioners with accessible tools, guidelines, and baseline implementations. This initiative not only helps streamline future VFU research but also encourages the development of robust and scalable solutions to advance the field.


## List of Papers

1. [Vertical Federated Unlearning on the Logistic Regression Model](https://www.mdpi.com/2079-9292/12/14/3182)
   - Unlearning Targets: Passive Party Unlearning
   - Abstract : Vertical federated learning is designed to protect user privacy by building local models over disparate datasets and transferring intermediate parameters without directly revealing the underlying data. However, the intermediate parameters uploaded by participants may memorize information about the training data. With the recent legislation on the “right to be forgotten”, it is crucial for vertical federated learning systems to have the ability to forget or remove previous training information of any client. For the first time, this work fills in this research gap by proposing a vertical federated unlearning method on logistic regression model. The proposed method is achieved by imposing constraints on intermediate parameters during the training process and then subtracting target client updates from the global model. The proposed method boasts the advantages that it does not need any new clients for training and requires only one extra round of updates to recover the performance of the previous model. Moreover, data-poisoning attacks are introduced to evaluate the effectiveness of the unlearning process. The effectiveness of the method is demonstrated through experiments conducted on four benchmark datasets. Compared to the conventional unlearning by retraining from scratch, the proposed unlearning method has a negligible decrease in accuracy but can improve training efficiency by over 400%.

3. [SecureCut: Federated Gradient Boosting Decision Trees with Efficient Machine Unlearning](https://arxiv.org/abs/2311.13174)
   - Unlearning Targets: Instance Unlearning, Feature Unlearning
   - Abstract : In response to legislation mandating companies to honor the right to be forgotten by erasing user data, it has become imperative to enable data removal in Vertical Federated Learning (VFL) where multiple parties provide private features for model training. In VFL, data removal, i.e., machine unlearning, often requires removing specific features across all samples under privacy guarentee in federated learning. To address this challenge, we propose a novel Gradient Boosting Decision Tree (GBDT) framework that effectively enables both instance unlearning and feature unlearning without the need for retraining from scratch. Leveraging a robust GBDT structure, we enable effective data deletion while reducing degradation of model performance. Extensive experimental results on popular datasets demonstrate that our method achieves superior model utility and forgetfulness compared to state-of-the-art methods. To our best knowledge, this is the first work that investigates machine unlearning in VFL scenarios.

5. [Efficient Vertical Federated Unlearning via Fast Retraining](https://dl.acm.org/doi/abs/10.1145/3657290)
   - Unlearning Targets: Passive Party Unlearning
   - Abstract : Vertical federated learning (VFL) revolutionizes privacy-preserved collaboration for small businesses that have distinct but complementary feature sets. However, as the scope of VFL expands, the constant entering and leaving of participants and the subsequent exercise of the “right to be forgotten” pose a great challenge in practice. The question of how to efficiently erase one’s contribution from the shared model remains largely unexplored in the context of VFL. In this article, we introduce a vertical federated unlearning framework, which integrates model checkpointing techniques with a hybrid, first-order optimization technique. The core concept is to reduce backpropagation time and improve convergence/generalization by combining the advantages of the existing optimizers. We provide in-depth theoretical analysis and time complexity to illustrate the effectiveness of the proposed design. We conduct extensive experiments on six public datasets and demonstrate that our method could achieve up to 6.3× speedup compared to the baseline, with negligible influence on the original learning task.

7. [A few-shot Label Unlearning in Vertical Federated Learning](https://arxiv.org/abs/2410.10922)
   - Unlearning Targets: Class Unlearning
   - Abstract : This paper addresses the critical challenge of unlearning in Vertical Federated Learning (VFL), an area that has received limited attention compared to horizontal federated learning. We introduce the first approach specifically designed to tackle label unlearning in VFL, focusing on scenarios where the active party aims to mitigate the risk of label leakage. Our method leverages a limited amount of labeled data, utilizing manifold mixup to augment the forward embedding of insufficient data, followed by gradient ascent on the augmented embeddings to erase label information from the models. This combination of augmentation and gradient ascent enables high unlearning effectiveness while maintaining efficiency, completing the unlearning procedure within seconds. Extensive experiments conducted on diverse datasets, including MNIST, CIFAR10, CIFAR100, and ModelNet, validate the efficacy and scalability of our approach. This work represents a significant advancement in federated learning, addressing the unique challenges of unlearning in VFL while preserving both privacy and computational efficiency.

9. [Vertical Federated Unlearning via Backdoor Certification](https://ieeexplore.ieee.org/document/10857418)
    - Unlearning Targets: Passive Party Unlearning
    - Abstract : Vertical Federated Learning (VFL) offers a novel paradigm in machine learning, enabling distinct entities to train models cooperatively while maintaining data privacy. This method is particularly pertinent when entities possess datasets with identical sample identifiers but diverse attributes. Recent privacy regulations emphasize an individual's right to be forgotten, which necessitates the ability for models to unlearn specific training data. The primary challenge is to develop a mechanism to eliminate the influence of a specific client from a model without erasing all relevant data from other clients. Our research investigates the removal of a single client's contribution within the VFL framework. We introduce an innovative modification to traditional VFL by employing a mechanism that inverts the typical learning trajectory with the objective of extracting specific data contributions. This approach seeks to optimize model performance using gradient ascent, guided by a pre-defined constrained model. We also introduce a backdoor mechanism to verify the effectiveness of the unlearning procedure. Our method avoids fully accessing the initial training data and avoids storing parameter updates. Empirical evidence shows that the results align closely with those achieved by retraining from scratch. Utilizing gradient ascent, our unlearning approach addresses key challenges in VFL, laying the groundwork for future advancements in this domain.

11. [Unlearning Clients, Features and Samples in Vertical Federated Learning](https://arxiv.org/abs/2501.13683)
    - Unlearning Targets: Passive Party Unlearning, Feature Unlearning, Instance Unlearning
    - Abstract : Federated Learning (FL) has emerged as a prominent distributed learning paradigm. Within the scope of privacy preservation, information privacy regulations such as GDPR entitle users to request the removal (or unlearning) of their contribution from a service that is hosting the model. For this purpose, a server hosting an ML model must be able to unlearn certain information in cases such as copyright infringement or security issues that can make the model vulnerable or impact the performance of a service based on that model. While most unlearning approaches in FL focus on Horizontal FL (HFL), where clients share the feature space and the global model, Vertical FL (VFL) has received less attention from the research community. VFL involves clients (passive parties) sharing the sample space among them while not having access to the labels. In this paper, we explore unlearning in VFL from three perspectives: unlearning clients, unlearning features, and unlearning samples. To unlearn clients and features we introduce VFU-KD which is based on knowledge distillation (KD) while to unlearn samples, VFU-GA is introduced which is based on gradient ascent. To provide evidence of approximate unlearning, we utilize Membership Inference Attack (MIA) to audit the effectiveness of our unlearning approach. Our experiments across six tabular datasets and two image datasets demonstrate that VFU-KD and VFU-GA achieve performance comparable to or better than both retraining from scratch and the benchmark R2S method in many cases, with improvements of (0-2\%). In the remaining cases, utility scores remain comparable, with a modest utility loss ranging from 1-5\%. Unlike existing methods, VFU-KD and VFU-GA require no communication between active and passive parties during unlearning. However, they do require the active party to store the previously communicated embeddings.



## Proposed Datasets

| No. | Datasets | Data Type |
| --- | --- | ---|
| 1. | [CIFAR10/100](https://www.cs.toronto.edu/~kriz/cifar.html) | Image |
| 2. | [Cod-RNA](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary.html#cod-rna) | Tabular |
| 3. | [Yahoo Answer](https://www.kaggle.com/datasets/soumikrakshit/yahoo-answers-dataset) | Text |
| 4. | [Speech Commands](https://www.kaggle.com/datasets/neehakurelli/google-speech-commands) | Audio |
| 5. | [Brain Tumor MRI](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) | Medical Image |



## Proposed Evaluation Metrics


## Future Direction


# Contributing
We welcome contributions to expand and improve this repository! Here’s how you can help:
1. Add papers
   - Fork the repository, add a paper on README, and submit a pull request.

3. Contributors
   - Hong Xi Tae
   - [Chee Seng Chan](http://cs-chan.com/)
