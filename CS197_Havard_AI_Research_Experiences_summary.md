* Summary and lessons from - CS197 Harvard: AI Research Experiences
1. Approach
1.1 Reading Wide

1.2 Between Wide and Deep

1.2.1 Related Work
- At this stage, I'll find it effective to read the related works sections of these papers: They often
make it clear how researchers in the field have traditionally approached the prolems and
 what the emerging trends are. It's important to pick papers that are recently published.
+++ Update your notes from variety published research.
1.2.2 Note taking structure (to answer several questions to better undertand a paper).

- General
******************Paper Title (Topic))*******************
***************      Link     ******************
***************      Objective - Task   ********
**************       Methods            ********
**************       Dataset            ********
**************       Evaluation         ********

- Details
+++ Abstract summary - summary main points in paper.
++++ Make yourself comments if it is neccessary, even to recall your understands.

- Survey paper (Google Scholar beside Paper with code)
+++ A survey can contain overall pov, trends in the domain study
+++ Make your notes

1.3 Reading Deep

Notice: Most papers are written for an audience that shares a common foundation: that's what allows
for the papers to be relatively concise. Building that foundation takes time, in the span of months, 
if not years. Thus reading a first paper on a topic can easily take over 10 hours (some papers have
definitely taken me 20 or 30 hours) and leave one feeling overwhelmed.

So I would like to take an incremental approach here. Understand that, in your first pass, you will not
understand more than 10% of the research paper. The paper may require us to read another more fundamental
paper (which might require reading a third paper and so on; it could be turtles all the way down)! Then,
in your second pass, you might understand 20% of the paper. Understanding 100% of a paper might require a
significant leap, maybe because it's poorly written, insufficiently detailed, or simply too technically/
mathematically advanced. We thus want to aim to build up to understanding as much of the paper as 
possible - I'll bet that 70-80% of the paper is a good target.

1.3.1 Introduction section
I will highlight what I find to be important parts of the introduction. The yellow highlights are the
problems/challenges, the pink highlights are the solutions to the challenges, and the orange highlights
are the main contributions of the work we're reading.

![Highlight taking][def]

Notice the alternating yellow/pink highlights. The paper is introducing a general problem, talking about
a solution to that problem, then a problem with the solution, and another solution to that problem. Four
levels deep, the paper specifies the problem it solves.

Notice then that the contribution of the paper is a specific solution for a specific problem of a more
general solution for a more general problem of an even more general solution to an even more general problem
etc. This is typical. We can summarize our understanding of this problem-solution chain:

'''
- Introduction:
    - Problem 1: How to find alignment between image and text modalities?
	+ Solution 1: Pre-trained object detectors to find salient regions from images.
    - Problem 2: Limited by power of object detector and available annotations.
	+ Solution 2: Direct alignment without object detectors
    - Problem 2a: Efficiency because of lot of computation of self-attention on visual sequences
    - Problem 2b: Information asymmetry because text is short compared to info in image.
        + Solution 2a: connected attention network, using single transformer for early fusion. Has
                       problems 2a and 2b.
        + Solution 2b: cross attention network, does fusion on both modalities independently. No longer
                       has problem 2b, but still has 2a.
        + Solution 3 (proposed solution): cross-modal skip connections. Solves problem 2a abd 2b.
	
'''

![Introduction review][def2]

-->>> Need a figure to illustrate the proposed approach to compare with other methods.

![Model preview][def3]

'''
- Method section:
    - Need a figure which presents a simpler description of the architecture and objectives of the proposed model.
    - In general, well constructed figures and algorithm pseudocode can be of huge help to us!
    - What we can do for the methods section is maintain a list of concepts that we haven't quite understood.
'''

![Model illustration][def4]

You would have thus created a list of concepts you need to learn about, and the relevant paper for each,
if the paper specifies any.

Let continue reading, making our way through the methods sections, and the experiments section, highlighting the 
parts that we consider relevant to our understanding of the method as it relates to image captioning (for instance)
+ highlights the data setup, includes methods and evaluation metrics that may be unfamiliar to us, and we can make not
of that in our "To understand" list.

![To understand][def5]
'''
We continue reading through the rest of the experiments section.
'''

![To understand][def6]

While we can read through the results on tasks other than "the topic", I have ignored highlighting them. When reading 
papers, we are often being presented with a firehose of information, and it's useful to be selective in what we pay 
attention to. Let's continue reading.

![New approaches][def7]

You can now see that we have found another section of experiments. Zero-shot transferability may not be a concept we're
familiar with, so we likely will have to add that to our "to understand" list.

Finally, let's read the conclusion of the paper.












  


[def]: ./image/note_taking.png
[def2]: ./image/introduction_review.png
[def3]: ./image/model_preview.png
[def4]: ./image/model_illustration.png
[def5]: ./image/to_understand.png
[def6]: ./image/to_understand_update.png
[def7]: ./image/new_method_capturing.png