## Box plot

```@raw html
<pre class='hljl'>
<span class='hljl-t'>
</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-t'>

</span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-t'>


</span><span class='hljl-n'>d</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;Ecdat&quot;</span><span class='hljl-p'>,</span><span class='hljl-s'>&quot;Fatality&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-nf'>boxplot</span><span class='hljl-p'>(</span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>d</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-sc'>:Year</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:Perinc</span><span class='hljl-p'>)</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//box_plot/media/image.png" alt="">

    </p>
</div>

```
