# Pulser
Python and MATLAB based tools for use in the Pulser project at PUFFIN. There are currently three programs:
  - RLC Jupyter code that plots current v.s. time both analytically and numerically for an ideal RLC circuit.
  - Pulser simulink program that models both the charging and pulse/discharging effect of an ideal circuit.
  - Resistor model program that models two different interpretations of the spark gap time-dependent variable resistor: Braginsky and Weizel-Rompe.

## RLC Jupyter
In order to run these jupyter notebooks, use shift+right click>"open command window here" in the folder containing the notebook you want to use. Type 'jupyter notebook' at the command line and hit enter.

The initial conditions (initial current and initial voltage across capacitor) and RLC values should be changed in the input cell. Run the program by pressing Ctrl+Enter.

At the bottom, the RLC, damping coefficient, natural frequency, angular frequency, rise time, peak current, and type of second order system (overdamped, underdamped, or critically damped) is printed. Also, three graphs are shown: the numerical, analytical, and both plots of current v.s. time.

This program is a great way to garner an ideal representation of the system at hand.

## Pulser Simulink
The MATLAB software must be installed to run the program.

Values of elements are changed by double-clicking on the respective component; however, be cautious, since the name of the component does not automatically change. One has to manually change the name of the component by clicking on the name and changing. To get a good reading of measurents, the "Stop Time" at the top must be changed to roughly however long of a time step of the pulse you would like to see (should be around a microsecond or a nanosecond for pulses and tens of seconds for charging)(a good value is roughly ten rise times for pulses). Run the simulation by clicking the green run button at the top. View the current v.s. time by double-clicking on the scope.

Good to get more of a realistic example of what may happen in the system.

## Resistor Models Simulink
The MATLAB software must be installed to run the program.

Values of elements are changed by double-clicking on the respective component; however, be cautious, since the name of the component does not automatically change. One has to manually change the name of the component by clicking on the name and changing. For the Weizel-Rompe model, the channel length and a coefficient that is determined empirically must be known. For the Braginsky model, channel conductivity, gas density ahead of the shockwave, and a dimensionless constant related to channel conductivity must be known. For more information, look at [this paper](https://www.researchgate.net/publication/272255962_Energy_loss_in_spark_gap_switches).

This program is still under construction. Helpful to have more of a realistic form of the spark gap switch.
