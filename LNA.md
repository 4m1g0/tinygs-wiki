## Using LNA

OK, you have got your first signal but it is unstable, or you want to catch signal from satellites with QRP (low transmission power) such as SDSat? Sometimes using a good antenna is not good enough, you need to use Low Noise Amplifier. 
An amplifier is supposed to, well, amplify signal. But in reality it will amplify everything including unwanted signals a.k.a. noise. So how can you filter the signal to those that you want? What is the best configuration, filter first or LNA first? What is the gain needed? Which brand is good? And what the heck is Bias Tee? Let's take a look one by one.

## How to use LNA

Most people believe: [Antenna](Antenna.md) - LNA - [Filter](Filter.md) - receiver. I use: [Antenna](Antenna.md) - [Filter](Filter.md) - LNA - receiver. That's what giving better noise floor on my Software Defined Radio (SDR), some other people swear I committed sin for doing that, I don't care, it works for me. Just try both and see which one is better for you. Using Filter is a must when you are using LNA. See more about Filter [here](Filter.md).

## Which LNA is good?

What is good for me not always good for everyone. Most LNAs work for both 433 and 915 MHz, but you should check before buying an LNA.
It is called Low Noise Amplifier / LNA because the amplifier itself is also producing noise. 
A good LNA should give minimal noise. From my previous non scientific experiment shows that an underpowered LNA could produce more noise.

I have tested the following LNAs:

### [WINSINN 0.1-2000MHz SDR LNA WideBand RF Amplifier 30DB High Gain Low Noise](https://www.amazon.com/gp/product/B084YQ8V2H/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&psc=1)

Result: good with the power supply of 6V and above. It won't work with 5V. Have not measure the gain using VNA but a simple RSSI comparison suggests it gives 20dB+. I burnt this LNA when giving 12V. 
Use Bias Tee: NO.
Recommend: YES (with caution on voltage)

### [Nooelec Lana - Ultra Low-Noise Amplifier (LNA) Module for RF](https://www.amazon.com/gp/product/B07XNLJ9X2/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&psc=1)

The upscaled LNA, nice build quality. Mine broken after 1 month, it is the USB regulator that is broken so power is not coming. I repaired it by soldering the power to antenna out (Bias Tee). Stable gain at 8-15dB. 
Bias Tee: YES.
Recommend: NO.

### [RF Broadband Amplifier, Durable LNA Amplifier](https://www.amazon.ae/gp/product/B08L52PMS3/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)

I am happy with this LNA, bought another one and so far working fine. Only give 20dB but good enough to receive all sats on 433 band. I like the screw in power line. 
Use Bias Tee: NO.
Recommend: YES.

### [RF Wideband Amplifier LNA 0.1M-2G Gain 60dB Two-stage Amplification](https://www.banggood.com/RF-Wideband-Amplifier-LNA-0_1M-2G-Gain-60dB-Two-stage-Amplification-p-1253132.html?rmmds=myorder&cur_warehouse=CN)

Claimed to have 60dB amplification gain. In reality gives around 50dB. But with tinyGS this does not really give much advantage as the noise level also increase. Especially if you are in the city area.
Use Bias Tee: NO.
Recommend: NO.

Note on online shopping: similar items are sold in different sites at different prices, I can't tell if they are the same or not, most likely yes as most of them are coming from the same country anyway.

## Important Note about Bias Tee

Be careful when using some LNA with Bias Tee capability they routed DC back to the LoRa module. I assumed that the LoRa module has LC circuit that filters the working RF freq and supposedly also protects against DC current, but apparently doesn't last for long. Over few weeks my board cannot take it anymore and the LoRa chip failed. It becomes very hot and ultimately fried. If you have to use LNA with Bias Tee capabilty please make sure you use DC blocker such as [this one](https://www.amazon.com/Nooelec-SMA-DC-Block-50kHz-8GHz/dp/B07YYLHJKS/) to protect your LoRa board: 

There are many other LNAs that I have not tried, but some friends are recommending. Such as [LNA for all](https://lna4all.blogspot.com/) and the premium [Cubesat filtered amp products from Uputronics](https://store.uputronics.com/index.php?route=product/product&path=59&product_id=124).

Again, whichever product you choose, it might or might not work for you as there are many other factors that affecting our success in receiving satellite signals.

### Authors of this page
- [@Judhi](https://github.com/judhi) - 2021/04/17
