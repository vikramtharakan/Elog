# Elog
Create an NLP pipeline that categorizes Elog entries.

## Overview
The goal is to first extract the data in a json file from the Elog and import it into a workable format. Then we want to apply some sort of natural language processing algorithm on it to classify it into one of the three entry categories. <br>
Twist: The actual model created won't be able to work immediately as the data it is getting trained on is incorrectly tagged and the tags will also likely change. However the idea (initially) is to creat a backbone for a structure that can create a working model. We (as operators) will likely have to tag entries correctly for about a a long time (let's say a few months) before there will be enough data to comprehensively train this model

## Files
* <b>elog.ipynb</b>: Jupyter notebook contains all the steps taken from extracting data to creating the model
