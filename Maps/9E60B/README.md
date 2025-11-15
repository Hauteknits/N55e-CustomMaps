# Custom Maps
There are 6 maps in here

All maps are tested and daily driven for ~2000-5000mi unless otherwise stated

Flame - Only difference is timing retardation at high RPM and low load
Flame2 - Same as above but runs a bit richer at high RPM and low load
2Stp - WOTBox compatible map
2StpTuner - WOTBox compatible with certain tuner codes disabled

1. 9E60B_STOCK > Self Explanitory
2. 9E60B_STOCK - Flame(Untested) > Stock mapping with flames at ~5k RPM (Untested, but should be fine)
3. 9E60B_PUMP2 - Flame > BMS PUMP2 BEF map with Flames (Tested, only use with JB4!)
4. 9E60B_PUMP2 - Flame2 > Same as above but with a -0.589 change in the fuel tables from 20-30 load and 5k-7k RPM.
5. 9E60B_E85 - Flame2 > BMS E85 BEF map with Flame2 changes made. Recommended for mixtures of E50 and up
6. 9E60B_E85_PI - Flame2  > BMS E85_PI map with Flame2 changes. Recommended for PI of E50 and up.
7. 9E60B_E85_PI - Flame2 - 2StpTuner > Personal Map. Same as above but for E50+ w/ PI
8. 9E60B_E85_PI - 2StpTuner > Personal Map, same as above but with no flames
9. 9E60B_STOCK - 2Stp > Stock map with WOTBox compatibility
10. 9E60B_E85_PI_THR - FullCustom > Maybe full custom is a stretch here, but this is my new daily map. Updated fuel scalar, S55 Oil Pressure, WOTBox compatible.
---
Use at your own risk! Flame tunes can really mess up your car. I have had metal shavings come out my exhaust in a video I took, so take that into consideration. Don't be upset if you blow your turbo or melt your cats
Do not, ever, run these tunes without catless DPs or DP cutouts, you will melt your cats

### Important Note for Port Injection!
I've been testing the PI maps as I recently installed port injection. The timing corrections are really aggressive at ~5k RPM and 10-30% pedal. The entire car lurches and can cause issues. The solution is to not light throttle it around 5k but I'd like to fix these issues at some point. These maps are fine to run daily, but just be warned and don't hold the car at that RPM.
Further Notes: The car has been jerking pretty heavily with these maps at certain RPMs, I'd be careful and mindful. I still daily these maps and don't have many issues, but defiantly keep this in mind as going from E85 to E85_PI with PI seems to have a large difference between the two

### Interesting observation with 9E60B_E85_PI_THR
My car has had a history of bad starts and maxing trims. I decided to check out the fuel start tables on my BIN and noticed they were absurdly high compared to the rest of the BINs provided by Burger Motorsport. Did some digging and found the scalars were also higher than the non THR map. Seems to me that other THR maps don't touch these tables either. In my FullCustom map, I reverted the fuel start to stock, and the fuel scalar to the nonTHR map. I'll update once I test.

***USE ALL OF THESE AT YOUR OWN RISK!! THESE FILES COME WITH ABSOLUTELY NO WARRENTY, TO THE EXTENT PROVIDED BY APPLICABLE LAW***