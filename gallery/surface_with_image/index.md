## Surface with image

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-t'>
 </span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>xy_data</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>sqrt</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>^</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>==</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-t'> </span><span class='hljl-oB'>?</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-n'>r</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>surf_func</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nf'>Float32</span><span class='hljl-p'>(</span><span class='hljl-nf'>xy_data</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>*</span><span class='hljl-n'>i</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>*</span><span class='hljl-n'>i</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-nf'>surface</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>surf_func</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>RGBAf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>124</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>124</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//surface_with_image/media/image.jpg" alt="">

    </p>
</div>

```
