## heatmap interpolation

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>hbox</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>vbox</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>data</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>p1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-n'>data</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>interpolate</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>p2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-n'>data</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>interpolate</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>s</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-nf'>title</span><span class='hljl-p'>(</span><span class='hljl-n'>p1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;interpolate = true&quot;</span><span class='hljl-p'>;</span><span class='hljl-t'>  </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>15</span><span class='hljl-p'>),</span><span class='hljl-t'>
    </span><span class='hljl-nf'>title</span><span class='hljl-p'>(</span><span class='hljl-n'>p2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;interpolate = false&quot;</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>15</span><span class='hljl-p'>),</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//heatmap_interpolation/media/image.png" alt="">

    </p>
</div>

```
