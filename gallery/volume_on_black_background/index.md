## Volume on black background

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>);</span><span class='hljl-t'>  </span><span class='hljl-cs'># our value range</span><span class='hljl-t'>

 </span><span class='hljl-nf'>ρ</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>exp</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-p'>(</span><span class='hljl-nf'>abs</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)))</span><span class='hljl-t'> </span><span class='hljl-cs'># function (charge density)</span><span class='hljl-t'>

 </span><span class='hljl-cs'># create a Scene with the attribute `backgroundcolor = :black`,</span><span class='hljl-t'>
 </span><span class='hljl-cs'># can be any compatible color.  Useful for better contrast and not killing your eyes with a white background.</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>backgroundcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:black</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nf'>volume!</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'>          </span><span class='hljl-cs'># coordinates to plot on</span><span class='hljl-t'>
     </span><span class='hljl-n'>ρ</span><span class='hljl-p'>,</span><span class='hljl-t'>                </span><span class='hljl-cs'># charge density (functions as colorant)</span><span class='hljl-t'>
     </span><span class='hljl-n'>algorithm</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:mip</span><span class='hljl-t'>  </span><span class='hljl-cs'># maximum-intensity-projection</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>]</span><span class='hljl-oB'>.</span><span class='hljl-n'>names</span><span class='hljl-oB'>.</span><span class='hljl-n'>textcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:gray</span><span class='hljl-t'> </span><span class='hljl-cs'># let axis labels be seen on dark background</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-cs'># show scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/volume_on_black_background/media/image.jpg" alt="">

    </p>
</div>

```
