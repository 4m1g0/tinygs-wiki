## When Filter is needed?

Using filter is a must when you use LNA. Otherwise you are risking your LoRa module getting oversaturated and will not get the signal at all. 
You can also use filter even when not using LNA, if you believe there are strong interference in your neighborhood (eg: strong FM/TV transmitter).
  
## Which filter is good?
There are two types of filter: Bandpass Filter (BPF) and Bandstop (Notch) filter.

I have tried the following:

[Bandpass Filter BPF 2.45G 433M/1575M/900M/1090M Anti-jamming Noise Reduction LC Filtering SAW Filter](https://www.banggood.com/Bandpass-Filter-BPF-2_45G-433M1575M900M1090M-Anti-jamming-Noise-Reduction-LC-Filtering-SAW-Filter-p-1500155.html)
This is my favourite. Make sure you order the 433 MHz version. Working frequency is around 420 to 450, good enough for Norby and SDSat. I also have 915 version but have not get a chance to try it on satellite as VR3X sats are now sleeping.

[Distill:FM Barebones - Broadcast FM Bandstop (Notch) Filter for Software Defined Radio (SDR) Applications](https://www.amazon.com/gp/product/B076D354LW/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
I use this filter mainly when using SDR to monitor not just satellite but also Air Band, Marine band, etc. Without this filter, the FM interference is jacking up noise floor like crazy. But I also have many successful satellite receival just using this filter + LNA.

