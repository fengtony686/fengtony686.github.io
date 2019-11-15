---
layout:     post
title:      Development of NAS
subtitle:   A Survey Of Neural Architecture Search
date:       2019-11-15
author:     Tony Feng
header-img: img/AutoML.jpg
catalog: true
tags:
    - 论文
    - 学习
    - CS
---

# Abstract
NAS is a set of algorithms to search for the neural architectures. From 2017, the publication date of the first essay delivered by Google Brain about NAS (Zoph and Le, 2016), NAS has become one of the topics of machine learning. In our survey, we will demonstrate the development of NAS from the conventional NAS to PNAS and ENAS. Simultaneously, in the fourth part of our survey, we will demonstrate an application of the NAS algorithms in the ﬁeld of image recognition. In the fifth section, to demonstrate the convenience of NAS, we have done an experiment using AutoKeras on Colab. In the last part of our survey, we show a big picture of the researches done on NAS and then list several possible improvements of NAS in the future years.

# Development of NAS
[**Download PDF**](https://fengtony686.github.io/essay/survey_of_NAS.pdf)\\
[**BibTex**](https://fengtony686.github.io/essay/survey_of_NAS.txt)

# References
Han Cai, Ligeng Zhu, and Song Han. Proxylessnas: Direct neural architecture search on target task and hardware. arXiv preprint arXiv:1812.00332, 2018.\\
F. Chollet. Xception: Deep learning with depthwise separable convolutions. In 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), pages 1800–1807, July 2017. doi: 10.1109/CVPR.2017.195.\\
Boyang Deng, Junjie Yan, and Dahua Lin. Peephole: Predicting network performance before training. ArXiv, abs/1712.03351, 2017.\\
Matthias Feurer, Aaron Klein, Katharina Eggensperger, Jost Springenberg, Manuel Blum, and Frank Hutter. Eﬃcient and robust automated machine learning. In C. Cortes, N. D. Lawrence, D. D. Lee, M. Sugiyama, and R. Garnett, editors, Advances in Neural Information Processing Systems 28, pages 2962–2970. Curran Associates, Inc., 2015. URL http://papers.nips.cc/paper/5872-efficient-and-robust-automated-machine-learning.pdf.\\
Golnaz Ghiasi, Tsung-Yi Lin, and Quoc V Le. Nas-fpn: Learning scalable feature pyramid architecture for object detection. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, pages 7036–7045, 2019.\\
Zichao Guo, Xiangyu Zhang, Haoyuan Mu, Wen Heng, Zechun Liu, Yichen Wei, and Jian Sun. Single path one-shot neural architecture search with uniform sampling. arXiv preprint arXiv:1904.00420, 2019.\\
J. Hu, L. Shen, and G. Sun. Squeeze-and-excitation networks. In 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition, pages 7132–7141, June 2018. doi: 10.1109/CVPR.2018.00745.\\
Haifeng Jin, Qingquan Song, and Xia Hu. Auto-keras: An eﬃcient neural architecture search system. In Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, pages 1946–1956. ACM, 2019.\\
Rafal Jozefowicz, Wojciech Zaremba, and Ilya Sutskever. An empirical exploration of recurrent network architectures. In International Conference on Machine Learning, pages 2342–2350, 2015.\\
FF Li and J Li. Cloud automl: Making ai accessible to every business. Internet: https://www.blog.google/topics/google-cloud/cloud-automl-making-ai-accessibleeverybusiness, 2018.\\
Liam Li and Ameet Talwalkar. Random search and reproducibility for neural architecture search. arXiv preprint arXiv:1902.07638, 2019.\\
Chenxi Liu, Barret Zoph, Maxim Neumann, Jonathon Shlens, Wei Hua, Li-Jia Li, Li Feifei, Alan L. Yuille, Jonathan Huang, and Kevin Murphy. Progressive neural architecture search. ArXiv, abs/1712.00559, 2017.\\
Chenxi Liu, Liang-Chieh Chen, Florian Schroﬀ, Hartwig Adam, Wei Hua, Alan L Yuille, and Li Fei-Fei. Auto-deeplab: Hierarchical neural architecture search for semantic image segmentation. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, pages 82–92, 2019.\\
Hanxiao Liu, Karen Simonyan, and Yiming Yang. Darts: Diﬀerentiable architecture search. arXiv preprint arXiv:1806.09055, 2018.\\
Renqian Luo, Fei Tian, Tao Qin, Enhong Chen, and Tie-Yan Liu. Neural architecture optimization. In Advances in neural information processing systems, pages 7816–7827, 2018.\\
Hieu Pham, Melody Y. Guan, Barret Zoph, Quoc V. Le, and Jeﬀ Dean. Eﬃcient neural architecture search via parameter sharing. ArXiv, abs/1802.03268, 2018.\\
Esteban Real, Alok Aggarwal, Yanping Huang, and Quoc V Le. Regularized evolution for image classiﬁer architecture search. In Proceedings of the AAAI Conference on Artiﬁcial Intelligence, volume 33, pages 4780–4789, 2019.\\
George Seif. Google’s automl will change how businesses use machine learning. Internet: https://towardsdatascience.com/googles-automl-will-change-how-businesses-usemachine-learning-c7d72257aba9, 2018a.\\
George Seif. Everything you need to know about automl and neural architecture search. Internet: https://towardsdatascience.com/everything-you-need-to-know-about-automl-andneural-architecture-search-8db1863682bf, 2018b.\\
Karen Simonyan and Andrew Zisserman. Very deep convolutional networks for large-scale image recognition. arXiv 1409.1556, 09 2014.\\
David R So, Chen Liang, and Quoc V Le. The evolved transformer. arXiv preprint arXiv:1901.11117, 2019.\\
Kevin Swersky, Jasper Snoek, and Ryan P. Adams. Multi-task bayesian optimization. In Proceedings of the 26th International Conference on Neural Information Processing Systems - Volume 2, NIPS’13, pages 2004–2012, USA, 2013. Curran Associates Inc. URL http://dl.acm.org/citation.cfm?id=2999792.2999836.\\
Favio Vzquez. Auto-keras, or how you can create a deep learning model in 4 lines of code. Internet: https://towardsdatascience.com/auto-keras-or-how-you-can-create-adeep-learning-model-in-4-lines-of-code-b2ba448ccf5e, 2018.\\
Sirui Xie, Hehui Zheng, Chunxiao Liu, and Liang Lin. Snas: stochastic neural architecture search. arXiv preprint arXiv:1812.09926, 2018.\\
Barret Zoph and Quoc V. Le. Neural architecture search with reinforcement learning. ArXiv, abs/1611.01578, 2016.\\
Barret Zoph, Vijay Vasudevan, Jonathon Shlens, and Quoc V. Le. Learning transferable architectures for scalable image recognition. 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition, pages 8697–8710, 2017.
