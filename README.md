# FlipperZero remote app for AC Fujitsu General ASHG12KPCE

## Warning

- The remote is build for and testd with model `Fujitsu General ASHG12KPCE`.
- Uing this app with incompatible A/C can lock the A/C up until it's physically power-cycled
- Check the [compatibility](REMOTE_COMPATIBILLITY.md) page for info on other models.

# Usage

The app has 3 main views. Change views with `InputKeyLeft` and `InputKeyRight`

## View 1

### Navigation

- Turn on/off the AC with the `InputKeyOk`
- Change temperatrue using the `InputKeyUp` and `InputKeyDown` (temperature is displayes in degrees celsius)

### Description

- The first clock icon will be visible only if there is a sleep or on/off timers set.
- Second icon indicates if Auto Swing is set on/off
- Third icon indicates the current fan speed.

![view1](./docs/img/Screenshot-1.png)


## View 2

### Navigation

- Change selected button using the `InputKeyUp` and `InputKeyDown`
- Press the selected button using `InputKeyOk`

### Description

- First button cycles trough the AC modes (Auto, Cool, Heat, Fan, etc.)
- Second button toggles Economy mode
- Third button changes the airflow direction (Set button on the original AC remote) (disables auto swing)
- Foruth button toggles auto swing
- Fifth button cycles trough fan speeds.

![view2](./docs/img/Screenshot-2.png)


## View 3

### Navigation

- Change selected button using the `InputKeyUp` and `InputKeyDown`
- Press the selected button using `InputKeyOk`

### Description

- `Timer` - Opens a view for configuring AC ON/OFF timers
- `Cancel` - Cancels all timers (ON/OFF and Sleep)
- `Sleep` - Opens a view for configuring a sleep timer
- `Power` - Toggles Powerfull mode of the AC

![view3](./docs/img/Screenshot-3.png)


## View 3 - Timer

### Navigation

- Use `InputKeyUp` and `InputKeyDown` to select an item.
- Use `InputKeyLeft` and `InputKeyRight` to select a value for that item
- Select `Confirm` item and press `InputKeyOk` button to send the signal to the AC

### Description

- `ON Time` and `OFF Time` configure the ON and OFF timer values

- Modes
  - `ON` - Turn ON the AC after configured `ON Time`
  - `OFF` - Turn OFF the AC after configured `OFF Timer`
  - `ON->OFF` - Turn ON the AC after configured `ON Time`, then turn OFF the AC after the configured `OFF Time` (Turn ON the AC after 30 min(`ON Time` = 30min), then turn OFF the ac after 30 minutes(`OFF Time` = 30min))
  - `OFF->ON` - Same as `OFF-ON` but first turn off the AC, then turn it ON


![view3-timer](./docs/img/Screenshot-3-timer.png)

## View 3 - Sleep

### Navigation

- Use `InputKeyUp` and `InputKeyDown` to select an item.
- Use `InputKeyLeft` and `InputKeyRight` to select a value for that item
- Select `Confirm` item and press `InputKeyOk` button to send the signal to the AC


### Description

- Set a sleep timer for the AC


![view3-sleep](./docs/img/Screenshot-3-sleep.png)


# Building the app from source

1) Clone the repo and cd into it.

2) Create a python venv and activate it (optional)

```
python3 -m venv .venv --prompt="fuji-general"
source .venv/bin/activate
```

3) Install [ufbt](https://github.com/flipperdevices/flipperzero-ufbt) (Check the ufbt page in case installation instructions changed)

```
python3 -m pip install --upgrade ufbt
```

4) Setup VS code dev envirionment (optional)

```
ufbt vscode_dist
```

5) Build the app

```
ufbt
```


If flipper is connected via usb, you can upload and launch it using this command

```
ufbt launch
```


# Credits

- All assest were drawn using this great and free web app - [piskelapp](https://www.piskelapp.com/)


- Developing the app was made much more easier by [this great tutorial](https://instantiator.dev/post/flipper-zero-app-tutorial-01/) by [instantiator.dev](https://instantiator.dev)

