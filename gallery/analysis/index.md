## Analysis

```@raw html
<pre class='hljl'>
<span class='hljl-t'> </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>DataFrames</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-t'> </span><span class='hljl-cs'># for data</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>smooth</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linear</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Distributions</span><span class='hljl-t'>


 </span><span class='hljl-n'>mtcars</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;datasets&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;mtcars&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>    </span><span class='hljl-cs'># load dataset of car statistics</span><span class='hljl-t'>
 </span><span class='hljl-n'>iris</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;datasets&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;iris&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>disallowmissing!</span><span class='hljl-oB'>.</span><span class='hljl-p'>([</span><span class='hljl-n'>mtcars</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>iris</span><span class='hljl-p'>])</span><span class='hljl-t'>  </span><span class='hljl-cs'># convert columns from Union{T, Missing} to T</span><span class='hljl-t'>
 </span><span class='hljl-cs'># We can use this because the dataset has no missing values.</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-cs'># kde</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>density</span><span class='hljl-p'>,</span><span class='hljl-t'>           </span><span class='hljl-cs'># the type of analysis</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>mtcars</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-sc'>:MPG</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:Cyl</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-cs'># histogram</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>histogram</span><span class='hljl-p'>,</span><span class='hljl-t'>         </span><span class='hljl-cs'># the type of analysis</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>mtcars</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-sc'>:MPG</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:Cyl</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-cs'># frequency analysis</span><span class='hljl-t'>

 </span><span class='hljl-n'>d</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-nf'>Poisson</span><span class='hljl-p'>(),</span><span class='hljl-t'> </span><span class='hljl-ni'>1000</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>frequency</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>d</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-n'>xs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>ys</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>rand</span><span class='hljl-oB'>.</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot!</span><span class='hljl-p'>(</span><span class='hljl-n'>smooth</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot!</span><span class='hljl-p'>(</span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image5.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image6.jpg" alt="">

    </p>
</div>

```
