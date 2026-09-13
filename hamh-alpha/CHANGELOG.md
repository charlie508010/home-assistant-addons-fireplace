# v2.1.0-alpha.902

- Expose custom Mode Select labels independently from Home Assistant's raw option values (for example, show `Stufe 0`–`Stufe 5` while sending `C0`–`C5`).

# v2.1.0-alpha.901

## Changes

- fix: expose a light with mapped fireplace stages as an On/Off Lamp plus Mode Select, so Alexa no longer presents or targets brightness
- test: verify that the combined Kamin endpoint has stages but no Matter Level Control cluster

## Upstream base

- docs: list the alpha.897 additions (912e3a6e)
- docs: vacuum updating section, alexa manual code and suffix, heap hints (965f0f91)
- fix(#461): drop a queued update when a composed endpoint closes (ab500d69)
- fix(#365): mark the water leak detector unsupported on alexa (6586947f)
- fix(#276): apply the registry name in server mode (77d94abf)
- fix: match the mutex closed message when stopping a bridge (d2914075)
- fix(#155): keep the camera token out of the devices api (047fbf11)

---
⚠️ **This is an alpha release** - use at your own risk!
