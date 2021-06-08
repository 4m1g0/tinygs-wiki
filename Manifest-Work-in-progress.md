TinyGS was originally created as a weekend project to listen to the FossaSAT-1 LoRa satellite, currently the community has grown and we have several satellites and ground stations around the world. The creators of TinyGS and in general the community of the project are passionate about space and want to learn and experiment about radio.

## Key principles of TinyGS?
* **Non profit.** The developers of TinyGS do this exclusively in our free time. Our respective companies have no relation to TinyGS. We do not accept any payment for our work on TinyGS.
* **Open.** All the data received by your station is available on your station console on TinyGS.com. The source code for the firmware, the website and the backend decoders is available on GitHub.
* **Neutrality.** The developers of TinyGS have no relation with any satellite operator and we want to remain independent. 
* **Fairness.** Every station operator in the community has exclusive control over their station and has the right to know what communications are being held through their station.

# A few definitions
TinyGS receive 3 different type of packets: 
1. Packets received by one or several stations with no information about them. These packets might be from a satellite, from a terrestrial radio or be just noise. We call these Unknown packets.
2. Identifiable packets from a known satellite whose information is publicly available and can be decoded. We call these Public packets.
3. Identifiable packets from a known satellite whose structure and content has not been published. For short, we call these Obscure packets. Because its information is hidden even if it is not encrypted.

## In order to meet this principles we take the following considerations
We think that keeping the costs of the servers down is key for the viability of this project. We are currently paying for the servers on our own. If we ever have to crowdsource the costs or accept collaboration from a third party it must be in a way that doesn't compromise any of the key principles. And the contributions must go directly to support the costs of the server infrastructure and nothing else and should not come from an interested party to ensure principles 1 and 3.

The network might be a good resource to get data from satellites with wide coverage around the world. However the community groundstations must not be used for profit. Obscured payloads are a threat for this. Its real content is hidden so there is no way to verify they meet key principles 1, 3 and 4, and they add no value to the community as its content has no readable information. Therefore the payload of non-public payloads will not be saved on the public TinyGS database. The packets will still be saved (with RSSI, SNR, Satellite, etc...) but with no payload.

The network welcomes any entity that wants to participate in the community as long as none of the key principles are violated.
Every station operator is in charge of managing their own transmissions, ensuring that they obey the rules and law for each region. TinyGS will not command transmissions without the intervention of the ground station operator. Moreover, the content of the communications must be public to ensure principle 4.

## FAQ
I am a satellite operator. Can I use TinyGS stations to get packets from my satellite? Yes, as long as the content of the payloads is public. This is the way to meet principle 4 so station operators know what type of communication is being held though their stations and study and learn from it.

I am a satellite operator. Can I use TinyGS stations to send tx to the satellite? Transmissions have to be done with the intervention of the station operators. TinyGS can act as coordinator for example to avoid packet collisions or meet rx window timers. However, we will never send transmissions without the operator intervention.

_WORK IN PROGRESS_
