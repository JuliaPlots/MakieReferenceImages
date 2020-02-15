## MakieLayout with GeoMakie

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeoMakie</span><span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>


</span><span class='hljl-n'>lons</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>179.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>179.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>360</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>lats</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>89.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>89.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>180</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>field</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>exp</span><span class='hljl-p'>(</span><span class='hljl-nf'>cosd</span><span class='hljl-p'>(</span><span class='hljl-n'>l</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>(</span><span class='hljl-n'>y</span><span class='hljl-oB'>/</span><span class='hljl-ni'>90</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>l</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>lons</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>lats</span><span class='hljl-p'>]</span><span class='hljl-t'>

</span><span class='hljl-n'>source</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LonLat</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>dest</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>WinkelTripel</span><span class='hljl-p'>()</span><span class='hljl-t'>

</span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>xygrid</span><span class='hljl-p'>(</span><span class='hljl-n'>lons</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>lats</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>Proj4</span><span class='hljl-oB'>.</span><span class='hljl-nf'>transform!</span><span class='hljl-p'>(</span><span class='hljl-n'>source</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>dest</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>vec</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>vec</span><span class='hljl-p'>(</span><span class='hljl-n'>ys</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>xmin</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xmax</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>extrema</span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>ymin</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ymax</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>extrema</span><span class='hljl-p'>(</span><span class='hljl-n'>ys</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>aspect_ratio</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>ymax</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>ymin</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>/</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>xmax</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>xmin</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>layoutscene</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1300</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>900</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>lsc</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LScene</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>scenekw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>scale_plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>splot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>surface!</span><span class='hljl-p'>(</span><span class='hljl-n'>lsc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>field</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>shading</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-nf'>geoaxis!</span><span class='hljl-p'>(</span><span class='hljl-n'>lsc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>180</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>180</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>90</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>90</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>crs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>src</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>source</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>dest</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>dest</span><span class='hljl-p'>,))</span><span class='hljl-t'>

</span><span class='hljl-nf'>coastlines!</span><span class='hljl-p'>(</span><span class='hljl-n'>lsc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>crs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>src</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>source</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>dest</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>dest</span><span class='hljl-p'>,))</span><span class='hljl-t'>

</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LColorbar</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>splot</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>label</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Arbitrary data&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>width</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-nf'>colsize!</span><span class='hljl-p'>(</span><span class='hljl-n'>layout</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Relative</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-nf'>rowsize!</span><span class='hljl-p'>(</span><span class='hljl-n'>layout</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Aspect</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>aspect_ratio</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LText</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;MakieLayout is cool!&quot;</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>40</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-k'>return</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//makielayout_with_geomakie/media/image.jpg" alt="">

    </p>
</div>

```