## Contour Function

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>512</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>y</span><span class='hljl-p'>))</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-oB'>&#39;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>contour</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>levels</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:viridis</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/contour_function/media/image.jpg" alt="">

    </p>
</div>

```
