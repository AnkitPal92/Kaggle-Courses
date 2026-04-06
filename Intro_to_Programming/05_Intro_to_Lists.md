# 05. Intro to Lists

## Intro
In Data Science, the preprocessing of data needs to organize them first to make it ready for the next operation. Organizing data, however, can be done in several ways with lists, tuples, dictionaries and sets. In this chapter, we will learn how to work with lists.

## Motivation

**What does list offer ?**

Let's analyse with an example, comapring two ways of oraganizing some species of flowers based only on its image (image classification): in a **String** and in a **List**.

First, we organize the names with a string.

    flowers = "pink primrose,hard-leaved pocket orchid,canterbury bells,sweet pea,english marigold,tiger lily,moon orchid,bird of paradise,monkshood,globe thistle"
        
    print(type(flowers))
    print(flowers)

> <class 'str'>

> pink primrose,hard-leaved pocket orchid,canterbury bells,sweet pea,english marigold,tiger lily,moon orchid,bird of paradise,monkshood,globe thistle
