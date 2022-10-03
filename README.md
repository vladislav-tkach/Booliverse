<!-- PHONY HEADING FOR CODE LINTER -->
<h1 hidden></h1>

<p align="center">
  <a href="https://github.com/vladislav-tkach/Booliverse/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/vladislav-tkach/Booliverse">
  </a>
  <a href="https://github.com/marketplace/actions/super-linter">
    <img src="https://github.com/vladislav-tkach/Booliverse/workflows/Run%20Super-Linter/badge.svg?&colorB=555">
  </a>
  <a href="https://github.com/marketplace/actions/cppcheck-action">
    <img src="https://github.com/vladislav-tkach/Booliverse/workflows/Run%20Cppcheck/badge.svg?&colorB=555">
  </a>
  <a href="https://github.com/marketplace/actions/flawfinder-action">
    <img src="https://github.com/vladislav-tkach/Booliverse/workflows/Run%20flawfinder/badge.svg?&colorB=555">
  </a>
  <a href="https://www.linkedin.com/in/vladyslav-tkach/">
    <img src="https://img.shields.io/badge/-LinkedIn-black.svg?&logo=linkedin&colorB=555">
  </a>
</p>



<!-- PROJECT LOGO -->
<p align="center">
  <h3 align="center">Booliverse</h3>

  <p align="center">
    Boolean logic simulator app
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
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
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Booliverse is a boolean logic simulation app inspired by [BOOLR](http://boolr.me/)([GitHub](https://github.com/GGBRW/BOOLR)).

There are many great logic simulation apps available for free as well as paid, however, I didn't find one that really suit my needs so I made this one. I want to create a free hardware design app for amateurs that enjoy engineering complex systems as well as for teachers and students that are studying computer science.

Key goals I pursue:
* Booliverse is fully free software
* Contribution is welcome and not limited in any way
* It has to be possible to create a complex logic board (for example CPU) without performance decrease

### Built With

* [Qt](https://www.qt.io/)



<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

I hate prerequisites/dependencies that you have to install globally on your PC only to build signle project and not use it anymore. Therefore the only thing you will need to build this project is the C++ toolkit i.e. CMake, build tool and C++ compiler of your choice. (<a href="#how-to-use-a-toolkit-without-installing-it">How to use a toolkit without installing it</a>)
If you don't have any (except C++ toolkit) dependency needed installed on your PC you have two options:
* To download it and install on your PC
* To download it without installing only to build this project

And both are automated! You only have to provide certain flags to CMake during build.

### Installation

1. Clone the repository
   ```sh
   git clone https://github.com/vladislav-tkach/Booliverse.git
   ```
2. Configure the project and generate build files
   ```sh
   cmake ./Booliverse
   ```
3. Build sources
   ```sh
   cmake --build ./Booliverse
   ```

#### How to use a toolkit without installing it

If you for any reason refuse to make changes to PATH environmental variable or you have several toolkits installed on your PC, CMake offers functionality to specify the exact paths to your tools without modifying the PATH. Please go to CMakeUserPresets.md for instructions



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. [Fork the Project](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. [Open a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Vladyslav Tkach - [@m11yy](https://t.me/m11yy) - vladislautkach@gmail.com

Project Link: [https://github.com/vladislav-tkach/Booliverse](https://github.com/vladislav-tkach/Booliverse)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Choose an Open Source License](https://choosealicense.com)
* [Img Shields](https://shields.io)