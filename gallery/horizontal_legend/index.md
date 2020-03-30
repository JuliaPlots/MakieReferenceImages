## Horizontal legend

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>px</span><span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>px</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>


</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>layoutscene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1400</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>900</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>ax</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>xs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-nfB'>0.5</span><span class='hljl-oB'>:</span><span class='hljl-ni'>10</span><span class='hljl-t'>
</span><span class='hljl-n'>ys</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>lin</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>ax</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>sca</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>ax</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>15</span><span class='hljl-n'>px</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>leg</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LLegend</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-n'>lin</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sca</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>lin</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-s'>&quot;a line&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;some dots&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;line again&quot;</span><span class='hljl-p'>])</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>leg</span><span class='hljl-t'>

</span><span class='hljl-n'>leg_horizontal</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LLegend</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-n'>lin</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sca</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>lin</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-s'>&quot;a line&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;some dots&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;line again&quot;</span><span class='hljl-p'>],</span><span class='hljl-t'>
</span><span class='hljl-n'>orientation</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:horizontal</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>width</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Auto</span><span class='hljl-p'>(</span><span class='hljl-kc'>false</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>height</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Auto</span><span class='hljl-p'>(</span><span class='hljl-kc'>true</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>leg_horizontal</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//horizontal_legend/media/image.jpg" alt="">

    </p>
</div>

```