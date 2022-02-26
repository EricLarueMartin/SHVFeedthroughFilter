# SHVFeedthroughFilter
Coaxial feedthrough filter that mounts on an SHV bulkhead.

Version with two SHV bulkhead jacks.
![SHV to SHV Feedthrough Filter](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/DoubleSHVFeedthroughFilter.png)

SHV bulkhead connectors on both ends allow mounting the filter such that the body of the filter is on either side of the bulkhead, which may be helpful for space constraints.

Uses commercially available parts to make a high voltage filter that fits on a standard SHV bulkhead connector.
This filter was designed for use biasing cryogenically cooled solid state detectors, which have very low leakage current making high resistance series elements suitable.

Resistors are axial lead able to handle the high voltage while the sides of the resistor body are near ground, such as Ohmite MOX112523*. This series of resistor is highly recommend due to the low (0.25 pF) capacitance, even though a shorter resistor would fit.

![Mini-Mox Construction](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/Mini-MoxInternalConstruction.jpg)

Connector used for protoype was TE Connectivity AMP Connectors 5225059-3, this is out of production and an alternative will become necessary when stocks depleate. The BM61482 from Bracke Manufacturing appears to be a direct replacement. 

![5225059-3](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/5225059-3.webp)

The BM60261 connector for use with RG-8 would allow more room for the resistor. As the outer body has a 3/4 inch maximum diameter it could be butt soldered to a shorter tube or the connector could be trimmed down. 

![BM60261](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/BM60261.jpg)

The BM60829 would certainly give ample room for the resistor, but the overall length of the filter would increase.

![BM60829](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/BM60829.jpg)

Capacitors are 6kV 2225 package, such as Vishay Vitramon HV2225*

The center piece for the capacitors to solder to is a brass standoff, 6 mm hex diameter and 5 mm or 6mm height are both suitable.

The tube is a 0.686 inch ID brass or copper tube. A 3/4 inch 0.032 inch wall tube is readily available and suitable.

The other end can be another SHV connector, HV pigtail, whatever is desired. 

Version with a pigtail.
![SHV to Pigtail Feedthrough Filter](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/SHVFeedthroughFilter.png)
For this pigtail the filter is sealed with a 11/16 inch OD copper washer soldered to the tube, wire braid soldered to the washer, and the gap around the cable sealed with epoxy. This results in a complete Faraday cage around the filter.

A bleeder resistor on the load side of this filter will result in voltage drop across the series resistors. Bleeder resistors are not required if stored energy is under 10 J. 

The prototype filter used six 2.7 nF capacitors, which will only result in 0.3 J of stored energy at 6 kV. With 100 Mohm series resistors the maximum current the filter can produce is only 60 microamps at 6 kV, which is negligible compared to the ~10 mA requires to produce a dangerous shock. With 0.25 pF of parallel capacitance this high of a ressistance isn't effective at frequencies above 10 kHz. 5 Mohm resistors would still limit the current from a shock to ~ 1 mA and performance at power distribution frequencies would still be better than 100 dB.

If a fitler with a larger capacitance and smaller resistors is constructed pay attention to potentiol electrical shock hazzards.

The filter attenuation is excellent. Pigtail version measured from 30 kHz to 100 MHz using a network analyzer.
![Filter attenuation](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/FilterAttenuation.jpg)
The reduced performance above 90 MHz might be due to pickup noise after the filter on the line to the network analyzer. With an output power of -3 dBm the measured signal for -80 dB is only 5 pW, and an even stronger signal was measured for an open connection.

![Measured attenuation for an open](https://github.com/EricLarueMartin/SHVFeedthroughFilter/blob/main/OpenAttenuation.jpg)
