# Overlay an image over detected faces

## Overlay an image over detected faces

Overlay another image of your choice on top of the faces which are automatically detected in your image. This is done by setting the `overlay` parameter \(`l` in URLs\) to the overlay image's public ID while setting the `gravity` parameter to `faces` \(`g_faces` in URLs\).

Cloudinary automatically detects and searches for faces within an image. There are various Cloudinary tools that you can use with the detected faces' coordinates, such as [Faces-based cropping](https://cloudinary.com/cookbook/face_detection_based_image_cropping), [Faces-based blurring and pixelating](https://cloudinary.com/cookbook/blur_or_pixelate_faces) and more.

Here's an example of an image automatically fetched from Wikimedia Commons:

![](https://res.cloudinary.com/demo/image/fetch/http://upload.wikimedia.org/wikipedia/commons/4/45/Spain_national_football_team_Euro_2012_final.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text


```
{% endcode-tabs-item %}
{% endcode-tabs %}

Here's an example of taking an image with the **`badge`** public ID, resizing it to 30 pixels-wide and overlaying it on top of all detected faces in the image:

![](https://res.cloudinary.com/demo/image/fetch/l_badge,g_faces,w_30/http://upload.wikimedia.org/wikipedia/commons/4/45/Spain_national_football_team_Euro_2012_final.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text
https://res.cloudinary.com/demo/image/fetch/l_badge,g_faces,w_30/http://upload.wikimedia.org/wikipedia/commons/4/45/Spain_national_football_team_Euro_2012_final.jpg
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Instead of specifying a fixed value for the `badge` image's width, you can tell Cloudinary to resize the badge's width relative to the main image. This is done by setting the `width` parameter to a decimal value defining the size and setting the **`flags`** parameter to **`relative`** \(**`fl_relative`** in URLs\). For example, positioning multiple badges while resizing them to 10% of the width of the containing image:

![](https://res.cloudinary.com/demo/image/fetch/l_badge,g_faces,w_0.1,fl_relative/http://upload.wikimedia.org/wikipedia/commons/4/45/Spain_national_football_team_Euro_2012_final.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text


```
{% endcode-tabs-item %}
{% endcode-tabs %}

Cloudinary can even take this one step further with the option of automatically positioning the badges and resizing them to cover 100% of the width & height of each detected face. This is done by setting the **`flags`** parameter to **`region_relative`**, **`fl_region_relative`** in URLs\). By doing so, all overlays will be stretched to cover the whole face:

![](https://res.cloudinary.com/demo/image/fetch/l_badge,g_faces,w_1.0,h_1.0,fl_region_relative/http://upload.wikimedia.org/wikipedia/commons/4/45/Spain_national_football_team_Euro_2012_final.jpg)

{% code-tabs %}
{% code-tabs-item title="URL" %}
```text


```
{% endcode-tabs-item %}
{% endcode-tabs %}



