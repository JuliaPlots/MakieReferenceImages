## Available markers

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>collect</span><span class='hljl-p'>(</span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-n'>_marker_map</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>positions</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Point2f0</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-n'>positions</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>last</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-p'>),</span><span class='hljl-t'>
    </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.8</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>marker_offset</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec2f0</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.4</span><span class='hljl-p'>),</span><span class='hljl-t'>
    </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>annotations!</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>string</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;:&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>first</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-p'>)),</span><span class='hljl-t'>
    </span><span class='hljl-n'>positions</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:right</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:center</span><span class='hljl-p'>),</span><span class='hljl-t'>
    </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.4</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>update_cam!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>FRect</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>2.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//available_markers/media/image.jpg" alt="">

    </p>
</div>

```
