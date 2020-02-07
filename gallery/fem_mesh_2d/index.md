## FEM mesh 2D

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

</span><span class='hljl-n'>coordinates</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>1.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>1.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>1.0</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>;</span><span class='hljl-t'>
</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>connectivity</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-t'>
    </span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-t'> </span><span class='hljl-ni'>6</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'> </span><span class='hljl-ni'>6</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'> </span><span class='hljl-ni'>8</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-ni'>7</span><span class='hljl-t'> </span><span class='hljl-ni'>8</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>5</span><span class='hljl-t'> </span><span class='hljl-ni'>6</span><span class='hljl-t'> </span><span class='hljl-ni'>9</span><span class='hljl-p'>;</span><span class='hljl-t'>
    </span><span class='hljl-ni'>5</span><span class='hljl-t'> </span><span class='hljl-ni'>8</span><span class='hljl-t'> </span><span class='hljl-ni'>9</span><span class='hljl-p'>;</span><span class='hljl-t'>
</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.375</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>]</span><span class='hljl-t'>
</span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-n'>coordinates</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>connectivity</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>shading</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>wireframe!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>][</span><span class='hljl-ni'>1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:black</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.6</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//fem_mesh_2d/media/image.jpg" alt="">

    </p>
</div>

```
