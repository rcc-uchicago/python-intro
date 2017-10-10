---
layout: page
title: Setup
permalink: /setup/
---

You need to download some files to follow this lesson:

1. Make a new folder on your Desktop called `python-intro-inflammation`.
2. Download [python-intro-inflammation-data.zip][zipfile] and move the file to this folder.
3. If it's not unzipped yet, double-click on it to unzip it. You should end up with a new folder called `data`.
4. You can access this folder from terminal using the followig commands:

~~~
$ cd
$ cd Desktop/python-intro-inflammation/data
~~~
{: .source}

If you will be using the Jupyter (IPython) notebook for the lesson,
you have one of the following options:

1. Install [Anaconda](http://swcarpentry.github.io/workshop-template/#python) on your computer which includes the notebook.
2. Use [Jupyter Online](https://try.jupyter.org) (This server disconnects every few minutes so it is not reliable to use)
3. Use [Jupyter hub](https://jupyter.rcc.uchicago.edu) if you have an RCC account. The Jupyter hub on RCC uses Anaconda Python 2 by default. Please login to Midway1 and run the following commands to add Anaconda Python 3 to the Jupyter notebook:

~~~
$ module load Anaconda3
$ python -m ipykernel install --user --name ipy35 --display-name "Python 3"
~~~
{: .source}

> ## Using other versions of Python
> If you want to use a version of Python other than Anaconda, you need to edit the `kernel.json` file to setup the `LD_LIBRARY_PATH` correctly. The following commands load a version of Python on Midway and create a new kernel:
>
> ~~~
> $ module load python/3.4-2015q1
> $ python -m ipykernel install --user --name ipy34 --display-name "Python 3.4-2015q1"
> ~~~
> {: .source}
>
> Then, you need to edit the `~/.local/share/jupyter/ipy34/kernel.json` file to look like this:
>
> ~~~
> {
> "display_name": "Python 3.4-2015q1",
> "language": "python",
> "argv": [
>  "/software/python-3.4-2015q1-el6-x86_64/bin/python",
>  "-m",
>  "ipykernel",
>  "-f",
>  "{connection_file}"
> ],
> "env":{
>     "LD_LIBRARY_PATH":"/software/python-3.4-2015q1-el6-x86_64/lib"}
> }
> ~~~
> {: .source}
{: .callout}

To start the notebook, do one of the following (depending on which of the above methods you have selected):

1. Start a browser on your computer and access one of the websites mentioned in item 3 or 4 (above) to launch the Jupyter notebook
  * You need to upload the data folder to the remote server. Once you launched the notebook, use the New button to create a new folder and the Upload button to upload the content of the data folder to the folder that you created. (Please see the following figure.)
  
  ![jupyter interface](../fig/jupyter.jpg) 
2. Start a terminal and type the following command (assuming you are in the `data` folder):

~~~
$ jupyter notebook
~~~
{: .source}


[zipfile]: {{ page.root }}/data/python-intro-inflammation-data.zip
