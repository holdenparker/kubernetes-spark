FROM jupyter/pyspark-notebook:python-3.9

# Setup password authentication so we don't have to remember tokens (password: "jupyter")
RUN echo "{ \"NotebookApp\": { \"password\": \"sha1:ad16e87de314:a02efac10ccd7ead24e845f438b2b87fe8bc2d0f\" } }" >> ~/.jupyter/jupyter_notebook_config.json
RUN mkdir -p ~/.ipython/profile_default
RUN echo "c.TerminalInteractiveShell.editing_mode = 'vi'" >> ~/.ipython/profile_default/ipython_config.py

RUN conda install -y geopandas
COPY ./MidCoastLakes /home/jovyan/MidCoastLakes
COPY ./jupyter/SIE555-Final.ipynb /home/jovyan
