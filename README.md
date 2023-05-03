Download Link: https://assignmentchef.com/product/solved-cs2030s-lab-7-java-streams
<br>
<table width="683">

 <tbody>

  <tr>

   <td width="683">There are several tasks in this assignment.For each task, you are to define the appropriate method(s) within the Main class in Main.java. You may also submit other utility classes if necessary.<strong>Task 1 — Count Twin Primes</strong>A prime number is a natural number greater than 1 that is only divisible by 1 and itself. A twin prime is one of a pair of prime numbers with a difference of 2. For example, 41 and 43 are twin primes.Define the method countTwinPrimes in class Main which takes in an integer n and counts the number of distinct twin primes from 0 until n inclusive.

    <table width="609">

     <tbody>

      <tr>

       <td width="609">static long countTwinPrimes(int n)</td>

      </tr>

     </tbody>

    </table>Save your Main class in the file Main.java.

    <table width="609">

     <tbody>

      <tr>

       <td width="609">jshell&gt; Main.countTwinPrimes(100)$.. ==&gt; 15 jshell&gt; Main.countTwinPrimes(2)$.. ==&gt; 0 jshell&gt; Main.countTwinPrimes(3)$.. ==&gt; 1</td>

      </tr>

     </tbody>

    </table><strong>Task 2 — Reverse String</strong>Define the method reverse in class Main that takes in a String str and returns the reverse of str.

    <table width="609">

     <tbody>

      <tr>

       <td width="609">static String reverse(String str)</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

Save your Main class in the file Main.java.

jshell&gt; Main.reverse(“orange”)

$.. ==&gt; “egnaro”




jshell&gt; Main.reverse(“one two three”)

$.. ==&gt; “eerht owt eno”




jshell&gt; Main.reverse(“”)

$.. ==&gt; “”




jshell&gt; Main.reverse(“the quick brown fox jumps over the lazy dog.”)

$.. ==&gt; “.god yzal eht revo spmuj xof nworb kciuq eht”

<strong>Task 3 — Counting Repeats</strong>

Define the method countRepeats in class Main that takes in an integer array of digits 0 to 9 and returns the number of occurrences of adjacent repeated digits.  You may assume that there are at least three elements in the array.

static long countRepeats(int… array)

For example,

the array {0, 1, <u>2, 2</u>, 1, <u>2, 2</u>, 1, <u>3, 3</u>, 1} has three occurrences of repeated digits the array {0, <u>1, 1</u>,<u> 1</u>,<u> 1</u>, 2} has one occurrence

Save your Main class in the file Main.java.

jshell&gt; Main.countRepeats(0,1,2,2,1,2,2,1,3,3,1) $.. ==&gt; 3

<strong>Task 4 — Normalized Mean</strong>

Given a list T of n integers t<sub>i</sub>, the normalized value of each t<sub>i</sub> is defined as where min<sub>T</sub> and max<sub>T</sub> represent the minimum and maximum values among all n values in T.

For example, the list of values {1,2,3,4,5} upon normalizing will become {0,0.25,0.5,0.75,1} since min<sub>T</sub> = 1 and max<sub>T</sub>=5.With the set of normalized values generated, the normalized mean can be easily computed to be 0.5.

Notice from the above that finding the normalized mean requires values in the list to be accessed twice: once for finding the maximum/minimum, and a second time to compute each normalized value and finding the mean.

Alternatively, we can re-expressed the normalized mean as

This way we need to only access each element in the list exactly once.

Define the method normalizedMean in class Main that takes in a Stream of Integer elements and returns the normalized mean

static double normalizedMean(Stream&lt;Integer&gt; stream)

Save your Main class in the file Main.java.

jshell&gt; Main.normalizedMean(Stream.&lt;Integer&gt;of(1, 2, 3, 4, 5))

$.. ==&gt; 0.5




jshell&gt; Main.normalizedMean(Stream.&lt;Integer&gt;of(1, 1))

$.. ==&gt; 0.0




jshell&gt; Main.normalizedMean(Stream.&lt;Integer&gt;of(1))

$.. ==&gt; 0.0







<table width="683">

 <tbody>

  <tr>

   <td width="37"></td>

   <td width="609">jshell&gt; Main.normalizedMean(Stream.&lt;Integer&gt;of()) $.. ==&gt; 0.0</td>

   <td width="37"><a href="https://www.nus.edu.sg/campusmap/">p</a></td>

  </tr>

 </tbody>

</table>