# Arno's Engram key layout

The [Engram layout](https://github.com/binarybottle/engram-layout) is a keyboard layout optimized for comfortable touch typing in English created by [Arno Klein](https://binarybottle.com), with open source code to create other optimized key layouts.

                   K  P  U  Y        G  R  D  W  Q
                   I  O  E  A        H  T  S  N  J
                   V  Z  X  C        L  B  F  M

The Shift key accesses characters (top) that look similar to the numbers:

                   !  =  ?  +  $  @  ^  &  %  *
                   1  2  3  4  5  6  7  8  9  0

and accesses related but less common punctuation (top):

                `    \    ;    :    {    }    |    _
                '    "    ,    .    (    )    /    -

Swapping the Backspace and Caps lock keys completes the layout:


          ~        !  =  ?  +  $  @  ^  &  %  *  <  >
          #        1  2  3  4  5  6  7  8  9  0  [  ]     Caps

        Tab        K  P  U  Y  '  "  G  R  D  W  Q  -     /
        Back       I  O  E  A  ,  .  H  T  S  N  J        Enter
        Shift      V  Z  X  C  (  )  L  B  F  M           Shift

        Ctrl  Fn  Cmd  Alt  Space   Alt  Ctrl       Arrows

## Rationale <a name="rationale">

**Why?** <br>
In the future, I hope to include an engaging rationale for why I took on this challenge.
Suffice to say that I have battled repetitive strain injury since I worked
on an old DEC workstation at the MIT Media Lab while composing my thesis back in the mid-90s.
Ever since then I have used different key layouts (Dvorak, Colemak, my own, etc.),
and have primarily used Colemak for almost 10 years.  I find that they all place too much stress on tendons, with lateral extension of the index and little fingers,
and on uniform distribution of finger use, which has damaged my little fingers.
I have also experimented with a wide variety of human interface technologies
(voice dictation, one-handed keyboard, keyless keyboard, foot mouse, and ergonomic keyboards like the Kinesis Advantage. I recently got an Ergodox that I am looking forward to trying out with the Engram layout.

**"Engram"?** <br>
The name is a pun, referring both to "n-gram", letter permutations used to compute this layout, and "engram", or memory trace, the postulated change in neural tissue to account for the persistence of memory.

## Comparison with other key layouts

Despite the fact that the Engram layout was designed to reduce strain and discomfort, not to reduce finger travel from the home row, it scores higher than all other key layouts (Colemak, Dvorak, QWERTY, etc.) I've tested using the online Keyboard Layout Analyzer, for all of the examples of prose and tweet data I've tried, including the data sets below:

- [See the complete analysis](http://patorjk.com/keyboard-layout-analyzer/#/load/x0WPtw3x)
of __Alice in Wonderland__ provided by the Keyboard Layout Analyzer 

- All __20,000 tweets__ from [Gender Classifier Data](https://www.kaggle.com/crowdflower/twitter-user-gender-classification) <br>
Added: November 15, 2015 by CrowdFlower

- The first __100,000 tweets__ from: [Sentiment140 dataset](https://data.world/data-society/twitter-user-data) training data <br>
Go, A., Bhayani, R. and Huang, L., 2009. <br>
Twitter sentiment classification using distant supervision. <br>
CS224N Project Report, Stanford, 1(2009), p.12.

According to the [Keyboard Layout Analyzer](http://patorjk.com/keyboard-layout-analyzer/):

"The optimal layout score is based on a weighted calculation that factors in the distance your fingers moved (33%), how often you use particular fingers (33%), and how often you switch fingers and hands while typing (34%)."

## Factors used to compute the layout
  - **N-gram letter frequencies** <br>
    
    [Peter Norvig's analysis](http://www.norvig.com/mayzner.html) of data from Google's book scanning project
  - **Flow factors** (transitions between ordered key pairs) <br>
    These factors are influenced by Dvorak's 11 criteria (1936) that can be summarized as follows:
      - Alternate between hands and balance finger loads.
      - Avoid using the same finger.
      - Avoid the upper and lower rows.
      - Avoid skipping over the home row ("hurdling").
      - Avoid tapping adjacent rows ("reaching") with (same or) adjacent fingers.
  - **Finger strengths** (peak keyboard reaction forces) <br>
      "Keyboard Reaction Force and Finger Flexor Electromyograms during Computer Keyboard Work", BJ Martin, TJ Armstrong, JA Foulke, S Natarajan, Human Factors,1996,38(4),654-664.
  - **Speed** (unordered interkey stroke times) <br>
      "Estimation of digraph costs for keyboard layout optimization", A Iseri, Ma Eksioglu, International Journal of Industrial Ergonomics, 48, 127-138, 2015. <br>
      _NOTE: Speed data were only used for exploration of early key layouts._
      
## Guiding criteria

1.  Assign 24 letters to keys that don't require lateral extension of index or little fingers.
2.  Group letters for common command shortcut keys (F,C,Z,Y,X,V) close together.
3.  Assign punctuation to keys that require lateral extension of index or little fingers.
4.  Assign easier-to-remember characters to the shift-number keys.
5.  Arrange letters so that more frequent bigrams are faster and easier to type.
6.  Balance finger loads according to their relative strength.
7.  Promote alternating between hands over typing with the same hand.
8.  Promote little-to-index-finger roll-ins over index-to-little-finger roll_outs.
9.  Avoid extending nearer, shorter fingers to upper rows.
10. Avoid using the same finger.
11. Avoid the upper and lower rows.
12. Avoid skipping over the home row.

## Summary of steps and results

- Step 1: Arrange the most frequent vowels and consonants
- Step 2: Arrange the remaining letters (except for command characters Z,X,C,V)
- Step 3: Add command shortcut characters
- Step 4: Arrange punctuation marks in easy-to-remember places

### Step 1: Arrange the most frequent vowels and consonants

My goal was to arrange 24 of the 26 letters in 8 columns of keys requiring no lateral movements, with 2 middle columns reserved for punctuation.

First, I selected 5 keys on the left and right sides having the strongest finger positions, and assigned to these keys the top-scoring arrangement of the 5 vowels and of the 5 most frequent consonants. In prior experiments, vowels on the left got consistently higher scores, so we will continue with vowels on the left:

#### **E**, T, **A, O, I**, N, S, R, H, L, D, C, **U**, M, F, P, G, W, Y, B, V, K, X, J, Q, Z
#### E, **T**, A, O, I, **N, S, R, H**, L, D, C, U, M, F, P, G, W, Y, B, V, K, X, J, Q, Z
    
                      Left:            Right:

                   -  -  U  -        -  R  -  - 
                   I  O  E  A        H  T  S  N
                   -  -  -  -        -  -  -  -
                   
This arrangement is very reasonable, as it places vowels of decreasing frequency in positions of decreasing strength, and the most common bigrams are easy to type.
     
#### Details
The optimization algorithm finds every permutation of a given set of letters (40,320 for this intial set of 8), maps these letter permutations to a set of keys, and ranks these letter-key mappings according to a score reflecting ease of typing key pairs and frequency of letter pairs (bigrams). The score is the average of the scores for all possible bigrams in this arrangement. The score for each bigram is a product of the frequency of occurrence of that bigram and the factors Flow, Strength, and Speed: 

**Flow**: measure of ease of a finger transition from the first in a pair of letters to the second

Flow factors to _penalize_ difficult key transitions include:
    
- roll out from index to little finger
- index or little finger on top row
- middle or ring finger on bottom row
- index above middle, or little above ring 
- index above ring, or little above middle
- ring above middle
- use same finger twice for a non-repeating letter
- at least one key not on home row
- one key on top row, the other on bottom row

**Strength**: measure of the average strength of the finger(s) used to type the two letters

Finger strengths are based on peak keyboard reaction forces (in newtons) from "Keyboard Reaction Force and Finger Flexor Electromyograms during Computer Keyboard Work", BJ Martin, TJ Armstrong, JA Foulke, S Natarajan, Human Factors,1996, 38(4), 654-664.

**Speed**: normalized interkey stroke times

These are left-right averaged versions derived from the study data below, to compensate for right-handedness of participants in the study (we used this data for early experimentation):

"Estimation of digraph costs for keyboard layout optimization", 
A Iseri, Ma Eksioglu, International Journal of Industrial Ergonomics, 48, 127-138, 2015. 

    
### Step 2: Arrange the remaining letters (except for command characters Z,X,C,V)

I reserve the familiar location of the bottom left row for common command shortcut letters Z, X, C, and V, and place Q and J, the least common letters (after Z) in the hardest-to-reach locations:
    
#### E, T, A, O, I, N, S, R, H, **L, D**, [C], U, **M, F, P, G, W, Y, B**, [V], **K**, [X], [J], [Q], [Z]

                   -  -  U  -        -  R  -  -  [Q]
                   I  O  E  A        H  T  S  N  [J]
                   *  *  *  *        -  -  -  -
    
### Step 3: Add command shortcut characters

Arrange the common command characters (Z,X,C,V) in the bottom left row:

                   K  P  U  Y        G  R  D  W  [Q]
                   I  O  E  A        H  T  S  N  [J]
                   V  Z  X  C        L  B  F  M    
    
I choose the sequence V,Z,X,C so that the more frequent letters V and C are accessible by folding the smaller fingers, repeated shortcuts V and Z (paste and undo) are closer to the Ctrl/Cmd key, and the sequence is close to the familiar Z,X,C,V (with V on the left side).
    
### Step 4. Arrange punctuation marks in easy-to-remember places

**Frequency of punctuation** 

These sources helped guided our arrangement:
    
  - "Punctuation Input on Touchscreen Keyboards: Analyzing Frequency of Use and Costs" <br>
    S Malik, L Findlater - College Park: The Human-Computer Interaction Lab. 2013 <br>
    https://www.cs.umd.edu/sites/default/files/scholarly_papers/Malik.pdf

  - "Frequencies for English Punctuation Marks" by Vivian Cook <br>
    http://www.viviancook.uk/Punctuation/PunctFigs.htm

  - "Computer Languages Character Frequency" <br>
    Xah Lee. Date: 2013-05-23. Last updated: 2020-06-29. <br>
    http://xahlee.info/comp/computer_language_char_distribution.html

Resulting in:

                   K  P  U  Y  '  "  G  R  D  W  Q
                   I  O  E  A  ,  .  H  T  S  N  J
                   V  Z  X  C  (  )  L  B  F  M    

Shift accesses similar-looking characters above the numbers:

                ~  !  =  ?  +  $  @  ^  &  %  *  [  ]
                #  1  2  3  4  5  6  7  8  9  0  <  >

Shift accesses less common, but similar-meaning punctuation:

                `    \    ;    :    {    }    |    _
                '    "    ,    .    (    )    /    -
             
**Rationale for shift-characters**

**#** &nbsp;&nbsp; The pound/hash represents numbers, and sits to the left of the number keys. <br>
**~** &nbsp;&nbsp; The tilde has several meanings, including "approximately equal to" <br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (here "similar-looking" to the numbers), and is in the standard location.

**'** &nbsp;&nbsp; Single quotation marks are used to quote text for 'emphasis', or to quote text within a quote. <br>
**`** &nbsp;&nbsp; One use of the backquote is to quote computer code. It is used in an analogous manner as a single quote <br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; in a quote, to quote code within code for command substitution (to replace a command with output).

**"** &nbsp;&nbsp; "Double quotation marks are used to quote direct speech?" <br>
**\** &nbsp;&nbsp; The backslash is an escape character used to quote special characters in regular expressions.

**,** &nbsp;&nbsp; The comma is used to separate text, for example in lists, or to provide a pause. <br>
**;** &nbsp;&nbsp; The semicolon provides a stronger separation or pause; it can be used in place <br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; of the comma to separate items in a list, especially if those items contain commas. <br>
   
**.** &nbsp;&nbsp; The period ends a sentence. <br>
**:** &nbsp;&nbsp; The colon similarly ends a statement but precedes something following: explanation, quotation, list, etc.

**|** &nbsp;&nbsp; The pipe connects commands in computer code. <br>
**/** &nbsp;&nbsp; The slash connects conjunctions/disjunctions/alternatives, or locations such as file paths or urls.

**-** &nbsp;&nbsp; The dash connects side-by-side words, or can surround a phrase for emphasis. <br>
**_** &nbsp;&nbsp; The underscore connects strings within variable or file names, or can _underline a phrase_ for emphasis.
