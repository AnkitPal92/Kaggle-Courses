# 05. Intro to Lists

## Intro
In Data Science, the preprocessing of data needs to organize them first to make it ready for the next operation. Organizing data, however, can be done in several ways with lists, tuples, dictionaries and sets. In this chapter, we will learn how to work with lists.

## Motivation

**What does list offer ?**

Let's analyse with an example, comapring two ways of oraganizing some species of flowers based only on its image (image classification): in **Python** **String** and **List**.

First, we organize the names with a string.

    flowers = "pink primrose,hard-leaved pocket orchid,canterbury bells,sweet pea,english marigold,tiger lily,moon orchid,bird of paradise,monkshood,globe thistle"
        
    print(type(flowers))
    print(flowers)

> <class 'str'>

> pink primrose,hard-leaved pocket orchid,canterbury bells,sweet pea,english marigold,tiger lily,moon orchid,bird of paradise,monkshood,globe thistle

Now, let's try organising the names with a list. Note here that, a list is created using [] brackets, every item inside the [] barckets is enclosed in quotation marks and separated by a comma.

    flowers_list = ["pink primrose", "hard-leaved pocket orchid", "canterbury bells", "sweet pea", "english marigold", "tiger lily", "moon orchid", "bird of paradise", "monkshood", "globe thistle"]
    
    print(type(flowers_list))
    print(flowers_list)

> <class 'list'>

> ['pink primrose', 'hard-leaved pocket orchid', 'canterbury bells', 'sweet pea', 'english marigold', 'tiger lily', 'moon orchid', 'bird of paradise', 'monkshood', 'globe thistle']

The difference between the above two ways to orgnaise datas may not so apparent at the first glance. But if we notice difference, it will be clearer that list offers some advantages over string, such as enumerated below.

+ Getting an item at a specified position is easier with the list.
+ Checking the number of items is easier too.
+ It is also easier to add and remove items.

## Some basic operations on the List

### Length

The length of a list refers to the number of entries in it which can be determined by **len()** opertor by putting the name of the list within the parentheses.

    # The list has ten entries
    print(len(flowers_list))

> 10

### Indexing

Indexing means referring to an item in the list according to its position(first, second, third). Python has zero-based indexing, i.e., the first entry can be referred to with 0 and hence the last entry is referred to with a number one less than the total entries(the length of the list).

    print("First entry:", flowers_list[0])
    print("Second entry:", flowers_list[1])
    
    # The list has length ten, so we refer to final entry with 9
    print("Last entry:", flowers_list[9])

> First entry: pink primrose

> Second entry: hard-leaved pocket orchid

> Last entry: globe thistle

The above operation can also be done with single print statement by putting the Python strings and its values separated by comma.

### Slicing

Slicing refers to pulling out a segment of the list (either first few entries or last few entries or entries specified by positions).

Use:
+  [:x], to pull out first x entries.
+  [-y:], to pull out last y entries.
+  [-1], to pull out last item only.
+  [:-2], to pull out everything except the last two entries.

        print("First three entries:", flowers_list[:3])
        print("Final two entries:", flowers_list[-2:])

> First three entries: ['pink primrose', 'hard-leaved pocket orchid', 'canterbury bells']

> Final two entries: ['monkshood', 'globe thistle']

Observe, in the above example, we obtained a new shortened list after slicing the original list(i.e., flowers_list).

### Removing items

An item from a list can be removed using **.remove()** by putting the item to be removed in the parentheses.

    flowers_list.remove("globe thistle")
    print(flowers_list)

> ['pink primrose', 'hard-leaved pocket orchid', 'canterbury bells', 'sweet pea', 'english marigold', 'tiger lily', 'moon orchid', 'bird of paradise', 'monkshood']

