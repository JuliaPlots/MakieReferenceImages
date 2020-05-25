## algorithm

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-n'>sc</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
    </span><span class='hljl-nf'>volume</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>32</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>algorithm</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:mip</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-cs'>#with mip algorithm</span><span class='hljl-t'>
    </span><span class='hljl-nf'>volume</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>32</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>algorithm</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:absorptionrgba</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-cs'>#with AbsorptionRGBA algorithm</span><span class='hljl-t'>
</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//algorithm/media/image.png" alt="">

    </p>
</div>

```
