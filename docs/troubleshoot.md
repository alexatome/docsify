# Troubleshooting

## Beacons on but no workers present
If the Home Base App is not showing that workers are present when beacon is transmitting (i.e., pull tab is not in beacon) & the beacon is within range of the app, then attempt the following: 

### Step 1: Verify Permissions
Verify that all [necessary permissions](install_apps#verify-app-permissions) are in place

### Step 2: Ensure Beacons are configured properly on BeaconX Pro app
*Due to a firmware issue with the Moko M1 beacons, it is possible that the Beacon will reset itself to its default configuration if you turn the beacon on and off too quickly (within 5 seconds). Reconfiguring the beacon with the appropriate settings generally fixes the issue.*

1. Open BeaconX Pro app 
    - See installation instructions [here](install_apps#install-beaconx-pro).
2. On the 'Beacon Firmware Options' screen, select **'BXP-Nordic series'**
3. If you see a beacon with device name as **'SafetyWorkerBeacon'** then the beacon is *not* the problem and you may move on to other troubleshooting options. Otherwise, continue to Step 4 below. 
4. Select the device named **'Beacon X Pro'** and reconfigure it as follows: 
    1. Enter 'Moko4321' as the password.
    2. Select SLOT 1
    3. Set frame type to 'Device Info'
    4. Change device name to ‘SafetyWorkerBeacon’
        - NOTE: Spelling and capitalization matter! 
    5. Change Adv Interval to 1
    6. Change TX Power to -20dbm
    7. Click Save icon in top right corner
    8. Change password from default ‘Moko4321’ to ‘TomeInc’ <!-- TODO: keep or remove this step? -->
5. Force close & reopen Home Base App. Beacon should be detected now and workers should show as present.

## Lost Pull Tab for Beacons
You may purchase more pull tabs for the beacon [here](https://www.digikey.com/en/products/detail/keystone-electronics/119/9739865).