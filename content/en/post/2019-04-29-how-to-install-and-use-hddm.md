---
id: 861
title: How to install and use HDDM
date: 2019-04-29T02:13:27+08:00
author: Chuanpeng Hu
layout: post
guid: http://www.huchuanpeng.com/?p=861
permalink: /2019/04/29/how-to-install-and-use-hddm/
categories:
  - Modelling
  - Methods
tags:
  - DDM
  - perceptual decision-making
  - python
---

**Feburary 14, 2021 update: Please note that this blog post was outdated because of the updates of Anaconda/miniconda.**

August 2020 update: I've created a [HDDM docker image](https://hub.docker.com/r/hcp4715/hddm), which can be easily installed and used after installing [docker](https://www.docker.com/).

HDDM is a python package for drift diffusion model (DDM, see http://ski.clps.brown.edu/hddm_docs/). I used it to decompose the reaction time and accuracy data in my recent manuscript: <a rel="noreferrer noopener" aria-label="Good Me Bad Me: Does Valence Influence Self-Prioritization During Perceptual Decision-Making (opens in a new tab)" href="https://psyarxiv.com/9fczh" target="_blank">Good Me Bad Me: Does Valence Influence Self-Prioritization During Perceptual Decision-Making</a>.

Here are a few tips on how to install and use HDDM, in case that you plan to replicate my analyses using the code and data I share <a rel="noreferrer noopener" aria-label="here on Github (opens in a new tab)" href="https://github.com/hcp4715/moralSelf_ddm" target="_blank">here on Github</a>. 

The targeted reader of this post are Windows users. (I assume that for most Linux users, you, in the most cases, can figure out how to install and use this package, at least with the help from the online forum (https://groups.google.com/forum/#!forum/hddm-users)). 

My system information: Win 10 pro, 64 bit, 16 GB RAM

### Step 1: prepare the python environment: 

1.1. Download and install Anaconda 3.6 or 3.7 from https://www.anaconda.com/distribution/.

1.2. Create virtue python 3.5 environment.

To do that, you need first run the **_Anaconda Prompt_**, which will be available after you installed Anaconda, as administrator, then run the following code: 

<pre class="wp-block-code"><code>conda create -vv -n py35 python=3.5 jupyter  # py35 is the name of the environment, which can be arbitrary </code></pre>

1.3. Activate the py35 env. :

<pre class="wp-block-code"><code># To activate this environment, use:

conda activate py35

# To deactivate an active environment, use:
conda deactivate</code></pre>

### **Step 2: install HDDM**  


Now you have a python 3.5 environment, you can then install the HDDM package. Of course, you need to activate the py35 environment first. Then:

2.1. Install HDDM by following code:

<pre class="wp-block-code"><code>conda install -c pymc hddm  # (or conda install -c pymc python=3.5 hddm )
-proceed?: y</code></pre>

2.2. Update kabuki, which is crucial package that HDDM depends on, to 0.6.2, otherwise models can not be saved). You can check the version of kabuki to make sure you do have installed 0.6.2

<pre class="wp-block-code"><code>pip install -U --no-deps kabuki --ignore-installed

conda list # check the version of kabuki </code></pre>

### **Step 3: use HDDM**

Now, we almost ready. A final step is to use an appropriate editor for editing and running the scripts. I used both jupyter lab (an updated version of jupyter notebook, but you can use jupyter notebook) and spyder. The script files of the former ends with &#8220;.ipynb&#8221;, the script files of the later one end with &#8220;.py&#8221;

To use jupyter lab, if you like, you need to install jupyter lab in your py35 env. As follows:

<pre class="wp-block-code"><code>
conda install jupyter lab
</code></pre>

After that, changing the working directory of _anaconda prompt_ to the folder where you stored the scripts and data, and type _jupyter lab_ to open run jupyter lab. Note the (weird) way to change directory in windows system.

<pre class="wp-block-code"><code>
cd /d c:\goodme\2_pilot_study\Results\4_hddm\  # in windows you have to add /d to change the directory

# run in jupyter lab or jupyter note book, for stim-based modelling

jupyter lab #(or jupyter notebook if you use jupyter notebook)

</code></pre>

Similarly, to run in spyder, you need to install spyder in this py35 env.&nbsp; 

<pre class="wp-block-code"><code>conda install spyder</code></pre>

Then, type _spyder_ to activate spyder

<pre class="wp-block-code"><code>spyder # you will need to change the working directory in the script.</code></pre>

**Final note**: I know that there exists _the curse of knowledge_, which means that I may assume you know what I know but you don&#8217;t. So please free feel to post comment or shout out on twitter (@hcp4715) to let me know if you encountered any problem when reproducing my analyses.