# animated-scroll-effect
Animated images are more engaging to site visitors than static images. In this tutorial, [Solodev](https://www.solodev.com/) will show you how to add an animated scroll effect to your website's images using [Animate.css](https://daneden.github.io/animate.css/) and the [Viewport checker](https://github.com/dirkgroenen/jQuery-viewport-checker) jQuery plugin. 

## Tutorial

For detailed instructions, view Solodev's [Adding an Animated Scroll Effect to your Images](https://www.solodev.com/blog/web-design/adding-an-animated-scroll-effect-to-your-images.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/nybm4pa7/).

## HTML

Within this tutorial, a specific image can be given the animated scroll effect by giving it the calss "featuredImage". Additionally, each image is initially given the "hiddenImg" class so that it is not visible upon immediate page load.

```
<section>
  <div class="row">
    <div class="col-md-8 col-md-push-4 text-center">
      <div class="featuredImage hiddenImg">
        <i class="fa fa-users"></i>
      </div>
    </div>
    <div class="col-md-4 col-md-pull-8 productFeature">
      <h2>Marketing</h2>
      <p>WebCorpCo is all about making sure your marketing stack is in alignment with your company as well as the customers you serve. There is no 'one size fits all' approach to marketing. Every business is unique, customers are unique, and your marketing should be as well.</p>
    </div>
  </div>
 </section>
```
## CSS

All required CSS is in animated-scroll-effect.css

## jQuery

The following jQuery will initialize the effect, finding each "featuredImage" class and appending the necessary animation classes.
```
jQuery(document).ready(function() {
	jQuery('.featuredImage').addClass("hiddenImg").viewportChecker({
	    classToAdd: 'visibleImg animated fadeInUp', // Class to add to the elements when they are visible
	    offset: 100    
	   });   
});            
```

## External Includes

This tutorial contains the following third party resources.
```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.6.3/css/font-awesome.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jQuery-viewport-checker/1.8.7/jquery.viewportchecker.min.js"></script>
```