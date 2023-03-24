# Code-Refactoring-Project 

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://www.w3schools.com/html/html_computercode_elements.aspL](https://www.w3schools.com/html/html_computercode_elements.asp) | 
| CSS     | [https://www.w3schools.com/css/](https://www.w3schools.com/css/)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

## Description 

[Visit the Deployed Site](https://youtu.be/BFyeuLhjcPY)

Our first Feature Request Challenge asked that we refactor existing code for a marketing agency that followed accessibility standards and optimized their site for search engines.

Code refactoring is changing or restructuring existing code without changing the external site. This process can improve the code's readability and remove redundancies. By using semantic HTML, each part of the code can be labeled appropriately to make future inquiries and changes of the code more efficient. A change to the column to the right will be properly labeled as an aside reducing confusion about where the images will load on a given page.

A review of accessibility standards was also necessary. The use of alt attributes for all active links and images will help someone with visual impairments navigate a site more effectively. Additionally, by ensuring that the text has good contrast makes reading the site easier for everyone. 

I utilized notes from class as well as online research to review the code and enter the semantic HTML elements.  All navigation buttons and images were given alt attributes with thorough descriptions for accessibility. Color contrast between text and background was reviewed and corrected. I paid attention to the order of my changes, such as ensuring that CSS code was in the same order/structure as the HTML. I reviewed the heading attributes to ensure they were in correct and sequential order. Lastly, I provided a more descriptive title element for our marketing agency client.


## Code Refactor Example
The original HTML lacked semantic HTML elements and needed to be made more accessible.

```html
    </div>
    <div class="benefits">   
        <div class="benefit-lead">   
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="benefit-brand">  UPDATE TO SECTION
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" />
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </div>
        <div class="benefit-cost">  
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png" />
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </div>
    </div>

```

By reviewing semantic HTML elements, the nonsemantic elements were located and given the appropriate [<aside> semantic element](https://www.w3schools.com/html/html5_semantic_elements.asp) and descriptive alt attributes for the visually impaired.

```html
 <aside class="benefits"> <!--Renamed aside-->
        <div class="aside-links" id="benefit-lead">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" alt=”picture of a funnel with items going in and resulting in money”/>
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="aside-links" id=benefit-brand">
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" alt="picture of a person experiencing a lightbulb moment" />
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </div>
        <div class="aside-links" id=benefit-cost">
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png" alt=”picture of gears and money symbols” />
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </div>
    </aside>
```
The CSS was also updated to correct redundancy with the creation of new classes. The above section of HTML now has the following CSS (https://www.w3schools.com/cssref/sel_class.php):

.aside-links {
    margin-bottom: 32px;
    color: #ffffff;
}
.aside-links h3 {
    margin-bottom: 10px;
    text-align: center;
}
.aside-links img {
    display: block;
    margin: 10px auto;
    max-width: 150px;


To provide contrast for the visually impaired, the CSS was also updated in the header section to allow for access to the play on words that is the Horiseon name: 

```css
.header h1 .seo {
    color: darkgray;
}
```

## Learning Points 

This was a great learning experience for me. I was able to see how changes in the HTML and the CSS can have a drastic effect on the site. This has improved my troubleshooting skills as well as reminding me to slow down and check my work methodically.

I utilized my skills with researching and implementing accessibility standards such as alt attributes; reviewing code in general; utilizing semantic HTML for a more clear structure; and using CSS .class selectors with id's to consolidate and reduce redundancy in the CSS. 


## Author Info

```md
TAMARA "T" DUSENBURY
    I am excited to take my knowledge of various industries into the virtual realm.

* [Portfolio](https://youtu.be/bHX54GCrDB4)
* [LinkedIn](https://www.linkedin.com/in/tamara-dusenbury-02ab8591/)
* [Github](https://github.com/tdusenbury)
```

## Credits

Thank you to @Zeroclucks on Discord for your patience and thoughtful explanations of concepts.


## License

MIT License

Copyright (c) 2023 tdusenbury

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.