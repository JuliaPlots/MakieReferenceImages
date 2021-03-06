## Coloured fractional Brownian noise field

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>FFTW</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>

</span><span class='hljl-s'>&quot;This example was contributed by Harmen Stoppels (@haampie)&quot;</span><span class='hljl-t'>


</span><span class='hljl-cs'># Obtain approximately fractal Brownian noise, appropriately damping</span><span class='hljl-t'>
</span><span class='hljl-cs'># the high frequencies of Fourier transformed spatial white noise,</span><span class='hljl-t'>
</span><span class='hljl-cs'># and (inverse) Fourier transforming the result back into the spatial domain.</span><span class='hljl-t'>
</span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>cloud</span><span class='hljl-p'>(</span><span class='hljl-n'>n</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>256</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.75f0</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>ωs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>fft</span><span class='hljl-p'>(</span><span class='hljl-nf'>randn</span><span class='hljl-p'>(</span><span class='hljl-n'>Float32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>n</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>n</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>n</span><span class='hljl-p'>))</span><span class='hljl-t'>
    </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Float32</span><span class='hljl-p'>[</span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-n'>n</span><span class='hljl-oB'>÷</span><span class='hljl-ni'>2</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>n</span><span class='hljl-oB'>÷</span><span class='hljl-ni'>2</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:-</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-p'>(</span><span class='hljl-nf'>iseven</span><span class='hljl-p'>(</span><span class='hljl-n'>n</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>?</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)]</span><span class='hljl-t'>
    </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>zs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>reshape</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>reshape</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>reshape</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-n'>ωs</span><span class='hljl-t'> </span><span class='hljl-oB'>./=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>1.0f0</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>xs</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>zs</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.^</span><span class='hljl-t'> </span><span class='hljl-n'>p</span><span class='hljl-p'>)</span><span class='hljl-t'>
    </span><span class='hljl-k'>return</span><span class='hljl-t'> </span><span class='hljl-n'>real</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-nf'>ifft</span><span class='hljl-p'>(</span><span class='hljl-n'>ωs</span><span class='hljl-p'>))</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>cloud</span><span class='hljl-p'>(</span><span class='hljl-ni'>256</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.75</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span><span class='hljl-nf'>volume</span><span class='hljl-p'>(</span><span class='hljl-n'>z</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>algorithm</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:mip</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colorrange</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>extrema</span><span class='hljl-p'>(</span><span class='hljl-n'>z</span><span class='hljl-p'>))</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//coloured_fractional_brownian_noise_field/media/image.png" alt="">

    </p>
</div>

```
