# Multipage hugo website

**Hugo version**: 0.151

This website is created for a renewable energy distribution company, has multiple pages along with blog facility enabled. The entire site is organisied in such production grade manner that any non-technical user can easily update the content of any sections from the its corresponding data file or site config for global resources (like, nav, footer,cta etc.).

It follows **Hybrid content management** model to structure the website in a way where reusable content or properties will be stored in data files and translations will be place inside i18n folder of the corresponding language It has multilingual config enabled such that anyone can add more languages and its relevant content for the site.

Additionally, this project has several high-level components like image and many others those can be reused across the entire site.

## Components

In this project, there are four types of component can be found,

- layout
- ui
- helpers
- sectionBlocks

### Layout

components those are used in every page, I put them in inside baseof.html file therefore, they render in each page without code dupliocation. Apart from the common components, `global-cta.html` is an extraction of `cta` component from `helper`, that is kind of compound component

### UI

compoents like forms, buttons are placed here

### Helpers

this is one of the most important folder in the entire project from the perspective of design organization, all components are explained below:

#### cta

since the design has many cta, I created one single component that has been repurposed in several parts of the site with different params

**@params**: **isVertical** determines direction of the cta content flow

**@params**: **withBackgroundColor** enables a predetermined bacground color for the cta else there will be none

**@params**: **heading** adds heading content

**@params**: **link** adds custom link component, it takes link specific params as an object or array or objects

**@params**: **images** is array of image paths to form an image grid

#### image

image component takes path/ src of any image stored in assets folder and returns an image in webp if the given path is not a svg

**@params**: **src** of any image of format (jpeg, png, jpg), images must be stored in assets folder

**@params**: **alt** is needed better seo performace, by default it is set to "Image"

**@params**: **height** of the image, default 600

**@params**: **width** of the image, default 800

**@params**: **classnames** of tailwind or custom gives flexibilty to customize styling of any image

#### section-renderer

this component renders a component based on the given section name

**@params**: **sections** are names of sections needed in a specific page mentioned in frontmatter
