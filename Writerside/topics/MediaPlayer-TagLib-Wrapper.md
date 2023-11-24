# TagLib Wrapper
A wrapper class for TagLib

## Enums
### Tag
The different tags that can be retrieved.
#### Enum Values
* Title
* Artist
* Album
* AlbumArtist
* Genre
* Year
* Track
* Disc
* Composer
* Conductor

## Methods
### GetTag
Get a specified [tag](#tag) from an audio file at the specified path.
#### Arguments {id="tag-arguments"}
* `String: filepath | The path to the audio file`
* `Tag : tag | The tag to grab`
#### Returns {id="tag-returns"}
* String of the specified field from the file.
#### Usage {id="tag-usage"}
`string artist = TagLib.GetTag("Path/To/File", TagLib.Tag.Artist);`

### GetCover
Get the album cover of the audio file at the specified path.
#### Arguments {id="cover-arguments"}
* `String: filepath | The path to the audio file`
#### Returns {id="cover-returns"}
* Texture2D of the file's album cover
#### Usage {id="cover-usage"}
`Texture2D cover = TagLib.GetCover("Path/To/File");`
### GetFilename
Get the filename of an audio file
#### Arguments {id="filename-arguments"}
* `String: filepath | The path to the audio file`
#### Returns {id="filename-returns"}
* String of the filename of the file.
#### Usage {id="filename-usage"}
`string filename = TagLib.GetFilename("Path/To/File");`

### Usage Example
An example on how to use it.

    using UnityEngine;
    using MediaPlayer;
    using TMPro;

    public class Thingy : MonoBehaviour
    {
        public TextMeshPro artistText;
        public TextMeshPro trackText;
        public MeshRenderer mesh;

        public void Start()
        {
            DoThing("C:/Users/joe/Pick It Up.mp3");
        }

        public void DoThing(string filepath)
        {
            var track = TagLib.GetTag(filepath, TagLib.Tag.Track);
            var artist = TagLib.GetTag(filepath, TagLib.Tag.Artist);
            var cover = TagLib.GetCover(filepath);
            trackText.text = track;
            artistText.text = artist;
            mesh.material.mainTexture = cover;
        }
    }