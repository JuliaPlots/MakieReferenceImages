## Layouting

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>p1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>p2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>p3</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>surface</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0..1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0..1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>p4</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-nfB'>0.1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>10</span><span class='hljl-t'>
 </span><span class='hljl-n'>p5</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-nfB'>0.1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>pscene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-n'>p1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>p2</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>p3</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-n'>p4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>p5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sizes</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.7</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.3</span><span class='hljl-p'>]),</span><span class='hljl-t'>
     </span><span class='hljl-n'>sizes</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.6</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//layouting/media/image.jpg" alt="">

    </p>
</div>

```
