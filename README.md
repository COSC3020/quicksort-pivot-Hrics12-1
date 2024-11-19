# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

We know from the slides that there is a 1/2 chance for a good pivot with picking the first (left most) element. We expect to pick a good pivot every two tries(Lecture 01_34). Whenn using the median of three, we're selecting the first element, last element, and the center. Then picking from those 3 elements the value between the min and max (median). This is our pivot to start. We need to know the probability of each possible permutations for the median of three to know the chances of getting a good pivot.

// It was suggested to me by Sean Wilson to write down each possible outcome to visualize the good pivots.

L=Low G=Good, H=High

(LLL),(LLG),(LLH),(LGL),(LHL),(LGG),(LHH),(LHG),(LGH)   
(GGG),(GGL),(GGH),(GLG),(GHG),(GLL),(GHH),(GLH),(GHL)
(HHH),(HHL),(HHG),(HLH),(HGH),(HLL),(HGG),(HGL),(HLG)

So for good pivots you have, <br>

(LGG) = $(1/4)(1/2)(1/2) = (1/16)$<br>
(LGH) = $(1/4)(1/2)(1/4) = (1/32)$<br>
(LHG) = $(1/4)(1/2)(1/4) = (1/32)$<br>
(GGG) = $(1/2)(1/2)(1/2) = (1/8)$<br>
(GGL) = $(1/2)(1/2)(1/4) = (1/16)$<br>
(GGH) = $(1/2)(1/2)(1/4) = (1/16)$<br>
(GLG) = $(1/2)(1/4)(1/2) = (1/16)$<br>
(GHG) = $(1/2)(1/4)(1/2) = (1/16)$<br>
(GLH) = $(1/2)(1/4)(1/4) = (1/32)$<br>
(GHL) = $(1/2)(1/4)(1/4) = (1/32)$<br>
(HGG) = $(1/4)(1/2)(1/2) = (1/16)$<br>
(HGL) = $(1/4)(1/2)(1/4) = (1/16)$<br>
(HLG) = $(1/4)(1/4)(1/2) = (1/16)$<br>

Summing the totals: $22/32$ = $68.75 PERCENT $
Median of three has a better probability to pick a good pivot then the 1/2 percent from picking the first element. 



I used this video to better understand the median of three https://youtu.be/A3vUFmpbFuI?si=eDOpMK3DtxKunfOu

I used the class slides, Lecture 1 slide 34

I took Sean's advice and wrote down each possible permutation to and went through recording each "good" pivot.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."

