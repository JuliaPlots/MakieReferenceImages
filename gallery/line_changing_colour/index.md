## Line changing colour

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>);</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-oB'>=</span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>255</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>framerate</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>60</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
        </span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>plots</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>][</span><span class='hljl-sc'>:color</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>RGBf0</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-oB'>/</span><span class='hljl-ni'>255</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>255</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-ni'>255</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># animate scene</span><span class='hljl-t'>
        </span><span class='hljl-cs'># `scene.plots` gives the plots of the Scene.</span><span class='hljl-t'>
        </span><span class='hljl-cs'># `scene.plots[1]` is always the Axis if it exists,</span><span class='hljl-t'>
        </span><span class='hljl-cs'># and `scene.plots[2]` onward are the user-defined plots.</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//line_changing_colour/media/line_changing_colour.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
