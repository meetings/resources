# Resources
This resources repository is meant for storing common cross project resources in a coder-friendly place. Also this README.md file should contain resource relevant documentation.

## Icons
All the icon files committed to this repository should be at least in png format. Before committing png files they should be minimised with the non-destructive *[image optim](https://imageoptim.com/)* freeware.

---

> Here is as list of different logo sizes that may be needed online as I could gather.
>
> We will not use all of them at once, but the list is here for reference.
> - Mikko

### List of fav, touch and tile icons for web.

Fav icon, 16 & 32px versions in one file

favicon.ico

#### iOS and older Android icons
| Size    | File        | Description                                                    |
|---------|-------------|----------------------------------------------------------------|
| 152x152 | icon152.png | For iPad with high-resolution Retina display running iOS ≥ 7   |
| 144x144 | icon144.png | For iPad with high-resolution Retina display running iOS ≤ 6   |
| 120x120 | icon120.png | For iPhone with high-resolution Retina display running iOS ≥ 7 |
| 114x114 | icon114.png | For iPhone with high-resolution Retina display running iOS ≤ 6 |
| 72x72   | icon72.png  | For first- and second-generation iPad                          |
| 57x57   | icon57.png  | For non-Retina iPhone, iPod Touch, and Android 2.1+ devices    |

#### General icons
| Size    | File        | Description                                                          |
|---------|-------------|----------------------------------------------------------------------|
| 228x228 | icon228.png | Opera Coast icon                                                     |
| 195x195 | icon195.png | Opera Speed Dial icon                                                |
| 152x152 | icon152.png | iPad retina touch icon (Change for iOS 7: up from 144x144)           |
| 144x144 | icon144.png | IE10 Metro tile for pinned site                                      |
| 128x128 | icon128.png | Chrome Web Store icon                                                |
| 120x120 | icon120.png | iPhone retina touch icon (Change for iOS 7: up from 114x114)         |
| 96x96   | icon96.png  | GoogleTV icon                                                        |
| 76x76   | icon76.png  | iPad mini i& iPad 2 touch icon (Change for iOS 7: up from 72x72)     |
| 72x72   | icon72.png  | iPad home screen icon                                                |
| 57x57   | icon57.png  | Standard iOS home screen (iPod Touch, iPhone first generation to 3G) |
| 32x32   | icon32.png  | Certain old but not too old Chrome versions mishandle ico            |


Twitter meta tags should contain only page specific content, for when user links this page in Twitter

facebook meta tags, for when user links this page to fb
200x200 minimum, 1500x1500 preferred (max 5MB), facebook.png

IE10 meta tags for win8 start screen tiles and such
Windows 8 navibutton color is needed: #ffffff

| Size    | File             | Description       |
|---------|------------------|-------------------|
| 144x144 | icon144.png      | IE10              |
| 70x70   | tile-70.png      | IE11              |
| 150x150 | tile-150.png     | IE11              |
| 310x150 | tile-310x150.png | IE11 (Wide tile!) |
| 310x310 | tile-310.png     | IE11              |

---
## Fonticons
We use [Icomoon](http://icomoon.io/) generator for creating the used icons in font formats. The CSS from icomoon ican be extended with [FontAwesome](http://fortawesome.github.io/Font-Awesome/) as it has some really nice features.

Normal HTML usage:
```html
<!-- Plain icon -->
<i class="icon icon-meetings"></i>

<!-- With text next to it -->
<i class="icon icon-add"></i><span>Add new item</span>

<!-- Inside a link -->
<a href="#add"><i class="icon icon-add"></i><span>Add new item</span></a>
```
Notice the ```<span>``` around the following text. This helps if we need to add spacing or other decorations later to links.

### Updating fonticons
1. Download and unzip the icomoon zip you received from Lotta.
2. Override icomoon styles on your project css with the style.css from the zip
3. Override icomoon fonts on your project fonts with the style.css from the zip
4. Check that your custom FontAwesome extensions did not get overridden
5. Check that old and new icons work. (A styleguide with all the different icons helps with this.)

### Extending fonticon features
If more features are wanted from [FontAwesome](http://fortawesome.github.io/Font-Awesome/examples/), they can be added to the sample css like the fixed-width font has been added in example below.

Add this to your project css:
```css
/* Font Awesome addition */
.icon{
  display: inline-block;
}
/* Fixed Width Icons */
.icon-fw {
  width: 1.2857142857em;
  text-align: center;
}
```
Then in html:
```html
<i class="icon icon-fw icon-meetings"></i>
```

Just remember to prefix with ```icon``` instead of the FontAwesome ```fa``` prefix.

---
## Fonts

Fonts in this repo should be only ones that are used in multiple projects. (iOS, Android, Desktop, etc.)

Bulletproof syntax for font embedding:
http://www.paulirish.com/2009/bulletproof-font-face-implementation-syntax/

The easiest way to add fonts is to use [Fontsquirrel webfont generator](http://www.fontsquirrel.com/tools/webfont-generator)

### MuseoSans
Here is a sample include of MuseoSans font. Notice the double definitions that are used for supporting both textual and numeric font weights.

| File prefix                  | Font weight  | Decoration |
|------------------------------|--------------|------------|
| museosans_300-webfont        | 300 / Normal | Normal     |
| museosans_300_italic-webfont | 300 / Normal | Italic     |
| museosans_500-webfont        | 500 / Bold   | Normal     |
| museosans_500_italic-webfont | 500 / Bold   | Italic     |

Notice also that not all of the formats are needed in every situation. For example iOS app most likely will not render with Internet Explorer, so eot-format is enough.

Remember always to check that the font path is correct (relative to the css file location).

```css
/* MuseoSans 300 normal */
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_300-webfont.eot');
  src: url('museosans_300-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_300-webfont.woff') format('woff'),
       url('museosans_300-webfont.ttf') format('truetype'),
       url('museosans_300-webfont.svg#webfont') format('svg');
  font-weight: 300;
  font-style: normal;
}
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_300-webfont.eot');
  src: url('museosans_300-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_300-webfont.woff') format('woff'),
       url('museosans_300-webfont.ttf') format('truetype'),
       url('museosans_300-webfont.svg#webfont') format('svg');
  font-weight: normal;
  font-style: normal;
}

/* MuseoSans 300 italic */
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_300_italic-webfont.eot');
  src: url('museosans_300_italic-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_300_italic-webfont.woff') format('woff'),
       url('museosans_300_italic-webfont.ttf') format('truetype'),
       url('museosans_300_italic-webfont.svg#webfont') format('svg');
  font-weight: 300;
  font-style: italic;
}
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_300_italic-webfont.eot');
  src: url('museosans_300_italic-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_300_italic-webfont.woff') format('woff'),
       url('museosans_300_italic-webfont.ttf') format('truetype'),
       url('museosans_300_italic-webfont.svg#webfont') format('svg');
  font-weight: normal;
  font-style: italic;
}

/* MuseoSans 500 normal */
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_500-webfont.eot');
  src: url('museosans_500-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_500-webfont.woff') format('woff'),
       url('museosans_500-webfont.ttf') format('truetype'),
       url('museosans_500-webfont.svg#webfont') format('svg');
  font-weight: 500;
  font-style: normal;
}
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_500-webfont.eot');
  src: url('museosans_500-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_500-webfont.woff') format('woff'),
       url('museosans_500-webfont.ttf') format('truetype'),
       url('museosans_500-webfont.svg#webfont') format('svg');
  font-weight: bold;
  font-style: normal;
}

/* MuseoSans 500 italic */
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_500_italic-webfont.eot');
  src: url('museosans_500_italic-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_500_italic-webfont.woff') format('woff'),
       url('museosans_500_italic-webfont.ttf') format('truetype'),
       url('museosans_500_italic-webfont.svg#webfont') format('svg');
  font-weight: 500;
  font-style: italic;
}
@font-face{
  font-family: 'Museo Sans';
  src: url('museosans_500_italic-webfont.eot');
  src: url('museosans_500_italic-webfont.eot?#iefix') format('embedded-opentype'),
       url('museosans_500_italic-webfont.woff') format('woff'),
       url('museosans_500_italic-webfont.ttf') format('truetype'),
       url('museosans_500_italic-webfont.svg#webfont') format('svg');
  font-weight: bold;
  font-style: italic;
}
```