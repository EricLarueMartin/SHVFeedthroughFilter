# SHVFeedthroughFilter
Coaxial feedthrough filter that mounts on an SHV bulkhead.

Version with two SHV bulkhead jacks.
![SHV to SHV Feedthrough Filter](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/DoubleSHVFeedthroughFilter.png)

SHV bulkhead connectors on both ends allow mounting the filter such that the body of the filter is on either side of the bulkhead, which may be helpful for space constraints.

Uses commercially available parts to make a high voltage filter that fits on a standard SHV bulkhead connector.
This filter was designed for use biasing cryogenically cooled solid state detectors, which have very low leakage current making high resistance series elements suitable.

Resistors are axial lead able to handle the high voltage while the sides of the resistor body are near ground, such as Ohmite MOX112523*. Though a shorter resistor would work the stray capacitance is important to performance and this model has the lowest stray capacitance at 0.25 pF.

![Mini-Mox Construction](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/Mini-MoxInternalConstruction.jpg)

Connector used for protoype was TE Connectivity AMP Connectors 5225059-3, this is out of production and an alternative will become necessary when stocks depleate. The BM61482 from Bracke Manufacturing appears to be a direct replacement. 

Capacitors are 6kV 2225 package, such as Vishay Vitramon HV2225*. Six 2.7 nF capacitors were used for the prototype, but three high capacitance X7R capacitors and three lower capacitance C0G capacitors would likely result in better high frequency performance.

The center piece for the capacitors to solder to is a brass standoff, 6 mm hex diameter and up to 6mm height.

The tube is a 0.686 inch ID brass or copper tube. A 3/4 inch 0.032 inch wall tube is readily available and suitable.

The other end can be another SHV connector, HV pigtail, whatever is desired. 

Version with a pigtail.
![SHV to Pigtail Feedthrough Filter](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/SHVFeedthroughFilter.png)
For this pigtail the filter is sealed with a 11/16 inch OD copper washer soldered to the tube, wire braid soldered to the washer, and the gap around the cable sealed with epoxy. This results in a complete ground shield around the filter.

A bleeder resistor on the load side of this filter will result in voltage drop across the series resistors. Bleeder resistors are not required if stored energy is under 10 J. 

The prototype filter used six 2.7 nF capacitors, which will only result in 0.3 J of stored energy at 6 kV. With 100 Mohm series resistors the maximum current the filter can produce is only 60 microamps at 6 kV, which is negligible compared to the ~10 mA requires to produce a dangerous shock. With 0.25 pF of parallel capacitance this high of a resistance isn't effective at frequencies above 10 kHz. 5 Mohm resistors would still limit the current from a shock to ~ 1 mA and performance at power distribution frequencies would still be better than 100 dB.

The filter attenuation is excellent. Filter attenutation measured with two SHV bulkhead connectors.
![Filter attenuation](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/AttenuationDoubleGuardRing.jpg)
Attenuation was measured using a FieldFox N9925A 9GHz network analyzer using the high signal strength setting and averaging 1000 samples. Comparing to the measured attenuation with the network analyzer receiver port open it is evident the filter performance is beyond the limit of what the network analyzer can measure except for a region around 500 MHz.

![Measured attenuation for an open](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/DisconnectedTransmissionFunction.jpg)

The cable ground of the recommended connector acts as a guard ring to reduce the effective capacitance between leads of the axial resistors, this stray capacitance dominates filter performance in the GHz range. A filter using two solder cup connectors was constructed and tested to demonstrate the impact of the guard ring. While attenuation was still too good to measure with the network analyzer used for most of the measured spectrum, it was significantly worse around 5 GHz.

![Measured attenuation for solder cup connector](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/AttenuationWithoutGuardRing.jpg)

