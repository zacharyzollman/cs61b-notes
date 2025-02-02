# Sorting

{% hint style="info" %}
This page is from my original notes, but will likely not upgrade it in the near future because I wrote a [guide on sorting](https://docs.google.com/document/d/1dUfzdh5V3okrwFbB9o0PgtEBaLHyCqJFwpQWyQ53IeU/edit) that covers all of the sorts in far greater detail 🙂
{% endhint %}

## Why sorting?

* Easier for searching (e.g. binary search)
* Easy to see if two items in list are equal (just compare neighbors)
* Get nearest neighbors

## Properties of a Sorting Algorithm

* Changes a sequence based on a **total order**
*   A sorting algorithm could be **stable**: does not change relative order of equivalent entries

    * Example: dictionary can have multiple definitions for a single word

    A total order is:

    * **Total:** All items can be compared with one another
    * **Reflexive:** An item can be compared to itself
    * **Antisymmetric:** x <= y AND y <= x IFF y == x
    * **Transitive:** If x <= y and y <= z, then x must be <= z

## Sorting Algorithm Classifications

* **Internal sort:** Keeps all data in primary memory
* vs. **External sort:** Processes data in batches, then merges them together at the end
* **Comparison-based sort:** The only thing we know about keys are their relative orders
* **Radix sort:** Uses information other than keys
* **Insertion sort:** Insert items at their appropriate positions one at a time
* **Selection sort:** Chooses items and places them in order

## Sorting in Java

```java
String[] x = new String[] {"Vat", "Bat", "Cat"};

Arrays.sort(x); // mutates x into Bat, Cat, Vat
Arrays.sort(x, Collections.reverseOrder()); // mutates x into Vat, Cat, Bat
Arrays.sort(x, 0, 2) // sorts the first two elements, leaving the rest unchanged (Cat, Vat, Bat)
```

## Inversions

* Used as a measure for how sorted a list is
* 0 inversion = perfectly sorted
* N\*(N-1)/2 inversions = reversed

## The Guide to Sorting Algorithms

[A comprehensive guide to sorting algorithms, now with memes!](https://docs.google.com/document/d/1dUfzdh5V3okrwFbB9o0PgtEBaLHyCqJFwpQWyQ53IeU/edit)
