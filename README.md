Since this plugin builds on top of [jQueryUI's autocomplete](http://jqueryui.com/demos/autocomplete/) widget,
pretty much all of autocomplete's options/events are applies to it as well,
with the exception of `source`.

Google Suggest for jQuery itself has 2 options: service and secure.

Demo:
=====
[Simple demo](http://googlesuggest-jquery.googlecode.com/svn/trunk/demo.html)

Options:
========

| option  | type    | default | note
|---------|---------|---------|-----
| service | string  | ""      | It's used to specify what Google service to query against. It can be "web", "youtube", "products", "books", "news", "images", "recipes", or "" (empty string). By default it queries Google's web auto suggestions (the "web" option).
| secure  | boolean | false   | It's used to specify whether to use HTTPS or not. By default it doesn't use secure connection.

Example: 
========

    //uses default settings
    $("#selector").googleSuggest(); 

    //uses HTTPS
    $("#selector").googleSuggest({secure: true});

    //queries Google Products
    $("#selector").googleSuggest({service: "products"});

    //alerts the selected value
    $("#selector").googleSuggestion({select: function(event, ui){ alert(ui.item.value); }});

You can access the autocomplete settings directly.

Example:
--------

    $("selector").autocomplete("option", "disable");
