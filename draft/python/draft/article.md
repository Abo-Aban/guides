Pygal is amazing for creating customizable SVG's that can easily scale.  



<br>
<br>

You can easiely and minimally create line charts, bar graphs, even Radar Chars with very little code. 
<br>

---
#### <b>Let's Begin with an Install</b>

Open Terminal
```
$  pip install Pygal
```
<b>Extra Help:</b>  Installing and Dependencies  - http://www.pygal.org/en/stable/installing.html

---

#### <b>Step 1:  Import</b>

```
import pygal
```

#### <b>Step 2: Create a Variable to Store Your Graph</b>
For our first example we'll create a bar chart.  We simply need to create a varible and store ```pygal.Bar()``` inside.

```
b_chart = pygal.Bar()
```
You can easily use ```pygal.Line```, ```pygal.pie``` etc.


#### <b>Step 3: Let's Add Some Values</b>
Next we need to start creating our chart.  I will be using Data that I scraped from a gaming tracker for the game <b>Destiny 2.</b>  Eventually the graph will be live and I can see my stats change, hopefully in real time.  <i>Let's not get ahead of our selves.</i>

We need to give our chart a title.
```
b_chart.title = "Destiny Kill/Death Ratio"
```
Now we can start adding some data. I need 3 bars for each player.
```
b_chart.add("Dijiphos", [0.94])
b_chart.add("Punisherdonk", [1.05])
b_chart.add("Musclemuffins20", [1.10])
```

Technically we can be finished without further customization.  We can now render this quickly to a browser using ```render_in_browser()```:
```
b_chart.render_in_browser()
```
---
<details>
<summary><b>```Click``` To Reveal Our Example</b></summary>
<br>
![description](https://raw.githubusercontent.com/pluralsight/guides/master/images/ec4a6f0d-9cde-4785-8a76-2b819df70775.gif)
</details>

---

<br>



#### <b>Let's Customize</b>
Lets say we want some custom colors added to our graph<br>
![#E80080](https://placehold.it/15/e80080/000000?text=+) `#E80080`
![#404040](https://placehold.it/15/404040/000000?text=+) `#404040`
![#9bc850](https://placehold.it/15/9bc850/000000?text=+) `#9BC850`

This is easy to do, actually, it can be done multiple ways.
First, import ```style```.
```
from pygal.style import Style
```
Then you can change a number of objects by adding:
```
custom_style = Style(
```
_Notice I left the perenteses open_

---
<details>
<summary><b>```Click``` To Reveal Some Objects</b></summary>
<br>
Properties & Description

```plot_background ```The color of the chart area background<br>
``` background```The color of the image background<br>
```foreground ```|The main foregrond color<br>
``` colors```The serie color list<br>
``` value_colors```The print_values color list<br>
Complete List: http://www.pygal.org/en/stable/documentation/custom_styles.html
</details>

----

Let's change the color of our bars. _Don't forget to indent and close our final perecteses._
```
    colors=('#E80080', '#404040', '#9BC850'))
```
Now all we need to do is pass ```style=custom_style``` in our ```pygal.Bar()```
```
b_chart = pygal.Bar(style=custom_style)
```

---
<details>
<summary><b>```Click``` To Reveal Our Example</b></summary>
<br>


![description](https://raw.githubusercontent.com/pluralsight/guides/master/images/f522dcab-e4f3-4a1e-9e94-0e318634c7ee.gif)
</details>

----










