###Notes

Tailwind, postcss, autoprefixer

    npm init -y
    npm install -D tailwindcss postcss autoprefixer
    create postcss.config.js for module.exports
    pull in tailwindcss npx tailwindcss init
    store the dirs in the tailwind.config.js content array
    scan all files there with "./**/*.{liquid, json}"
    import tailwind components in src/tailwind.css w/ directives
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    create stylesheet
    npx tailwind -i ./src/tailwind.css -o ./assets/tailwind.css --watch
    
Building the nav

    Remove all the theme kit stuff in layout/theme.liquid
    keep the main tag and the content_for_layout
    
JSON Templates

    You can only update the json templates in the templates folder.
    When using json templates you can delete it's liquid counterpart.
    There are 5 attributes you can use in the templates
        name - **required
        layout - by default uses the theme.liquid layout
        wrapper - wrap your template with an html tag
        sections - create your section ids and sections **required
        order - order of sections **required

    The layout folder is where you store a custom layout.

        It's important to remember you'll need a custom header
        and a place for the layout object.
    
    Specifying type in the sections attr is how to tell what section
    you're using from the sections folder.

    The order attribute requires and array containing the order of sections.

    Inside the theme editor the dropdown at the top should contain your 
    custom template under the "others" menu item.

The t filter

    This refers the en.default.json file in the locales folder
    <h1>{{ 'general.404.title' | t }}</h1>
    points to the title key in the general object in the 404 object.
