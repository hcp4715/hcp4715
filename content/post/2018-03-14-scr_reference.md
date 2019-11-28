---
id: 717
title: References for beginners on skin conductance response (SCR)
date: 2018-03-14T06:36:08+08:00
author: Chuanpeng Hu
layout: post
guid: http://www.huchuanpeng.com/?p=717
permalink: /2018/03/14/scr_reference/
categories:
  - Methodology
  - Social Neuroscience
---
Skin conductance response (SCR) is a widely used psychophysiological measurement in psychology, especially emotion studies. Even it is a relatively old method used in psychology, it seems that there is no explicit standard you can use, more or less the tips are told by your colleagues instead of from an explicit guidebook.

Here I record the articles, books, and manuals that helped me to know more about SCR, which I will be used in a fear extinction study.

The workflow of the SCR is not complex, only three steps:

**Recording.**The most or lest important thing you need to care, depending on your lab&#8217;s experience. It is the most important thing because data quality is always the most important aspect of research. &#8220;garbage in, garbage out&#8221;. It is the lest important thing because usually you just follow the way your lab&#8217;s done before. The question in this step is: which part of the body will you stick the electrode, how can you get good signals.

**Preprocessing**.surprising! With a cognitive psychology background, I&#8217;ve thought that only EER & MRI data need a preprocess, but actually, SCR data need that too (actually all kinds of data need a preprocess, the only difference is how much time it cost and how complicated it is).

The preprocess of SCR data usually include a low-pass filtering or down-sampling. After that, you begin to deal with the real data.

The question at this stage is: first, the time point of the onset of SCR (<a href="http://onlinelibrary.wiley.com/doi/10.1111/j.1469-8986.1985.tb01626.x/full" data-blogger-escaped-target="_blank">Levinson and Edelberg 1985</a> reported that 1000 ms ~ 4 000ms after the onset of stimuli were used most frequently, from Boucsein, 2013; we use 900 ms ~ 4 000 ms).

Second, after knowing the onset, the next step is how to calculate the magnitude (**Important Note:** amplitude and magnitude are different things in SCR,<span class="fontstyle0">sum non-zero amplitudes / number of non-zero responses = mean amplitude; mean magnitude </span>= mean value computed across all stimulus presentations including those without a measurable response). which threshold used to judge one trial has SCR or not (zero-response)? There is also no standard way for this. Braithwaite et al. (2015) mentioned that historically the most common threshold is 0.05 µS, but now the common threshold is range from 0.01 to 0.04 µS. In our study, we used 0.02 µS.

After extract the SCR amplitude value, the data need to be normalized and standardized. Braithwaite et al. (2015) make a good distinction between the two: Normalization is to make data of each participant more like parametric data (therefore can subject to parametric data analysis), which is necessary; standardized is between participants, to make each participants&#8217; data comparable to each other, which is not always necessary. There are many different ways to do the normalization and standardization, Braithwaite et al. (2015) give many typical approaches, please check the document (p10 ~ p11).

In our lab, we used magnitude, which is the normalized log transformation (log(S+1), S = raw magnititude); for standardization, we used the range-correction ((SCL &#8211; SCLmin) / (SCLmax &#8211; SCLmin: Dawson et al., 2001)).

**Analyzing**: after preprocessing, do whatever statistic you like.

&nbsp;

**Related software**:

http://ledalab.de/

https://github.com/johnksander/BreatheEasyEDA

http://pspm.sourceforge.net/

Of course, my understanding might be wrong, cause I am also a beginner in this field. So here are the references and what I learned from each:

First of all, EDA or SCR is not as simple as it appears to be. At least there are books about it. Here are two examples:

_Boucsein (2012), Electrodermal Activity (2nd). Springer_

_Greco, et al., (2016), Advances in Electrodermal Activity Processing with Applications for Mental Health. Springer._

Second of all, check the guideline from the Society of Psychophysiology, the have a <a href="https://www.ncbi.nlm.nih.gov/pubmed/22680988" data-blogger-escaped-target="_blank">Publication recommendation for electrodermal measurements</a>. In section 3.1, there is one paragraph about the latency of SCR, which is a good rule of thumb about how you shall decide which part of your data is SCR. This section also mentioned different index of SCR: amplitude, area under the EDR curve etc.

Then, there are some terms that you might want to know before jump into all the mess, and Boucsein (2012) have made a table to make life easier:

Braithwaite et al. from Birmingham have a very clearly explained online guide. If you only want to read one document, this one is recommended. The link is <a href="https://www.birmingham.ac.uk/Documents/college-les/psych/saal/guide-electrodermal-activity.pdf" data-blogger-escaped-target="_blank">here</a>.

Braithwaite, Watson, Jones, & Rowe, A Guide for Analysing Electrodermal Activity (EDA) & Skin Conductance Responses (SCRs) for Psychological Experiments

For a practical and brief introduction, please see:

B. Cowley, M. Filetti, K. Lukander, J. Torniainen, A. Henelius, L. Ahonen, O. Barral, I. Kosunen, T. Valtonen, M. Huotilainen, N. Ravaja, G. Jacucci, The Psychophysiology Primer: A Guide to Methods and a Broad Review with a Focus on Human–Computer Interaction DOI: 10.1561/1100000065.

Another often-mentioned book chapter (of which book the founder of social neuroscience John Cacioppo is the editor):

Dawson, M. E, et al. (2000). <a href="https://ccsn.uchicago.edu/sites/ccsn.uchicago.edu/files/uploads/Chapter%208.pdf" data-blogger-escaped-target="_blank">The electrodermal system</a>. In Cacioppo, J. T, Tassinary, L. G. & Berntson, G. (ed), Handbook of Psychophysiology. Cambridge University Press, Cambridge UK, 2nd edition, 2000.