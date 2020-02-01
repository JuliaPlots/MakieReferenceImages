## ManualTicks

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>MakieLayout</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1000</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1000</span><span class='hljl-p'>));</span><span class='hljl-t'>
 </span><span class='hljl-nf'>campixel!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>);</span><span class='hljl-t'>

 </span><span class='hljl-n'>maingl</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>GridLayout</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>alignmode</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Outside</span><span class='hljl-p'>(</span><span class='hljl-ni'>30</span><span class='hljl-p'>))</span><span class='hljl-t'>

 </span><span class='hljl-n'>la</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>maingl</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LAxis</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>la</span><span class='hljl-oB'>.</span><span class='hljl-n'>attributes</span><span class='hljl-oB'>.</span><span class='hljl-n'>yautolimitmargin</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>0f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.05f0</span><span class='hljl-p'>)</span><span class='hljl-t'>


 </span><span class='hljl-nf'>poly!</span><span class='hljl-p'>(</span><span class='hljl-n'>la</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>BBox</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=:</span><span class='hljl-n'>blue</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>poly!</span><span class='hljl-p'>(</span><span class='hljl-n'>la</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>BBox</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>7</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=:</span><span class='hljl-n'>red</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>poly!</span><span class='hljl-p'>(</span><span class='hljl-n'>la</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>BBox</span><span class='hljl-p'>(</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=:</span><span class='hljl-n'>green</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>la</span><span class='hljl-oB'>.</span><span class='hljl-n'>attributes</span><span class='hljl-oB'>.</span><span class='hljl-n'>xticks</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>ManualTicks</span><span class='hljl-p'>([</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>2.5</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-s'>&quot;blue&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;red&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;green&quot;</span><span class='hljl-p'>])</span><span class='hljl-t'>
 </span><span class='hljl-n'>la</span><span class='hljl-oB'>.</span><span class='hljl-n'>attributes</span><span class='hljl-oB'>.</span><span class='hljl-n'>xlabel</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Color&quot;</span><span class='hljl-t'>
 </span><span class='hljl-n'>la</span><span class='hljl-oB'>.</span><span class='hljl-n'>attributes</span><span class='hljl-oB'>.</span><span class='hljl-n'>ylabel</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Value&quot;</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/manualticks/media/image.jpeg" alt="">

    </p>
</div>

```
