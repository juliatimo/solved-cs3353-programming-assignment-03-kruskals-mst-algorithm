Download Link: https://assignmentchef.com/product/solved-cs3353-programming-assignment-03-kruskals-mst-algorithm
<br>
5/5 - (1 vote)

<span style="font-size: 2em;">Overview</span>




In this project, you’ll implement Kruskal’s algorithm for finding the minimum spanning tree of a graph.

<h2>Disjoint Set Data Structure<a href="#_ftn1" name="_ftnref1"><sup><strong>[1]</strong></sup></a></h2>

Implementation of Kruskal’s algorithm requires management of a <em>collection</em> <em>of disjoint sets</em>.   A disjoint-set data structure contains a set of unique elements (like a set), but where these elements are partitioned into disjoint (non-overlapping) subsets.

For example, consider the following set of elements:

{1, 2, 5, 6, 9, 10, 12, 14, 18}

The following would represent a disjoint-set:

{[1, 2, 9], [5, 10, 12], [6], [14, 18]}

However, this organization of data would not because 6 and 10 appear in two different subsets: {[1, 2, 5],[6], [9, 6, 10], [10, 12, 14, 18]}

The major operations on a disjoint-set data structure are:

<ul>

 <li><strong>makeSet</strong>(someVal) – creates a new set in the collection with someVal</li>

 <li><strong>find</strong>(x) – returns some identifier of the set of the collection that contains the element x.</li>

 <li><strong>union</strong>(a, b) – creates a new set in the collection that is the union of the sets containing elements a &amp; b.</li>

</ul>

<em>Example Operations and Effects on the Container</em>

<strong><u> Operation:                                         Contents of disjoint set collection: </u></strong>

–                                                           {}

makeSet(10)                                       {[10]}

makeSet(15)    {[10], [15]} makeSet(20)            {[10], [15], [20]} makeSet(25) {[10], [15], [20], [25]} find(15)<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a><sup>              </sup>{[10], [15], [20], [25]} union(15, 25)         {[10], [15, 25], [20]} union(15, 20)     {[10], [15, 25, 20]} The trivial implementation of a disjoint set data structures is a set of linked lists.  As part of this project, you’ll implement this trivial version as well as a more sophisticated version based upon independent research.

<h2>Your Tasks</h2>

<ol>

 <li>Implement a templated disjoint set data structure. You should have two versions that share the same interface which is inherited from a super class: a)         Trivial implementation using a set of linked lists</li>

 <li>b) More sophisticated implementation based upon independent research you will do</li>

 <li>Implement Kruskal’s algorithm on a graph read in from a file. The output should consist of the set of edges that are part of the MST and the sum of the weights of the edges of the MST.  Your implementation should follow the general pseudocode as it appears in the MST PDF from lecture.</li>

 <li>Generate (or locate) sample graphs of increasing size (number of nodes) and density (number of edges compared to the number of nodes). Analyze how Kruskal’s algorithm performs when the underlying disjoint set uses linked lists or your more sophisticated implementation.</li>

</ol>

<strong>What You Will Submit</strong>

<ul>

 <li>Full source code implementation of your project following best practices in design and implementation.</li>

</ul>

◦ The result of building and executing the project you submit must <strong>completely reproduce</strong><a href="#_ftn3" name="_ftnref3"><strong><sup>[3]</sup></strong></a> from top to bottom the data used in analysis for point 3 below.

◦ The run process should not require any command line arguments to execute.

◦ All output should be to one or multiple files that are easily recognized by the user (Morgan and me).

<ul>

 <li>A set of at least 10 test graphs that are used in your performance analysis<a href="#_ftn4" name="_ftnref4"><sup>[4]</sup></a></li>

 <li>A short analysis paper not to exceed 2 typed, single-spaced, 10 pt font (times or arial) pages with maximum 1” margins. No more than 25% of the paper can be consumed by graphs.</li>

</ul>

<h2>Implementation Notes</h2>

<ul>

 <li>We are not dictating the input file format. You may devise your own or use a standard such as GML (Graph Modeling Language) for example.</li>

 <li>We are not dictating the output file format. You may write the output to files in your own format with the only restriction of being able to match one input graph with the output of processing that graph.</li>

</ul>

◦ This doesn’t mean it can be completely disorganized and require some amount of mindreading.  I should be able to look at the set of input files and easily determine which output file (or section in the output file) goes with a particular input file.

<ul>

 <li>You should make use of compiler optimization flags where useful.</li>

</ul>

<h2>Point Allocation for Grading</h2>

<h3>Total Points: 100</h3>

<table width="392">

 <tbody>

  <tr>

   <td width="331">Disjoint Set – Trivial Implementation</td>

   <td width="61">5 points</td>

  </tr>

  <tr>

   <td width="331">Disjoint Set – Robust Implementation</td>

   <td width="61">10 points</td>

  </tr>

  <tr>

   <td width="331">Proper Kruskal’s Implementation</td>

   <td width="61">20 points</td>

  </tr>

  <tr>

   <td width="331">Code Quality</td>

   <td width="61">10 points</td>

  </tr>

  <tr>

   <td width="331">Clarity of Building and Execution</td>

   <td width="61">15 points</td>

  </tr>

  <tr>

   <td width="331">Analysis Paper</td>

   <td width="61">40 points</td>

  </tr>

 </tbody>

</table>




<a href="#_ftnref1" name="_ftn1">[1]</a> Also called the Union-Find data structure

<a href="#_ftnref2" name="_ftn2">[2]</a> Returns some unique identifier such that if compared to the result of separate find(15) call would result in a finding of equivalence.

<a href="#_ftnref3" name="_ftn3">[3]</a> For more info on reproducible research, see <a href="https://www.displayr.com/what-is-reproducible-research/">https://www.displayr.com/what-is-reproducible-research/</a> or <a href="https://lib.colostate.edu/services/data-management/reproducible-analysis/">https://lib.colostate.edu/services/data-management/reproducible-analysis/</a><a href="https://lib.colostate.edu/services/data-management/reproducible-analysis/">.</a>