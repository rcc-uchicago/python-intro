---
layout: page
title: Setup
permalink: /setup/
---

You need to download some files to follow this lesson:

1. Make a new folder on your Desktop called `python-intro-inflammation`.
2. Download [python-intro-inflammation-data.zip][zipfile] and move the file to this folder.
3. If it's not unzipped yet, double-click on it to unzip it. You should end up with a new folder called `data`.
4. You can access this folder from the Unix shell with:

~~~
$ cd
$ cd Desktop/python-novice-inflammation/data
~~~
{: .source}

If you will be using the Jupyter (IPython) notebook for the lesson,
you have one of the following options:

1. Install [Anaconda](http://swcarpentry.github.io/workshop-template/#setup) on your computer which includes the notebook.
2. Use [Jupyter Online](https://try.jupyter.org)
3. Use https://jupyter.rcc.uchicago.edu if you have an RCC account. The Jupyter notebook on RCC uses Python 2 by default. Please login to Midway1 and run the following commands to add Python 3 to the Jupyter notebook:

~~~
$ module load python/3.4-2015q1
$ python -m ipykernel install --user --name py35 --display-name "Python 3"
~~~
{: .source}

To start the notebook, depending on which of the above methods you have selected, you could use your browser or start a terminal and type the command:

~~~
$ jupyter notebook
~~~
{: .source}


[zipfile]: {{ page.root }}/data/python-intro-inflammation-data.zip
