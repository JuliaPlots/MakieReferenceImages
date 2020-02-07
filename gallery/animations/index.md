## animations

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>mytime</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>g</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-n'>f</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>mytime</span><span class='hljl-p'>),</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-n'>g</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>mytime</span><span class='hljl-p'>),</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:orange</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
    </span><span class='hljl-n'>mytime</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//animations/media/animations.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
