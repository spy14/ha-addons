# Home Assistant Add-on: iSponsorBlockTV

Run iSponsorBlockTV on a computer that has network access. Auto discovery will require the computer to be on the same network as the device during setup. This addon uses host networking for this.

It connects to the device, watches its activity and skips any sponsor segment using the SponsorBlock API. It can also skip/mute YouTube ads.

## How to use

The easiest way to get started is to generate a config file by running this app on another machine.

You will need to get a connection key by opening the Youtube app on your device, going to settings and selecting tv link.

```
rm -rf /tmp/config && mkdir /tmp/config && docker run --rm -it -v /tmp/config:/app/data --net=host ghcr.io/dmunozv04/isponsorblocktv --setup-cli && cat /tmp/config/config.json
```

You can then pick the bits out that you need.

You must also set a YouTube API key as apikey.
