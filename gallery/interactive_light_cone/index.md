## Interactive light cone

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>linesegments</span><span class='hljl-p'>([</span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>2</span><span class='hljl-p'>)],</span><span class='hljl-n'>scale_plot</span><span class='hljl-oB'>=</span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>show_axis</span><span class='hljl-oB'>=</span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>get_lightcone</span><span class='hljl-p'>(</span><span class='hljl-n'>pos</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-t'>
    </span><span class='hljl-n'>len</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>sqrt</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>^</span><span class='hljl-ni'>2</span><span class='hljl-oB'>+</span><span class='hljl-ni'>2</span><span class='hljl-oB'>^</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-k'>return</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-t'>
            </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-n'>v</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-oB'>/</span><span class='hljl-n'>len</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-oB'>/</span><span class='hljl-n'>len</span><span class='hljl-p'>),</span><span class='hljl-t'>
            </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-oB'>/</span><span class='hljl-n'>len</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-oB'>/</span><span class='hljl-n'>len</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-p'>),</span><span class='hljl-t'>
            </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-n'>v</span><span class='hljl-p'>)</span><span class='hljl-t'>
        </span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span><span class='hljl-n'>visible</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>events</span><span class='hljl-oB'>.</span><span class='hljl-n'>mousebuttons</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>mb</span><span class='hljl-t'>
    </span><span class='hljl-n'>visible</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>ispressed</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>Mouse</span><span class='hljl-oB'>.</span><span class='hljl-n'>left</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span><span class='hljl-n'>coords</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>events</span><span class='hljl-oB'>.</span><span class='hljl-n'>mouseposition</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>mp</span><span class='hljl-t'>
    </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>to_world</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>mp</span><span class='hljl-p'>))</span><span class='hljl-t'>
    </span><span class='hljl-k'>return</span><span class='hljl-t'> </span><span class='hljl-nf'>get_lightcone</span><span class='hljl-p'>(</span><span class='hljl-n'>pos</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span><span class='hljl-nf'>linesegments!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>coords</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>visible</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>visible</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-cs'># Do not execute beyond this point!</span><span class='hljl-t'>

</span><span class='hljl-nf'>RecordEvents</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//interactive_light_cone/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
