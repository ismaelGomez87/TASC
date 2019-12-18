# A Tool for Allergy Severity Scoring (TASC)

In this repository, we introduce a tool to score allergic reactions on the basis of their symptoms. This tool was developed and validated under the scope of food allergic reactions, but should be applicable to any allergic reaction.

## Requirements

This tool was developed under R version 3.2.2, and tested under versions up to 3.6.1. RStudio is not needed but recommended for its use. You can download R and RStudio for free from the following links:

https://cran.r-project.org/bin/
https://rstudio.com/

## General description

The TASC software tool is designed to score allergic reactions on the basis of two aspects:
1) The organs/systems affected.
2) The symptoms within those organs/systems.

The way these scores are generated is described in here [LINK to paper]. This tool is capable of automatically processing data files of patients and their symptoms, generating new files with the nFASS, oFASS-5 and oFASS-3 scores attached as new variables to be used for further processing. The tool is also capable of generating descriptives of the population, including descriptives of severity.

## User guide

The TASC software tool is written in R, and can be executed using this software. Instead of working as an R repository available for download and install as an R package, this tool should be used independently. 

The TASC tool reads files written in table format. The main format is .csv, but it supports other formats (see below). Symptoms should be encoded in binary variables, with one value indicating the presence of the symptom and other value indicating its absence. If symptoms are graded in levels of intensity, the data should be converted to binary form before it's provided to the tool. There is no need to have specific variables indicating which organs are affected. This information is tied to the symptoms and has to be specified to the program as indicated below.

The TASC tool exploits the property of R of variables being inherited by sub-environments. This way, key variables for computation can be defined in an external file. There, the user can describe his/her database names, allowing the TASC tool to identify them and use them internally. In this way, datasets with different symptoms defined can be analyzed with help of this tool, just by specifying key aspects such as the symptoms, systems associated to those symptoms, exponents and weights. In case you don't know what exponents to use, we recommend sticking to the values predefined on the intial work, that can be found in here.

[PENDING - LINK to paper].

The TASC tool will take an input file, that can be in the following formats: .xls, .csv, .dta (STATA), .sav (SPSS), and will return the following:
- A new file (.csv) with recoded symptoms (will keep the original values) and the nFASS, oFASS-5 and oFASS-3 scores.
- A population descriptive (in the Results/1\ -\ DatabaseDescriptive folder).
- A descriptive of severity of the population (in the Results/5\ -\ SeverityStudies folder).
...

To make use of this tool, the data files should be inserted in the Data folder. Then, the TASC_input.R file should be edited. The TASC_input.R file contains all the values that are specific to the dataset that's being analyzed, including the data file name, variable names, variable values (i.e. how positive and negative values are encoded) and groupings of symptoms within organs/systems. The user must edit this file to make this values correspond to those on his/her dataset, allowing TASC to read it, process it, and generate the FASS scores.

## Tutorial

[TO BE DONE]

## Acknowledgements

This work was developed within the scope of the ARADyAL network, within the IdISSC institute at Hospital Clínico San Carlos (Spain).

www.idissc.org

[LOGO ARADYAL]



## Rename this repository to publish your site

We've already set-up a GitHub Pages website for you, based on your personal username. This repository is called `hello-world`, but you'll rename it to: `username.github.io`, to match your website's URL address. If the first part of the repository doesn’t exactly match your username, it won’t work, so make sure to get it right.

Let's get started! To update this repository’s name, click the `Settings` tab on this page. This will take you to your repository’s settings page. 

![repo-settings-image](https://user-images.githubusercontent.com/18093541/63130482-99e6ad80-bf88-11e9-99a1-d3cf1660b47e.png)

Under the **Repository Name** heading, type: `username.github.io`, where username is your username on GitHub. Then click **Rename**—and that’s it. When you’re done, click your repository name or browser’s back button to return to this page.

<img width="1039" alt="rename_screenshot" src="https://user-images.githubusercontent.com/18093541/63129466-956cc580-bf85-11e9-92d8-b028dd483fa5.png">

Once you click **Rename**, your website will automatically be published at: https://your-username.github.io/. The HTML file—called `index.html`—is rendered as the home page and you'll be making changes to this file in the next step.

Congratulations! You just launched your first GitHub Pages website. It's now live to share with the entire world

## Making your first edit

When you make any change to any file in your project, you’re making a **commit**. If you fix a typo, update a filename, or edit your code, you can add it to GitHub as a commit. Your commits represent your project’s entire history—and they’re all saved in your project’s repository.

With each commit, you have the opportunity to write a **commit message**, a short, meaningful comment describing the change you’re making to a file. So you always know exactly what changed, no matter when you return to a commit.

## Practice: Customize your first GitHub website by writing HTML code

Want to edit the site you just published? Let’s practice commits by introducing yourself in your `index.html` file. Don’t worry about getting it right the first time—you can always build on your introduction later.

Let’s start with this template:

```
<p>Hello World! I’m [username]. This is my website!</p>
```

To add your introduction, copy our template and click the edit pencil icon at the top right hand corner of the `index.html` file.

<img width="997" alt="edit-this-file" src="https://user-images.githubusercontent.com/18093541/63131820-0794d880-bf8d-11e9-8b3d-c096355e9389.png">


Delete this placeholder line:

```
<p>Welcome to your first GitHub Pages website!</p>
```

Then, paste the template to line 15 and fill in the blanks.

<img width="1032" alt="edit-githuboctocat-index" src="https://user-images.githubusercontent.com/18093541/63132339-c3a2d300-bf8e-11e9-8222-59c2702f6c42.png">


When you’re done, scroll down to the `Commit changes` section near the bottom of the edit page. Add a short message explaining your change, like "Add my introduction", then click `Commit changes`.


<img width="1030" alt="add-my-username" src="https://user-images.githubusercontent.com/18093541/63131801-efbd5480-bf8c-11e9-9806-89273f027d16.png">

Once you click `Commit changes`, your changes will automatically be published on your GitHub Pages website. Refresh the page to see your new changes live in action.

:tada: You just made your first commit! :tada:

## Extra Credit: Keep on building!

Change the placeholder Octocat gif on your GitHub Pages website by [creating your own personal Octocat emoji](https://myoctocat.com/build-your-octocat/) or [choose a different Octocat gif from our logo library here](https://octodex.github.com/). Add that image to line 12 of your `index.html` file, in place of the `<img src=` link.

Want to add even more code and fun styles to your GitHub Pages website? [Follow these instructions](https://github.com/github/personal-website) to build a fully-fledged static website.

![octocat](./images/create-octocat.png)

## Everything you need to know about GitHub

Getting started is the hardest part. If there’s anything you’d like to know as you get started with GitHub, try searching [GitHub Help](https://help.github.com). Our documentation has tutorials on everything from changing your repository settings to configuring GitHub from your command line.
