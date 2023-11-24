# TagLib Wrapper

## Enums
### Tag
The different tags that can be retrieved.
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
Get a specified tag from an audio file at the specified path.
#### Arguments {id="tag-arguments"}
* String: filepath | The path to the audio file
* Tag : tag | The tag to grab
#### Returns {id="tag-returns"}
* String of the specified field from the file.
#### Usage {id="tag-usage"}
`string artist = TagLib.GetTag("Path/To/File", TagLib.Tag.Artist);`
### GetCover
Get the album cover of the audio file at the specified path.
#### Arguments {id="cover-arguments"}
* String: filepath | The path to the audio file
#### Returns {id="cover-returns"}
* Texture2D of the file's album cover
#### Usage {id="cover-usage"}
`Texture2D cover = TagLib.GetCover("Path/To/File");`
### GetFilename
Get the filename of an audio file
#### Arguments {id="filename-arguments"}
* String: filepath | The path to the audio file
#### Returns {id="filename-returns"}
* String of the filename of the file.
#### Usage {id="filename-usage"}
`string filename = TagLib.GetFilename("Path/To/File");`