---
draft: true
date: 2023-08-18
categories:
    - neuroscience
---

# Will systems neuroscience succeed?
The current approach to systems neuroscience (i.e. find representations and study how they are transformed) is not up for the job.
<!-- more -->
A central idea in modern neuroscience is that of the brain as a computer. But what do we mean by *compute*? Although the brain is quite different from the silicon-based digital computer in its parts, they share the commonality that they both transform representations. 

What is the most important concept in neuroscience? I think the answer is clear: *representation*. The goal of neuroscience is continuous with disciplines like psychology, cognitive science, and artificial intelligence: it is to understand intelligent systems. The brain, of course, the prototypical example of an intelligent system (the only one, in fact, we know for sure is intelligent). And neuroscientists look at the implementational level (networks of biological neurons) to understand how they may give rise to intelligence. To do so, the stories we tell primarily depends on the idea of representation. For example, we may say that a particular type of retinal ganglion cell represents an object moving in a particular direction. Simialrly, hippocampal pyramidal cells represent the animla's current location in the enviornment, and the neurons of primate IT cortex represent faces. Under this framework, the job of the neuroscientist is to identify where in the brain different representations are located, and to trace how they are *computed*: i.e. how one representation is transformed to another.
Therefore much effort has been invested in trying to record from more and more nueorns (because the critical unit of representation is thought to be the single neuron). Theorists build models of the brain to explain how the transfomraiton of representation (which can in general mathematical function) can be implemnted by biological neurla netowrks, e.g. how a group of neurons can maintain the memory of a recenlty experienced stimulus until a decision is made. We also track the same set of neurons to see how the representatiosn evolve over time -- this is called learning and it is largely thought to occur through modification of the strengths of the connections between neurons. Some might complain this is a bit too simplistic but for the most part I take this as uncontroversial.[^1] 

So we often think of the hippocampus as represneting some place; the basal ganglia as representing (one's expectation of) reward; and higher order visual cortical areas as representing object identities. This way of thinking naturally lends itself to extension; for example, when we see unexpectedly meet someone we like in a partiuclar location, we would expect the hippocampus, basal ganglia, and the IT cortex to all "light up" at the same time, this co-activity essentially encoding the animla's experinece. In other words, our view of neural representations are simple (i.e. there is nothing to seeing a face other than the activity of face selective neuron), localized (different areas represent different things), and picture-like (so that coactivity essentially 'paitns the scene', each part of the scene delegated to discrete brain regions). Note that the story doesn't change one bit if we change the talk of single nueron to a group of neurons whose acitivyt may be confined to some low dimensional space.

[^1]: I'm aware that there are people who disagree with this represnetation-centric account of brain function. But I think the vast majority of neuroscientists are represnetiaotnlaists, and the alternative theories (e.g. dyanmcial systems approach) just havne't bene veyr convincing in understanding . Even if that might be true it could be that we need to use the concept of representaiton if we are to udnerstand these -- I take this as what someone liek Dennett believes.

But there are reasons to be pessimimstic about this approach leading to understadnign of brain function:
- despite decades of neurophysiology, we stil don't understand what many neurons or groups of neurons in the brain represent; this is simliar to the situation in deep learning, where the represntaiton at many intermediate layers are simply not interpretable
- The representations can change abrupty; we either have incomplete information or there is plasticity
- They also represent multiple things, depending on the context
- even in deep learning, we have not been able to figure out exactly how the representations are 
This makes me think that it will be impossible to find the complete mapping from neurons / groups of neurons to representations, let alone 

Even if this project is successful, it is unclear what we will get out of it. The current approach resembels the Empiricist idea of the mental representation as a picture. But a picture is limited; what you want is language; something that you can use to verify truth, test hypotheses, etc. We are still stuck with some form of associationism / behaviorism that follows from this idea. Aritifical neural networks / connectionism is also from this. These are not adequate to model cognition / intelligence.

If this is right, there are two ways to remedy it. 

1. Demand more from representations
This is already what most neuroscientists think implicitly. Many neuroscientists claim to be connectionists but are really Fodorians. For example, how are internal models that operate on the structure of input supposed to arise out of neural networks? The problem for this view is that it is unclear how biology implements Turing machine.

1. Drop repesentations / the idea of the brain as a computer altogether
This is more radical. Not sure if we can do this.