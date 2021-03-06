This is GitBook plugin created for you to separate the page into sections, and add buttons to allow readers to control the visibility of each section.

## Example

You can see it at work here: [Click here](http://ymcatar.gitbooks.io/gitbook-test/content/testing_sectionx.html)

## Changelog

**2.0.3:**: Change default collapse behaviour item

## How to use section?

### Defining new section

You can define a new section with the use of tag:

```
<!--sec data-title="Introduction" data-id="section0" data-show=true ces-->

Insert markdown content here (you should start with h3 if you use heading).

<!--endsec-->
```

A section will take three arguments, listed as follows:

* **data-title:** the title of the section, it will appear as the title of the bootstrap panel (with size of h2).
	* Please note that you cannot use the character ```"``` in the title, please use ```&quot;``` instead.
* **data-id:** the id of the section, it is useful for button control (discussed in next section).
* **data-show:** a boolean value denoting by default, whether or not the panel content will be visible.
	* **true:** the panel content is visible to user by default, the panel title will be clickable.
	* **false:** the panel content is hidden to user by default, the panel title is not clickable and can only be viewed by adding a custom button (discussed in next section).
* **data-nopdf:** a boolean value denoting whether or not the section will be hidden in pdf exports.
	* **true**: the panel will not be shown in .pdf or .epub.

### Using a button to control section visibility

By adding inline HTML in the GitBook, the following code can add a button to allow you to view or hide other sections. Here are the explanation of each tags:

```
<button class="section" target="section1" show="Show next section" hide="Hide next section"></button>
```

* **class:** the button has to belong to the class "section".
* **target:** when pressed, the section with the id of target will be toggled.
* **show:** the text on the button when the target section is hidden.
* **hide:** the text on the button when the target section is visible.

Note that you can leave 'show' and 'hide' undefined, in this case, an up-arrow or down-arrow will be displayed instead. The button will not be outputed if exported to .pdf or other formats.
