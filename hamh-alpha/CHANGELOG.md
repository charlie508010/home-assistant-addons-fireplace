# v2.1.0-alpha.907

- Expose a Home Assistant select as either a Matter On/Off Light (`0x0100`) or On/Off Plug-in Unit (`0x010A`) while preserving the configured select-option actions.
- Send a separate custom `NodeLabel` for every test device so Alexa can import and display each controller-facing name independently.
- Keep Mode Select out of this compatibility test.

# v2.1.0-alpha.906

- Allow a custom controller-facing name on every composed sub-endpoint.
- Support the Matter-correct fireplace test topology: `Kamin` as the primary endpoint with `Flammenfarbe`, plus the child Mode Select endpoint `Flammenhelligkeit`.
- Add a regression test for both named Mode Select controls in one composed Matter device.

# v2.1.0-alpha.905

- Keep Kamin as one Extended Color Light endpoint and declare Mode Select as a second device type on that same endpoint.
- Expose `Flammenfarbe` and `Stufe 0`–`Stufe 5` without presenting an undeclared extra cluster to Alexa.

# v2.1.0-alpha.903

- Declare the combined Kamin endpoint as both Matter On/Off Light and Mode Select, without Level Control, so Alexa can map power and named fireplace stages on one device.

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
