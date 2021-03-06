## Arrows on hemisphere

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.9f0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>transparency</span><span class='hljl-oB'>=</span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>alpha</span><span class='hljl-oB'>=</span><span class='hljl-nfB'>0.05</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>cosine_weighted_sample_hemisphere</span><span class='hljl-p'>()</span><span class='hljl-t'>
    </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>acos</span><span class='hljl-p'>(</span><span class='hljl-nf'>sqrt</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>()))</span><span class='hljl-t'>
    </span><span class='hljl-n'>ϕ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>π</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>()</span><span class='hljl-t'>

    </span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>ϕ</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>ϕ</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-t'>

</span><span class='hljl-n'>dirs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>cosine_weighted_sample_hemisphere</span><span class='hljl-p'>()</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>N</span><span class='hljl-p'>]</span><span class='hljl-t'>

</span><span class='hljl-nf'>arrows!</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-nf'>fill</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>),</span><span class='hljl-t'>
    </span><span class='hljl-n'>dirs</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>arrowcolor</span><span class='hljl-oB'>=:</span><span class='hljl-n'>red</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>arrowsize</span><span class='hljl-oB'>=</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'>
    </span><span class='hljl-n'>linecolor</span><span class='hljl-oB'>=:</span><span class='hljl-n'>red</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//arrows_on_hemisphere/media/image.png" alt="">

    </p>
</div>

```
