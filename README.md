# Combining Signals for Enhanced Alpha

### Project Motivation:

1. To combine signals using a random forest model to create an enhanced alpha from an ensemble of other alpha factors and features.

### The notebook is separated into three parts:
1. The first part covers data collection and inspection, stock universe construction, and definition and construction of alpha factors.
    - note this project makes specific use of the Zipline library which was created by Quantopian, a crowd-sourced investment fund, which closed in 2020. The library is still maintained by Stefan Jansen, author of the book 'Machine Learning for Algorithmic Trading.' See [zipline homepage](https://zipline.ml4trading.io/) for specifics.
2. The second part covers building and training different size random forest classifiers using the alpha factors and a few additional features, and evaluating the different models accuracy in comparison to the alpha factor's individual performance.
3. The third part covers methods for making sure the the samples used to fit the random forest are independent and identically distributed (IID) to mitigate overfitting.

### File Descriptions:


    project_7.ipynb
    | - Jupyter notebook containing all data collection, cleaning, and data frame construction, alpha factor definition and construction, random forest model definition, construction and testing, and overlapping sample removal.
    helper.py
    |- helper file to abstract some data collection and import statements
    project_helper.py
    |- helper file to abstract graphing functions
    project_test.py
    |- unit tests to flag any major errors
    README.md


### Installations:
- This project uses a dataset hosted on Udacity instances for the "AI for Trading" course, constructed as a bundle using the 'Zipline' library. You can swap out the code for extracting the dataset with your own custom data access/collection logic.
- Zipline was created by Quantopian, a crowd-sourced investment fund, which closed in 2020. The library is still maintained by Stefan Jansen, author of the book 'Machine Learning for Algorithmic Trading.' See [zipline homepage](https://zipline.ml4trading.io/) for specifics.
- You will need a python environment with the following:
    - see the `requirements.txt` file for specific packages and versions
    - python verson 3.7 or higher

### Instructions:
1. Run each cell in 'project_7.ipynb' in sequence. Make sure the Jupyter notebook is in the same level of the directory as 'helper.py', 'project_helper.py', 'project_tests.py', and 'tests.py'.