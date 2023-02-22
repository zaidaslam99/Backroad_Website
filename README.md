
# Backroads Website

This website template can be used for the purpose of a website that offers travel services.

## 🛠 Frontend 

* JavaScript 
* HTML 
* CSS


## Screenshots

![hero_shot](https://github.com/zaidaslam99/Backroad_Website/blob/main/project_screenshot/hero_shot.png?raw=true)

![about_shot](https://github.com/zaidaslam99/Backroad_Website/blob/main/project_screenshot/about_shot.png?raw=true)

![services_shot](https://github.com/zaidaslam99/Backroad_Website/blob/main/project_screenshot/services_shot.png?raw=true)

![contact_gallery_shot](https://github.com/zaidaslam99/Backroad_Website/blob/main/project_screenshot/contact_gallery_shot.png?raw=true)

![footer_shot](https://github.com/zaidaslam99/Backroad_Website/blob/main/project_screenshot/footer_shot.png?raw=true)
## Lessons Learned

The one thing that was done differently on this website is that we linked different sections of the page to their respective tab in the header section. This design concept makes it easier for the user to navigate through the page, and not have to scroll all the way down to get to the section that they want to see.

### HTML

Notice when it comes to the `<a>` tag in our href= what we did was we passed in #id. The benefit of doing this is when we use a `<section>` or `<article>` we can then pass in the same id attribute, and those tags are going to be linked to that specific spot. 

```html
<ul class="nav-links" id="nav-links">
    <li>
    <!-- single link -->
    <a href="#home" class="scroll-link nav-link">
        home
    </a>
    </li>
    <!-- end of single link -->
    <!-- single link -->
    <li>

    <a href="#about" class=" scroll-link nav-link">
        about
    </a>
    </li>
    <!-- end of single link -->
    <!-- single link -->
    <li>

    <a href="#services" class="nav-link scroll-link">
        services
    </a>
    </li>
    <!-- end of single link -->
    <!-- single link -->
    <li>


    <a href="#featured" class="nav-link scroll-link">
        featured
    </a>
    </li>
    <!-- end of single link -->
    <!-- single link -->
    <li>

    <a href="#gallery" class="nav-link scroll-link">
        gallery
    </a>
    </li>
    <!-- end of single link -->
</ul>
```
When it comes to the about section (down below) notice the id="about" this correlates to the logic that we mentioned above. As far as section design, we designed it in two parts, the first being the title and the second being a section with the picture and info. The important thing to understand here is these individual blocks are styled using CSS. What CSS allows us to do is style the title to be centered and the image to the left and the text to right. Doing this allows the page a good flow, it makes it easier for the user to read.

```html
<!-- about section -->
<section class="section" id="about">
    <!-- title  -->
    <div class="section-title">
    <h2>about <span>us</span></h2>
    </div>
    <!-- end of title  -->
    <!-- about-center -->
    <div class="section-center about-center">
    <!-- about img wrapper-->
    <div class="about-img">
        <img
        src="./images/about.jpeg"
        class="about-photo"
        alt="awesome beach"
        />
    </div>
    <!-- about info -->
    <article class="about-info">
        <h3>explore the difference</h3>
        <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur
        quisquam harum nam cumque temporibus explicabo dolorum sapiente odio
        unde dolor?
        </p>
        <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur
        quisquam harum nam cumque temporibus explicabo dolorum sapiente odio
        unde dolor?
        </p>
        <a href="#" class="btn">read more</a>
    </article>
    </div>
</section>
```
### CSS

In this part, we are going to be talking about the about section in more depth when it comes to CSS. 

```css
/*
=============== 
About
===============
*/
/* section added to globals */
/* title added to globals */
/* section center added to globals */
.about-img,
.about-info {
  margin-bottom: 2rem;
}

@media screen and (min-width: 992px) {
  .about-center {
    /* flex parent */
    display: flex;
    justify-content: space-between;
  }
  .about-img,
  .about-info {
    /* children */
    flex: 0 0 calc(50% - 2rem);
    align-self: center;
    margin-bottom: 0;
  }
}
@media screen and (min-width: 1170px) {
  .about-img::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    border: 0.5rem solid var(--clr-primary-5);
    box-sizing: border-box;
    top: -1.5rem;
    left: -1.5rem;
  }

  .about-img {
    position: relative;
  }
  .about-photo {
    position: relative;
  }
}
```
As you can see when it comes to styling the about section we have two media queries that are being used here. An important point to understand here is that we need to style the about section width to different pixel levels. This is a very simple point to understand, however, it makes all the difference; by doing this we impact the user experience to be smooth and proficient.  

