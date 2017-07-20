# My Notes

## Installing

copy to `c:\python27\Scripts`, ensure it is in the search PATH

* `psd2pcap.py` (renamed `tibtle2pcap.py`)
* `pcapdump.py`

create `psd2pcap.bat` with content

```bat
python.exe -B %~dp0psd2pcap.py %*
```

## Links

* https://lacklustre.net/bluetooth/wireshark.html
* https://github.com/greatscottgadgets/ubertooth/wiki/Capturing-BLE-in-Wireshark

* Go to Edit -> Preferences
* Under Protocols in the left pane type in "DLT" and select DLT_USER
* Click Edit and a window should pop up
* Click New, enter btle in "Payload Protocol", and click ok
* Keep clicking OK until all your preference windows are closed

filters:

* `btatt`
* `btle.data_header.length > 0 || btle.advertising_header.pdu_type == 0x05`