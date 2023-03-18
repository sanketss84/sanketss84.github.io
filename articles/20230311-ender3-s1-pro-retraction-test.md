## Ender3 S1 Pro Retraction Test Findings

Author: Sanket Sonavane   
Publish Date: 2023-03-11   
Last Updated: 2023-03-12

<div style="color: #084298; background-color: #cfe2ff; padding: 10px; border: 1px solid #b6d4fe; border-radius: 5px;">  
Hello! Dear Visitor the site is now migrated to [sanketsjournal.com](https://www.sanketsjournal.com).  <br>
It has a better design, dark mode, article search and category pages.  <br>
All my findings and latest adventures will be published on the new address. <br>  
Hope you enjoy the new experience.  
</div> <br>

> NOTE:  
> This is a live article i.e. as and when new information is observed or found it will be  
> 1. appended with time stamps to the end  
> 2. corrected in place, if earlier documentation was incorrect  
  
## what I am using
- Ender 3 S1 Pro on stock marlin firmware 
- Cura 522 as slicer of choice

## quick summary
after a lot of tests and trying to find the best value so far I have found that for Ender 3 S1 PRO with esun PLA+ filament produced best results 
- retraction distance 0.8mm
- retraction speed 40 and 50 mm/s 
- fan speed 100% 

I have not been able to better the fine threads much despite all tests 0.7 and 0.8mm are sweet spots.

## common settings for all retraction tests
- 0.3 Layer height was used for all
- 3 wall perimeter
- infill density 20
- infill pattern cubic
- initial temp 205nozzle 70bed
- temperatures 205 nozzle 60bed

## approaches to try 
these are summary of suggestions which I have received from various communities on discord and reddit

- [x] &nbsp; retraction speed 25mm/s
- [x] retraction speed 50mm/s
- [x] retraction distance 1.0mm
- [x] retraction distance 1.5mm and retraction speed 30mm/s
- [x] check [Retraction Calibration Tool](http://retractioncalibration.com/)
- [x] slowing down fan speed
- [ ] check combing options
- [ ] adding wipe distance
- [ ] check out teaching tech's calibration page
    - [ ] teaching tech retraction test

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

## retraction calibration tool
2023-03-12

[Retraction Calibration Tool](http://retractioncalibration.com/) this is an interesting test to help narrow down the retraction settings.

This is how I set the two tests up
![](/assets/img/s1-pro/retraction-calibration/s1pro-retraction-calibration-cnxsoft.png)

### attempt 1
2023-03-12

top  
![top](/assets/img/s1-pro/retraction-calibration/attempt1/top_med.jpg)

top-2  
![top-2](/assets/img/s1-pro/retraction-calibration/attempt1/top-2_med.jpg)

front  
![front](/assets/img/s1-pro/retraction-calibration/attempt1/front_med.jpg)

right  
![right](/assets/img/s1-pro/retraction-calibration/attempt1/right_med.jpg)

back  
![back](/assets/img/s1-pro/retraction-calibration/attempt1/back_med.jpg)

left  
![left](/assets/img/s1-pro/retraction-calibration/attempt1/left_med.jpg)


front-right  
![front-right](/assets/img/s1-pro/retraction-calibration/attempt1/front-right_med.jpg)

front-left  
![front-left](/assets/img/s1-pro/retraction-calibration/attempt1/front-left_med.jpg)

back-right  
![back-right](/assets/img/s1-pro/retraction-calibration/attempt1/back-right_med.jpg)

back-left  
![back-left](/assets/img/s1-pro/retraction-calibration/attempt1/back-left_med.jpg)


observations 
- anything above retraction distance of 2.25mm was producing stringing so skip those for next tests
- as the tower height increases more of the fine threads are observed
- walls have less gap from retraction distance 1.0mm onwards
- as layer height increases the fine threads start increasing so to test this hypothesis I need to increase number of layers for each retraction speed from 25 to 50 layers and see if this behaviour is observed

### attempt 2
2023-03-12

top  
![top](/assets/img/s1-pro/retraction-calibration/attempt2/top_med.jpg)

front  
![front](/assets/img/s1-pro/retraction-calibration/attempt2/front_med.jpg)

right  
![right](/assets/img/s1-pro/retraction-calibration/attempt2/right_med.jpg)

back  
![back](/assets/img/s1-pro/retraction-calibration/attempt2/back_med.jpg)

left  
![left](/assets/img/s1-pro/retraction-calibration/attempt2/left_med.jpg)


front-threads  
![○front-threads](/assets/img/s1-pro/retraction-calibration/attempt2/front-threads_med.jpg)

right-threads  
![○right-threads](/assets/img/s1-pro/retraction-calibration/attempt2/right-threads_med.jpg)

back-threads  
![○back-threads](/assets/img/s1-pro/retraction-calibration/attempt2/back-threads_med.jpg)

left-threads  
![○left-threads](/assets/img/s1-pro/retraction-calibration/attempt2/left-threads_med.jpg)


front-right  
![front-right](/assets/img/s1-pro/retraction-calibration/attempt2/front-right_med.jpg)

back-left  
![back-left](/assets/img/s1-pro/retraction-calibration/attempt2/back-left_med.jpg)


observations
- for back side, ignore retraction distance 1.3 to 1.6 as fine threads observed on the outside as well on inside.
- for left side, ignore retraction distance 1.7 to 2.0mm, while there are less of the fine threads but they are still there.
- as the tower height increases more of the fine threads are observed 
    - so for all sides with retraction speed for 10mm/s there is less of those fine threads.
    - these threads are visible on affected sides as we start going upwards in retraction speed 20, 30, 40, 50mm/s tests    
- after inspecting all sides and individual walls settled for retraction distance 0.9mm and retraction speed 40mm the 0.8mm is also good but 0.9mm looks better. 
- however actual test prints with 0.9 were not that good so reverted to 0.8mm

### normal retraction tower test
to test all the results of the above test here is the output of 

retraction distance  0.8mm retraction speed 40mm/s fan speed 100% and this looks good. 

[IMAGE ADD] 

retraction distance  0.7mm retraction speed 40mm/s fan speed 100% and this looks good as well. 

[IMAGE ADD]

## fan speed tests
2023-03-12

### attempt 1
retraction distance at 0.7mm and speeds at 40mm/s for this test

- testing at 50% ❌
[IMAGE ADD]
    - result: had far more fine threads than fan running at 100%

- testing at 70% 
    - skipped 

## references
reddit 
- [S1 Pro how to get rid of these fine threads that occur during prints : Ender3S1](https://www.reddit.com/r/Ender3S1/comments/11moh4t/s1_pro_how_to_get_rid_of_these_fine_threads_that/)

retraction calibration tool
- [Retraction Calibration Tool](http://retractioncalibration.com/)
- [3D Printer Retraction Calibration Vol II - Calibration Generator Program Release - CNX Software](https://www.cnx-software.com/2020/07/08/3d-printer-retraction-calibration-vol-ii-calibration-generator-program-release/#3d-printer-retraction-calibration-vol-ii)
- [How to Easily Calibrate Retraction in 3D Printers - CNX Software](https://www.cnx-software.com/2019/09/05/how-to-easily-calibrate-retraction-in-3d-printers/)

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

