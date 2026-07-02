# Building-a-SOM

---

## Installation
1. Create and activate a virtual environment:
   - python -m venv venv
   - source venv/bin/activate  (macOS / Linux)
   - venv\Scripts\activate     (Windows)

2. Install dependencies:
   - pip install -r requirements.txt

3. Start Jupyter:
   - jupyter lab
   or
   - jupyter notebook

4. Open `notebooks/Building-a-SOM.ipynb` (or the notebook at repo root).

To run the notebook non‑interactively:
- jupyter nbconvert --to notebook --execute notebooks/Building-a-SOM.ipynb --output executed.ipynb

---

## Usage
The notebook is structured so you can run cells sequentially. Typical flow:
1. Load dataset (Iris example provided). Replace with your own CSV if desired.
2. Preprocess: scaling (StandardScaler), optional PCA for initialization/visualization.
3. Initialize SOM grid size and weights (random or PCA init).
4. Train SOM across epochs with learning rate decay and radius decay.
5. Compute and plot U‑Matrix, hits, component planes.
6. Inspect prototypes and nearest training samples for interpretability.

Example snippet (to run inside a Python cell or script):
```python
from sklearn import datasets
X, y = datasets.load_iris(return_X_y=True)
# scale X, create SOM and train...
