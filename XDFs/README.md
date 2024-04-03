***USE ALL OF THESE AT YOUR OWN RISK!! THESE FILES COME WITH ABSOLUTELY NO WARRENTY, TO THE EXTENT PROVIDED BY APPLICABLE LAW***

# How I found the tables/Dissertation
So some random dude on E90Post says he's going to find some tables that popular tuning companies didn't find (paraphrased from original WOTBox install guide), and then he comes along and claims he's done it. I'll admit it, I'm a random guy and nowhere near the reputation of Anjuna, but here is how I acomplished what I claim.
### Getting Started
So I initially started with decompiling the MSD80 and 9E60B bins from tricore back to C. This approach was completely flawed. Not only are the values we need not in the decomp (and everything is a static address lookup), but the MSD80 and the MEVD17.xxx are entirely different.

I then started looking desperatly for a 9E60B A2L, searching all matters of forums, private trackers, etc, and came up short. There are companies claiming to sell the complete DAMOS for the 9E60B, but I highly doubt its legit as I'm pretty sure someone on the internet would have leaked it by now. I ended up finding a 2EH0B A2L (X5 xDrive35i), which was a complete A2L+Hex and as the xDrive35i also used the N55B30, it was just a matter of time and effort to find the tables I needed. BMW, is a German company, and Bosch, is also German. So it was no suprise the entire A2L was in German. I wrote a simple JavaScript program to translate the entire A2L to English via Google Translate APIs, and I was set.

### Finding Tables
Here is a simple flow: 
1. Find the table I want in WinOLS (X5)
2. Look at surrounding data, bytes that would be constant between files (i.e. spacing bytes, table ranges)
3. Search for matching bytes in the 9E60B bin in HxD
4. Add respective table to 9E60B xdf

There are a ton of tables in WinOLS, most of the work was just sifting through most of them and seeing if I could find something of use. As a proof of concept, I found the table "Pre-control correction bank 2/1 in the function monitoring" by just sifting through the Hex data, there was a single 1:1 match between the 2 files. So I figured it had to be the matching table. I then found 2 tables in the field "DMDMIL: "1.119.0 Diagnosis misfire detection - statistics, error handling and MIL control", which sounded like exactly the category I was looking for. The tables were "Misfire frequency per bank to achieve a fuel cutoff" and "Frequency of interruptions to achieve the hiding of further functions", which sounded like *exactly* what was happening with the DME handling the WOTBox. In the X5 A2L, the values were 2500 and 65535 respectivly. I followed the above steps until I found a 1:1 string of bytes matching, and then looked for 0x09C4, which was exactly the value I was looking for. Based on locality, and the equivalence of values between the 2 files, I believe all the tables I added are accurate. Testing is needed to confirm, and is why I must say..

***USE ALL OF THESE AT YOUR OWN RISK!! THESE FILES COME WITH ABSOLUTELY NO WARRENTY, TO THE EXTENT PROVIDED BY APPLICABLE LAW***

Feel free to submit any issues, or contact me on e90post with any questions