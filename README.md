<H1>ioBroker automatic smart dosing system for your pool</H1><br>
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/360993ba-7bee-4244-af24-dc68bc84c292" />
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/c98a46a7-58fe-4930-9cf6-0dbd4641376a" />
<img width="800" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/334a1773-f809-4697-b298-da825a4191d5" />

<br>
<br>

:rotating_light:**THIS TEXT WILL BE UPDATED**:rotating_light:

Official script can be found here on GITHUB only. Other sources are outdated.<br><br>
Download rtf file open it with texteditor or smililar. Import text in Blocklyeditor<br><br>
This dosing system is a DIY project that I designed for my pool. It is intended for a Bestway Steel Pro Max 427x122 with a volume of 15 cubic meters. I can be used for any other pool with a pipesystem. 

The entire project is subject to changes or updates to bring it up to the latest standard.
The system construction takes about 48 hours, depending on craftsmanship skills.

My dosing script is working for almost 2 years, almost without any failure. 

<h3>Key features:</h3>
1. The run times are self-calculating.<br>
2. Weather influences are automatically corrected.<br>
3. You can add water to your pool at any time without worrying about the pH value.<br>
4. When the pool is covered, automatic run time optimization occurs, using less chemicals.<br>
5. There are error messages if there are issues with the suction, which could indicate empty canisters or problems with the hose routing.<br>
6. The goal is to gradually reduce the pH to 7.2 and below over several days with smaller amounts of chemicals.<br>
7. Alias binding for you datapoints. Just enter sensors and fire up the script.
<br>
<br>
<img width="570" alt="Bildschirmfoto 2025-07-02 um 13 29 52" src="https://github.com/user-attachments/assets/75340805-8403-42bd-9166-e9bcaf7bc2af" />

<br>
<br>
This comprehensive setup ensures your pool maintenance is automated, efficient,and adaptable to different pool sizes and conditions.

Here you can see the control of PH value
<br>
<br>
<img width="570" alt="Bildschirmfoto 2025-07-02 um 11 17 22" src="https://github.com/user-attachments/assets/8473c399-2f72-4d61-acdc-ae8c564107d8" />

Here you can see Redox value
<br>
<br>
<img width="570" alt="Bildschirmfoto 2025-07-02 um 11 18 41" src="https://github.com/user-attachments/assets/614d3ad7-4499-4a48-b809-245e74a0b342" />


:white_check_mark: A long-term test is done for script logic

Since I use a solar system for this pool, I installed a D50 PVC fixed piping system. It's important to know this as the dosing system works best with it.

> [!WARNING]
>**Please note: 
>You always act at your own risk. Minor electrical work is required, and safe handling of chemicals is essential for safe operation. Please do not put yourself in danger, and consult a >professional if unsure. You act at your own risk. Furthermore, I emphasize that I am not a professional and have acquired the necessary expertise on my own.
>I do not accept any liability or warranty for your actions in any form.**

<h3>Step 1: Automatically measure pH and Redox values.</h3>

For beginners:<br>
In general, you can use any sensor that gives you the pH value or the redox. In the beginning, I used iopool.
iopool is a brilliant sensor that takes the hassle out of measuring pH levels. You can view live data from the pool, and for newcomers to pool maintenance, it's a real game-changer. Simple and very accurate. A parallel measurement with Poollab 2.0 showed an estimated 95% accuracy.
Make sure you can measure your pH value automatically. It's the most expensive part of your system, but crucial for integrating the data into my smart home. There are also other methods to measure pH. 

This is my current way to measure the values. Communication is via mqtt. You can find it on amazon. Important to know that you need additional probes. You can order them via aliexpress or amazon. Approx. 8€-35€

<img width="570" alt="Bildschirmfoto 2025-07-02 um 11 52 58" src="https://github.com/user-attachments/assets/78024595-4599-4e51-b3e7-38d8f98adc14" />

 
<h3>Step 2: Fixed Piping</h3><br>
 
A D50 fixed piping system is the best thing you can do for your pool. Please educate yourself on this topic. It makes sense to use D50 piping for pools of a certain size; it's essential for good pool operation. Check YouTube for more information; there are hundreds of videos on this topic.
 
The injection site has 3 openings for so-called injection valves. You can find the link to these in the BOM below. The 3 injection sites have ½ inch threads. I also got the injection valves from the same manufacturer. The hose connection is 4/6. The valve thread is 3/8. To fit the 3/8 inch valve into the ½ inch thread, a reducing thread is required. You can also get this through the website. Unfortunately, I no longer have the link, but you can simply contact the manufacturer or call them!
 

<h3>Step 3: ioBroker Smart Home</h3><br>
No separate control unit is needed for this WiFi-operated dosing system. The calculations and operation times for dosing are managed through the smart home. ioBroker is the tool of choice here. If you're not familiar with ioBroker, check YouTube to learn the basics. If you already have ioBroker up and running, congratulations. Just import the script and adjust it to your data points and preferences. Further instructions are in the comment boxes of the script.

Attention: I am currently working intensively on the script. Please read the updates.
Here is the logic of Script V4.0 alpha
 
pH Value<br>
***description coming soon***

Chlorine and Redox<br>
***description coming soon***


 ***BOM coming soon*** <br>
For further details on the BOM (Bill of Materials) and the associated links you need, please check this page in future. There, you will find information about the required materials, such as electrode holders, injection sites, pumps, hoses, and electronic components, along with direct links to their purchase pages. If you have specific questions about individual parts of the BOM or need help locating certain information, let me know! 

<h3>Link list</h3><br>
Bracket for pump https://makerworld.com/de/models/552588-eng-ger-smart-dosing-system-pool-iopool-iob#profileId-473624 <br><br>


I appreciate your likes and comments.

Best regards
