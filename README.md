# OfficeOccupancySensingWithWifiCSI

This repo hosts the utilities for collecting WIFI-CSI-Signals over long time periods. The project is based on the Linux 802.11n CSI Tool. See the project website for more info and setup of drivers (http://dhalperi.github.io/linux-80211n-csitool/). 

Unlike the original supplementary-tools (https://github.com/dhalperi/linux-80211n-csitool-supplementary) for collecting and processing recorded data, there is no requirement of MATLAB and no need to dump all scans locally into a large file. WIFI-Scans are collected in a Streaming Fashion, where each scan gets stored as a record into a Database. Currently there exists one connector for MonogDB.


USAGE:

Build everything:
cd csi/supplementary
make

Start the server:
python csi/server.py

Start consuming the socket:
./csi/supplementary/log_to_server.c