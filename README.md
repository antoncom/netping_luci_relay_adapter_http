# netping_luci_relay_adapter_http

OpenWrt LuCI HTTP adapter for NetPing Relay module

## Directory structure

```bash
.
├── luasrc
│   ├── model
│   │   └── netping
│   │       └── relay
│   │           └── adapter
│   │               └── netping_luci_relay_adapter_http.lua
│   └── view
│       └── netping_luci_relay
│           └── ui_adapter
│               ├── netping_luci_relay_adapter_http.css.htm
│               ├── netping_luci_relay_adapter_http.js.htm
│               └── netping_luci_relay_adapter_http.valid.js.htm
├── Makefile
├── README.md
└── root
    └── etc
        └── config
            └── netping_luci_relay_adapter_http
```

## How-To install (OpenWrt 19.7, x86, LuCI)

1. Download an IPK-file from [releases](https://github.com/antoncom/netping_luci_relay_adapter_http/releases)
2. Copy the ipk-file into the device file structure, e.g. to /tmp directory.
3. Install using opkg:
* opkg update
* opkg install PATH-TO-IPK-FILE --force-reinstall

NOTE:
If you need to compile ipk-file for another architecture (or processor type), then use this instruction: [How to make a specific architecture based OpenWrt package as IPK file](https://netping.atlassian.net/wiki/spaces/PROJ/pages/3194945556/LuCI+.ipk)


## How-To create new adapter based on the present one

1. Git clone the present repo
2. Rename all files to "netping_luci_relay_adapter_ADAPTER-NAME"
3. Edit "template" section in config file according to new adapter options.
4. Edit model (lua) file accordingly
5. Edit view (js/css) files accordingly
6. Compile and add validator declarations in .valid.js.htm using this specification: [https://netping.atlassian.net/wiki/spaces/PROJ/pages/2809857522](https://netping.atlassian.net/wiki/spaces/PROJ/pages/2809857522)

## Screencast Demo

[Adapter installation from .ipk file](https://www.youtube.com/watch?v=Qj2uZqPfCm4)
