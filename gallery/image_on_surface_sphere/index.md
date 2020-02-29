## Image on Surface Sphere

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>n</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-t'>
</span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-ni'>0</span><span class='hljl-p'>;(</span><span class='hljl-nfB'>0.5</span><span class='hljl-oB'>:</span><span class='hljl-n'>n</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-n'>n</span><span class='hljl-p'>;</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>φ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[(</span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-n'>n</span><span class='hljl-oB'>-</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-ni'>2</span><span class='hljl-oB'>/</span><span class='hljl-p'>(</span><span class='hljl-ni'>2</span><span class='hljl-n'>n</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>);</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>cospi</span><span class='hljl-p'>(</span><span class='hljl-n'>φ</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-nf'>sinpi</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>sinpi</span><span class='hljl-p'>(</span><span class='hljl-n'>φ</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-nf'>sinpi</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>cospi</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>θ</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-n'>φ</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-nf'>rand</span><span class='hljl-p'>([</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-n'>pts</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>vec</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-nf'>surface</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>logo</span><span class='hljl-p'>(),</span><span class='hljl-t'> </span><span class='hljl-n'>transparency</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//image_on_surface_sphere/media/image.jpg" alt="">

    </p>
</div>

```
