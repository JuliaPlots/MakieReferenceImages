## Streamplot 3D

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

 </span><span class='hljl-k'>struct</span><span class='hljl-t'> </span><span class='hljl-nf'>FitzhughNagumo</span><span class='hljl-p'>{</span><span class='hljl-n'>T</span><span class='hljl-p'>}</span><span class='hljl-t'>
     </span><span class='hljl-n'>ϵ</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-t'>
     </span><span class='hljl-n'>s</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-t'>
     </span><span class='hljl-n'>γ</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-t'>
     </span><span class='hljl-n'>β</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>

 </span><span class='hljl-n'>P</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>FitzhughNagumo</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.8</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>P</span><span class='hljl-oB'>::</span><span class='hljl-n'>FitzhughNagumo</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-oB'>-</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-oB'>-</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-oB'>^</span><span class='hljl-ni'>3</span><span class='hljl-oB'>+</span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>s</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>ϵ</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>γ</span><span class='hljl-oB'>*</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-oB'>-</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>2</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>β</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>γ</span><span class='hljl-oB'>*</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-oB'>-</span><span class='hljl-n'>x</span><span class='hljl-p'>[</span><span class='hljl-ni'>3</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>P</span><span class='hljl-oB'>.</span><span class='hljl-n'>β</span><span class='hljl-p'>,</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>P</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>streamplot</span><span class='hljl-p'>(</span><span class='hljl-n'>f</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>1.5</span><span class='hljl-oB'>..</span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>1.5</span><span class='hljl-oB'>..</span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>1.5</span><span class='hljl-oB'>..</span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:magma</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>gridsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>arrow_size</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.06</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/streamplot_3d/media/image.jpg" alt="">

    </p>
</div>

```
