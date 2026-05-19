# NaCs 2.0 Cs System Streamlit App

Browser version of the NaCs 2.0 cesium D2 frequency graph GUI.

## Local run

```bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
pip install -r requirements.txt
streamlit run streamlit_app.py
```

On Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run streamlit_app.py
```

## Files

- `cs_frequency_model.py`: physics, AOM metadata, directed frequency graph.
- `streamlit_app.py`: browser GUI.
- `requirements.txt`: packages used by Streamlit Cloud.

## Updating the experiment graph

Edit `cs_frequency_model.py`. The main things to edit are:

- `DEFAULT_RF`
- `AOMS`
- `FREQUENCY_GRAPH_EDGES`
- optionally `BEAM_COLORS`

AOM shift rule:

```text
Delta f_AOM = order * passes * f_RF
```

RF values are positive magnitudes in MHz. The selected AOM order belongs in the
`AOMS` metadata.
