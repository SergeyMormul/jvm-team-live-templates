# Spock Testing
Describes live templates which are good to use in creating tests within [Spock Framework](http://spockframework.org/spock/docs/1.3/all_in_one.html).

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>set</code></td>
    <td>Creates a <code>setup</code> method.</td>
    <td>
      <pre lang='Groovy'>
def setup() {
    |
}</pre>
    </td>
  </tr>
  <tr>
    <td><code>test</code></td>
    <td>Creates an empty test. Adds an empty line below test declaration.<br/>
      Enter points:<br/>
      <ol>
        <li>Test name</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
def 'test name'() {
<br/>
    |
}</pre>
    </td>
  </tr>
  <tr>
    <td><code>gi</code></td>
    <td>Creates a <code>given:</code> label.<br/>
      Enter points:<br/>
      <ol>
        <li>Label description</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
given: 'label description'
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>an</code></td>
    <td>Creates an <code>and:</code> label.<br/>
      Enter points:<br/>
      <ol>
        <li>Label description</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
and: 'label description'
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>wn</code></td>
    <td>Creates a <code>when:</code> label.<br/>
      Enter points:<br/>
      <ol>
        <li>Label description</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
when: 'label description'
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>th</code></td>
    <td>Creates a <code>then:</code> label.<br/>
      Enter points:<br/>
      <ol>
        <li>Label description</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
then: 'label description'
|</pre>
    </td>
  </tr>
  <tr>
      <td><code>with</code></td>
      <td>Creates a <code>with</code> block for verification.<br/>
        Enter points:<br/>
        <ol>
          <li>Variable name</li>
        </ol>
      </td>
      <td>
        <pre lang='Groovy'>
with( variableName ) {
    |
}</pre>
      </td>
  </tr>
</table>
