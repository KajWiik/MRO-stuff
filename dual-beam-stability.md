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

where $T_{\mathrm{s}}$ is *system temperature*,
$\Delta t$ is *integration time* and $B$ is *effective bandwidth* of
the radiometer.

DPFU (Degrees Per Flux Unit) is a measure of the antenna performance, it is defined as

$$ \mathrm{DPFU} = \frac{A_e}{2k}\cdot 10^{-26} \, \left[\frac{\mathrm{K}}{\mathrm{Jy}}\right]
$$

For example, DPFU is about 0.027 and 1.4 for Metsähovi and Effelsberg, respectively.



## Gain stability criterion for a two beam continuous comparison total power radiometer

A two beam continuous comparison radiometer can be constructed using
two independent radiometers and calculating a difference of the
outputs:

$$ 
\Delta P = g_{\mathrm{A}} T_{\mathrm{s}} - g_{\mathrm{B}} T_{\mathrm{s}}
$$

By rearranging and setting

$$
 g_{\mathrm{B}} = \frac{g_{\mathrm{A}}}{k}
$$
we get
$$
\Delta P = g_{\mathrm{A}} T_{\mathrm{s}}(1-\frac{1}{k})
$$

The gain difference between chains that amounts to a power difference
equal to the RMS noise of the radiometer can be found by

$$
 g_{\mathrm{A}} T_{\mathrm{s}}(1-\frac{1}{k}) = g_{\mathrm{A}}\frac{T_{\mathrm{s}}}{\sqrt{\Delta t \cdot B}}
$$
so
$$
k = 1 - \frac{1}{1 - \frac{1}{\sqrt{\Delta t \cdot B}}}
$$

E.g. for $t$ = 1 s, $B$ = 8 GHz, $(k - 1) \sim 10^{-5} = 50$ dB or $k = 
0.000005$ dB.


## Gain difference calibration methods

If the gains of the branches can be measured, the difference can be naturally
compensated. Another way is to use fast beam switching (Dicke-related
method) or continuous comparison (or pseudocorrelation) scheme where
the gain variations are subjected to the difference of
the noise temperature of the brances, like

$$
\Delta P = g_{\mathrm{A}} g_{\mathrm{B}} (T_{\mathrm{s,A}} - T_{\mathrm{s,B}})
$$

yielding much relaxed demands for the stability of the
amplifiers. This is the reason for popularity of continuous comparison
radiometers especially in applications that require high level of
accuracy and sensitivity (e.g. WMAP, Planck).



### Noise diode calibration

To calibrate gains to a given level, the injected noise power level
must be high enough to give xxx signal to noise (SNR) level.

For example if $T_{\mathrm{s}} = 100 \, \mathrm{K}$, $B = 8 \,
\mathrm{GHz}$ and $\Delta t = 1 \, \mathrm{s}$, the radiometer noise
level is $\Delta T_{\mathrm{min}} = 1 \, \mathrm{mK}$.  

If stability requirement is e.g. 50 dB (see above), the noise diode
level must be in the order of

$$
T_{\mathrm{N}} = 10^{50/10} \cdot 1 \, \mathrm{mK} = 100 \, \mathrm{K}
$$

This high value is unreasonable since it is the same order of the
total system temperature and reduces the overall sensitivity of the
radiometer considerably.


### Coherent pilot tone calibration

A narrowband pilot tone can be used in gain calibration. Its effect to
the system temperature can be compensated by filtering it out before
average in the backend as long as it is spectrally clean and does not
saturate the receiver.

Also the required power level is much lower due to the narrowband
detection.

For example if the detection is done in 1 Hz band (i.e. every second)
for the figures in the previous example, the required power level is 1
Hz/8 GHz, i.e. the effect to the system temperature is in the order of
$1/8e6 \cdot 100 \, \mathrm{K} = 12 \mu \mathrm{K}$, which is
negligible.

However, it should be noted that one pilot tone probes only one
frequency of the passband, the passband may (and will) vary because of
changing reflections from the subreflector support structure and the
radome.

## Inherent gain stability of HEMT amplifiers

How necessary the calibration actually is? If the temperatures are kept stable, the gains stay stable too, right? Unfortunately there are semiconductor level processess inherent to the HEMT structure that create 1/f-type noise in gain.

In [this](https://upcommons.upc.edu/bitstream/handle/2117/1047/very%20low%20noise01440723.pdf) article (page 2059) this 

So, to keep gain less than the radiometer RMS noise so that differences are undetectable is a formidable problem.

With e.g. $T_{\mathrm{s}} = 100 \, \mathrm{K}$, $B = 8 \, \mathrm{GHz}$ and $\Delta t = 1 \, \mathrm{s}$, $\Delta T_{\mathrm{min}} = 28 \, \mathrm{mK}$ which translates to about 1 Jy for Metsähovi 13.7 m antenna.
If the difference between chains for an equal input noise temperature should be less than $\Delta T_{\mathrm{min}}$, the relative gain difference should be less than


 and relative stability requirement is $0.0004$ or $1/2830$ or 0.0015 dB


https://upcommons.upc.edu/bitstream/handle/2117/1047/very%20low%20noise01440723.pdf Page 259
