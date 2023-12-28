# Introduction to Julia for Data Science
## Working with tabular data
Day 1 (Tuesday, Jan 16, 2024, 11:00am – 12:30pm)



**Julia installation instructions**

© 2024 Przemysław Szufel under the terms of MIT License


**What is Julia**

Julia is a new Open Source language designed for science and data analysis. With the stable 1.0 version released in August 2018, an exponential growth of language popularity has been observed and the language is in the top-20 programming languages in IEEE Spectrum ranking and top-10 programming languages developed on GitHub. Julia takes “walks like Python, runs like C” approach and is a perfect replacement for Matlab, Python and R scientific data workflow, yet due to its speed it can be also used to implement computation intensive algorithms that are normally implemented in languages such as Java or C++. Nowadays, the most popular Julia applications include computations related to data science, machine learning, numerical simulation, quantitative economics, applied mathematics, physics, astronomy, chemistry, and bioinformatics.

**Installation instructions**

1. Please download Julia from [https://julialang.org/downloads/](https://julialang.org/downloads/) and follow the installation instructions presented at https://julialang.org/downloads/platform/. During the workshop we will be using the Stable Release **v1.10.0**. The 64-bit version is recommended. (Note that there is a problem with installer of the latest 1.10.0 version of Julia on Windows which might cause problems with package installation in some cases).

2. Install Julia packages that will be used throughout the workshop. Once Julia is installed please follow the steps:

    1. Clone this repository by running the following git command:
        ```
        git clone https://github.com/pszufe/2024_MIT_18.S097_Introduction-to-Julia-for-Data-Science.git
        ```

    2. Change the directory to where `Project.toml` and `Manifest.toml` files are located
        ```
        cd "2024_MIT_18.S097_Introduction-to-Julia-for-Data-Science"
        ```
    3. Run the Julia console or in the command line (run command **julia** in the project folder). Once Julia interpreter is running paste the following Julia code:
        ```
        using Pkg
        pkg"activate ."
        pkg"instantiate"
        using Conda
        Conda.runconda(`install jupyter --yes`)
        Conda.runconda(`install matplotlib --yes`)

        ```

4. The recommended programming environment for the Julia language is Visual Studio Code (https://code.visualstudio.com/) with Julia extension. Please follow the steps below:

    a) Download and install VS Code (available at https://code.visualstudio.com/download/)

    b) Start VS Code, click View->Command Palette...  and type `View: Show Extensions` to go to the extension manager

    c) In the extension manager search box type “Julia”

    d) On the top of the extension list you should see “Julia Language Support” – click *Install* to install the extension.

    If you run into any installation problem, more detailed instructions can be found in https://github.com/julia-vscode/julia-vscode#getting-started


5. During the workshop will be mostly working with Julia within Jupyter notebook (this can be also used instead of VS Code)

    To run Julia inside a Jupyter notebook start the Julia console (this assumes that the console is run in the main folder of this repository) and run the two following commands:
    ```
    using Pkg
    Pkg.activate(".")
    using IJulia
    notebook(dir=".")
    ```
    After running the above commands a new web browser tab should open with Jupyter Notebook.



**Literature**

1. Julia Language Manual, https://docs.julialang.org/en/v1/

2. The Julia Express - A concise Julia language introductory manual for programmers, https://github.com/bkamins/The-Julia-Express/

3. B. Kaminski: Julia for Data Analysis, Manning, 2023, https://www.manning.com/books/julia-for-data-analysis
