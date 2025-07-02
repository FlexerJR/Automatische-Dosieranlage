<H1>Automatic smart dosing system for your pool</H1>

![IMG_4430](https://github.com/user-attachments/assets/c98a46a7-58fe-4930-9cf6-0dbd4641376a)

Description below.

THIS TEXT WILL BE UPDATED

Official script can be found here GITHUB VERSION 4.0 alpha is online

This dosing system is a DIY project that I designed for my pool. It is intended for a Bestway Steel Pro Max 427x122 with a volume of 15 cubic meters. I can be used for any other pool with a pipesystem. 

The entire project is subject to changes or updates to bring it up to the latest standard.
The system construction takes about 48 hours, depending on craftsmanship skills.

My dosing script is working for almost 2 years, almost without any failure. 

Key features:
- The run times are self-calculating.
- Weather influences are automatically corrected.
- You can add water to your pool at any time without worrying about the pH value.
- When the pool is covered, automatic run time optimization occurs, using less chemicals.
- There are error messages if there are issues with the suction, which could indicate empty canisters or problems with the hose routing.
 
The goal is to gradually reduce the pH to 7.2 and below over several days with smaller amounts of chemicals.

A long-term test is done!
 
I appreciate your likes and comments.

Since I use a solar system for this pool, I installed a D50 PVC fixed piping system. It's important to know this as the dosing system works best with it.
 
<style=“color:red“>Please note: 
You always act at your own risk. Minor electrical work is required, and safe handling of chemicals is essential for safe operation. Please do not put yourself in danger, and consult a professional if unsure. You act at your own risk. Furthermore, I emphasize that I am not a professional and have acquired the necessary expertise on my own.
I do not accept any liability or warranty for your actions in any form.
</style>




Functionality & Installation
Step 1: Automatically measure pH and Redox values.
 
iopool
iopool is a brilliant sensor that takes the hassle out of measuring pH levels. You can view live data from the pool, and for newcomers to pool maintenance, it's a real game-changer. Simple and very accurate. A parallel measurement with Poollab 2.0 showed an estimated 95% accuracy.
 
Make sure you can measure your pH value automatically. I use the Smart Pool Monitor from iopool for this purpose. It's the most expensive part of your system, but crucial for integrating the data into my smart home. There are also other methods to measure pH. For now, I might expand this project later to include Arduino-based pH/Redox probes.
 
Link: https://iopool.com/de-de/
 
Step 2: Fixed Piping
 
A D50 fixed piping system is the best thing you can do for your pool. Please educate yourself on this topic. It makes sense to use D50 piping for pools of a certain size; it's essential for good pool operation. Check YouTube for more information; there are hundreds of videos on this topic.
 
The injection site has 3 openings for so-called injection valves. You can find the link to these in the BOM below. The 3 injection sites have ½ inch threads. I also got the injection valves from the same manufacturer. The hose connection is 4/6. The valve thread is 3/8. To fit the 3/8 inch valve into the ½ inch thread, a reducing thread is required. You can also get this through the website. Unfortunately, I no longer have the link, but you can simply contact the manufacturer or call them!
 
Smart Home
ioBroker & Grafana
Step 3: ioBroker Smart Home
No separate control unit is needed for this WiFi-operated dosing system. The calculations and operation times for dosing are managed through the smart home. ioBroker is the tool of choice here. If you're not familiar with ioBroker, check YouTube to learn the basics. If you already have ioBroker up and running, congratulations. Just import the script and adjust it to your data points and preferences.
Attention: I am currently working intensively on the script. Please read the updates at the end for the current status.
Here is the logic of Script V3
 
pH Value
The pH value is checked three times a day at 08:05, 12:00, and 16:00. If the pH exceeds a threshold, such as 7.2, a pH reducer is added. The duration for this action is taken from the current run time data point. One hour later, it checks whether the pH has decreased. If not, an error message is issued. If the pH has decreased, no message is sent. After 23 hours and 55 minutes, it checks how much the pH has decreased. If the difference between the old and new values is greater than 0.3, 20 seconds are subtracted from the run time (e.g., from 120 seconds). If the difference is less than 0.2, 20 seconds are added to the run time. In the next version, I will make the addition of seconds adjustable. For smaller pools, 20 seconds might be too much or too little for larger pools.

Chlorine and Redox
The logic for Redox and chlorine is nearly identical to that of pH Minus. Here too, it checks whether the chlorine content has increased. If the Redox value is higher one hour after dosing, all is well.
Six hours after dosing, it calculates the run time for chlorine, requiring a target value above the decision value.
If the Redox value is above the target, the run time is decreased by 30 seconds. If it is below the target, 30 seconds are added. An update to the seconds will be included in Script V3.2.

Example: Decision value 750, target value 780

The actual bracket discussed here can be downloaded from the following link. The bracket can be fixed with small Spax screws. Be careful not to overtighten as the pumps are not the quietest. If I find quieter ones, I will update. Each bracket requires 2xM3 heat inserts and screws, as shown in the images.
 
Bracket for Wago
https://makerworld.com/en/models/192672#profileId-212959
 
This comprehensive setup ensures your pool maintenance is automated, efficient, and adaptable to different pool sizes and conditions.
 
For further details on the BOM (Bill of Materials) and the associated links you need, please check below in your document or in the compilation I have already shared with you. There, you will find information about the required materials, such as electrode holders, injection sites, pumps, hoses, and electronic components, along with direct links to their purchase pages. If you have specific questions about individual parts of the BOM or need help locating certain information, let me know! 
