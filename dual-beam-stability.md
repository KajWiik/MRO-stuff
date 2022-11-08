# Stability calculations of a two beam continuous comparison total power radiometer

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

where $T_{\mathrm{s}}$ is *system temperature* of the radiometer.

DPFU (Degrees Per Flux Unit) is a measure of the antenna performance, it is defined as

$$ \mathrm{DPFU} = \frac{A_e}{2k}\cdot 10^{-26} \, \left[\frac{\mathrm{K}}{\mathrm{Jy}}\right]
$$

For example, DPFU is about 0.027 and 1.4 for Metsähovi and Effelsberg, respectively.

## Two beam continuous comparison total power radiometer

A two beam continuous comparison radiometer can be constructed using two independent radiometers. 

With e.g. $T_{\mathrm{s}} = 100 \, \mathrm{K}$, $B = 8 \, \mathrm{GHz}$ and $\Delta t = 1 \, \mathrm{s}$, $\Delta T_{\mathrm{min}} = 28 \, \mathrm{mK}$ which translates to about 1 Jy for Metsähovi 13.7 m antenna.



If the difference between chains for an equal input noise temperature should be less than $\Delta T_{\mathrm{min}}$, the relative gain difference should be less than


 and relative stability requirement is $0.0004$ or $1/2830$ or 0.0015 dB

### Testing1

#### Testing2

https://upcommons.upc.edu/bitstream/handle/2117/1047/very%20low%20noise01440723.pdf Page 259

$$ 
\Delta P = g_{\mathrm{A}} T_{\mathrm{s}} - g_{\mathrm{B}} T_{\mathrm{s}}
$$

By rearranging and setting

$$
 g_{\mathrm{B}} = kg_{\mathrm{A}}
$$
we get
$$
\Delta P = g_{\mathrm{A}} T_{\mathrm{s}}(1-k)
$$

The gain difference between chains that amounts to a power difference equal to the RMS noise of the radiometer can be found by 

$$
 g_{\mathrm{A}} T_{\mathrm{s}}(1-k) = g_{\mathrm{A}}\frac{T_{\mathrm{s}}}{\sqrt{\Delta t \cdot B}}
$$
so
$$
k = 1 - \frac{1}{\sqrt{\Delta t \cdot B}}
$$

E.g. for $t$ = 1 s, $B$ = 8 GHz, $(1 - k) \sim 1 \cdot 10^{-5} = -50$ dB or $k = 
-0.00005$ dB.
