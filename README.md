# LinearTRV

Home Assistant automation blueprint that forwards Versatile Thermostat proxy
valve commands (opening/closing degree helpers) to a physical TRV, with
two-slope linearisation and slam closing.

Based on the original blueprint by [caiusseverus](https://github.com/caiusseverus):
https://gist.github.com/caiusseverus/abe064b3f8d96896ab377766916e456a

## Changes from the original

- New `demand_threshold` input, separate from `min_valve_position`: below the
  threshold the valve closes, at the threshold it jumps straight to
  `min_valve_position` (e.g. a quiet 20% opening instead of a noisy small one).
- `max_valve_position` slider minimum lowered from 50 to 15.

## Import

[![Open your Home Assistant instance and show the blueprint import dialog.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fadrian-argasinski%2Flinear_trv%2Fblob%2Fmain%2FLinearTRV.yaml)
