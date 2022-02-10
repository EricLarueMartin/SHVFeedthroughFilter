# SHVFeedthroughFilter
Coaxial feedthrough filter that mounts on an SHV bulkhead.
Uses commercially available parts to make a high voltage filter that fits on a standard SHV bulkhead connector.

Connector is TE Connectivity AMP Connectors 5225059-3

Resistors are axial lead able to handle the high voltage while the sides of the resistor body are near ground, such as Ohmite MOX112523*.
This series of resistor is highly recommend due to the low (0.25 pF) capacitance, even though a shorter resistor would fit.
This filter was designed for use biasing cryogenically cooled solid state detectors, which have very low leakage current. If the filter is used for a significant current inductors must be used instead.
Whatever the series component is it should fit inside the cable end of the connector. Some resistors may require sanding down slightly to fit.

Capacitors are 6kV 2225 package, such as Vishay Vitramon HV2225*

The center piece for the capacitors to solder to is a brass standoff, 5.5 mm hex diameter 1/4 inch tall.

The tube is a 0.686 inch ID brass or copper tube. A 3/4 inch 0.032 inch wall tube works and is common. It may need to be expanded slightly to fit over the connector, it's a very tight fit.

The other end can be another SHV connector, HV pigtail, whatever is desired. 
For a pigtail recommend capping the tube with a 3/4 inch OD brass or copper washer soldered to the tube and sealing the gap around the cable with epoxy.

The SHV connect pin should be placed on the axial lead of the resistor and up against the resistor body, this will allow apply sufficient force to fully insert the pin.

Recommend filling the tube with silicone oil and sealing the fill port with electrical tape. The oil will leak out the pin on the SHV connector if not sealed.

Recommend sealing around the pin with some slow curing high viscosity epoxy that has been degassed using a centrifuge and/or vacuum.
Place epoxy around base of pin where it meets resistor and keep it positioned so it doesn't flow along pin until after inserted into connector, then flip it so the epoxy flows down to seal the pin penetration in the connector while curing. 
Epoxy only needs to seal in oil, not provide high voltage insulation, recommend a small amount.

A bleeder resistor on the load side of this filter will result in voltage drop across the series resistors. Bleeder resistors are not required if stored energy is under 10 J. The series resistance of the filter itself is likely too high to be dangerous for the greater than a megaohm resistors likely to be chosen. The 2225 6 kV capacitors from Vishray Vitramon are available at a maximum of 100 nF. 600 nF at 6 kV would be 10.8 J and a series resistor of at least 1.2 megaohms would be recommended to limit the current to 5 mA. 

If built with a different capacitor geometry it is suggested to place identical capacitors on opposite sides. This will cancel out any radiation from current flow on the capacitors that would bypassing the output resistor. Given the perpendicular placement of the capacitors and the output resistor this should already be minor.
