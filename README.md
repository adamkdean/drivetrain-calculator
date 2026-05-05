# Drivetrain Calculator

Drivetrain calculator for robotics. Computes gearbox reduction and wheel/tread linear speed from a configurable multi-stage gear train.

![Drivetrain Calculator](https://github.com/user-attachments/assets/ab2ebfdb-9b09-4ba4-ae06-a3aecd1b4f4c)

View the [demo](https://adamkdean.github.io/drivetrain-calculator/).

## Gearbox

Configurable gear train of simple and compound stages with a motor input RPM.

- Stage ratio: `r_i = N_driven / N_driver`
- Total reduction: `R = ∏ r_i`
- Output speed: `ω_out = ω_motor / R`

Reports total reduction, mechanical advantage (`R`), output RPM, and stage count.

## Wheel / Tread

Solves `v = π · D · ω` for whichever variable is unlocked. Two of the three (`D`, `ω`, `v`) are locked as inputs; the third is computed.

- `D` (wheel diameter): mm, cm, m, in
- `ω` (wheel rotational speed): RPM
- `v` (linear speed): mm/s, cm/s, m/s, km/h, mph

Wheel ω can be linked to the gearbox output, in which case it tracks the gearbox computation rather than accepting direct input.

Derived outputs: circumference, time per revolution, RPS, and `v` in multiple units.

