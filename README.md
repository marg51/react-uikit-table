<div><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/uikit/2.24.2/css/uikit.almost-flat.min.css"/><section><h1>Table</h1><p class="uk-article-lead">Create nice looking tables.</p></section><section><h2>Usage</h2><p><code>npm install react-uikit-table --save;</code></p><p>ES6 <br/><code>import Table from &#x27;react-uikit-table&#x27;;</code><br/></p><p>ES5 <br/><code>var Table = require(&#x27;react-uikit-table&#x27;);</code></p><p><span class="uk-badge  uk-badge-danger">Note</span>  UIkit css is not included. You can get it from <a href="http://getuikit.com/">getuikit.com</a>. This has been tested with UIKit version 2.24.2.</p><hr class="uk-article-divider"/><h3 class="example">Example</h3><p>Table can be type declaitively or generated by passing a JSON object to the <code>body</code> prop.</p><p><span class="uk-badge">Note</span>  Nested properties are not supported at this time.</p><table class="uk-table"><caption>Table 1 - Generated table.</caption><thead><tr><th>Heading</th><th>Heading</th><th>Heading</th></tr></thead><tbody><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr></tbody></table><table class="uk-table"><caption>Table 2 - From Children.</caption><thead><tr><th class="uk-text-left">Heading</th><th class="uk-text-left">Heading</th><th class="uk-text-left">Heading</th></tr></thead><tbody><tr><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td></tr><tr><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td></tr><tr><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td><td class="uk-text-left">Data</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const data = [
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;}
];

&lt;Table caption=&#x27;Table 1 - Generated table.&#x27; head={[&#x27;Heading&#x27;, &#x27;Heading&#x27;, &#x27;Heading&#x27;]} body={data}/&gt;

&lt;Table caption=&#x27;Table 2 - From Children.&#x27;&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th className=&#x27;uk-text-left&#x27;&gt;Heading&lt;/th&gt;
      &lt;th className=&#x27;uk-text-left&#x27;&gt;Heading&lt;/th&gt;
      &lt;th className=&#x27;uk-text-left&#x27;&gt;Heading&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;

  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
      &lt;td className=&#x27;uk-text-left&#x27;&gt;Data&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/Table&gt;
</code></pre></section><section><h2>Table Head</h2><p>Table heaings can be set by passing a list of heading to the <code>head=[]</code> prop.<br/>Alternatively if the body prop is being used to genterate table data heading can also be generated using the JSON keys<code>head=&#x27;*&#x27;</code>.</p><p><span class="uk-badge">Note</span>  Keys generate a list of headings in the order they appears. Also the keys will be case insensitve.</p><h3 class="example">Example</h3><table class="uk-table  uk-table-condensed"><caption>Table 1 - Headings from body keys.</caption><thead><tr><th>name</th><th>score</th><th>height</th></tr></thead><tbody><tr><td>OTIS</td><td>39</td><td>5.6</td></tr><tr><td>jocelyn</td><td>65</td><td>4.8</td></tr><tr><td>Ania</td><td>-50</td><td>6.1</td></tr></tbody></table><table class="uk-table  uk-table-condensed"><caption>Table 2 - Headins from prop.</caption><thead><tr><th>Heading</th><th>Heading</th><th>Heading</th></tr></thead><tbody><tr><td>OTIS</td><td>39</td><td>5.6</td></tr><tr><td>jocelyn</td><td>65</td><td>4.8</td></tr><tr><td>Ania</td><td>-50</td><td>6.1</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const items = [
  {
    Name: &#x27;OTIS&#x27;,
    score: 39,
    height: 5.6
  }, {
    name: &#x27;jocelyn&#x27;,
    score: 65,
    height: 4.8
  }, {
    name: &#x27;Ania&#x27;,
    score: -50,
    height: 6.10
  }
];

&lt;Table caption=&#x27;Table 1 - Headings from body keys.&#x27; condensed head=&#x27;*&#x27; body={items}/&gt;

&lt;Table caption=&#x27;Table 2 - Headins from prop.&#x27; condensed head={[&#x27;Heading&#x27;, &#x27;Heading&#x27;, &#x27;Heading&#x27;]} body={items}/&gt;
</code></pre></section><section><h2>Table condensed</h2><p>To make the table move compact add the <code>condensed</code> prop to the Tables props.</p><h3 class="example">Example</h3><table class="uk-table  uk-table-condensed"><caption>Condensed table</caption><thead><tr><th>Heading</th><th>Heading</th><th>Heading</th></tr></thead><tbody><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const data = [
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;}
];
&lt;Table caption=&#x27;Condensed table&#x27; condensed head={[&#x27;Heading&#x27;, &#x27;Heading&#x27;, &#x27;Heading&#x27;]} body={data}/&gt;
</code></pre></section><section><h2>Table Hover</h2><p>To highlight a row when it is hovered add the <code>hover</code> prop to the Tables props.</p><h3 class="example">Example</h3><table class="uk-table  uk-table-hover"><caption>Hoverable table</caption><thead><tr><th>Heading</th><th>Heading</th><th>Heading</th></tr></thead><tbody><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const data = [
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;}
];

&lt;Table caption=&#x27;Hoverable table&#x27;  hover head={[&#x27;Heading&#x27;, &#x27;Heading&#x27;, &#x27;Heading&#x27;]} body={data}/&gt;
</code></pre></section><section><h2>Table striped</h2><p>Add zebra-striping to table by adding the <code>striped</code> prop to the Tables props.</p><h3 class="example">Example</h3><table class="uk-table  uk-table-striped"><caption>Striped table</caption><thead><tr><th>Heading</th><th>Heading</th><th>Heading</th></tr></thead><tbody><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr><tr><td>Data</td><td>Data</td><td>Data</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const data = [
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;},
  {d1: &#x27;Data&#x27;, d2: &#x27;Data&#x27;, d3: &#x27;Data&#x27;}
];

&lt;Table caption=&#x27;Striped table&#x27;  striped head={[&#x27;Heading&#x27;, &#x27;Heading&#x27;, &#x27;Heading&#x27;]} body={data}/&gt;
</code></pre></section><section><h2>Table sort</h2><p>Generated tables can be sorted by passing the keys names to the <code>sort</code> prop. The sort prop can either be sting for a single sort or a list for multiple sort. <br/>To reverse the sort on a feild put &#x27;-&#x27; in from of the key name.</p><h3 class="example">Example</h3><table class="uk-table"><caption>Sortable table</caption><thead><tr><th>name</th><th>score</th><th>height</th></tr></thead><tbody><tr><td>OTIS</td><td>39</td><td>5.6</td></tr><tr><td>Ania</td><td>-50</td><td>6.1</td></tr><tr><td>jocelyn</td><td>65</td><td>4.8</td></tr></tbody></table><h4 class="code">Code</h4><pre class="xml"><code class="xml">const items = [
  {
    Name: &#x27;OTIS&#x27;,
    score: 39,
    height: 5.6
  }, {
    name: &#x27;jocelyn&#x27;,
    score: 65,
    height: 4.8
  }, {
    name: &#x27;Ania&#x27;,
    score: -50,
    height: 6.10
  }
];

&lt;Table caption=&#x27;Condensed table&#x27; sort={[&#x27;name&#x27;, &#x27;-height&#x27;]} head=&#x27;items&#x27; body={items}/&gt;
</code></pre></section><section><h2>Table props</h2><p><code>&lt;Table&gt;</code> props and their types.</p><p>See <a href="https://github.com/otissv/react-uikit-base">base</a> for additional props.</p><table class="uk-table"><thead><tr><th class="uk-text-left">Prop</th><th class="uk-text-left">Type</th></tr></thead><tbody><tr><td class="uk-text-left"><code>body</code></td><td class="uk-text-left">array</td></tr><tr><td class="uk-text-left"><code>caption</code></td><td class="uk-text-left">string</td></tr><tr><td class="uk-text-left"><code>condensed</code></td><td class="uk-text-left">bool</td></tr><tr><td class="uk-text-left"><code>hover</code></td><td class="uk-text-left">bool</td></tr><tr><td class="uk-text-left"><code>head</code></td><td class="uk-text-left">oneOfType<br/>array or string</td></tr><tr><td class="uk-text-left"><code>overflow</code></td><td class="uk-text-left">bool</td></tr><tr><td class="uk-text-left"><code>sort</code></td><td class="uk-text-left">oneOfType<br/>array or string</td></tr><tr><td class="uk-text-left"><code>striped</code></td><td class="uk-text-left">bool</td></tr></tbody></table></section><section><h2>Tests</h2><p><code>npm run test</code> to run tests with minimal output.<br/><code>npm run test:spec</code> to run tests with detailed output.<br/><code>npm run test:watch</code>watches all directories and run tests with minimal output on file changes.<br/></p></section><section><h2>Build</h2><p><code>npm run build</code> to build files fro distribution.<br/><code>npm run build:watch</code> watches src directory and builds files on changes.<br/></p></section><section><h2>Lint</h2><p><code>npm run lint</code> lints scripts in src directory.<br/><code>npm run lint:watch</code> watches src directory and lints scripts in src directory.<br/></p></section><section><h2>License</h2><p>MIT</p></section></div>