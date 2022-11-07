# Stability calculations of a two beam differencing total power receiver

## Basics 

Total power output of a radiometer for an input noise temperature of $T$ Kelvins can be defined as 
$$
P = g \cdot T
$$
where $g$ is conversion factor or _gain_ of the radiometer.

The minimum detectable noise temperature or RMS noise of a total power radiometer is
$$
\Delta T_{\mathrm{min}} = \frac{T_{\mathrm{s}}}{\sqrt{\Delta t \cdot B}}
$$

With e.g. $T_{\mathrm{s}} = 100 \, \mathrm{K}$, $B = 8 \, \mathrm{GHz}$ and $\Delta t = 1 \, \mathrm{s}$, $\Delta T_{\mathrm{min}} = 28 \, \mathrm{mK}$ which translates to about 1 Jy for Metsähovi 13.7 m antenna.

If the difference between chains for an equal input noise temperature should be less than $\Delta T_{\mathrm{min}}$, the relative gain difference should be less than


 and relative stability requirement is $0.0004$ or $1/2830$ or 0.0015 dB


