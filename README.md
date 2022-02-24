# SHVFeedthroughFilter
Coaxial feedthrough filter that mounts on an SHV bulkhead.
Uses commercially available parts to make a high voltage filter that fits on a standard SHV bulkhead connector.
This filter was designed for use biasing cryogenically cooled solid state detectors, which have very low leakage current making high resistance series elements suitable.

Connector used for protoype was TE Connectivity AMP Connectors 5225059-3, this is out of production and an alternative will become necessary when stocks depleate. The BM60321 from Bracke Manufacturing is likely a direct swap replacement. A part to seal the tube with a front side nut mounting and a hole for the more common SHV rear side nut bulkhead connector, such as PE3239 from Pasternack or 51494-2 from TE Connectivity AMP Connectors, is also included. Using the adapter will result in a longer filter and a different tube jig is required.

Resistors are axial lead able to handle the high voltage while the sides of the resistor body are near ground, such as Ohmite MOX112523*. This series of resistor is highly recommend due to the low (0.25 pF) capacitance, even though a shorter resistor would fit.

Capacitors are 6kV 2225 package, such as Vishay Vitramon HV2225*

The center piece for the capacitors to solder to is a brass standoff, 6 mm hex diameter and 5 mm or 6mm heigh are both suitable.

The tube is a 0.686 inch ID brass or copper tube. A 3/4 inch 0.032 inch wall tube is readily available and suitable.

The other end can be another SHV connector, HV pigtail, whatever is desired. 
For a pigtail the filter is sealed with a 11/16 inch OD copper washer soldered to the tube, wire braid soldered to the washer, and the gap around the cable sealed with epoxy. This results in a complete Faraday cage around the filter.
SHV bulkhead connectors on both ends would allow mounting the filter such that the body of the filter is external to the crate, which may be helpful to keep more space avilable inside the crate.

A bleeder resistor on the load side of this filter will result in voltage drop across the series resistors. Bleeder resistors are not required if stored energy is under 10 J. 

The prototype filter used six 2.7 nF capacitors, which will only result in 0.3 J of stored energy at 6 kV. With 100 Mohm series resistors the maximum current the filter can produce is only 60 microamps at 6 kV, which is negligible compared to the ~10 mA requires to produce a dangerous shock.

If a fitler with a larger capacitance and smaller resistors is constructed pay attention to potentiol electrical shock hazzards.
