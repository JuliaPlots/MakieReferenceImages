## Geographical axes

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeoMakie</span><span class='hljl-t'>


 </span><span class='hljl-n'>projections</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Projection</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;+proj=longlat&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Standard lon-lat&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Projection</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;+proj=robin&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>   </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Robinson&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Projection</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;+proj=moll&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>    </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Molleweide&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Projection</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;+proj=vandg&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>   </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;van der Grinten I&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Projection</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;+proj=wintri&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>  </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Winkel Tripel&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
 </span><span class='hljl-p'>]</span><span class='hljl-t'>

 </span><span class='hljl-n'>geoaxis_scenes</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Scene</span><span class='hljl-p'>[]</span><span class='hljl-t'>

 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>projection</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>titlestr</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>projections</span><span class='hljl-t'>
     </span><span class='hljl-nf'>push!</span><span class='hljl-p'>(</span><span class='hljl-n'>geoaxis_scenes</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>title</span><span class='hljl-p'>(</span><span class='hljl-nf'>geoaxis</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>180</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>180</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>90</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>90</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>crs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>dest</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>projection</span><span class='hljl-p'>,),</span><span class='hljl-t'> </span><span class='hljl-n'>scale_plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>titlestr</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>

 </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-n'>geoaxis_scenes</span><span class='hljl-oB'>...</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>parent</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1440</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>200</span><span class='hljl-p'>)))</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/geographical_axes/media/image.jpg" alt="">

    </p>
</div>

```
