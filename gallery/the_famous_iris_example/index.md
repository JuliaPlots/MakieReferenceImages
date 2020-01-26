## The famous iris example

```@raw html
<pre class='hljl'>
<span class='hljl-t'> </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>DataFrames</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-t'> </span><span class='hljl-cs'># do Pkg.add.([&quot;DataFrames&quot;, &quot;RDatasets&quot;]) if you don&#39;t have these packages installed</span><span class='hljl-t'>

 </span><span class='hljl-n'>iris</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;datasets&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;iris&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>iris</span><span class='hljl-p'>[</span><span class='hljl-oB'>!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalWidth</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>iris</span><span class='hljl-p'>[</span><span class='hljl-oB'>!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>]</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>colors</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:green</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-cs'>#color incrementer</span><span class='hljl-t'>
 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>sp</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-nf'>unique</span><span class='hljl-p'>(</span><span class='hljl-n'>iris</span><span class='hljl-p'>[</span><span class='hljl-oB'>!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:Species</span><span class='hljl-p'>])</span><span class='hljl-t'>
     </span><span class='hljl-n'>idx</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>iris</span><span class='hljl-p'>[</span><span class='hljl-oB'>!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:Species</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>.==</span><span class='hljl-t'> </span><span class='hljl-n'>sp</span><span class='hljl-t'>
     </span><span class='hljl-n'>sel</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>iris</span><span class='hljl-p'>[</span><span class='hljl-n'>idx</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-sc'>:SepalWidth</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>]]</span><span class='hljl-t'>
     </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sel</span><span class='hljl-p'>[</span><span class='hljl-oB'>:</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>sel</span><span class='hljl-p'>[</span><span class='hljl-oB'>:</span><span class='hljl-p'>,</span><span class='hljl-ni'>2</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>colors</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>limits</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>FRect</span><span class='hljl-p'>(</span><span class='hljl-nfB'>1.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>4.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>3.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>4.0</span><span class='hljl-p'>))</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-oB'>+</span><span class='hljl-ni'>1</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-cs'># get axis</span><span class='hljl-t'>
 </span><span class='hljl-nf'>xlabel!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Sepal width&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>ylabel!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Sepal length&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery/the_famous_iris_example/media/image.jpg" alt="">

    </p>
</div>

```
