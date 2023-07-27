# JUnit Testing
Describes live templates which are good to use in creating tests within [JUnit Framework](https://junit.org/junit5/).

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
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
      <pre lang='Java'>
@Test
void test_name() {
<br/>
    |
}</pre>
    </td>
  </tr>
  <tr>
    <td><code>mock</code></td>
    <td>Creates a variable for a Mockito mocked object.<br/>
        Omits .class in the variable name.<br/>
      Enter points:<br/>
      <ol>
        <li>The method argument</li>
      </ol>
    </td>
    <td>
    <pre lang='Java'>
var myClass = Mockito.mock( MyClass.class )
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>gmock</code></td>
    <td>Creates a test class field for a Mockito mocked object.<br/>
      Omits .class in the variable name.<br/>
      Class type is defined by the method argument.<br/>
      Enter points:<br/>
      <ol>
        <li>The method argument</li>
      </ol>
    </td>
    <td>
    <pre lang='Java'>
private final MyClass myClass = Mockito.mock( MyClass.class );
|</pre>
    </td>
  </tr>
</table>
