[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sfarrens/pysap-wtemts-2021/blob/main/Hand-OnPySAP.ipynb)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sfarrens/pysap-wtemts-2021/HEAD?filepath=Hand-OnPySAP.ipynb)

# Hand-On Image Processing with PySAP

> Author: [Samuel Farrens](http://www.cosmostat.org/people/sfarrens)    
> [Where the Earth Meets the Sky workshop](https://indico.nbi.ku.dk/event/1330/), May 2021

<img src="https://github.com/CEA-COSMIC/pysap/raw/master/doc/images/schema.jpg" width=400>

#### Abstract

PySAP (Python Sparse data Analysis Package) is an open-source, multidisciplinary image processing tool developed in collaboration between astrophysicists and biomedical imaging experts at CEA Paris-Saclay through the [COSMIC project](http://cosmic.cosmostat.org/) (see [Farrens et. al (2020)](https://arxiv.org/abs/1910.08465)). The objective of this collaboration being to share the image processing experience gained in different domains with the community.

In this hands-on session I will demonstrate some of the "out of the box" image processing tools available in the PySAP-MRI and PySAP-Astro plugins. In particular, I will focus on some standard problems like denoising or deconvolving galaxy images, and reconstructing subsampled MRI scans of a brain. I will also show how to use some of the modular features of PySAP to design image processing tools for new problems of even different imaging domains.

Throughout the session I will endeavour to provide some basic technical background and present the problems such that it should be possible for everyone in the audience to follow. I will also include links to tutorials for more in-depth explanations of some of these topics for those who are interested.

Finally, I will reserve a few minutes at the end to explain how you can contribute to the development of PySAP.

## Installation

If you are on a computer running Linux or macOS with Python >= 3.6 then it should be as simple as

```bash
$ pip install python-pysap
```

> Here `$` represents your terminal prompt.

this should install the full PySAP suite along with all the required dependencies. Note that if you install the macOS 10.15 wheel you will also need to manually install PyQT5 and the PySAP plug-ins.

```bash
$ pip install pyqt5 pysap-astro pysap-mri
```

If you are running Windows or if the `pip install` fails you can also download the PySAP [Docker](https://www.docker.com/) image as follows

```bash
$ docker pull ceacosmic/pysap
```

which comes with PySAP pre-installed.

> See the [PySAP repository](https://github.com/CEA-COSMIC/pysap#installation) for more installation details and options.

## Running this notebook

Once you have PySAP and [Jupyter](https://jupyter.org/) installed you should be able to run all of the exercises and examples in this notebook without any issues. If you installed PySAP via `pip` then simply run the following command.

```bash
$ jupyter notebook
```

If you installed PySAP via the Docker image then run the following command.

```bash
$ docker run -p 8888:8888 -v ${PWD}:/home ceacosmic/pysap
```

This will run launch Jupyter notebook as usual where you have access to your current working directory but using a Docker container as the backend.

Alternatively, this notebook can be run remotely using either Google Colab or Binder (see badges above).
