# Classical and Quantum Generative Modeling for Finance

In an era where data-driven insights and predictive analytics play an increasingly critical role in the financial sector, the fusion of classical and quantum generative models, with a special emphasis on Generative Adversarial Networks (GANs), offers an exciting frontier of innovation.

Financial time series data, with its complex, multifaceted nature, has been a longstanding challenge for data scientists, traders and analysts. Traditional approaches often fall short in capturing the intricate patterns and dynamics inherent to financial markets. This repository is dedicated to exploring cutting-edge techniques and methodologies that empower us to generate realistic and informative financial time series data, revolutionizing how we model, forecast and analyze financial markets.

The goal is to provide a comprehensive resource for researchers, developers and enthusiasts in the fields of finance, machine learning and quantum computing. Here, you will find a wealth of code, tutorials and resources designed to demystify generative models, especially GANs, and their applications in the context of financial time series. Whether you are an experienced practitioner or just beginning your journey, this repository aims to be the guiding light through the intricacies of data generation, enabling you to unlock new possibilities in understanding and predicting financial markets.

This repository was created for the needs of the main part of my thesis titled 'Quantum Computing for Generative Modeling and Applications', where the problem of synthetic data generation is tackled. Contributions, questions and insights are invaluable as we can collectively delve into this dynamic and transformative field.

As yet, the following are included:
 - A classical Wasserstein GAN with gradient penalty (WGAN-GP) for generating synthetic loagrithmic returns with the S&P 500 Index as a benchmark.
 - A quantum Wasserstein GAN with gradient penalty (QWGAN-GP) for generating synthetic loagrithmic returns with the S&P 500 Index as a benchmark, featuring diverse architectures based on the parameters and topology of the entangling layers of the quantum generator circuit.

### Wasserstein GAN with Gradient Penalty (WGAN-GP)
In the notebook titled 'WGAN_S&P500' in folder 'Wasserstein GANs', a thorough analysis of several properties that real-world financial data exhibit is conducted. Based on this information, an attempt to implement a Wasserstein GAN with gradient penalty that generates financial time series with such properties is made. As a benchmark, the daily closing values of the S&P 500 Index are used. The WGAN-GP algorithm is based on 'Improved Training of Wasserstein GANs' by I. Gulrajani et. al, publised in 2017 and can be found in https://arxiv.org/pdf/1704.00028.pdf. A similar work may be found in https://studenttheses.universiteitleiden.nl/handle/1887/3278321 by E. Schwander, where his thesis was published in 2022.


### Quantum Wasserstein GAN with Gradient Penalty (QWGAN-GP)
In folder 'Quantum Wasserstein GANs', there are several implementations regarding hybrid classical-quantum generative modeling. The generator of the classical WGAN-GP is replaced by a parameterized quantum circuit, featuring diverse architectures. Schwander conducted a thorough research in terms of the number of qubits and layers used in the quantum generator. In his work, he utilizes non-parameterized entangling layers using CZ gates for coupling and studies two topologies. Motivated by this, we try to reproduce the results and consider additional topologies. Moreover, the quantum circuit architecture is adjusted by introducing entangling layers with trainable parameters using Mølmer-Sørensen gates.

For a detailed description, please check my thesis at: https://doi.org/10.26233/heallink.tuc.98643
