"# hello-world" 
Here on my github I plan to start another open source motor controls project soon. It is going to be loosely based on the famous "VESC" project by benjamin vedder. 
So why another open source motor controller ? Well-mainly for modularity
The main goal is to have a controller that does exactly what you need for a good price on every level. 
Therefore hardware is going to be split into 3 categories that first have to be defined with all their requirements resulting in interfaces. A Design requirement is that every implementation of one of those categories is compatible with every implementation of the two others so if for instance 3 implementations of each exist one could configure 27 different controllers.
  1. A logic board containing at least an STM32 microprocessor (Variants with more or less calc power, interfaces,peripherals, - also main intention like servo Drive or BLDC driver for skateboard/bike RC car etc. )
  2. A predriver stage containing MOSFET drivers as well as all the voltage "grooming" buck and boost converters (mainly different different target Voltages)
  3. A power stage containing the main leads, the big input filter caps, and of course the MOSFETs/IGBTs, shunts, shunt amps, temp sens (mainly different target currents but also voltages) 
  
I do understand it is not going to be possible to completely seperate 2 and 3 while keeping them compatible over huge ranges of supply voltages and targeted currents but I want to keep them separate anyway mainly for ease of exchange of parts in case of accidents.
