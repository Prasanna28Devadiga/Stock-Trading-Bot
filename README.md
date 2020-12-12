<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the Stock-Trading-Bot and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
***
***
***
*** To avoid retyping too much info. Do a search and replace for the following:
*** Prasanna28Devadiga, Stock-Trading-Bot, twitter_handle, prasanna2019@iiitkottayam.ac.in, upgraded-spork, Agent that used Deep-Q Learning and Experienced replay to make trades(buy/sell/hold) on single stocks
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />

  <h3 align="center">Upgraded-Spork</h3>

  <p align="center">
    Agent that uses Deep-Q Learning and Experienced replay to make trades(buy/sell/hold) on single stocks
    <br />
    <a href="https://github.com/Prasanna28Devadiga/Stock-Trading-Bot">View Demo</a>
    ·
    <a href="https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/issues">Report Bug</a>
    ·
    <a href="https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Beginner-friendly approach at building a single stock trading bot using Reinforcement Learning. Originally intended as a project for a course I took at college, I do plan to make improvements (better algorithms!). Have hardcoded the values for the window size(32) and number of episodes(5000). Have tried training the model on a few equities for a 10-15 episodes and ended up with ~5% profit (could just be noise :smile:). I believe it needs to be trained for atleast a couple hundred episodes before we can see it perform well consistently. 
(P.S. make sure the input data file follows the format as mentioned below)

### Built With

* [Tensorflow](https://www.tensorflow.org/)
* [Keras](https://keras.io/)


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Setting up the Environment
1.Installing TensorFlow
  ```
  [root@host3 ~]# pip install --upgrade pip
You are using pip version 7.1.0, however version 20.0.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Collecting pip
  Downloading https://files.pythonhosted.org/packages/54/0c/d01aa759fdc501a58f431eb594a17495f15b88da142ce14b5845662c13f3/pip-20.0.2-py2.py3-none-any.whl (1.4MB)
    100% |████████████████████████████████| 1.4MB 481kB/s 
Installing collected packages: pip
  Found existing installation: pip 7.1.0
    Uninstalling pip-7.1.0:
      Successfully uninstalled pip-7.1.0
Successfully installed pip-20.0.2
  ```
2. Next, we want to update our setup tools to prevent the following errors if the standard setup tools are used.
  ```
  pip install --upgrade setuptools
Collecting setuptools
  Downloading setuptools-46.0.0-py3-none-any.whl (582 kB)
     |████████████████████████████████| 582 kB 1.5 MB/s 
Installing collected packages: setuptools
  Attempting uninstall: setuptools
    Found existing installation: setuptools 18.0.1
    Uninstalling setuptools-18.0.1:
      Successfully uninstalled setuptools-18.0.1
Successfully installed setuptools-46.0.0
[root@host conf]#
  ```
3. Next, we can move on to installing the current stable release of TensorFlow for CPU and GPU.
  ```
  [root@host3 ~]# pip install tensorflow
Collecting tensorflow
  Downloading tensorflow-2.1.0-cp35-cp35m-manylinux2010_x86_64.whl (421.8 MB)
     |████████████████████████████████| 421.8 MB 15 kB/s 
Collecting keras-applications>=1.0.8
  Downloading Keras_Applications-1.0.8-py3-none-any.whl (50 kB)
     |████████████████████████████████| 50 kB 17.9 MB/s 
Collecting gast==0.2.2
  Downloading gast-0.2.2.tar.gz (10 kB)
Collecting opt-einsum>=2.3.2
  Downloading opt_einsum-3.2.0-py3-none-any.whl (63 kB)
     |████████████████████████████████| 63 kB 7.6 MB/s 
Collecting termcolor>=1.1.0
  Downloading termcolor-1.1.0.tar.gz (3.9 kB)
Collecting six>=1.12.0
  Downloading six-1.14.0-py2.py3-none-any.whl (10 kB)
Collecting numpy<2.0,>=1.16.0
  Downloading numpy-1.18.1-cp35-cp35m-manylinux1_x86_64.whl (19.9 MB)
     |████████████████████████████████| 19.9 MB 6.2 kB/s 
Collecting wheel>=0.26; python_version >= "3"
  Downloading wheel-0.34.2-py2.py3-none-any.whl (26 kB)
Collecting protobuf>=3.8.0
  Downloading protobuf-3.11.3-cp35-cp35m-manylinux1_x86_64.whl (1.3 MB)
     |████████████████████████████████| 1.3 MB 76.8 MB/s 
Collecting tensorflow-estimator<2.2.0,>=2.1.0rc0
  Downloading tensorflow_estimator-2.1.0-py2.py3-none-any.whl (448 kB)
     |████████████████████████████████| 448 kB 77.3 MB/s 
Collecting google-pasta>=0.1.6
  Downloading google_pasta-0.1.8-py3-none-any.whl (57 kB)
     |████████████████████████████████| 57 kB 18.0 MB/s 
Collecting wrapt>=1.11.1
  Downloading wrapt-1.12.1.tar.gz (27 kB)
Collecting grpcio>=1.8.6
  Downloading grpcio-1.27.2-cp35-cp35m-manylinux2010_x86_64.whl (2.7 MB)
     |████████████████████████████████| 2.7 MB 71.3 MB/s 
Collecting absl-py>=0.7.0
  Downloading absl-py-0.9.0.tar.gz (104 kB)
     |████████████████████████████████| 104 kB 88.2 MB/s 
Collecting scipy==1.4.1; python_version >= "3"
  Downloading scipy-1.4.1-cp35-cp35m-manylinux1_x86_64.whl (26.0 MB)
     |████████████████████████████████| 26.0 MB 69.9 MB/s 
Collecting keras-preprocessing>=1.1.0
  Downloading Keras_Preprocessing-1.1.0-py2.py3-none-any.whl (41 kB)
     |████████████████████████████████| 41 kB 651 kB/s 
Collecting tensorboard<2.2.0,>=2.1.0
  Downloading tensorboard-2.1.1-py3-none-any.whl (3.8 MB)
     |████████████████████████████████| 3.8 MB 79.3 MB/s 
Collecting astor>=0.6.0
  Downloading astor-0.8.1-py2.py3-none-any.whl (27 kB)
Collecting h5py
  Downloading h5py-2.10.0-cp35-cp35m-manylinux1_x86_64.whl (2.8 MB)
     |████████████████████████████████| 2.8 MB 76.5 MB/s 
Requirement already satisfied: setuptools in /opt/rh/rh-python35/root/usr/lib/python3.5/site-packages (from protobuf>=3.8.0->tensorflow) (18.0.1)
Collecting google-auth-oauthlib<0.5,>=0.4.1
  Downloading google_auth_oauthlib-0.4.1-py2.py3-none-any.whl (18 kB)
Collecting google-auth<2,>=1.6.3
  Downloading google_auth-1.11.2-py2.py3-none-any.whl (76 kB)
     |████████████████████████████████| 76 kB 19.0 MB/s 
Collecting werkzeug>=0.11.15
  Downloading Werkzeug-1.0.0-py2.py3-none-any.whl (298 kB)
     |████████████████████████████████| 298 kB 72.9 MB/s 
Collecting markdown>=2.6.8
  Downloading Markdown-3.2.1-py2.py3-none-any.whl (88 kB)
     |████████████████████████████████| 88 kB 26.9 MB/s 
Collecting requests<3,>=2.21.0
  Downloading requests-2.23.0-py2.py3-none-any.whl (58 kB)
     |████████████████████████████████| 58 kB 20.8 MB/s 
Collecting requests-oauthlib>=0.7.0
  Downloading requests_oauthlib-1.3.0-py2.py3-none-any.whl (23 kB)
Collecting pyasn1-modules>=0.2.1
  Downloading pyasn1_modules-0.2.8-py2.py3-none-any.whl (155 kB)
     |████████████████████████████████| 155 kB 83.1 MB/s 
Collecting cachetools<5.0,>=2.0.0
  Downloading cachetools-4.0.0-py3-none-any.whl (10 kB)
Collecting rsa<4.1,>=3.1.4
  Downloading rsa-4.0-py2.py3-none-any.whl (38 kB)
Collecting urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1
  Downloading urllib3-1.25.8-py2.py3-none-any.whl (125 kB)
     |████████████████████████████████| 125 kB 73.9 MB/s 
Collecting certifi>=2017.4.17
  Downloading certifi-2019.11.28-py2.py3-none-any.whl (156 kB)
     |████████████████████████████████| 156 kB 80.8 MB/s 
Collecting chardet<4,>=3.0.2
  Downloading chardet-3.0.4-py2.py3-none-any.whl (133 kB)
     |████████████████████████████████| 133 kB 87.7 MB/s 
Collecting idna<3,>=2.5
  Downloading idna-2.9-py2.py3-none-any.whl (58 kB)
     |████████████████████████████████| 58 kB 20.3 MB/s 
Collecting oauthlib>=3.0.0
  Downloading oauthlib-3.1.0-py2.py3-none-any.whl (147 kB)
     |████████████████████████████████| 147 kB 82.4 MB/s 
Collecting pyasn1<0.5.0,>=0.4.6
  Downloading pyasn1-0.4.8-py2.py3-none-any.whl (77 kB)
     |████████████████████████████████| 77 kB 8.7 MB/s 
Installing collected packages: numpy, six, h5py, keras-applications, gast, opt-einsum, termcolor, wheel, protobuf, tensorflow-estimator, google-pasta, wrapt, grpcio, absl-py, scipy, keras-preprocessing, oauthlib, urllib3, certifi, chardet, idna, requests, requests-oauthlib, pyasn1, pyasn1-modules, cachetools, rsa, google-auth, google-auth-oauthlib, werkzeug, markdown, tensorboard, astor, tensorflow
    Running setup.py install for gast ... done
    Running setup.py install for termcolor ... done
    Running setup.py install for wrapt ... done
    Running setup.py install for absl-py ... done
Successfully installed absl-py-0.9.0 astor-0.8.1 cachetools-4.0.0 certifi-2019.11.28 chardet-3.0.4 gast-0.2.2 google-auth-1.11.2 google-auth-oauthlib-0.4.1 google-pasta-0.1.8 grpcio-1.27.2 h5py-2.10.0 idna-2.9 keras-applications-1.0.8 keras-preprocessing-1.1.0 markdown-3.2.1 numpy-1.18.1 oauthlib-3.1.0 opt-einsum-3.2.0 protobuf-3.11.3 pyasn1-0.4.8 pyasn1-modules-0.2.8 requests-2.23.0 requests-oauthlib-1.3.0 rsa-4.0 scipy-1.4.1 six-1.14.0 tensorboard-2.1.1 tensorflow-2.1.0 tensorflow-estimator-2.1.0 termcolor-1.1.0 urllib3-1.25.8 werkzeug-1.0.0 wheel-0.34.2 wrapt-1.12.1
[root@host conf]# 
  ```
4. To confirm that our installation is successful, we can run one of the following two commands. 
```
[root@host ~]# pip list | grep tensorflow
tensorflow 2.1.0
tensorflow-estimator 2.1.0
[root@host conf]#
```
5. Installing Keras
  ```
  [root@host ~]# pip install keras
Collecting keras
  Downloading Keras-2.3.1-py2.py3-none-any.whl (377 kB)
     |████████████████████████████████| 377 kB 1.5 MB/s 
Requirement already satisfied: scipy>=0.14 in /opt/rh/rh-python35/root/usr/lib64/python3.5/site-packages (from keras) (1.4.1)
Requirement already satisfied: h5py in /opt/rh/rh-python35/root/usr/lib64/python3.5/site-packages (from keras) (2.10.0)
Requirement already satisfied: six>=1.9.0 in /opt/rh/rh-python35/root/usr/lib/python3.5/site-packages (from keras) (1.14.0)
Requirement already satisfied: keras-preprocessing>=1.0.5 in /opt/rh/rh-python35/root/usr/lib/python3.5/site-packages (from keras) (1.1.0)
Requirement already satisfied: numpy>=1.9.1 in /opt/rh/rh-python35/root/usr/lib64/python3.5/site-packages (from keras) (1.18.1)
Collecting pyyaml
  Downloading PyYAML-5.3.tar.gz (268 kB)
     |████████████████████████████████| 268 kB 6.4 MB/s 
Requirement already satisfied: keras-applications>=1.0.6 in /opt/rh/rh-python35/root/usr/lib/python3.5/site-packages (from keras) (1.0.8)
Building wheels for collected packages: pyyaml
  Building wheel for pyyaml (setup.py) ... done
  Created wheel for pyyaml: filename=PyYAML-5.3-cp35-cp35m-linux_x86_64.whl size=44228 sha256=60be7547ea2c16c5d689381cf523c6ce9bf7c03e55cc81a8dd9b830a16fc22cd
  Stored in directory: /root/.cache/pip/wheels/4d/28/ad/d9c3d2a22dbe17b0d7019bbe876af34feabf61a214973481e9
Successfully built pyyaml
Installing collected packages: pyyaml, keras
Successfully installed keras-2.3.1 pyyaml-5.3
[root@host conf]#
  ```
6. Again, we check the output of the version installed.
  ```
[root@host conf]# pip list | grep Keras
Keras                2.3.1     
Keras-Applications   1.0.8     
Keras-Preprocessing  1.1.0     
[root@host conf]#
  ```
7. Preparing the Data <br>
    Download the stock data you plan on training the agent from [Yahoo Finance](https://in.finance.yahoo.com/). 
    Drop the Date column (or shift it to another location)<br>
    A simple moving point average can be used (period = last 5/7 days) to help remove noise from the data<br>
    The input file must be in a csv format<br>
    
8. Clone the Stock-Trading-Bot
   ```sh
   git clone https://github.com/Prasanna28Devadiga/Stock-Trading-Bot.git
   ```
<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Prasanna Devadiga - [@Prasanna280](https://twitter.com/https://twitter.com/Prasanna280) - prasanna2019@iiitkottayam.ac.in

Project Link: [https://github.com/Prasanna28Devadiga/Stock-Trading-Bot](https://github.com/Prasanna28Devadiga/Stock-Trading-Bot)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* Amazing tutorial on setting up the required environment for this project by [liquidweb.com](https://www.liquidweb.com/kb/how-to-install-keras/#:~:text=There%20are%20two%20ways%20of,that%20is%20the%20one%20recommended.&text=Again%2C%20we%20check%20the%20output%20of%20the%20version%20installed.)
* Tutorial to build the bot from [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2020/10/reinforcement-learning-stock-price-prediction/)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/Prasanna28Devadiga/Stock-Trading-Bot.svg?style=for-the-badge
[contributors-url]: https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Prasanna28Devadiga/Stock-Trading-Bot.svg?style=for-the-badge
[forks-url]: https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/network/members
[stars-shield]: https://img.shields.io/github/stars/Prasanna28Devadiga/Stock-Trading-Bot.svg?style=for-the-badge
[stars-url]: https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/stargazers
[issues-shield]: https://img.shields.io/github/issues/Prasanna28Devadiga/Stock-Trading-Bot.svg?style=for-the-badge
[issues-url]: https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/issues
[license-shield]: https://img.shields.io/github/license/Prasanna28Devadiga/Stock-Trading-Bot.svg?style=for-the-badge
[license-url]: https://github.com/Prasanna28Devadiga/Stock-Trading-Bot/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/prasanna-devadiga/
