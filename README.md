[![Documentation Status](https://readthedocs.org/projects/ichywt-docs/badge/?version=latest)](http://ichywt-docs.readthedocs.io/en/latest/?badge=latest)

# ICanHelpYouWithThat Documentation

This is the base git project that will contain the documentation for ICHYWT. The documentation can be found at [http://ichywt-docs.readthedocs.io/](http://ichywt-docs.readthedocs.io/).

The "Read the docs" build page is here: [https://readthedocs.org/projects/ichywt-docs/](https://readthedocs.org/projects/ichywt-docs/)
---

# Pre-requisites

  - Python > 2.7
  - `pip install sphinx sphinx-autobuild sphinxcontrib-openapi recommonmark sphinx_rtd_theme`

---

# Local setup for Editors
- Clone the repo locally
- Navigate into the repo directory, and run `make clean html` and the output will be in `./build/html/index.html`
- To run an auto-updating "live" server, run `make livehtml` and access the documentation locally at `http://127.0.0.1:8000/`
    - Note: Run `make html` once for now since livehtml would fail if the "build" directory is missing.
    - Note: This wouldnt update navigation or newer files, which would require a "clean" build
- Once you are satisfied, push the changes to the repo
