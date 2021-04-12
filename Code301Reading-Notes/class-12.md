# EJS Partials
Partials come in handy when you want to reuse the same HTML across multiple views.
* you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file and include it wherever you need it.
* In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by `<% %>` delimiters
* You use `<%- include( PARTIAL_FILE ) %>` where the partial file is relative to the template you use it in.
* creating and including partials is very straightforward with EJS.
* You don’t need to include a DOCTYPE and HTML tag in the Partials file because it would be included with them in tha HTML files that they would be called in

> Note: The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important when using the include() statement since you don’t want EJS to escape your HTML characters like `‘<’, ‘>’`, etc…