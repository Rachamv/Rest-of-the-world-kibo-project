# Recreate the Rest of World Homepage

This project will stretch your Web Design skills. You’ll work to recreate the awesome landing page from [restofworld.org](https://web.archive.org/web/20220428094707/http://restofworld.org/).

The landing page is more complicated than the practice sites you've been working with. It's a real site, with tons of links, images, and content.

## About Rest of World

> Rest of World is an international nonprofit journalism organization. We document what happens when technology, culture and the human experience collide, in places that are typically overlooked and underestimated. We believe the story about technology is as big as the world that’s using it, and that everyone — from those building technology to those using it — can benefit from a broader global perspective.
> 
> _https://restofworld.org/about/_

Rest of World writes great articles about what's happening around the world. Important for us, they also do a great job presenting their stories beautifully. The design of the site is worth mimicking; so here we are.

They've graciously allowed us to use their landing page for this project (thank you!)

## Your Task

If you run the code as-is, you will see a bunch of unstyled elements. It looks a mess.

You will add styles piece by piece in `style.css`, and the page will gradually come to life. Since we have a design for the page already, you'll be applying the specific CSS styles to the right elements to achieve the exact result of the page.

## Instructions

In `index.html` is a trimmed-down version of the homepage for restofworld.org. Your goal is to add styles to `styles.css` to make your version of the site look like the real thing.

We'll provide you with pointers on where to start and what steps to follow in what order, but we won't tell you exactly how to do it. You may have to use the DevTools to look for the right elements and the right values on https://restofworld.org/ itself to figure out some of the values.

The recommended order to proceed is to first style the text, then add the colors, and then to lay out the page and position the elements.

## Starter code

We cut a lot of pieces out from the restofworld homepage. Still, the code in index.html is almost 400 lines long!

Navigating a big file like this and understanding how it fits together takes a couple tricks.

* Look at the original site
* Think in sections
* Click the > to fold in your code editor
* Use the inspector
* Read the classnames

Click to see this video: [How to Navigate the Starter Code](https://www.loom.com/share/ee8ad2b07e4d49b393588b86edcbdc41)

### Text Styling

First, focus on styling the text. On the original website, there are three font families used, in a few different colors and sizes.

The font stacks that restofworld.org uses:

* `Moderat, sans-serif;` (h1, bylines)
* `"GT Sectra", serif;` (body and descriptions)
* `"Input Mono",SFMono-Regular,"Roboto Mono","Lucida Console",Monaco,Courier,monospace;` (banners, links)

We don't have those exact fonts (they are paid, professional fonts), so here's what you'll use instead:

* `sans-serif` (h1, bylines)
* `serif` (body and descriptions)
* `SFMono-Regular,"Roboto Mono","Lucida Console",Monaco,Courier,monospace` (banners and links)

The only font that has a `<link>` is Roboto Mono. The headers and body will use the default sans-serif and serif fonts.

* Apply the right fonts to the right elements
* Inspect the restofworld homepage to find the right font sizes, then use those font sizes
* Check how links and lists are styled on Rest of World, and then apply the appropriate `text-decoration` and `list-item-style` to your version

### Color Palette

Rest of World uses a different color palette for different users. If you go to https://restofworld.org/labs/, you can find your `_palette` value. If you delete the value and refresh the page, you'll get a new random palette from their collection of palettes.

Since we want to pick a single palette, we're going to use palette-50: 

Here's the palette, using the CSS variables trick we learned for colors:

```css
html {
    --bright: #D231A0;
    --accent: #E3FFF7;
    --body: #F3FFFC;
    /* these are for dark mode - the dark mode accent and body colors */
    --dma: #E3FFF7;
    --dmb: #D231A0;
  }
```

You'll have to decide which elements to select to apply these colors. When you do, you can use `var(--bright)` or `var(--accent)` instead of typing out `#D231A0` or `#E3FFF7`.

The other colors that restofworld.org uses are white, black, and gray:

```css
html {
    --white: white;
    --black: black;
    --charcoal: #111111;
    --basalt: #262626;
    --ash: #555555;
    --pumice: #CACACA;
}
```

* Look on the Rest of World page to see where the different colors are applied, and which elements get which colors.
* Apply the colors to the elements. Don't forget the background colors!
* Elements will have different colors depending on where they are on the page. Be sure to use the right selectors to style those elements.

### Layout, Spacing, and positioning

Now that the text and colors are applied, add the space and layout to the page so that it looks like the original. Start with the spacing and borders. Check different elements in the original page to see their margin, padding, and borders. You will also apply the colors to the borders.

Once the boxes are the right sizes, it's time to lay them out on the page. To get the styles to look like the original homepage, you'll use lots of flexboxes with different properties. 

Take the sections one by one. Figure out what elements are inside each box, and think about what flexbox properties would get the elements to be positioned and spaced that way.

* Remember: you can use the DevTools to see how RestOfWorld did it.
* Also: there are different ways to achieve the same style!

### Note

Layout takes a long time. This is where you'll likely spend a lot of time on the project. Try to get things as good as you can, but don't worry if it's not all finished.

## Rest of World: Content Note

So that it's clear that Kibo student projects aren't the _actual_ Rest of World landing page, we're doing a couple things:

- including a disclaimer on the page that it's not really Rest of World, and where to go to find the actual landing page
- adding a tag `<meta name="robots" content="noindex">` to tell search engines not to index this page

We're also not hotlinking to the (beautiful) restofworld.org fonts, since that would be impolite (and the fonts aren't licensed for that!)

We're really grateful to restofworld for being a willing example. Thank you!