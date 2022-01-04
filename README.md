# Squarespace Upsell Plugin

A small bit of custom code, made specially for NYC Crit Club, that allows you to pop up a page when a user adds to cart. You can also block the upsell from appearing on certain products.  

### Requirements
- Squarespace 7.0
- Use with Product Pages

### Demo and Installation Video

HERE: https://youtu.be/CCtkLkIMuto


![video](https://img.youtube.com/vi/CCtkLkIMuto/0.jpg)

### Installing

- Go to a product page
- Hover over a products block
- Settings > Advanced > Page Header Code Injection 
- Paste the following code
https://raw.githubusercontent.com/sticknor/SquareSpaceUpsellPlugin/main/plugin.html

### Changing Pop Up Page (see video)
- In the plugin code, change line 95 to the handle of the page you would like to pop up. Make sure to include `#content` after the handle. E.g.
```
CHANGE
$('#upsell-content').load('/membership-upsell #content');
TO
$('#upsell-content').load('/new-upsell-page #content');
```

### Blocking Upsell (see video)

If you want to block an upsell from a particular product, edit the product. In additional info, add a code block with this content:
```
<div id="block-upsell"></div>
```

### Limitations

The pop up page is limited in the features that work well when 'popped-up'
- The product-embed is hit or miss, so it is better to include a link to the product page. 
- The image blocks are hit or miss, so you want to embed images in the code blocks. 
Any images in the page that you want to pop up should be defined in code blocks. 
The following sample code makes a 3x2 grid of images, with links.
```
<div style="display:flex;flex-wrap:wrap;width:100%;">
    <a href="https://sunyou.us/index.html" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689156422-T3P368T3HZLR9Z2IKLM2/Sun_You_web.jpg?format=500w" /></a>
    <a href="http://www.didierwilliam.com/" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689154904-I92Y9WHH7YU5BGHB1QQZ/Didier_William_web.jpg?format=500w" /></a>
    <a href="https://daniellejmckinney.com/" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689154492-EKE4EKSPBMUXYKU8JQEN/Danielle_Mckinney_web.jpg?format=500w" /></a>
    <a href="http://dominiquefung.com/" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689155158-BCMIR684N3B2HUQZ6X44/Dominique_Fung_web.jpg?format=500w" /></a>
    <a href="https://www.kourpour.com/" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689155993-U6AQIAS8ETAFX0Y4946O/Kour_Pour_web.jpg?format=500w" /></a>
    <a href="https://gina-beavers-6csm.squarespace.com/" target="_blank" style="padding:10px;flex:1;min-width:150px;flex-basis:28%;"><img style="width:100%;" src="https://images.squarespace-cdn.com/content/v1/5aabd69185ede1fd2a51ddde/1639689155707-881LR1AVDS5ZOQ4UV6U5/Gina_Beavers_web.jpg?format=500w" /></a>
</div>
```

### Questions?

Reach out to Sam Ticknor, the creator of this plugin.
