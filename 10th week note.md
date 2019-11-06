# 第十周笔记



## Today Reading 

Mon, Nov 4, 2019

[Habitat: A Platform for Embodied AI Research](http://arxiv.org/abs/1904.01201)

### Abstract 

We present Habitat, a platform for research in embodied artificial intelligence (AI). Habitat enables training embodied agents (virtual robots) in highly efficient photorealistic 3D simulation. Specifically, Habitat consists of: 

+ (i) Habitat-Sim: 

  a flexible, high-performance 3D simulator with configurable agents, sensors, and generic 3D dataset handling. Habitat-Sim is fast – when rendering a scene from Matterport3D, it achieves several thousand frames per second (fps) running single-threaded, and can reach over 10,000 fps multi-process on a single GPU.

+  (ii) Habitat-API: 

  a modular high-level library for end-to- end development ofembodied AI algorithms – defining tasks (e.g. navigation, instruction following, question answering), configuring, training, and benchmarking embodied agents.

These large-scale engineering contributions enable us to answer scientific questions requiring experiments that were till now impracticable or ‘merely’ impractical. Specifically, in the context of point-goal navigation: (1) we revisit the comparison between learning and SLAM approaches from two recent works [19, 16] and find evidence for the opposite conclusion – that learning outperforms SLAM ifscaled to an order of magnitude more experience than previous investigations, and (2) we conduct the first cross-dataset generalization experiments {train, test} × {Matterport3D, Gibson} for multiple sensors {blind, RGB, RGBD, D} and find that only agents with depth (D) sensors generalize across datasets. We hope that our open-source platform and these findings will advance research in embodied AI.

---



## Today Reading 

Tus, Nov 5, 2019

[Few-Shot Image Recognition with Knowledge Transfer]()

### Abstract

Human can well recognize images of novel categories just after browsing few examples of these categories. One possible reason is that they have some external discriminative visual information about these categories from their prior knowledge. Inspired from this, we propose a novel Knowledge Transfer Network architecture (KTN) for few- shot image recognition. The proposed KTN model jointly incorporates visual feature learning, knowledge inferring and classifier learning into one unified framework for their optimal compatibility. First, the visual classifiers for novel categories are learned based on the convolutional neu- ral network with the cosine similarity optimization. To fully explore the prior knowledge, a semantic-visual mapping network is then developed to conduct knowledge inference, which enables to infer the classifiers for novel categories from base categories. Finally, we design an adaptive fusion scheme to infer the desired classifiers by effectively integrat- ing the above knowledge and visual information. Extensive experiments are conducted on two widely-used Mini- ImageNet and ImageNet Few-Shot benchmarks to evaluate the effectiveness of the proposed method. The results compared with the state-of-the-art approaches show the encouraging performance of the proposed method, especially on 1-shot and 2-shot tasks.

---



## Today Reading 

Wed, Nov 6, 2019

[Generation of 3D Brain MRI Using Auto-Encoding Generative Adversarial Networks](https://link.springer.com/chapter/10.1007%2F978-3-030-32248-9_14)

### Abstract

As deep learning is showing unprecedented success in medical image analysis tasks, the lack of sufficient medical data is emerging as a critical problem. While recent attempts to solve the limited data problem using Generative Adversarial Networks (GAN) have been successful in generating realistic images with diversity, most of them are based on image-to-image translation and thus require extensive datasets from different domains. Here, we propose a novel model that can successfully generate 3D brain MRI data from random vectors by learning the data distribution. Our 3D GAN model solves both image blurriness and mode collapse problems by leveraging *𝛼*α-GAN that combines the advantages of Variational Auto-Encoder (VAE) and GAN with an additional code discriminator network. We also use the Wasserstein GAN with Gradient Penalty (WGAN-GP) loss to lower the training instability. To demonstrate the effectiveness of our model, we generate new images of normal brain MRI and show that our model outperforms baseline models in both quantitative and qualitative measurements. We also train the model to synthesize brain disorder MRI data to demonstrate the wide applicability of our model. Our results suggest that the proposed model can successfully generate various types and modalities of 3D whole brain volumes from a small set of training data.