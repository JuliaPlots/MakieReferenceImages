## 3D scenes

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>layoutscene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-nf'>makescene</span><span class='hljl-p'>()</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LScene</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>cam3d!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>scenekw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>backgroundcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>RGBf0</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.9</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.9</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.9</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>clear</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'>   </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>makescene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'>   </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>makescene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>makescene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-n'>layout</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>makescene</span><span class='hljl-p'>()</span><span class='hljl-t'>
</span><span class='hljl-nf'>foreach</span><span class='hljl-p'>(</span><span class='hljl-n'>LScene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>layout</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>s</span><span class='hljl-t'>
    </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>s</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>));</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//3d_scenes/media/image.png" alt="">

    </p>
</div>

```
