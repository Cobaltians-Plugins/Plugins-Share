# Share Plugin

ShareIntent plugin allows you to share file from the web or internal application data.

## How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.share.js to your web JS folder
* Add an html link to the cobalt.share.js plugin script after the cobalt link in the HEAD tag

### Sharing files from JavaScript

use the `cobalt.share` shortcut like this:

cobalt.shareItem(data, 'callback');

where data is a JSON Object like:

### Examples

If you like to share:

1. Text
var data = [{
   'type': 'text',
   'content': 'ABCDEFGHIJKLMNOPQRSTUVWXYX',
   'title': 'alphabet' // optional
}];

2. Contact
var data = [{
   'type': 'contact',
   'name': 'Bernard Pivot',
   'mobile': "0102030405",
   'email': 'Monsieur.Chatouille@example.com', // optional
   'company': 'Cobaltians', // optional
   'postal': '1 rue chausette, Lannion, etc.', // optional
   'job': 'Developer', // optional
   'detail': 'some comments', // optional
}];

3. Image
var data = [{
   'type': 'image',
   'source': 'url',
   'path': 'http://example.com/images/cat.png',
   'title': 'Cat', // optional
   'detail': "playing with a goldfish" // optional
}];

4. Others examples with different source or file type
var data = [{
   'type': 'image',
   'source': 'resource',
   'path': "mypicture.png",
   'title': 'Cat', // optional
   'detail': "playing with a goldfish" // optional
}];

var data = [{
   'type': 'image',
   'source': 'resource',
   'id': app.page.myRessourceId // to get an id, use getResources().getIdentifier("nameofthefile", "drawable", getContext().getPackageName());
   'title': 'Cat', // optional
   'detail': "playing with a goldfish" // optional
}];
var data = [{
    'type': 'document',
    'source': 'url',
    'path': "http://example.com/files/pdf-sample.pdf",
}];
var data = [{
    'type': 'video',
    'source': 'url',
    'path': "http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4",
}];
var data = [{
    'type': 'data',
    'source': 'url',
    'path': "https://example.com/master/gradlew.bat",
    'title': 'A file from example.com', // optional
    'detail': "With some details" // optional
}];

//somewhere after cobalt inited
cobalt.share({ TODO } function(result){
   //TODO 
});

Current full returned fields are :

| field | type | description |
| ----- | ---- | ----------- |
| TODO | string     | TODO |
| TODO | string     | TODO |

Sample : 

    {
        TODO : "TODO",
        TODO : TODO
    }

### Other feature

BLABLA

Here is how to blabla :

    //somewhere after cobalt inited
    cobalt.share({
        //TODO
    });


##Want more ?

If you have any ideas or improvements to propose, please feel free to do so in the issues tracker!
