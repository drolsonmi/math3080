---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
marp: true
style: @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');

math: mathjax

---

# __Ethics of Graphing__
#### Principles of Graphing
Dr. Michael E. Olson<br>
MATH 3080 - Foundations of Data Science

---

# Methods of Graphing
* Variety of Graphs
  * Lineplot, Scatterplot, Bar graph, Boxplots, Histograms and KDE plots<br><br>
* Tools
  * Matplotlib, Seaborn, Plotly

---

# Mistake or Misleading?

Some graphs give readers incorrect impressions.

Sometimes, people honestly make mistakes

Sometimes, people purposefully use bad statistics to mislead readers

---

# Example of Misleading Statistics
In the 2020 election season, a news article said:
> Older, white voters are significantly more likely to vote by mail and have those ballots counted, studies show, while voters of color and younger voters are significantly more likely to have their ballots rejected.
[NBC News, Aug 9, 2020](https://www.nbcnews.com/politics/2020-election/white-person-black-person-vote-mail-same-state-whose-ballot-n1234126)

Could this be deceptive?

---

# Example of Misleadding Statistics
It likely isn't purposefully deceptive - just a wording issue. But here is a scenario where their statement is true, but completely misleading.

|         | White | Non-White |
| :------ | :---: | :-------: |
| Older   |  45%  |    25%    |
| Younger |  20%  |    10%    |

Younger AND non-white groups would be 20%+25%+10%=55%, <br>a majority, though the biggest problem is older white voters.

---

# Mistake or Misleading?
In the following slides, we will look at a few principles that could convey information incorrectly and how to avoid them.

Note that these figures come from our textbook: 
* [Irizarry, *Introduction to Data Science*, Chapter 9](https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles.html)

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/piechart-1.png" width=100% alt="Lack of Visual Cues">

</div>
<div>



</div>
</div>

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/piechart-1.png" width=100% alt="Lack of Visual Cues">

</div>
<div>

* Which had the largest?
* Did the size of Firefox users increase or decrease?

</div>
</div>

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/piechart-1.png" width=100% alt="Lack of Visual Cues">

</div>
<div>

Issues:
* No clear way to compare the size of each area between the two figures
* Sections are determined by both angle and area (two different dimensions)

</div>
</div>

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/donutchart-1.png" width=100% alt="Results with only area">

</div>
<div>

Solutions:
* Add labels to the graph
* Only use angle or area

Here is an example using a donut graph with the same data, but only using area.

No labels -- still not clear

</div>
</div>

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

| Browser | 2000  | 2015  |
| :------ | :---: | :---: |
| Opera   | 3     | 2     |
| Safari  | 21	  | 22    |
| Firefox | 23	  | 21    |
| Chrome  | 26	  | 29    |
| IE      | 28	  | 27    |

</div>
<div>

Sometimes, just giving the data in a table is clearer

</div>
</div>

---

# Visual Cues
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/two-barplots-1.png" width=100% alt="Pie chart compared to a bar graph">

</div>
<div>

... or use a bar graph.

</div>
</div>

---

# When to include 0
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/img/class2_8.jpg" width=100% alt="Bar graph without a 0 base">

</div>
<div>

</div>
</div>

---

# When to include 0
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/img/class2_8.jpg" width=100% alt="Bar graph without a 0 base">

</div>
<div>

Issues:
* Lines are not proportioned correctly

</div>
</div>

It looks like 2013 has tripled 2011, but really only increased by 16%

---

# When to include 0
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/barplot-from-zero-1-1.png" width=100% alt="Bar graph with a 0 base">

</div>
<div>

Solution:
* When the distance from 0 matters, make sure 0 is displayed in the graph
</div>
</div>

---

# When to include 0
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/img/venezuela-election.png" width=100% alt="Election results without a 0 base">

</div>
<div>


</div>
</div>

---

# When to include 0
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/img/venezuela-election.png" width=100% alt="Election results without a 0 base">

</div>
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/barplot-from-zero-3-1.png" width=100% alt="Election results with a 0 base">

</div>
</div>

---

# When including 0 isn't needed
<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/points-plot-not-from-zero-1.png" width=70% alt="Life Expectancy by continent - Clustered data">

In cases where we look at a distribution of values, the 0 is not really necessary

---

# Distorting Quantities
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/img/state-of-the-union.png" width=100% alt="World economy shown by radius, but area stands out">

</div>
<div>

</div>
</div>

---

# Distorting Quantities
<div class="grid grid-cols-2 gap-4">
<div>

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/area-not-radius-1.png" width=100% alt="World economy shown by radius and again by area">

</div>
<div>

Issues:
* The most obvious measure is the area (US 5x as large as China)
* Actually used radius/diameter (US 3x as large as China)

</div>
</div>

---

# Distorting Quantities
<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/barplot-better-than-area-1.png" width=55% alt="World economy shown as a bar graph">

A bar graph is easier

---

# Meaningful Order

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/do-not-order-alphabetically-1.png" width=55% alt="Murder rates by state alphabetically and again by rate order">

---

# Meaningful Order

<img src="https://rafalab.dfci.harvard.edu/dsbook-part-1/dataviz/dataviz-principles_files/figure-html/reorder-boxplot-example-1.png" width=65% alt="Income distributions by region alphabetically and again by income median">