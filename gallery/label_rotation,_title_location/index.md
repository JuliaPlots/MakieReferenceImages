## label rotation, title location

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>line</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-oB'>=</span><span class='hljl-nfB'>3.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=:</span><span class='hljl-n'>red</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>][</span><span class='hljl-sc'>:names</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:axisnames</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;text&quot;</span><span class='hljl-p'>,</span><span class='hljl-s'>&quot;&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>][</span><span class='hljl-sc'>:names</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:rotation</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>1.5</span><span class='hljl-n'>pi</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>leg</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>legend</span><span class='hljl-p'>([</span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>]],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-s'>&quot;line&quot;</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-n'>line</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>leg</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//label_rotation,_title_location/media/image.jpg" alt="">

    </p>
</div>

```
