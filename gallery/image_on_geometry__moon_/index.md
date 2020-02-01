## Image on Geometry (Moon)

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>FileIO</span><span class='hljl-t'>

 </span><span class='hljl-n'>moon</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-k'>try</span><span class='hljl-t'>
     </span><span class='hljl-nf'>load</span><span class='hljl-p'>(</span><span class='hljl-nf'>download</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;https://svs.gsfc.nasa.gov/vis/a000000/a004600/a004675/phases.0001_print.jpg&quot;</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-k'>catch</span><span class='hljl-t'> </span><span class='hljl-n'>e</span><span class='hljl-t'>
     </span><span class='hljl-nd'>@warn</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;Downloading the moon failed. Using random image, so this test will fail! (error: </span><span class='hljl-si'>$e</span><span class='hljl-s'>)&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>RGBAf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># don&#39;t error test when e.g. offline</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>moon</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>shading</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>center</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>update_cam!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>center</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'> </span><span class='hljl-cs'># prevent to recenter on display</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/image_on_geometry__moon_/media/image.jpg" alt="">

    </p>
</div>

```
