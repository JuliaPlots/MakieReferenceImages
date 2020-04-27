## Lots of Heatmaps

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>makeheatmaps</span><span class='hljl-p'>(</span><span class='hljl-n'>bufs</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>heatmaps</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>bufs</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>buf</span><span class='hljl-t'>
        </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-t'>
            </span><span class='hljl-n'>buf</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>padding</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>colorrange</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>),</span><span class='hljl-t'>
            </span><span class='hljl-n'>axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>names</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>axisnames</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;&quot;</span><span class='hljl-p'>),),)</span><span class='hljl-t'>
        </span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-k'>end</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-n'>heatmaps</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-p'>]),</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>size</span><span class='hljl-p'>(</span><span class='hljl-n'>bufs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>))</span><span class='hljl-oB'>...</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>last</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>heatmaps</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>
</span><span class='hljl-n'>datarows</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>datacols</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-t'>
</span><span class='hljl-n'>plotrows</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>plotcols</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-t'>
</span><span class='hljl-n'>bufs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>fill</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>datarows</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>datacols</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>_</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>plotrows</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>_</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>plotcols</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>hms</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>makeheatmaps</span><span class='hljl-p'>(</span><span class='hljl-n'>bufs</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-t'>
</span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
    </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>hm</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>buf</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-nf'>zip</span><span class='hljl-p'>(</span><span class='hljl-nf'>vec</span><span class='hljl-p'>(</span><span class='hljl-n'>hms</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>vec</span><span class='hljl-p'>(</span><span class='hljl-n'>bufs</span><span class='hljl-p'>))</span><span class='hljl-t'>
        </span><span class='hljl-n'>buf</span><span class='hljl-t'> </span><span class='hljl-oB'>.=</span><span class='hljl-t'> </span><span class='hljl-n'>rand</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>Float32</span><span class='hljl-p'>)</span><span class='hljl-t'>
        </span><span class='hljl-n'>hm</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>buf</span><span class='hljl-t'>
    </span><span class='hljl-k'>end</span><span class='hljl-t'>
    </span><span class='hljl-nf'>yield</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//lots_of_heatmaps/media/lots_of_heatmaps.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
