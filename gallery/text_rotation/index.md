## Text rotation

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>500</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>posis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[]</span><span class='hljl-t'>
 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>posis</span><span class='hljl-t'>
     </span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-nfB'>100.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-nf'>push!</span><span class='hljl-p'>(</span><span class='hljl-n'>posis</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>p</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>text!</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;test&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>p</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>rotation</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.5</span><span class='hljl-n'>pi</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:center</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:center</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>posis</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//text_rotation/media/image.jpg" alt="">

    </p>
</div>

```
