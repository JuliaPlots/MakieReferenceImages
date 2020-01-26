## Cube lattice

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>me</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[((</span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>./</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>./</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>./</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>)</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-oB'>=</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>=</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-oB'>=</span><span class='hljl-n'>r</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>me2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>me</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>abs</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>me</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.&gt;</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>contour</span><span class='hljl-p'>(</span><span class='hljl-n'>me2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:Set2</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/cube_lattice/media/image.jpg" alt="">

    </p>
</div>

```
