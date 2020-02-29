## Streamplot animation

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-nf'>v</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>::</span><span class='hljl-nf'>Point2</span><span class='hljl-p'>{</span><span class='hljl-n'>T</span><span class='hljl-p'>},</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-n'>where</span><span class='hljl-t'> </span><span class='hljl-n'>T</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2</span><span class='hljl-p'>{</span><span class='hljl-n'>T</span><span class='hljl-p'>}(</span><span class='hljl-nf'>one</span><span class='hljl-p'>(</span><span class='hljl-n'>T</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>])</span><span class='hljl-t'>

</span><span class='hljl-n'>sf</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-n'>Base</span><span class='hljl-oB'>.</span><span class='hljl-nf'>Fix2</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0e0</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>title_str</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;t = 0.00&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>sp</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>streamplot</span><span class='hljl-p'>(</span><span class='hljl-t'>
        </span><span class='hljl-n'>sf</span><span class='hljl-p'>,</span><span class='hljl-t'>
        </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>2..2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>2..2</span><span class='hljl-p'>;</span><span class='hljl-t'>
        </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'>
        </span><span class='hljl-n'>padding</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'>
        </span><span class='hljl-n'>arrow_size</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.09</span><span class='hljl-p'>,</span><span class='hljl-t'>
        </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=:</span><span class='hljl-n'>magma</span><span class='hljl-t'>
    </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>sc</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>title</span><span class='hljl-p'>(</span><span class='hljl-n'>sp</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title_str</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-oB'>*</span><span class='hljl-ni'>30</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
  </span><span class='hljl-n'>sf</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Base</span><span class='hljl-oB'>.</span><span class='hljl-nf'>Fix2</span><span class='hljl-p'>(</span><span class='hljl-n'>v</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-p'>)</span><span class='hljl-t'>
  </span><span class='hljl-n'>title_str</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;t = </span><span class='hljl-si'>$</span><span class='hljl-p'>(</span><span class='hljl-nf'>round</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>sigdigits</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>))</span><span class='hljl-s'>&quot;</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//streamplot_animation/media/streamplot_animation.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
