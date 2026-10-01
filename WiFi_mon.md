# Monitor Wifi

## Start logging
ip a
sudo airmon-ng start wlp0s20f3mon
sudo airmon-ng check                    # lists processing using wifi
sudo airmon-ng check kill               # stop processes
sudo airmon-ng                          # List interfaces

## start monitoring
sudo airmon-ng start wlp0s20f3          # turn on monitor mode
iw dev                                  # Shows interfaces w/ mon
sudo airodump-ng wlp0s20f3mon           # Start GUI
sudo airodump-ng --essid <SSID> wlp0s20f3mon    
ctrl-C to stop

## Restart no "mon"
sudo airmon-ng stop wlp0s20f3mon
sudo systemctl restart NetworkManager
ip a                                    # "mon" gone
