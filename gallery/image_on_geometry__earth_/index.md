## Image on Geometry (Earth)

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>FileIO</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>Colors</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>GeometryBasics</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>earth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>load</span><span class='hljl-p'>(</span><span class='hljl-n'>MakieGallery</span><span class='hljl-oB'>.</span><span class='hljl-nf'>assetpath</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;earth.png&quot;</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-n'>m</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>uv_mesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Tesselation</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-ni'>60</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-n'>m</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=</span><span class='hljl-n'>earth</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>shading</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//image_on_geometry__earth_/media/image.png" alt="">

    </p>
</div>

```
