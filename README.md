# Innovacer_Deduplication

## Scenario

Variation in names leads to difficulty in identifying a unique person and hence deduplication
of records is an unsolved challenge. The problem becomes more complicated in cases where
data is coming from multiple sources. Following variations are same as Vladimir Frometa:

Vladimir Antonio Frometa Garo
Vladimir A Frometa Garo
Vladimir Frometa
Vladimir Frometa G
Vladimir A Frometa
Vladimir A Frometa G

## Problem Statement

Train a model to identify unique patterns in the sample dataset. 

## Solution

The problem was solved using the fuzzwuzzy library in python to find the relation 
between words in names. A very simple and human approach was used to firstly filter out
the entries with same Date of birth, Sex, First Name. Having same value in all the
three columns is compulsory for the entries to even have a chance of being duplicates.

After filtering out the data we have to asuume the fact that for a given name the
longest string present in the entry must be having all the information there is 
eg:- for the name Andrew Tik Wells in the database if we have some other similar name
 like Andrew T wells or A T wells must be the same name and are just another way in 
which the name can be written or recorded. identifyting the relations just simply by 
matching the words is very similar to the way a normal person would do. that is why 
we get very good results using this method.