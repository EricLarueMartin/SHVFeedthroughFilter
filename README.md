# SHVFeedthroughFilter
Coaxial feedthrough filter that mounts on an SHV bulkhead.
Uses commercially available parts to make a high voltage filter that fits on a standard SHV bulkhead connector.

Connector is TE Connectivity AMP Connectors 5225059-3

Resistors are axial lead able to handle the high voltage while the sides of the resistor body are near ground, such as Ohmite MOX112523*.
This series of resistor is highly recommend due to the low (0.25 pF) capacitance, even though a shorter resistor would fit.
This filter was designed for use biasing cryogenically cooled solid state detectors, which have very low leakage current.
Capacitors are 6kV 2225 package, such as Vishay Vitramon HV2225*

The center piece for the capacitors to solder to is a brass standoff, 5.5 mm hex diameter 1/4 inch tall.

The tube is a 0.686 inch ID brass or copper tube. A 3/4 inch 0.032 inch wall tube works and is common.

The other end can be another SHV connector, HV pigtail, whatever is desired. 
For a pigtail recommend capping the tube with a 3/4 inch OD brass or copper washer soldered to the tube and sealing the gap around the cable with epoxy.

Recommend filling the tube with silicone oil and sealing the fill port with electrical tape.

A bleeder resistor on the load side of this filter will result in voltage drop across the series resistors. Bleeder resistors are not required if stored energy is under 10 J. The series resistance of the filter itself is likely too high to be dangerous for the greater than a megaohm resistors likely to be chosen, meaning the filter is safe to use without a bleeder resistor so long as the connected load has under 10 J of stored energy.
