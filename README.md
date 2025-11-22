# IDD_Final_Project

## Set-up 

One pi must host. The other Pis can act as instruments.

First-time set up:

```
python -m venv .venv
source .venv/bin/activate
pip install -r requirements-pi.txt
```

For the hosting Pi:
1. Set up Bluetooth speaker (can connect via VNC Viewer)
2. We use the class server. We can set up our viewer by running `python mqtt_viewer_instrument.py`

For the instrument Pis:
1. Run the corresponding publisher (`python <instrument_name>_publisher.py`)

## Generating Rhythm Charts
We're planning to use Tone.js to generate sounds. Please use `modified_song.json` as a reference.

Currently, for each track, we support the following action -> sound mapping (in `notes_to_utensil.json`)
- Tracks named "Instrument 1" map to the pan. 
    - Low flame ->  C4
    - Medium flame -> D4
    - High flame -> E4
- Tracks named "Instrument 2" map to the cutting board. 
    - Cutting object 1 -> A3
    - Cutting object 2 -> B3
    - Cutting object 3 -> C4
- Tracks named "Instrument 3" map to the mixing bowl. 
    - Right now, we just ensure the mixing bowl is moving when any note appears


## TO DO LIST:
- show beats on the frontend
- frontend: show instruments movement with real actions
- design/create physical prototypes
- create hold notes for both mixing bowl AND pan