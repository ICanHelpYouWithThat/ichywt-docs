# ICanHelpYouWithThat Documentation

This is the base git project that will contain the documentation for ICHYWT

---

# Pre-requisites

  - Python > 2.7
  - `pip install sphinx sphinx-autobuild sphinxcontrib-openapi recommonmark sphinx_rtd_theme`

---

# Local setup
- Clone the repo locally
- Navigate into the repo directory, and run `make clean html` and the output will be in `./build/html/index.html`
- To run an auto-updating "live" server, run `make livehtml` and access the documentation locally at `http://127.0.0.1:8000/`
    - Note: This wouldnt update navigation or newer files, which would require a "clean" build
- Once you are satisfied, push the changes to the repo
