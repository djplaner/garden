## How to 

Install Jekyll (once off)
- Following [Jekyll on Ubuntu instructions](https://jekyllrb.com/docs/installation/ubuntu/)

Run the site locally for testing

- Open a terminal in the garden repo and run `bundle exec jekyll serve`
- Open a browser to [http://localhost:4000/](http://localhost:4000/)

## Related example sites


- [Lou's Gardening and Landscaping Services](https://www.facebook.com/people/Lous-Gardening-and-Landscaping-Services/100086364647648/) - Facebook profile

    - Uses a logo embedded design for before and after images.
    - Specially adds _(chemical spray)_ to his description of "weed control"
    - Services within 20Km of Regency downs (Near Plainlands)

- [Clare James - Beautiful Gardens by Design](https://clarejames.com.au/)
- [Home - Garden Services](https://www.gardenservicesbrisbane.com.au/) 
- [Home - Signature Garden Services](https://signaturegardenservices.com.au/)
- [Services | All Seasons Garden Management | Queensland](https://www.asgm.com.au/services)
- [Queensland Gardening Services - Nerang QLD](https://www.serviceseeking.com.au/profile/91322-queensland-gardening-services)
- [Gardening & Maintenance Brisbane](https://queenslandhorticulture.com.au/our-services/garden-maintenance/)
- [Gardening Services Brisbane - Lawns, Weeds, Hedges & Clean Ups](https://www.greenteambrisbane.com.au/)



## Responsive images


| Tag | size | w | Description |
| --- | ----- | ----------- |
| xl | > 1200px | 1200w | Extra large desktop |
| lg | 992px - 1200px | 900w | Large desktop |
| md | 600 | 600w | Tablet |
| sm | 300 | 300w | Mobile |

Rainbow

| filename | w | 
| --- | --- |
| rainbow-hero.jpg | 1200 |
| rainbow-hero-lg.jpg | 900 |
| rainbow-hero-md.jpg | 600 |
| rainbow-hero-sm.jpg | 300 |



```html

<img 
  src="/images/{{ page.hero_image }}"
  srcset="images/{{ page.hero_image }}-sm.jpg 300w,
    images/{{ page.hero_image }}-md.jpg 900w,
    images/{{ page.hero_image }}-lg.jpg 900w,
    images/{{ page.hero_image }}-xl.jpg 1200w"
  sizes="(max-width: 640px) 100vw,
    (max-width: 960px) 80vw,
    60vw" 
  alt="{{ page.hero_alt }}">

``` 

## How to

### Collections pages - background image

Collections pages are the second level pages that contain a collection of items. For example, the _Gardening_ page contains a collection of gardening services. The visual design of these pages is to have

- an intro section with a heading and introductory text
- followed by a list of items in the collection 
- underneath all of this is a background image

    The background image is optional. If not specified the page will default to a plain background.

For the image to work you need to 

- add a _large_ and _small_ version of the image into the `images` folder (at a point of your choosing) both saved as `.jpg` files
- add the full path to the image (minus the `.jpg` extension) into the front matter of the relevant collection's markdown page

For example, 

- Gardening uses the mowing-bird image that can be found in [/images/gardening/mowing-bird.jpg (the large version)](/images/gardening/mowing-bird.jpg) and [/images/gardening/mowing-bird-sm.jpg (the small version)](/images/gardening/mowing-bird-sm.jpg)
- In the front matter of the `gardening.md` file you would add `background_image: "/images/gardening/mowing-bird"`

## To do

General design

- [x] check the size of the content images
- [x] check the meta data for images

- [ ] 1st level image re-design to be background

- [ ] is there a better design for content images (including a caption)

- [ ] "scrolling" page design

    2nd level pages, rather than a background banner image allow for the content to scroll over it.

    - [ ] make this change to all the 2nd level pages

- [ ] Should/can 3rd level pages have background images? or images placed somewhere else on the page

    Play around with the mowing bird photo placed into the content to break it up, rather than as a background

- [ ] 3rd level header design

    - [ ] Possible to include the name of the collection into the header/navigation for the items in the collection?

- [ ] Decide on whether or not the business name should be used in content, rather than "we"

- [ ] Make all the "contact us" (e.g. gardening services) into links to the contact page

- [ ] Develop an internal links style for longer pages (perhaps programatically through Jekyll)

    - [ ] About
    - [ ] Project pages

- [ ] Consider developing a table style


Home Page

- [x] "View all Design" add "services"
- [x] change headings for gardening and design to add services

Gardening 

- [ ] Mowing 

    - [x] Ensure the numbered list is a numbered list
    - [x] add in photo
        - [ ] Is this the best photo (format wise) for this? Duplicate of gardening

- [ ] Weeding

    - [ ] More content for the description **sandy**
    - [ ] Add the arrows back into the next/prev (probably due to the absence of font awesome)
        Need to look for a low weight way of adding in those icons

- [x] Tree care

    Remove mention of the business name

- [ ] Holiday care

    Add in a design for "note"

Design

- [ ] Not all services content written

- [x] Approach 

    - [x] Typo "WOrking closely with **your**"

- [ ] Process

    - [ ] write intro 
    - [ ] Need to remove the references to other sites (and stealing their content)

- [ ] Options

    - [ ] Does this get rolled into "approach"

- [ ] Example styles 

    - [ ] Should this be earlier?

Projects 

- [ ] Duck Meadows 

    - [x] Accept the suggestion
    - [x] the before image is missing
    - [x] remove the "refs" at the bottom of the page??

- [ ] Narelle's 

    - [x] re-write the intro
    - [x] superscript with m^2
    - [ ] get images from Sandy

About 

    - [x] rewrite - remove business name
    - [x] add links to web pages
    - [x] not so much "full and"
    - [ ] Move "locations and services" to other places? Perhaps implement as an include

        - Contact 
        - Design and gardening services (perhaps these each need to provide some detail)

Contact

- [ ] update page design
- [x] Remove "site test" section

