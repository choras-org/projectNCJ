# Project NCJ

Hello! This is a template repository in which you can upload your deliverables for the CHORAS ASSA Workshop. The deliverables are

1. 🎧 Impulse response from DE (.wav)

2. 📊 T30 results from DE in (.csv)

3. 5️⃣ Frequencies of first 5 modes from DG in (.csv)

4. (Optional) 📊 T30 results from DG (up to the 250Hz band) in (.csv) as calculated with pyfar

5. 📃 This readme filled with the correct information :)

_Feel free to remove this section when you're done :)_

## Members

- _Niels_
- _Christopher_
- _Jay_

## Process

This is where you can describe how you tackled the task

- First we did..
- Then we tried..
- Finally we..
- etc.

## Input settings

For reproducibility of your results we would like to know what inputs you used to complete your simulations.

### Geometry

Room2215_withAbs_

### Source position

- x: 9.5 m
- y: 6 m
- z: 1.7 m

### Receiver position

- x: 3 m
- y: 4.5 m
- z: 1 m

### Surfaces

If you created materials you can list them here with their absorption coefficients:

- _material name_: 63 Hz, 125 Hz, 250 Hz, 500 Hz, 1000 Hz, 2000 Hz, 4000 Hz

    _Example:_

- My new material, 0.1, 0.2, 0.3, 0.4, 0.5, 0.1, 0.1

Material properties:

- Surface [1]: Wood
- Surface [2]: Wood
- Surface [3]: Single pane of glass, >4 mm
- Surface [4]: Single pane of glass, >4 mm
- Surface [5]: Wood
- Surface [6]: Wood
- Surface [7]: Single pane of glass, >4 mm
- Surface [8]: Wood
- Surface [9]: Wood
- Surface [10]: Perforated panel, 20% open, 20 mm 149 kg/m3 absorber
- Surface [11]: Perforated panel, 20% open, 20 mm 149 kg/m3 absorber
- Surface [12]: Wood
- Surface [13]: Perforated panel, 20% open, 20 mm 149 kg/m3 absorber
- Surface [14]: Perforated panel, 20% open, 20 mm 149 kg/m3 absorber
- Surface [15]: Acoustic ceiling (rockwool), 40 mm, 100 kg/m3, suspended 200 mm
- Surface [16]: Corkfloor tiles


### Settings

You can paste the JSON here by clicking on the Open as JSON button in the Settings tab.

- DE

```json
{
  "sim_len_type": "edt",
  "de_ir_length": 0.5,
  "de_c0": 343,
  "edt": 35,
  "de_lc": 1
}
```

- DG

```json
{
  "dg_freq_upper_limit": 300,
  "dg_c0": 343,
  "dg_rho0": 1.213,
  "dg_ir_length": 1,
  "dg_poly_order": 4,
  "dg_ppw": 2,
  "dg_cfl": 1
}
```

## 3 proposals for improving CHORAS

Here you can list your 3 proposals for improving CHORAS. Out of the box ideas are welcome!

- Proposal 1: Add pause button for simulations.
- Proposal 2: JSON files to import/export source-receiver settings and material settings.
- Proposal 3: Estimation of computation time and mesh size would be really nice to also see in CHORAS itself.
- (Proposal 4: Would be nice to add a short bit of context to some of the more complex settings.)

## Functionality issues

Please list any functionality issues you found:

- When changing source/receiver positions or material types, occasionally the settings are reset to an earlier version.
- The geometry interface is somehow quite demanding for the GPU.
- For DE simulations the docker seems to use only 1 core and limits the frequency to 1.6 GHz instead of 3 GHz.


## Feedback / experience

Below you can tell us your feedback or describe your experience of working with CHORAS today! Please start every bullet with **I like..** or **I wish/wonder..**

- I like ..
- I wish ..
- I wonder ..
- ..
