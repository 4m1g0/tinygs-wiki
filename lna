#Using LNA

OK, you have got your first signal but it is unstable, or you want to catch signal from satellites with QRP (low transmission power) such as SDSat? Sometimes using a good antenna is not good enough, you need to use Low Noise Amplifier. 
An amplifier is supposed to, well, amplify signal. But in reality it will amplify everything including unwanted signals a.k.a. noise. So how can you filter the signal to those that you want? What is the best configuration, filter first or LNA first? What is the gain needed? Which brand is good? And what the heck is Bias Tee? Let's take a look one by one.

##Which LNA is good?

What is good for me not always good for everyone. Most LNAs work for both 433 and 915 MHz, but you should check before buying an LNA.
It is called Low Noise Amplifier / LNA because the amplifier itself is also producing noise. 
A good LNA should give minimal noise. From my previous non scientific experiment shows that an underpowered LNA could produce more noise.

I have tested the following LNAs:

###[WINSINN 0.1-2000MHz SDR LNA WideBand RF Amplifier 30DB High Gain Low Noise] (https://www.amazon.com/gp/product/B084YQ8V2H/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&psc=1)

Result: good with the power supply of 6V and above. It won't work with 5V. Have not measure the gain using VNA but a simple RSSI comparison suggests it gives 20dB+. I burnt this LNA when giving 12V. 
Use Bias Tee: NO.
Recommend: YES (with caution on voltage)

###[Nooelec Lana - Ultra Low-Noise Amplifier (LNA) Module for RF](https://www.amazon.com/gp/product/B07XNLJ9X2/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&psc=1)

The upscaled LNA, nice build quality. Mine broken after 1 month, it is the USB regulator that is broken so power is not coming. I repaired it by soldering the power to antenna out (Bias Tee). Stable gain at 8-15dB. 
Bias Tee: YES.
Recommend: NO.

###[RF Broadband Amplifier, Durable LNA Amplifier] (https://www.amazon.ae/gp/product/B08L52PMS3/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)

I am happy with this LNA, bought another one and so far working fine. Only give 20dB but good enough to receive all sats on 433 band. I like the screw in power line. 
Use Bias Tee: NO.
Recommend: YES.

###[RF Wideband Amplifier LNA 0.1M-2G Gain 60dB Two-stage Amplification] (https://www.banggood.com/RF-Wideband-Amplifier-LNA-0_1M-2G-Gain-60dB-Two-stage-Amplification-p-1253132.html?rmmds=myorder&cur_warehouse=CN)

Claimed to have 60dB amplification gain. In reality gives around 50dB. But with tinyGS this does not really give much advantage as the noise level also increase. Especially if you are in the city area.
Use Bias Tee: NO.
Recommend: NO.

Note on online shopping: similar items are sold in different sites at different prices, I can't tell if they are the same or not, most likely yes as most of them are coming from the same country anyway.
