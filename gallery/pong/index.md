## pong

```@raw html
<pre class='hljl'>
<span class='hljl-t'>

 </span><span class='hljl-n'>xyvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>2</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
 </span><span class='hljl-n'>velvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>2</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-t'>
 </span><span class='hljl-cs'># define some other parameters</span><span class='hljl-t'>
 </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-t'>
 </span><span class='hljl-n'>ts</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.03</span><span class='hljl-t'>
 </span><span class='hljl-n'>balldiameter</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
 </span><span class='hljl-n'>origin</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>xybounds</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>200</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>xyvec</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>balldiameter</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>RGBf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>limits</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>FRect</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xybounds</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>s</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-cs'># last plot in scene</span><span class='hljl-t'>

 </span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
     </span><span class='hljl-cs'># calculate new ball position</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>ts</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>xyvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>xyvec</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>velvec</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>ts</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>velvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>xyvec</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>xybounds</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>origin</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>velvec</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>p</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>o</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>vel</span><span class='hljl-t'>
         </span><span class='hljl-n'>boolvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>balldiameter</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.&gt;</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.|</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>.-</span><span class='hljl-t'> </span><span class='hljl-n'>balldiameter</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.&lt;</span><span class='hljl-t'> </span><span class='hljl-n'>o</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-n'>velvec</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>boolvec</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>vel</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-t'>
             </span><span class='hljl-n'>b</span><span class='hljl-t'> </span><span class='hljl-oB'>?</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-n'>v</span><span class='hljl-t'> </span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-t'>
         </span><span class='hljl-k'>end</span><span class='hljl-t'>
     </span><span class='hljl-k'>end</span><span class='hljl-t'>
     </span><span class='hljl-cs'># plot</span><span class='hljl-t'>
     </span><span class='hljl-n'>s</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>xyvec</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//pong/media/pong.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
