# White Noise Generator with LFO

A Python-based audio synthesis tool that generates ambient white noise processed with a low-pass filter to simulate the sound of rain. It features a configurable Low Frequency Oscillator (LFO) to introduce dynamic volume pulsing, creating a more natural and organic texture.

## 🎵 Features

* **White Noise Synthesis**: Generates pure white noise using NumPy.
* **Rain Simulation**: Applies a 5th-order Butterworth low-pass filter (2000 Hz cutoff) to soften the high frequencies, creating a "rain" texture.
* **LFO Modulation**: Implements a sine-wave Low Frequency Oscillator to modulate volume over time, adding movement to the static noise.
* **Auto-Normalization**: Automatically detects peak amplitude and normalizes audio to 0 dBFS to prevent clipping or low volume.
* **High Fidelity**: Operates at a standard 48kHz sample rate.

## 🛠 Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-username/white-noise-lfo.git](https://github.com/your-username/white-noise-lfo.git)
    cd white-noise-lfo
    ```

2.  **Install dependencies**
    It is recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Usage

This script is optimized for interactive environments like **Jupyter Notebook** or **Google Colab**, as it uses `IPython.display.Audio` to render playable audio widgets directly in the output.

### Running in Jupyter/Colab
1.  Open the script or copy the code into a notebook cell.
2.  Run the cell.
3.  The script will generate two audio widgets:
    * **Track 1**: Static rain sound (Filtered White Noise).
    * **Track 2**: Dynamic rain sound (Filtered White Noise + LFO Modulation).

### Running Locally
If running as a standard Python script (`python white_noise_generator_with_lfo.py`), the code will compile and execute, but you will not hear audio unless you export the file. *See the "Next Steps" section below regarding file export.*

## ⚙️ Configuration

You can tweak the sound generation by modifying the constants at the top of the script:

| Parameter | Default | Description |
| :--- | :--- | :--- |
| `RAIN_LFO_FREQ` | `1` | The speed of the volume pulse in Hz. (e.g., `0.2` = one pulse every 5 seconds). |
| `RAIN_LFO_DEPTH` | `0.63` | The intensity of the volume change (0.0 to 1.0). Higher values create deeper silence between pulses. |
| `DURATION` | `10` | Length of the audio generation in seconds. |
| `f_cutoff_rain` | `2000` | The cutoff frequency for the low-pass filter. Lower values sound muffled; higher values sound like hissing. |

## 📦 Dependencies

* `numpy` (Signal generation)
* `scipy` (Signal processing and filtering)
* `IPython` (Audio widget playback)

## 👤 Author

**Geoff Bremner**
* [Linktree](https://linktr.ee/gbaudio)

---
*Generated for the White Noise Generator with LFO project.*