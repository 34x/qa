# HTML & CSS

**Hypertext Markup Language (HTML)** is the standard markup language for creating web pages and web applications. 

[Wikipedia](https://en.wikipedia.org/wiki/HTML)

In non technical words **html** is the way you see a page on the screeen according to its marking.
```html
<html>
<head> 
	<title> My first web page</title>
</head>
<body>
	
	<h1>Documentation</h1> 
	
	<h2>Keyboards shortcuts</h2>
	
	<div><strong>ctrl+s</strong> - save document</div>
        <div><strong>ctrl+r</strong> - reload</div>

	<h2>Tags</h2>

	<div>&lt;strong&gt; or &lt;b&gt; - <strong>bold</strong></div>
	<div>&lt;i&gt; - <i>italic</i></div>	
	<div>&lt;hr/&gt; - horisontal line</div>
	<div>&lt;br/&gt; - brake line (перенос строки)</div>
	
	<h2>To do list</h2>

	<ol>
		<li>learn html</li>
		<li>find work</li>
		<li>buy tushenka</li>
	</ol>
	
	<div>&lt;ol&gt; - ordered list</div>	
	<div>&lt;li&gt; - separate line</div>
		
	<h2>HTML код таблицы, примеры</h2>

	<table border="0" cellspacing="30">
		<tr><th colspan="3">Berlin</th></tr>
	<tr>
		<td>ячейка 1, первый ряд</td>
		<td>ячейка 2, первый ряд</td>
		<td>ячейка 3, первый ряд</td>
	</tr>
	<tr>
		<td>ячейка 1, второй ряд</td>
		<td>ячейка 2, второй ряд</td>
		<td>ячейка 3, второй ряд</td>
	</tr>
	<tr>
		<td>ячейка 1, третий ряд</td>
		<td>ячейка 2, третий ряд</td>
		<td>ячейка 3, третий ряд</td>
	</tr>
	</table> 

<div>&lt;table&gt; - for a table creation</div>
<div>&lt;table border="0"&gt; - borderlines</div>
<div>&lt;table cellspacing="30"&gt; - cell width and height </div>
<div>&lt;tr&gt; - defines a standard line
<div>&lt;td&gt; - defines a standard cell
<div>&lt;th&gt; - elements are bold and centered by default

</body>
</html>
```

# CSS

**Cascading Style Sheets (CSS)** is a style sheet language used for describing the presentation of a document written in a markup language like HTML.

[Wikipedia](https://en.wikipedia.org/wiki/Cascading_Style_Sheets)

In non technical words **css** is the design of a page.

```html

<style type="text/css">
		
	* {
		color:white;
	  }
	body {
		background-color:lightgrey;
		font-family: Arial;
		font-size: 10pt;
		background-image: url("http://hdwpro.com/wp-content/uploads/2017/11/Free-Desktop-Background.jpeg");	
		background-attachment: fixed;	
  		}

	h1, h2, h3 {
		color:darkred;
		background-color:yellow;
		font-size: 200%;
		font-family: Courier;
		border-bottom: 2pt darkblue solid;
		text-align: center;
		padding: 1ex 4ex;
		}
	h2{
		font-size: 150%;
		}
	ol {
		font-size: 20px;
		}
	.tags{
		border-color:red;
		}
	</style>
```
```html
<style type="text/css"> - working with style
	
color:white;
background-color:lightgrey;
font-family: Arial;
font-size: 10pt;
background-image: url("http://...jpeg");	
background-attachment: fixed;
border-bottom: 2pt darkblue solid;
text-align: center;
margin: 1ex 4ex;
padding: 1ex 4ex;
