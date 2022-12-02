# A Training of Trainers Bootcamp on Machine Learning for Earth Observations 

This repository contains materials from the virtual ML4EO Bootcamp run from May 3 through May 14. 

## Organizers

This bootcamp is organized by [Radiant Earth Foundation](www.radiant.earth) and [Makerere University](https://air.ug/) wirth support from [GIZ FAIR Forward, Artificial Intelligence for All, program](https://www.giz.de/expertise/html/61982.html).

## Python Dependencies

In order to run the exercise notebooks, you will need to have Python 3.8 installed. You will also
need to install some Python dependencies. 

If you are running the notebooks using Binder, all dependencies should be included in the host 
environment.

If you are running the notebooks on your local computer, go to the project root and run:

```
pip install -r requirements_dev.txt
```

If you are running the notebooks in Google Colab, you will need to create a new cell in the notebook
with the following content:

```
from pathlib import Path
requirements = Path.cwd().parent.parent / 'binder' / 'requirements.txt'

!pip install -r $requirements
```

There is also an [`environment.yml`](./environment-dev.yml) file that can be used to create a
`conda` environment.

```
conda env create -n my-environment -f environment-dev.yml
```

> **Windows Users**
> 
> Some users were experiencing issues when trying to use `rasterio.warp` functions in a Windows
> environment. This is likely due to [this issue](https://github.com/mapbox/rasterio/issues/2079),
> which was fixed in version 1.2. If you are experiencing issues with `rasterio.warp` on Windows
> please verify that you are using `rasterio>=1.2.0`.
