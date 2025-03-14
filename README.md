
```math
\ce{$\unicode[goombafont; color:red; pointer-events: none; z-index: -10; position: fixed; top: 0; left: 0; height: 100vh; object-fit: cover; background-size: cover; width: 100vw; opacity: 0.5; background: url('https://github.com/aboveyunhai/aboveyunhai/assets/35160613/f5454270-9f18-45a7-8de6-2ad73d79ab21');]{x0000}$}
```
<sub>(Github readme might be a good spot to throw some silly thoughts I guess)</sub>
## My random programming wrong takes:

### 1-based indexing is superior to 0-based indexing in programming languages for general purposes.

  When we start learning programming, most of us are told that indexing starts from 0 instead of 1. While there are many reasons to justify this decision, if we truly consider the semantics of "index" as "position," I firmly believe that 0 is more of a convention, whereas 1 is the "natural" way humans would use "indexing."

   Some argumnets for 0-based index:
   
   1). `When humans are born, we start from 0 years old, we have 0 o'clock. So 0 is more natural.`.
   
   The first part of argument is logically incorrect, 0 holds no meaningful role here. It's not a natural way how humans express information.

   People typically say "a few months old" or "a few days old" rather than referring to an exact "0 years old." 

   It’s like if I gave you -3/0 candies. It's simply not natural as they claim.
   
   For 0 o'clock, 0 o'clock can be 12 o'clock as we need a way to differentiate two in 12 and 24. Physically the last digit of most of circular clocks we have today is 12 instead of 0. Digitally the `0` in `00:00` refers to a leading digit just like I have $0012 (12 dollars). It's not equivalent to the concept of "indexing"

   This argument attempts to force 0-based indexing into real life stuff as long as it contains 0 to justify it, but they are unrelated.

   2). `Coordinate System`.

   You might find 0-based indexing perfectly fits into Coordinate System, where the general starting point is `[0, 0]`.
   However it's more of a coincidence than a fundamental reason why arrays should be 0-based.

   We even use an `Array of Arrays` to represent matrices or coordinate systems.
   
   An `index` refers to the position of an item in the array, hence the **`"1" st`** (we wouldn't call it 0th) position in both x and y happens to be `[0,0]`, but just because the values align in a certain way, make calculation simplier, doesn’t mean that indexing must start from 0.

   3). `Math / programming languages starts from 0.`
   
   Besides the fact that this statement is factually incorrect (some formulas start from 0, others from 1, or even different numbers), it has nothing to do with whether indexing should be 0-based or 1-based.

   Some old programming languages used 1-based indexing. People often just push whatever they first learned as the "correct" way and find random examples to fit their narrative.
    
---

   Out of all the general arguments, `Memory Offset` is by far the only valid argument I accept, as it probably involves years of optimization in modern computing.

   I do believe that many **`index out of bounds`** and **`accessing [empty | null] element`** bug are **the secondery effect of the 0-based indexing**. 
   
   Many indexing-related bugs I’ve encountered involve off-by-one errors (-1 or +1 miscalculations).

   I somehow have a thought that if 1-based indexing became the "standard", it could reduce these issues since indexing as position would no longer require an offset for general cases (like array manipulation). You would only apply an index offset when solving a real problem, rather than compensating for the assumption that everything must start from 0.

   You could call it a skill issue, but if a problem is widespread and common, should we re-consider it a design flaw?

   Of course, this depends on how we approach programming language design. Should it align more with machine efficiency or with how humans naturally conceptualize problems?
   
   Maybe 1-based indexing would cause bigger issues in matrix calculations and other fields, leading to a net loss compared to 0-based indexing? who knows? :P
