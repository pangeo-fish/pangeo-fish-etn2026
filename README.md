# Fish geolocation with Pangeo-Fish - ETN Symposium 2026 workshop

The content of this repository (folder `docs`) is rendered as an online document using [Jupyter Book](https://jupyterbook.org/en/stable/intro.html). **You can access it [here](https://pangeo-fish.github.io/pangeo-fish-etn2026)**.

## Workshop: Fish geolocation with Pangeo-Fish

This hands-on workshop is given at the [European Tracking Network (ETN) Symposium 2026](https://europeantrackingnetwork.org/) (Thursday 15 October 2026, 15:00 - 16:00 CET, B!NGS Copenhagen). It introduces the [Pangeo](https://pangeo.io) ecosystem (Xarray, Dask, HEALPix) and walks participants through a complete [pangeo-fish](https://github.com/pangeo-fish/pangeo-fish) geolocation workflow on biologging data.

The notebooks run on [Pangeo@EOSC](https://pangeo-data.github.io/pangeo-eosc/) with the Docker image [`ghcr.io/pangeo-fish/pangeo-fish-notebook`](https://github.com/pangeo-fish/pangeo-fish-docker).

👉 **One-click start on Pangeo@EOSC** (login, start the pangeo-fish image, clone/update this repository and open the notebook):
[Start the workshop environment](https://pangeo-eosc.vm.fedcloud.eu/hub/spawn?profile=only-choice&profile-option-only-choice--image--unlisted-choice=ghcr.io%2Fpangeo-fish%2Fpangeo-fish-notebook%3A2026.06.04-aae6eb8&next=%2Fhub%2Fuser-redirect%2Fgit-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Fpangeo-fish%252Fpangeo-fish-etn2026%26urlpath%3Dlab%252Ftree%252Fpangeo-fish-etn2026%252Fdocs%252Fpangeo-fish.ipynb%26branch%3Dmain)

See [Registration to Pangeo@EOSC](https://pangeo-fish.github.io/pangeo-fish-etn2026/users-getting-started.html) for the registration steps (to be done **before** the workshop).

## Build the book locally

```bash
micromamba create -n etn2026 -f .binder/environment.yml
micromamba activate etn2026
jupyter-book build docs
```

The HTML is generated in `docs/_build/html`. The book is deployed automatically to GitHub Pages by [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) on every push to `main` touching `docs/`.

## Acknowledgements

This repository is derived from [pangeo-data/pangeo-bids25](https://github.com/pangeo-data/pangeo-bids25) (Pangeo tutorial at BiDS 2025). The GLORYS notebook (Xarray, Dask, Zarr, HEALPix) is adapted from its *Introduction to HEALPix and Dask* notebook. The pangeo-fish notebook comes from [pangeo-fish/pangeo-fish](https://github.com/pangeo-fish/pangeo-fish/blob/main/notebooks/pangeo-fish.ipynb).
