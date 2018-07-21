# Create your own Duotone Filter

A cool new design trend popularized by Spotify is Duotone imagery.  There’s a good post on the Shopify blog covering this and some other trends so you can read that there if curious ([4 Trendy Visual Design Trends - Shopify Blog](https://www.shopify.com/partners/blog/4-trendy-visual-design-techniques)).  In the spirit of Cloudinary Cookbooks, we’re going to get right down to business.

Here's the original image we’re going to work off:
![Original](https://res.cloudinary.com/demo/image/upload/q_auto,f_auto/18882410261_e4f9d25780_b_lked9y.jpg "thumb: w_400")

We need to do two things here, make it grayscale, then apply the duotone using our “tint” effect.
![Duotone Red](https://res.cloudinary.com/demo/image/upload/q_auto,f_auto/e_grayscale/e_tint:50:red/18882410261_e4f9d25780_b_lked9y.jpg "thumb: w_400")

You can adjust the color name, use a hex value, change the strength of tinting by changing that “50” number (higher number is stronger), etc., to achieve the desired effect.

You can also specify two different colors, here a blue and a yellow in hex:

![Blue/Yellow](https://res.cloudinary.com/demo/image/upload/q_auto,f_auto/e_grayscale/e_tint:100:0000ff:0p:ffff00:100p/18882410261_e4f9d25780_b_lked9y.jpg "thumb: w_400")

Changing grayscale to black and white creates this effect:

![Duotone Blue and Yellow - blackwhite, removing the implicit black and white](https://res.cloudinary.com/demo/image/upload/q_auto,f_auto/e_blackwhite/e_tint:100:0000ff:0p:ffff00:100p/18882410261_e4f9d25780_b_lked9y.jpg "thumb: w_400, skip:true")

As is typical with Cloudinary, there’s more than one way to skin a cat.  Try to come up with a better Duotone transformation and post it in the comments!

Effects documentation to help you in your endeavor:  [Cloudinary Effects Cheatsheet](https://cloudinary.com/documentation/image_transformation_reference#effect_parameter)
