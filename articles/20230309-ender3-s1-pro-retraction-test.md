## Ender3 S1 Pro Retraction Test Findings

Author: Sanket Sonavane   
Publish Date: 2023-03-11   
Last Updated: 2023-03-11  

> NOTE:  
> This is a live article i.e. as and when new information is observed or found it will be  
> 1. appended with time stamps to the end  
> 2. corrected in place, if earlier documentation was incorrect  
  
## what I am using
- Ender 3 S1 Pro on stock marlin firmware 
- Cura 522 as slicer of choice

## common settings for all retraction tests
- 0.3 Layer height was used for all
- 3 wall perimeter
- infill density 20
- infill pattern cubic
- initial temp 205nozzle 70bed
- temperatures 205 nozzle 60bed

## approaches to try 
these are summary of suggestions which I have received from various communities on discord and reddit

- [x] retraction speed 25mm/s
- [x] retraction speed 50mm/s
- [x] retraction distance 1.0mm
- [x] retraction distance 1.5mm and retraction speed 30mm/s
- [ ] check out teaching tech's calibration page
    - [ ] teaching tech retraction test
- [ ] check [Retraction Calibration Tool](http://retractioncalibration.com/)
- [ ] slowing down fan speed
- [ ] check combing options
- [ ] adding wipe distance

## test results 

![](/assets/img/s1-pro/s1pro-retraction-test-med.png)

2023-03-11
- TEST 1: retraction distance 0.8mm and retraction speed 40mm/s
    - result: same to one shown in screenshot
- TEST 2: retraction distance 1.5mm and retraction speed 30mm/s
    - result more stringing might be because of 1.5 so decided to go back to 0.8
- TEST 3: retraction distance 0.8mm and retraction speed 50mm/s
    - result : might be a bit less string compared to test 1
- TEST 4: retraction distance 0.8mm and retraction speed 25mm/s
    - result: same as 1 with fine stringing

2023-03-11 conclusions
- increasing the retraction distance from 0.8 to 1.0 to 1.5mm I observed more stringing hence reverted back to 0.8 and will keep that constant as I tried various retraction speeds.
- with retraction distance set as 0.8mm I tested retraction speeds of 25mm/s,40mm/s,50mm/s and while the stringing was looking similar it seems like higher speeds helps so I might continue further test with 50mm/s 
- so far option 3 looks best to me i.e. retraction speed of 50mm/s
- there are a few more suggestions that I need to look into like 
    - fan speeds 
    - combing modes
    - wipe distance options

## safe retraction speeds
according to [wevolver.com article](https://www.wevolver.com/article/the-best-ender-3-retraction-settings) retraction speeds of 30~50mm/s are safe for Ender3 and  I have tried to remain in these levels while performing my tests

Quoting a few points from the same article
> Note that some slicers (e.g. Cura) will allow you to set different speeds for retraction (pulling the filament back) and priming (returning the filament to its original position). However, if these fields are left blank, then the overall retraction speed will apply in both situations.

> Recommended Ender 3 retraction speed: 50 mm/s, decreasing in increments of 5 mm/s if filament grinding occurs


## references
reddit 
[S1 Pro how to get rid of these fine threads that occur during prints : Ender3S1](https://www.reddit.com/r/Ender3S1/comments/11moh4t/s1_pro_how_to_get_rid_of_these_fine_threads_that/)

articles
- [The best Ender 3 retraction settings](https://www.wevolver.com/article/the-best-ender-3-retraction-settings) 
- [3D Printer Retraction Speed – Simply Explained - All3DP](https://all3dp.com/2/3d-printer-retraction-speed-what-does-it-mean/)
- [The Best Ender 3 (V2/Pro) Retraction Settings to Stop Stringing - All3DP](https://all3dp.com/2/ender-3-pro-v2-retraction-settings-all-you-need-to-know/)
- [What is retraction in 3D printing? Definition and adjustments](https://filament2print.com/gb/blog/34_retraction-in-3d-printing.html)
- [How to Get the Best Retraction Length & Speed Settings – 3D Printerly](https://3dprinterly.com/best-retraction-length-speed-settings/) 

teaching tech articles and videos
- [Teaching Tech 3D Printer Calibration](https://teachingtechyt.github.io/calibration.html)    
- [Teaching Tech Calibration Site - The Mininimal Workflow](https://minimalworkflow.com/post/teaching-tech-calibration-site/)    
- [3D printer calibration revolutionised - Step by step to better print quality - YouTube](https://www.youtube.com/watch?v=rp3r921DBGI)    
- [3D printer calibration site V2 - Still free and better than ever! - YouTube](https://www.youtube.com/watch?v=9kDK7czgMxc)    
- [Superslicer in built calibration guide for better 3D prints - YouTube](https://www.youtube.com/watch?v=0ImurmbV5pE)    
