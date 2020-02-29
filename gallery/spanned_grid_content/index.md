## Spanned grid content

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>layoutscene</span><span class='hljl-p'>(</span><span class='hljl-ni'>4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1200</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1200</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;[1, 1:2]&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-oB'>:</span><span class='hljl-ni'>4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;[2:4, 1:2]&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-oB'>:</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;[:, 3]&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;[1:3, end]&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>title</span><span class='hljl-oB'>=</span><span class='hljl-s'>&quot;[end, end]&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//spanned_grid_content/media/image.jpg" alt="">

    </p>
</div>

```
