# Share Plugin

Share plugin allows you to share content or files from the web or internal application data to other applications.

## How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.share.js to your web JS folder
* Add an html link to the cobalt.share.js plugin script after the cobalt link in the HEAD tag

### Sharing files from JavaScript

use the `cobalt.share` shortcut like this:

```javascript
cobalt.share(myFileDatas);
```

where data need a JSON Object like:

```javascript
var myContent = {
'type': 'image',
'source': 'url',
'path': 'http://example.com/images/cat.png',
'title': 'Cat', // optional
'detail': "playing with a goldfish" // optional
};
```

### Fields description :

| Field | Description | Examples Values | Mandatory |
| ----- | ---- | ----------- | ----------- |
| source | source from where the file comes | 'url', 'local' | YES |
| path | local/remote path of the file     | 'http://example.com/pixel.png', 'files/pixel.png' | YES |
| type | file type   | 'text', 'image', 'contact', 'document', 'audio', 'video', 'data'| YES |
| name | contact name     | 'Jean Paul' | NO |
| mobile | contact number     | '+33201050602' | NO |
| email | contact email     | 'jeanpaul@example.com' | NO |
| company | contact company     | 'Jp Corp.' | NO |
| postal | contact postal    | '1 City Hall SQ, RM 612, Boston' | NO |
| job | contact job     | 'DRH' | NO |
| title | contact title    | 'This is something' | NO |
| detail | contact detail    | 'Some comments about this' | NO |


### Copy/paste examples

1.**Share some text**

```javascript
cobalt.share({
'type': 'text',
'content': 'ABCDEFGHIJKLMNOPQRSTUVWXYZ',
'title': 'alphabet'
});
```

2.**Share a contact**

```javascript
cobalt.share({
'type': 'contact',
'name': 'Jean Paul',
'mobile': "0102030405",
'email': 'jeanpaul@example.com', // optional
'company': 'Cobaltians', // optional
'postal': '1 City Hall SQ, RM 612, Boston, etc.', // optional
'job': 'Human Resources', // optional
'detail': 'foo', // optional
});
```

3.**Share an image**

```javascript
cobalt.share({
'type': 'image',
'source': 'url',
'path': 'http://example.com/images/cat.png',
'title': 'Cat', // optional
'detail': "playing with a goldfish" // optional
});
```

4.**Share a local document**

The document path starts at "app/src/main/assets/" on Android or in bundle root folder on iOS.

```javascript
cobalt.share({
'type': 'document',
'source': 'local',
'path': 'files/sample.pdf',
});
```

5.**Share a remote video**

```javascript
cobalt.share({
'type': 'video',
'source': 'url',
'path': "http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4",
'title': 'big buck bunny', // optional
});
```
