---
title: Interactive visualization of origin-destination matrices: a Shiny app and how to
date: 2020-10-28
math: true
diagram: true
image:
  placement: 3
  caption: 'Image credit: [**John Moeses Bauan**](https://unsplash.com/photos/OGZtQF8iC0g)'
---

Academic is designed to give technical content creators a seamless experience. You can focus on the content and Academic handles the rest.

**Interactive ODM explorer**
{{< myshortcode >}}
<html>
<head><title>Interactive ODM explorer</title></head>
<body>
<iframe id="InteractiveODM" src="https://yuanliao.shinyapps.io/InteractiveODM/" style="border: none; width: 100%; height: 850px" frameborder="0"></iframe>
</body>
</html>
{{< /myshortcode >}}

On this page, you'll find some examples of the types of technical content that can be rendered with Academic.

## Examples

### Code

Academic supports a Markdown extension for highlighting code syntax. You can enable this feature by toggling the `highlight` option in your `config/_default/params.toml` file.


```python
import pandas as pd
data = pd.read_csv("data.csv")
data.head()
```