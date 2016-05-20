# Share Plugin

ShareIntent plugin allows you to share file from the web or internal application data.

## How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.share.js to your web JS folder
* Add an html link to the cobalt.share.js plugin script after the cobalt link in the HEAD tag

### Sharing files from JavaScript

use the `cobalt.share` shortcut like this:

```javascript
cobalt.share(data: myFileDatas);
```

or with a callback:

```javascript
cobalt.share(data: myFileDatas, function(result){...});
```

where data need a JSON Object like:

```javascript
var myFileDatas = [{
'type': 'image',
'source': 'url',
'path': 'http://example.com/images/cat.png',
'title': 'Cat', // optional
'detail': "playing with a goldfish" // optional
}];
```

### Examples

If you like to share:

1.**Text**

```javascript
var myFileDatas = [{
'type': 'text',
'content': 'ABCDEFGHIJKLMNOPQRSTUVWXYX',
'title': 'alphabet'
}];
```

2.**Contact**

```javascript
var myFileDatas = [{
'type': 'contact',
'name': 'Jean Paul',
'mobile': "0102030405",
'email': 'jeanpaul@example.com', // optional
'company': 'Cobaltians', // optional
'postal': '1 City Hall SQ, RM 612, Boston, etc.', // optional
'job': 'Human Resources', // optional
'detail': 'foo', // optional
}];
```

3.**Image**

```javascript
var myFileDatas = [{
'type': 'image',
'source': 'url',
'path': 'http://example.com/images/cat.png',
'title': 'Cat', // optional
'detail': "playing with a goldfish" // optional
}];
```

4.**Share a local document**

The document must be stored in "app/src/main/assets/files/samples.pdf" (Android) or in iOS bundle

```javascript
var myFileDatas = [{
'type': 'document',
'source': 'local',
'path': 'files/sample.pdf',
}];
```

5.**Share a remote video**

```javascript
var myFileDatas = [{
'type': 'video',
'source': 'url',
'path': "http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4",
'title': 'big buck bunny', // optional
}];
```

And then:
```javascript
cobalt.share({data: myFileData});
```

### Existing fields to fill are :

| Field | Description | Examples Values | Mandatory |
| ----- | ---- | ----------- | ----------- |
| source | source from where the file comes | 'url', 'local' | YES |
| path | local/remote path of the file     | 'http://example.com/pixel.png', 'files/pixel.png' | YES |
| type | file type   | 'text', 'image', 'contact', 'document', 'audio', 'video', 'data'| YES |
| name | contact name     | 'Jean Paul' | YES |
| mobile | contact number     | '+33201050602' | YES |
| email | contact email     | 'jeanpaul@example.com' | NO |
| company | contact company     | 'Jp Corp.' | NO |
| postal | contact postal    | '1 City Hall SQ, RM 612, Boston' | NO |
| job | contact job     | 'DRH' | NO |
| title | contact title    | 'This is something' | NO |
| detail | contact detail    | 'Some comments about this' | NO |

## Want more ?

If you have any ideas or improvements to propose, please feel free to do so in the issues tracker!
