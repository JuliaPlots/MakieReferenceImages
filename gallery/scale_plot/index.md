## scale_plot

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-oB'>=</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-oB'>=</span><span class='hljl-ni'>500</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># time steps</span><span class='hljl-t'>
</span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>6</span><span class='hljl-n'>π</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'>    </span><span class='hljl-cs'># angles</span><span class='hljl-t'>
</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>cos</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># x coords of spiral</span><span class='hljl-t'>
</span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># y coords of spiral</span><span class='hljl-t'>
</span><span class='hljl-n'>p1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'>      </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>colormap</span><span class='hljl-t'>   </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:algae</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>linewidth</span><span class='hljl-t'>  </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>8</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>scale_plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//scale_plot/media/image.png" alt="">

    </p>
</div>

```
