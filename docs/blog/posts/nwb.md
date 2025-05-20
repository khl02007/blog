---
date: 2025-05-19 
tags: neuroscience, NWB
---

# A brief primer on the Neurodata Without Borders (NWB) format

You may have heard that NWB is a *format* for neuroscience data. But what does that mean? What exactly is a data format? And how do we use NWB? 

We can gain some intuition about data formats from the ones that we are familiar with, such as JPEG (for images) and MP3 (for audio). We typically identify them by the letters at the end of file names. What these indicate is the *rules for representing and storing the data in the file*. By following these rules, the computer can encode the contents of the file as 1s and 0s in the storage device. And knowing these rules, we can reverse them and decode the contents in a way that makes sense to humans. Every format has some technical specifications of how the data is to be encoded and decoded. These can be very complicated, and often involves a lot of clever engineering to make the encoding and decoding process efficient. 

But at the end of the day, a file format is just a set of rules for representing and storing data. Construed this way, one might think that making a format is easy: just set down some rules. Let's take a concrete example relevant to neuroscience. Say you have some extracellular electrophysiology data from a multichannel neural probe. It is natural to think of this as a 2D array, with the two dimensions being channels and time. Each data point would then be the voltage measured at a channel at a time point. Though this seems simple, there are many other issues that creep in when we try to read or write our data on the computer. For one, we need to know extra information about it. We need to know if the first dimension is channel or time. We also need to know the sampling rate and the bit depth. And there are all these choices about how to store the data; CSV? numpy array? As you can see, this quickly becomes very complicated. And imagine that everyone more or less has their own way of dealing with these issues! This would be a nightmare if you care about sharing data with others. 

So one reason for adopting the NWB format is to simplify your life: NWB is a result of many people having thought deeply about how to represent neuroscience data, and you don't need to waste brain power coming up with new rules about how your data is represented. 

Another challenge associated with creaitng a file format is sociological. As we alluded to earlier, there are many ways of dealing iwht data. 

Now that we discussed some challenges with file format and how NWB addresses them, let's get into how we can use them. I think that efficiently using NWB means that (i) you first get clear about what kind of data that you have and how they relate to each other; and (ii) learn about what kind of represnetaiton NWB provides to support the data; and (iii) code it up. This can be as simple as a field (e.g. experimenter) or as complex as a custom datatype that is only usppored by a NDX. You should also keep in min. 

For actually learning to code, the best place to start is the official documentation website. There is also Other important tools include NeuroConv. NWB GUIDE, a user friendly GUI that allows you to do this conversion. You may still want to learn a bit about the code, esp fi you plan to load the data and anlayze it, at which point you will have to write code anyway. 

Once you go through this (hopefully not so dofficult) process, you can reap the frutis of your labor. You ahve saved your data in a stadardized format suppoted by community; you can immediately share it by uploading it to public reposidotries like DANDI; you can apply it to work with analysis software, many of which support NWB format. Most importantly, you can rest assured that your data is now compliant with the data management plan that journals and funding agencies are imposing on you. 




Until recently, there was no format that was widely adopted by neuroscientists. This made it problematic for the community to share data: with other labs, or within labs, or even with your future self. NWB was born to serve as the standard answer to this problem. But as I said, a format has to be widely adopted to be useful. And to achieve that, it has to accommodate everyone's[^2] needs--after all, why would you use it if it doesn't work for you? And given that neuroscientists are famous for doing all kinds of different stuff, this is a really hard social engineering problem that no amount of technical chops alone will solve. 



This is because a format is only as useful as its reach. The more widely used it is, the more likely it will be adopted by new users, since their data will be intelligible to more people. In that sense it is a bit like other phenomena that display network effects, such as social media. 


I will explain how NWB deals with this issue and how it can accommodate your data in a bit. For now, I want to return to the idea that a format is a set of rules for how to store data. Construed this way, we don't need much to get a format. We literally just need some rules. Yes, the part about getting everyone in the community on board is tough, but making rules is a rather straightforward activity. Let's take a concrete example. Say you have some extracellular electrophysiology data with some high-channel count probe. It is natural to think of this as a 2D array, where the two dimensions are channels and time and each data point is the voltage measured a channel at a time point. Though this seems simple, there are many other issues that creep in when we try to save this on the cmoputer or to read it. For one, we need to know information about it, such as the sampling rate and bit depth. One can just say: "save as 2d array with ". You can just proclaim these rules, and have everyone just folow them. In fact, another format in the neuroscience community called ONE is just that. 

Even though we can have such "minimal" format, in practice this will have many issues. One reason is that it leaves too much to the user. For one, how can we be sure that the rules are actually followed? we need to check it somehow. More importantly, how will we access the files in practice? If the format is defined at such an abstrct level, then we would potentially need many different types of programs to open it. Clearly we need a more detailed specificaiton. 

NWB anticipates this problem and gives a detailed efinition. It uses a backend 

For example, let's say you have a electrophysiology recording saved on your disk. It's probably in some format. Maybe it is in binary format, which means it's a bunch of 0s and 1s that you can't read but your computer can. Maybe it is in text format, like a CSV file. Maybe it is in a format that you are't really familiar with, like the proprietary formats that the company that made the data acquisition hardware uses. None of these are great formats for your data. This is because they either make it very hard to know what it is or to work with it. 


## Conclusion

NWB is a data format for storing and sharing neuroscience data. It's like a recipe for how to bake a cake. If you follow the recipe, you'll get a cake. If you don't, you won't. NWB is special because it's a recipe that many people have agreed on. If you store your data in NWB, other people will be able to read and analyze it. If you don't, they won't.

[^1]: This is what happens when you open the file with a program.
[^2]: OK, maybe not *everyone*, but at least large enough fraction of the community to enjoy the network effect.