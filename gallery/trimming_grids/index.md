## Trimming grids

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>layoutscene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>600</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>600</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>framerate</span><span class='hljl-oB'>=</span><span class='hljl-ni'>1</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>io</span><span class='hljl-t'>

    </span><span class='hljl-n'>ax1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Axis 1&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>

    </span><span class='hljl-n'>ax2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Axis 2&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>

    </span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>ax2</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>

    </span><span class='hljl-nf'>trim!</span><span class='hljl-p'>(</span><span class='hljl-n'>layout</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>

    </span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-oB'>:</span><span class='hljl-ni'>4</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>ax1</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>

    </span><span class='hljl-nf'>trim!</span><span class='hljl-p'>(</span><span class='hljl-n'>layout</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-nf'>recordframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>io</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//trimming_grids/media/trimming_grids.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
