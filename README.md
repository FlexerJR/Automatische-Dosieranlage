<H1>ioBroker automatic smart dosing system</H1><br>
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/360993ba-7bee-4244-af24-dc68bc84c292" />
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/c98a46a7-58fe-4930-9cf6-0dbd4641376a" />
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/334a1773-f809-4697-b298-da825a4191d5" />
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/e71b5bd6-3fda-4838-aa85-a0039252e1cb" />

<br>
<br>
:rotating_light:Official script can be found here on GITHUB only. Other sources are outdated.:rotating_light:<br><br>
:rotating_light:Due to the high number of request via telegram i decided to create a FAQ for your questions.:rotating_light:<br><br> 

Please check this page for further updates. I'm sorry but it will take some time.<br>
Furthermore there are many setups of different pools out there. You should prepare your setup by yourself.<br>
I can give you some recommendations for the best course of action.<br>
If you have any questions feel free to contact me. I can provide a checklist for hardware installation.<br><br>
:bulb:Saltwater:bulb:<br>
I don't have a saltwater pool myself, so the script isn't optimized for saltwater yet. If you want to use it with your saltwater pool, just reach out and we can work on a version together. Volunteers welcome!<br><br>


This dosing system is a DIY project that I designed for my pool. It is intended for a Bestway Steel Pro Max 427x122 with a volume of 15 cubic meters. I can be used for any other pool with a pipesystem. 

The entire project is subject to changes or updates to bring it up to the latest standard.
The system construction takes about 48 hours, depending on craftsmanship skills.

My dosing script is working for almost 2 years, without any failure. <br>
Download rtf file open it with texteditor or smililar. Import text in Blocklyeditor<br>

<h3>Key features:</h3>

:white_check_mark: The run time of pump operation is self-calculating.<br>
:white_check_mark: A long-term test is done for script logic<br>
:white_check_mark: New safety feature. Kill function if wifi connection to pumps is lost.<br>
:white_check_mark: Automatic shutdown of automode if poolpump is stopped.<br>
:white_check_mark: Smooth release of chlorine to give constant redox level. Hell, thats hot!<br>
:white_check_mark: Automode is switched on after 30 minutes when poolpump is active again.<br>
:white_check_mark: You can use any pump system you want. We only need a switch for on/off.<br>
:white_check_mark: Weather influences are automatically corrected.<br>
:white_check_mark: Runtime will be corrected, if your chlorine becomes more and more inefficient.<br>
:white_check_mark: You can add water to your pool at any time without worrying about the pH value.<br>
:white_check_mark: When the pool is covered, automatic run time optimization occurs, using less chemicals.<br>
:white_check_mark: The goal is to gradually reduce the pH to 7.2 (adjustable) and below over several days with smaller amounts of chemicals.<br>
:white_check_mark: Alias binding for your datapoints. Just enter your sensors and fire up the script.<br>
:white_check_mark: New mechanism for chlorine.<br>
:white_check_mark: pH has priority over chlorine.<br>
:white_check_mark: (Coming soon) There are error messages if there are issues with the suction, which could indicate empty canisters or problems with the hose routing.<br>

<br>

<h3>Outlook of future version:</h3><br>
:smiley: Automatic shock chlorination mode. Can be configured based on time intervals or specific date and time<br>
:smiley: After calibration of your ph/orp sensors the script will pause operation for one hour<br>
:smiley: If your pump isn't operation 24/7, script will ignore redox value if poolpump is off<br>
:smiley: Script will operate only if poolpump is working again. Check future F.A.Q.<br>
:smiley: Enhanced autocalibration mode for chlorine runtime in different situations.<br>
:smiley: Long term warning if your chemicals become ineffective<br>
:smiley: Auto recalibration if autocalibration doesn't match anymore<br>
<br>

<h3>Hardware/Software needed</h3><br>
:wrench:Javascript Adapter 9.0.9. or higher<br>
:wrench:Ping adapter iobroker<br>
:wrench:Sonoff adapter or similar<br>
:wrench:Sensor for pH and redox<br>
:wrench:Switch for pool pump<br>
:wrench:Switch for pH pump<br>
:wrench:Switch for redox pump<br>
:wrench:All sensors and switches must be controllable via iobroker<br>

<br>


<H4>Here one screenshot of V4.1.6. beta (released)</H4>
<br>

Here you can see the delta value. The red line shows the deviation from selected redox target. The white line shows runtime in seconds.
<br><br>

<img width="583" alt="Bildschirmfoto 2025-07-28 um 21 35 49" src="https://github.com/user-attachments/assets/f33ab79e-4f98-44fd-86ea-6fe444df3372" />
<br>
<img width="583" alt="Bildschirmfoto 2025-07-28 um 21 34 48" src="https://github.com/user-attachments/assets/1d17d3ef-ad98-4e07-b2b2-33d05d52f810" />
<br>
<img width="583" alt="Bildschirmfoto 2025-07-05 um 20 11 26" src="https://github.com/user-attachments/assets/05bf7508-4ae1-4f86-8ff4-83c3a57747da" />
<br>
<br>

<br>
<br>


> [!WARNING]
>**Please note: 
>You always act at your own risk. Minor electrical work is required, and safe handling of chemicals is essential for safe operation. Please do not put yourself in danger, and consult a professional if unsure. You act at your own risk. Furthermore, I emphasize that I am not a professional and have acquired the necessary expertise on my own.
I do not accept any liability or warranty for your actions in any form.**
>

Check wiki page for further explanation https://github.com/FlexerJR/Automatische-Dosieranlage/wiki/List-of-Datapoints <br><br>

<img width="570" alt="Bildschirmfoto 2025-07-02 um 13 29 52" src="https://github.com/user-attachments/assets/75340805-8403-42bd-9166-e9bcaf7bc2af" />

<br>
<br>
This comprehensive setup ensures your pool maintenance is automated, efficient and adaptable to different pool sizes and conditions.

<h3>Step 1: Automatically measure pH and Redox values.</h3>

First things first<br>
Since I use a solar system for this pool, I installed a D50 PVC fixed piping system. It's important to know this as the dosing system works best with it.
In general, you can use any sensor that gives you the pH value or the redox. In the beginning, I used Iopool.
Iopool is a brilliant sensor that takes the hassle out of measuring pH levels. You can view live data from the pool, and for newcomers to pool maintenance, it's a real game-changer. Simple and very accurate. A parallel measurement with Poollab 2.0 showed an confirmed 95% accuracy.
Make sure you can measure your pH value automatically. It's the most expensive part of your system, but crucial for integrating the data into your smart home. There are also other methods to measure pH. 

In the picture below you can see my current way to measure the values. Communication is via mqtt every 5 seconds. You can find it on amazon. Important to know that you need additional probes. You can order them via aliexpress or amazon. Approx. 8€-35€

<img width="570" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/78024595-4599-4e51-b3e7-38d8f98adc14" />

 
<h3>Step 2: Fixed Piping</h3><br>
 
A D50 fixed piping system is the best thing you can do for your pool. Please educate yourself on this topic. It makes sense to use D50 piping for pools of a certain size; it's essential for good pool operation. Check YouTube for more information; there are hundreds of videos on this topic.
 
The injection site has 3 openings for so-called injection valves. You can find the link to these in the BOM below. The 3 injection sites have ½ inch threads. I also got the injection valves from the same manufacturer. The hose connection is 4/6. The valve thread is 3/8. To fit the 3/8 inch valve into the ½ inch thread, a reducing thread is required. You can also get this through the website. Unfortunately, I no longer have the link, but you can simply contact the manufacturer or call them!
 

<h3>Step 3: ioBroker Smart Home</h3><br>
No separate control unit is needed for this WiFi-operated dosing system. The calculations and operation times for dosing are managed through the smart home. ioBroker is the tool of choice here. If you're not familiar with ioBroker, check YouTube to learn the basics. If you already have ioBroker up and running, congratulations. Just import the script and adjust it to your data points and preferences. Further instructions are in the comment boxes of the script.

Attention: I am currently working intensively on the script. Please read the updates.
Here is the logic of Script V4.0 alpHa
 
<h3>pH Value</h3><br>

In the upper part of the video you can see release of pH-.<br>

https://github.com/user-attachments/assets/e2681d96-8c47-4640-99c9-1a5f30d189ee

<br>
<h3>Chlorine and Redox</h3>
<br>
In the upper part of the video you can see increase of redox level.
<br>
<br>

https://github.com/user-attachments/assets/a9bfb397-abb6-4b71-b898-89e757398501 

<br>
<br>
Feel free to contact me
<br><br>
<img width="300" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/2709624f-8e4c-436c-8098-ca5dfe410f84" />

<br>
<br>

 ***BOM*** <br>
For further details on the BOM (Bill of Materials) and the associated links you need, please check this page in future. There, you will find information about the required materials, such as electrode holders, injection sites, pumps, hoses, and electronic components, along with direct links to their purchase pages. It is only one example how to setup a pipesystem. If you have specific questions about individual parts of the BOM or need help locating certain information, let me know! List not completed.

| Amount  | Typ | Link  |
| ------------- | ------------- | ------------- |
|1|Elektrodenhalter|[ PVC Welt  ](https://www.pvc-welt.de/PVC-U-Elektrodenhalter-HTC-transparent-2fach-2-3-Verschraubung)|
|1-3|Alternative Impfstelle|[ PVC Welt  ](https://www.pvc-welt.de/Elektrodenhalter-Impf-Dosieranschluss-auf-Anbohrschelle_2)|
| 1-3 |Fafeicy G528 DC12V Mini|[ Amazon  ](https://www.amazon.de/dp/B08FR9N3PQ?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|1-3|Very good pump|[ Amazon  ](https://www.amazon.de/dp/B06ZZDLTJ7?ref=ppx_yo2ov_dt_b_fed_asin_title)|
| 1-3 |Reduzierstück 3/8 auf 1/2|Missing Link|
| 1-3 |Sonoff 4ch Pro|[ Amazon  ](https://www.amazon.de/sonoff-4ch-pro/s?k=sonoff+4ch+pro)|
|3|Gewindestopfen|[ Amazon  ](https://www.amazon.de/dp/B00512O0WQ?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|1|Teflonband|[ Amazon  ](https://www.amazon.de/s?k=teflonband+gewindedichtband&crid=24MYZBZUUGVMY&sprefix=teflonband%2Caps%2C102&ref=nb_sb_ss_pltr-xclick_2_10)|
|5m-25m|Schlauch 4/6|[ Amazon  ](https://www.amazon.de/dp/B005JYLABK?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|1|15W Netzteil|[ Amazon  ](https://www.amazon.de/dp/B09MHYD1FG?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|2x5|Wago-Klemmen|[ Amazon  ](https://www.amazon.de/dp/B077J2GWM8?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|1|Tangit Kleber|[ Amazon  ](https://www.amazon.de/dp/B00DY40144?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|1|PVC-Reiniger|[ Amazon  ](https://www.amazon.de/dp/B00BNSS4CE?psc=1&ref=ppx_yo2ov_dt_b_product_details)|
|2-6|M3 Schrauben|Missing Link|
|2-6|M3 Gewindeeinsätze|[ Content Cell  ](https://www.amazon.de/s?k=m3+heat+insert&crid=2GVKFLDHMI3L9&sprefix=m3+heat%2Caps%2C122&ref=nb_sb_ss_pltr-xclick_1_7)|



<h3>Link list</h3><br>
Bracket for pump https://makerworld.com/de/models/552588-eng-ger-smart-dosing-system-pool-iopool-iob#profileId-473624 <br>
Bracket for wago https://makerworld.com/de/models/192672-wago-221-modular-mount-organiser-for-all-types#profileId-212959<br><br>

I appreciate your likes and comments.

Best regards<br><br>


<h3>:white_check_mark:Changelog & Todo 17.07.2025</h3>

Wiki page<br>
-Recommendations for hardware installation<br>
-F.A.Q., Documentation for script, and so on<br>
-Update wiki due to new logic<br>
-Further explanation datapoints
<br>
<br>

Todo and upcoming feautures <br>
-Automatic shock chlorination mode<br>
-Rebuild of error and warning messages<br>
-Some datapoints are unnecessary for new logic and have to be deleted. <br><br>

Changes 4.1.6 beta: <br>
-This version is tested for 7 days. No bugs, no failures. Final release of stable after stress test.<br>

Changes 4.1.5 alpha: <br>
-Introduced surveillance with ping adapter. This is very important! If you are loosing WIFI connection to your PH/Chlorine pumps while the pump is active, the pump will not receive a stop signal. <br> With this new version the script will monitor connection of your pumps and will switch it off when reconnected<br>

Changes 4.1.4 alpha: <br>
-Minor bug fix<br>

Changes 4.1.3 alpha: <br>
-Minor bug fixes of PH Minus calculation<br>

Changes 4.1.2 alpha: <br>
-Minor bug fixes<br>
-Rebuild of variables<br>

Changes 4.1.1 alpha: <br>
-Minor bug fixes<br>
-Abgabeintervall_Minuten deactivated for debugging<br>
-Introduced Debugmode. You can ignore it. Default value is false<br><br>

Changes 4.1.0 alpha: <br>
-Integrated new logic of pump operation for chlorine.<br>
-Minor Bug fixes of datapoints. <br>
--------------------------------------------------- <br><br>





