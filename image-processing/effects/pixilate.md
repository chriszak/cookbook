# Pixelate an image or a region

## Pixelate an image or a region

Apply a pixelization effect to an image by setting the **`effect`** parameter to **`pixelate`**   
\(**`e_pixelate`** in URLs\). You can choose to pixelate the whole image or just a certain region of the image, and the size of the squares is customizable.

Here's an original image fetched on-the-fly from a public remote HTTP URL at Wikimedia Commons:  


![](https://res.cloudinary.com/demo/image/fetch/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Using the **`pixelate`** effect to apply pixelization on the whole image:

![](https://res.cloudinary.com/demo/image/fetch/e_pixelate/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/e_pixelate/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Control the effect’s intensity by specifying the size of the pixelization squares \(numeric value, in pixels\). In the following example, we applied the pixelate effect using 10 pixel blocks on the image:

![](https://res.cloudinary.com/demo/image/fetch/e_pixelate:10/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/e_pixelate:10/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You can also blur only a certain region of the image based on the position \(**`x`, `y`**\) and dimensions \(**`width`** and **`height`**\) of the region by using the **`pixelate_region`** effect. This technique can be used to pixelate only the car's license plates in the following example:

![](https://res.cloudinary.com/demo/image/fetch/c_fill,e_pixelate_region,h_80,w_200,x_170,y_260/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/c_fill,e_pixelate_region,h_80,w_200,x_170,y_260/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg

```
{% endcode-tabs-item %}
{% endcode-tabs %}

The **`pixelate_region`** effect also supports customizing the squares' size, this time we'll make them bigger:

![](https://res.cloudinary.com/demo/image/fetch/c_fill,e_pixelate_region:30,h_80,w_200,x_170,y_260/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg%20)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/c_fill,e_pixelate_region:30,h_80,w_200,x_170,y_260/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg

```
{% endcode-tabs-item %}
{% endcode-tabs %}

With the **`pixelate`** effect you can create nice looking effects, for example:

![](https://res.cloudinary.com/demo/image/fetch/a_45/e_pixelate:10/a_-45/e_trim/w_0.9,c_crop/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/a_45/e_pixelate:10/a_-45/e_trim/w_0.9,c_crop/http://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Austin_A110_Westminster_MkII_tail.jpg/550px-Austin_A110_Westminster_MkII_tail.jpg
```
{% endcode-tabs-item %}
{% endcode-tabs %}



