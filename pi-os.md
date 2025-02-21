# Software Setup

If you have done a full Raspberry Pi OS install, Git should already be installed. But just in case, let's ensure Git is installed, clone the repository, switch to the `no_mic` branch, and run the installer:

1. **Install Git:**
    ```bash
    sudo apt install git -y
    ```

2. **Clone the Repository:**
    ```bash
    sudo git clone https://github.com/naztronaut/dancyPi-audio-reactive-led.git
    ```

3. **Switch to `no_mic` Branch:**
    ```bash
    cd dancyPi-audio-reactive-led
    sudo git checkout no_mic
    ```

4. **Navigate to the Install Directory:**
    ```bash
    cd python/install
    ```

Once you're in the `install/` directory, you'll see a few files. The one we're interested in is `install.py`. Running this script will install all the dependencies needed for this project, including `numpy`, `scipy`, `pyqtgraph`, `pyaudio`, `rpi_ws281x`, and `pydub`. This script will also copy `asound.conf` and set up virtual audio devices.

5. **Run the Install Script:**
    ```bash
    sudo python3 install.py
    ```

The setup can take a few seconds to a few minutes, depending on how many dependencies you already have installed. The script runs a series of commands for you, so you can start it and walk away.

6. **Reboot the Pi:**
    ```bash
    sudo reboot
    ```

After rebooting, connect your Bluetooth or USB Speaker. Bluetooth can be connected either through the GUI or command line, and a USB Speaker should be plug and play. For the next steps, use the GUI either via VNC viewer or with a regular keyboard, monitor, and mouse.

## Config.py

Next, let's look at `config.py`:

```python
DEVICE = 'pi'
LED_PIN = 18
USE_GUI = False
DISPLAY_FPS = False
N_PIXELS = 144
MIC_RATE = 44100
FPS = 50
```

- `MIC_RATE`: This branch uses 44100 Hz as it provides the best results. The Mic version uses 48000 Hz.
- `N_PIXELS`: It's important to set this correctly as it determines the center of the 'dancing' LEDs. The value must be divisible by 2.

## Running the Software

If everything installed correctly, you can run the project with this command:

```bash
sudo python3 visualization.py scroll
```

### Run Visualization.py in GUI

Run the above command in a shell window in the GUI. You can replace the `scroll` argument with any of the following:

- `spectrum`
- `scroll`
- `energy`
- `scroll_in`
- `scroll_quad`

The last two visualizations are additional ones. If `DISPLAY_FPS` is set to `True`, you will see an FPS value every second or so.

The virtual mic will pick up any audio played on the Pi. This can be from VLC, a Python script, YouTube on a browser, or Spotify.
