## Installing Home Assistant Core on Android: Simple and Fast, No Root, No QEMU

Got an old Android phone and don’t want to buy a Raspberry Pi or a PC to host Home Assistant? This tutorial is for you!

**Requirements: Android Phone – No Root Required**

**Credit: Special thanks to [George-Seven for the Termux-Udocker repository](https://github.com/George-Seven/Termux-Udocker).**

---

### Step 1: Install the Termux app from F-Droid.org

**Note:**
- Although Termux is also available on the Play Store, according to the Termux developers, the version on F-Droid is the most stable.
- After installing Termux, it is recommended, though not required, to install OpenSSH and enable remote access from a PC for easier interaction with the Termux Terminal. For details on setting up Termux remote access, see: [Termux Remote Access Guide](https://wiki.termux.com/wiki/Remote_Access).

### Step 2: Install Git in Termux:

```bash
# Update & Upgrade Termux packages
pkg update && pkg upgrade

# Install git
pkg install git
```

### Step 3: Install HomeAssistant-Termux


```bash
git clone https://github.com/huytungst/HomeAssistant-Termux.git
```

Go to the root directory of HomeAssistant-Termux:

```bash
cd HomeAssistant-Termux
```

Install Udocker from the cloned repository:

```bash
./install_udocker.sh
```

Run the script home-assistant-core.sh:

```bash
./home-assistant-core.sh
```

## Wait about 10 minutes, then you can access Home Assistant on port 8123 (http://localhost:8123/)

**Also, you can install and run the Python Matter Server to enable Matter compatibility.**


Run the script matter-server.sh:

```bash
./matter-server.sh
```

This completes the setup for running Home Assistant Core and the Matter Server on Android without root.

### !!! Known Issue: Home Assistant setup failed for some dependencies, including 'bluetooth,' 'usb,' 'zeroconf,' etc. Any help would be appreciated!