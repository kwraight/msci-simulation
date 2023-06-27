# msci-simulation

Allpix based masters project telescope simulation

Useful links:
 - [allpix**2](https://allpix-squared.docs.cern.ch/docs/)
 - [markdown](https://www.google.com/search?client=safari&rls=en&q=github+markdown+cheat+sheet&ie=UTF-8&oe=UTF-8)

---

## Notebooks

Python based Jupyter notebooks for simple analysis and data visualiastion

---

## Runnning Notebooks with Docker

Using docker for Jupyter [instructions](https://towardsdatascience.com/how-to-run-jupyter-notebook-on-docker-7c9748ed209f)

Quick set-up:
 - run docker jupyter container interactively (use -it arguments)
    >  docker run -it -p 8888:8888 -v $(pwd):/home/jovyan/work jupyter/minimal-notebook /bin/bash
     - mapped to port 8888
     - local directory mounted (for Windows $(pwd) --> $PWD)
     - running bash
 - when inside container, install python packages
    > python -m pip install -r /home/jovyan/work/requirements.txt
 - run notebook
    > jupyter notebook

    You should see output in the terminal like:

    >[I 12:10:59.961 NotebookApp] Jupyter Notebook 6.5.4 is running at:
    >[I 12:10:59.961 NotebookApp] http://e403f18e2f9c:8888/?>token=e1a72ce91c01d41f010a710e60d31e0070d2398f0c621eb5
    >[I 12:10:59.961 NotebookApp]  or http://127.0.0.1:8888/?>token=e1a72ce91c01d41f010a710e60d31e0070d2398f0c621eb5
    >[I 12:10:59.961 NotebookApp] Use Control-C to stop this server and >shut down all kernels (twice to skip confirmation).

 - open Jupyter GUI in browser with '127.0.0.1' link, e.g. here: 
    > http://127.0.0.1:8888/?token=e1a72ce91c01d41f010a710e60d31e0070d2398f0c621eb5
     - __NB__ you must include the token
 - navigate to notebooks and run
     - to close notebooks:
         - ctrl+c in terminal running docker
         - if browser tab doesn't close, enter different URL and close
