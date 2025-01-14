## Members

<dl>
<dt><a href="#boxChars">boxChars</a></dt>
<dd><p>This function is used to truncate a string adding ... at the end.</p></dd>
</dl>

## Constants

<dl>
<dt><a href="#boxChars">boxChars</a> : <code>Object</code></dt>
<dd><p>The characters used to draw the box.</p></dd>
</dl>

## Functions

<dl>
<dt><a href="#styledToSimplifiedStyled">styledToSimplifiedStyled(styled)</a> ⇒ <code>*</code></dt>
<dd><p>This function is used to convert a styled element to a simplified styled element.</p></dd>
<dt><a href="#simplifiedStyledToStyled">simplifiedStyledToStyled(simplifiedStyled)</a> ⇒ <code>*</code></dt>
<dd><p>This function is used to convert a simplified styled element to a styled element.</p></dd>
</dl>

## Typedefs

<dl>
<dt><a href="#RGB">RGB</a> : <code>string</code></dt>
<dd><p>The type of the HEX color.</p></dd>
</dl>

## Interfaces

<dl>
<dt><a href="#StyleObject">StyleObject</a> : <code>Object</code></dt>
<dd><p>The type containing all the possible styles for the text.</p></dd>
<dt><a href="#StyledElement">StyledElement</a> : <code>Object</code></dt>
<dd><p>The type of the single styled text, stored in a line of the PageBuilder.</p></dd>
<dt><a href="#SimplifiedStyledElement">SimplifiedStyledElement</a> : <code>Object</code></dt>
<dd><p>The type containing all the possible styles for the text and the text on the same level. It's used on the higher level.</p></dd>
<dt><a href="#PhisicalValues">PhisicalValues</a></dt>
<dd><p>The type that contains the phisical values of an element (x, y, width, height)</p></dd>
</dl>

<a name="StyleObject"></a>

## StyleObject : <code>Object</code>
<p>The type containing all the possible styles for the text.</p>

**Kind**: global interface  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| [color] | <code>chalk.ForegroundColorName</code> \| <code>HEX</code> \| [<code>RGB</code>](#RGB) \| <code>&quot;&quot;</code> | <p>The color of the text taken from the chalk library.</p> |
| [backgroundColor] | <code>chalk.BackgroundColorName</code> \| <code>HEX</code> \| [<code>RGB</code>](#RGB) \| <code>&quot;&quot;</code> | <p>The background color of the text taken from the chalk library.</p> |
| [italic] | <code>boolean</code> | <p>If the text is italic.</p> |
| [bold] | <code>boolean</code> | <p>If the text is bold.</p> |
| [dim] | <code>boolean</code> | <p>If the text is dim.</p> |
| [underline] | <code>boolean</code> | <p>If the text is underlined.</p> |
| [inverse] | <code>boolean</code> | <p>If the text is inverse.</p> |
| [hidden] | <code>boolean</code> | <p>If the text is hidden.</p> |
| [strikethrough] | <code>boolean</code> | <p>If the text is strikethrough.</p> |
| [overline] | <code>boolean</code> | <p>If the text is overlined.</p> |

**Example**  
```js
const textStyle = { color: "red", backgroundColor: "blue", bold: true, italic: true }
```
<a name="StyledElement"></a>

## StyledElement : <code>Object</code>
<p>The type of the single styled text, stored in a line of the PageBuilder.</p>

**Kind**: global interface  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| text | <code>string</code> | <p>The text of the styled text.</p> |
| style | [<code>StyleObject</code>](#StyleObject) | <p>The style of the styled text.</p> |

**Example**  
```js
const styledText = { text: "Hello", style: { color: "red", backgroundColor: "blue", bold: true, italic: true } }
```
<a name="SimplifiedStyledElement"></a>

## SimplifiedStyledElement : <code>Object</code>
<p>The type containing all the possible styles for the text and the text on the same level. It's used on the higher level.</p>

**Kind**: global interface  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| text | <code>string</code> | <p>The text of the styled text.</p> |
| [color] | <code>chalk.ForegroundColorName</code> \| <code>HEX</code> \| [<code>RGB</code>](#RGB) \| <code>&quot;&quot;</code> | <p>The color of the text taken from the chalk library.</p> |
| [backgroundColor] | <code>chalk.BackgroundColorName</code> \| <code>HEX</code> \| [<code>RGB</code>](#RGB) \| <code>&quot;&quot;</code> \| <code>&quot;&quot;</code> | <p>The background color of the text taken from the chalk library.</p> |
| [italic] | <code>boolean</code> | <p>If the text is italic.</p> |
| [bold] | <code>boolean</code> | <p>If the text is bold.</p> |
| [dim] | <code>boolean</code> | <p>If the text is dim.</p> |
| [underline] | <code>boolean</code> | <p>If the text is underlined.</p> |
| [inverse] | <code>boolean</code> | <p>If the text is inverse.</p> |
| [hidden] | <code>boolean</code> | <p>If the text is hidden.</p> |
| [strikethrough] | <code>boolean</code> | <p>If the text is strikethrough.</p> |
| [overline] | <code>boolean</code> | <p>If the text is overlined.</p> |

**Example**  
```js
const textStyle = { color: "red", backgroundColor: "blue", bold: true, italic: true }
```
<a name="PhisicalValues"></a>

## PhisicalValues
<p>The type that contains the phisical values of an element (x, y, width, height)</p>

**Kind**: global interface  
<a name="boxChars"></a>

## boxChars
<p>This function is used to truncate a string adding ... at the end.</p>

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | <p>The string to truncate.</p> |
| n | <code>number</code> | <p>The number of characters to keep.</p> |
| useWordBoundary | <code>boolean</code> | <p>If true, the truncation will be done at the end of the word.</p> |

**Example**  
```js
CM.truncate("Hello world", 5, true) // "Hello..."
```
<a name="boxChars"></a>

## boxChars : <code>Object</code>
<p>The characters used to draw the box.</p>

**Kind**: global constant  
<a name="styledToSimplifiedStyled"></a>

## styledToSimplifiedStyled(styled) ⇒ <code>\*</code>
<p>This function is used to convert a styled element to a simplified styled element.</p>

**Kind**: global function  
**Returns**: <code>\*</code> - <p>{SimplifiedStyledElement}</p>  

| Param | Type |
| --- | --- |
| styled | [<code>StyledElement</code>](#StyledElement) | 

**Example**  
```js
const simplifiedStyledElement = styledToSimplifiedStyled({ text: "Hello world", style: { color: "red", backgroundColor: "blue", bold: true, italic: true } })// returns { text: "Hello world", color: "red", backgroundColor: "blue", bold: true, italic: true }
```
<a name="simplifiedStyledToStyled"></a>

## simplifiedStyledToStyled(simplifiedStyled) ⇒ <code>\*</code>
<p>This function is used to convert a simplified styled element to a styled element.</p>

**Kind**: global function  
**Returns**: <code>\*</code> - <p>{StyledElement}</p>  

| Param | Type |
| --- | --- |
| simplifiedStyled | [<code>SimplifiedStyledElement</code>](#SimplifiedStyledElement) | 

**Example**  
```js
const styledElement = simplifiedStyledToStyled({ text: "Hello world", color: "red", bold: true })// returns { text: "Hello world", style: { color: "red", bold: true } }
```
<a name="RGB"></a>

## RGB : <code>string</code>
<p>The type of the HEX color.</p>

**Kind**: global typedef  
**Example**  
```js
const hexColor = "#FF0000"
```
**Example**  
```js
const rgbColor = "rgb(255, 0, 0)"
```
