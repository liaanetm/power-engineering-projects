# One-Line Diagram — Building Electrical Distribution

## Purpose
It shows how electricity flows from the utility source to every load in a building using a single line to represent all 3 phases.

## System Overview

```
UTILITY 13.8kV
       |
XFMR 480Y/277V 500kVA
       |
   MSB 800A
       |
   ┌───┼───┐
   |   |   |
 LP1  PP1  MP1
```

## Component Breakdown

**UTILITY 13.8kV**
The power company (OUC in Orlando). 13.8kV is the distribution voltage on the street. Too high for a building — needs a transformer to step it down.

**XFMR 480Y/277V 500kVA**
Transformer that steps voltage down from 13.8kV to 480/277V for the building. Wye (Y) connection means 480V between lines, 277V phase-to-neutral (because 277 × √3 = 480). 500kVA is the transformer's capacity (apparent power).

**MSB 800A**
Main Switchboard — the big equipment that receives ALL power from the transformer and distributes it to the panels. Rated at 800 amps total capacity.

**LP1 - LIGHTING 200A**
Lighting panel. Feeds all light fixture circuits in the building. Uses 277V (phase-to-neutral) because higher voltage = less current = thinner wires = cheaper. That's why commercial buildings don't use 120V for lighting.

**PP1 - POWER 200A**
Power/receptacle panel. Feeds wall outlets. Needs a smaller transformer to step down from 480V to 120/208V for normal plug-in equipment.

**MP1 - MECHANICAL 200A**
Mechanical panel for HVAC, pumps, and motors. Uses 480V directly because large motors are more efficient at higher voltage.

## Key Concepts Used

- **Three-phase power:** 3 wires carrying voltage signals 120° apart — more efficient than single-phase because you transmit more power with less copper
- **Wye vs Delta:** Wye (Y) has a neutral wire and gives two voltage levels; Delta (Δ) has no neutral
- **V_line = V_phase × √3:** The relationship between line-to-line and line-to-neutral voltage in a Wye system
- **Power types:** Real power (P, Watts) does useful work; Reactive power (Q, VAR) sustains magnetic fields; Apparent power (S, VA) is what you size equipment for
- **Power factor:** PF = P/S — closer to 1 is more efficient

## AutoCAD Techniques Used

- **Layers:** E-DIAG (cyan) for diagram symbols, E-TEXT (yellow) for labels
- **Symbols:** Utility = circle with internal lines, Transformer = two overlapping circles, Switchboard/Panels = rectangles
- **OSNAP:** Endpoint snapping for precise line connections
- **MTEXT:** Labels with component name, voltage, and amperage
