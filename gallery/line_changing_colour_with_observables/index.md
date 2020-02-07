## Line changing colour with Observables

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

 </span><span class='hljl-s'>&quot;&#39;Time&#39; - an Observable that controls the animation&quot;</span><span class='hljl-t'>
 </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-s'>&quot;The colour of the line&quot;</span><span class='hljl-t'>
 </span><span class='hljl-n'>c</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'>
         </span><span class='hljl-nf'>RGBf0</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-oB'>/</span><span class='hljl-ni'>255</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>255</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-ni'>255</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-k'>end</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>);</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-oB'>=</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>c</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>255</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>framerate</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>60</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
     </span><span class='hljl-n'>t</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-cs'># update `t`&#39;s value</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//line_changing_colour_with_observables/media/line_changing_colour_with_observables.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
