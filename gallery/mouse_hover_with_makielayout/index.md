## Mouse hover with MakieLayout

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>
</span><span class='hljl-k'>import</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>
</span><span class='hljl-k'>import</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>LAxis</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>GridLayout</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-k'>let</span><span class='hljl-t'> </span><span class='hljl-n'>nrows</span><span class='hljl-oB'>=</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ncols</span><span class='hljl-oB'>=</span><span class='hljl-ni'>1</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(;</span><span class='hljl-t'> </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-n'>campixel!</span><span class='hljl-p'>,</span><span class='hljl-t'>
        </span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>800</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>800</span><span class='hljl-p'>),</span><span class='hljl-t'>
        </span><span class='hljl-n'>backgroundcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:white</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>gl</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>GridLayout</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>nrows</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ncols</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>alignmode</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-oB'>.</span><span class='hljl-nf'>Outside</span><span class='hljl-p'>(</span><span class='hljl-ni'>30</span><span class='hljl-p'>))</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>gl</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>laxis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;workspace&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>mouseposition</span><span class='hljl-p'>(</span><span class='hljl-n'>laxis</span><span class='hljl-oB'>.</span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>mousemarker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>laxis</span><span class='hljl-oB'>.</span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>events</span><span class='hljl-oB'>.</span><span class='hljl-n'>mouseposition</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>mp</span><span class='hljl-t'>
    </span><span class='hljl-n'>area</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>pixelarea</span><span class='hljl-p'>(</span><span class='hljl-n'>laxis</span><span class='hljl-oB'>.</span><span class='hljl-n'>scene</span><span class='hljl-p'>)[]</span><span class='hljl-t'>
    </span><span class='hljl-n'>mp</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>mp</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.-</span><span class='hljl-t'> </span><span class='hljl-nf'>minimum</span><span class='hljl-p'>(</span><span class='hljl-n'>area</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>to_world</span><span class='hljl-p'>(</span><span class='hljl-n'>laxis</span><span class='hljl-oB'>.</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>mp</span><span class='hljl-p'>))]</span><span class='hljl-t'>
    </span><span class='hljl-k'>return</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>
</span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>laxis</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>mousemarker</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-oB'>=</span><span class='hljl-ni'>3</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span><span class='hljl-cs'># Do not execute beyond this point!</span><span class='hljl-t'>

</span><span class='hljl-nf'>RecordEvents</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//mouse_hover_with_makielayout/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
