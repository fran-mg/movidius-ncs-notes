
## So what's inside my Movidius NCS 

As well as showing you pictures of what's inside the shiny blue stick in your hand, 
let's have a quick history lesson on the people that put it there.

Intel's Neural Compute Stick (NCS) is based on the Myriad 2 Visual Processing Unit (VPU). 
The company Movidius was started by a couple of guys from Dublin in 2005, 
Dr Sean Mitchell and David Moloney.
In 2013 they took Remi El-Ouazzane as their CEO, 
a bright young chap who'd made his name at renowned global chipmaker Texas Instruments, 
with numerous successes behind some of the processors 
that helped drive the growth in smart phones in previous years. 

Movidius contributed VPUs to the Google Tango project, with the 'Peanut' phone in 2014. 
And in January 2016 they announced a partnership with Google to power a VR headset 
to replace the Google Cardboard.
Their previous successes had allowed them to raise up to $90m dollars in funding, 
up until they announced their Fathon in April 2016. 
[https://www.bdti.com/InsideDSP/2016/05/26/Movidius](Details about the Fathon) explained that
it was a software framework for developing, learning then recognising, as well as 
a Neural Compute Stick. So they had got the words right, but the looks just weren't quite there.

But unlike the Intel version, you can see Inside (R).

[[https://www.bdti.com/sites/default/files/insidedsp/articlepix/201604/movidius-fathom.jpeg|Movidius Fathom USB stick in see thru case]]

So, you wanted to know about the technical inside too?! Well 
It uses the good old MA2450 variant of Myriad2, 
and includes and also containing 512 Mbytes of LPDDR3 SDRAM. 
The data sheet says the Myriad2 can deliver TeraFLOPS 
(trillions of floating-point operations per second) 
but that might be in ideal conditions, 
but it likely comes from the fact that there are 12 individual 'SHAVE' processors onboard. 

But what is being processed, where is the data? 
Like most CPUs there is some 'level 2 cache' where 256K is right there next to the processors. 
That's a quarter of a Meg, which is not masses, 
so the Myriad has an additional 2MB 'on the die' (in other words, inside the chip). 
The NCS stick has 512 MBytes of memory sitting next to the VPU, which 
claims to have a 4Gbit/s bandwidth (bit not Byte, so 400MB per second). 
If video is running at 25 frames per second, 
then those 12 processors can get their hands on 16MB per frame. 
Even if it's not enough for 14-bit RAW images 
from a high end camera's 'charged-couple device' (CCD) sensor, 
it's plenty enough for the kind of images you're likely to 
get from your mobile or Pi camera, or PC webcam. 

Whilst on the subject of data, the [https://www.bdti.com/InsideDSP/2016/05/26/Movidius](BDTI article on the Fathom) 
also includes a useful insight into the what is being processed where in the over workflow. 

[[https://www.bdti.com/sites/default/files/insidedsp/articlepix/201604/FathomGen.png]]

Back to the hardware. 
One of it's chief claims is low power consumption, 
and they say it will run at leass than one watt (1W), 
which compared to the 3W drawn by typical modern samrtphone CPUs is low. 
In my tests, the full NCS package, including additional circuitry, 
ran 60mW when idle, and up to 200mW when sending jobs or recieving results. 
(I have yet to test full blown continuous visual processing)

If you want to see more detail on the VPU itself, then you will find loads in 
the [https://uploads.movidius.com/1503680554-2016-12-12_VPU_ProductBrief.pdf](MA2450 product brief). 
This explains that there are 12 individual 'SHAVE' processors, 
which are based on Very Long Instruction Word (VLIW) technology. 
Microprocessors were originally built to run software programmes 
based on logical concept we human programmers came up with. 
The problem is that we were asking them to handle so many varied kinds of step 
that they were not very efficient at doing them quickly and easily. 
The mobile phone generation, and single board computers like Pis, 
used a 'new paradigm' of Reduced Instruction Set Computing (RISC) 
which were more efficient (faster but consuming less power) 
because they were actually a bit dumber (could handle a less varied range of tasks themselves). 
VLIW takes this idea further, by making the software designer have to do more of the hard work, 
so that the processor can just get on with going crunch -crunch -crunch 
with all the data you throw at it, and it is designed to do it in parallel. 
If you really want to get the best series of images 'showing' you what is inside the NCS, 
this [https://en.wikichip.org/wiki/movidius/microarchitectures/shave_v2.0](excellent wikichip article) 
gives you a plethora to choose from. 

So here you have the Fathom stick, doesn't look _that_ bad, does it.

[[https://cache.movidius.com/images/made/images/remote/http_movidius-uploads.s3.amazonaws.com/1461855269-Screen-Shot-2016-04-27-at-3.13.16-PM_1425_830_s_c1.png]]

A few months after the Fathom was announced, in autumn 2016, 
Intel decided they wanted in on the action and bought the company. 
It is clear that the Intel product designers were given two main objectives in their brief. 
The marketeers wanted them to turn it from a cheap looking pen drive 
into something sexy looking that geeks would associate with serious visual computing horse-power. 
And the engineers must have mentioned that the chip gets a little bit hot when processing, 
(if you remember the first law of thermodynamics, that one watt of energy has to go somewhere) 
so they found a way to dissipate that safely by turning the body into a heat sink.

So there you have the product that enthusiasts across the world now have in their hand.
For some reason Intel are very tight lipped about what they have included in their package: 
if you look at their [https://docs-emea.rs-online.com/webdocs/15c9/0900766b815c9668.pdf](data sheet) 
you see little more than the external physical dimensions that your own hand can tell you. 

And if you want to see what else you could get your hands on soon, 
[https://hackaday.com/2017/12/17/googles-aiy-vision-kit-augments-pi-with-vision-processor/](Google have made another AIY 'hat'), 
their VisionBonnet for the Pi Zero, also based on the MA2450 Myriad2.

[[https://hackadaycom.files.wordpress.com/2017/12/aiy-visionkit-bonnet_cr1.jpg|alt=Google AIY Vision Bonnet board]]

And what's more, not only will it be smaller and less power hungry than the Pi + NCS, 
but look where the camera module plugs in, direct to the board with the Myriad - 
that has to be a more efficient way to go.

