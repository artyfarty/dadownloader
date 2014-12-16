# DeviantArt Downloader

A simple python program to help you download your favourite deviations from
[DeviantArt](http://www.deviantart.com).

## Installation

## Usage

Navigate to the folder where you would like to download the deviations and execute the following command:

````bash
$ dadl <username>
````
where `<username>` is the username of the DeviantArt user whos favourites you
want to download. It is suggested you only execute `dadl` in an empty folder or a folder in which `dadl` was previously executed.

### File Descriptions

`dadl` will create a directory structure similar to the following:

````bash
working-directory/
├── cookies
├── credentials
├── <username>.json
└── <username>/
    ├── <collection-one-name>/
    │   ├── avatars/
    │   │   ├── <avatar-one-filename>
    │   │   ├── <avatar-two-filename>
    │   │
    │   ├── descriptions/
    │   │   ├── imgs/
    │   │   │   ├── <img-one-filename>
    │   │   │   ├── <img-two-filename>
    │   │   │
    │   │   ├── <description-one-name>.html
    │   │   ├── <description-one-name>.original
    │   │   ├── <description-two-name>.html
    │   │   ├── <description-two-name>.original
    │   │
    │   ├── <deviation-one-filename>
    │   ├── <deviation-two-filename>
    │
    ├── <collection-two-name>/
    │   ├── avatars/
    │   ├── descriptions/
````

- **cookies**  
  Stores cookies the last time `dadl` was used and successfully logged in to
  DeviantArt.
- **credentials**  
  Stores your username and password from the last time `dadl` was used and
  successfully logged in to DeviantArt. This means you don't have to re-enter
  your username and password every time authenticated cookies in `cookies`
  become
  invalid.
- **&lt;username&gt;.json**  
  Stores a json representation of &lt;username&gt;'s favourites.
- **&lt;username&gt;**  
  Folder in which all deviations, deviation descriptions and avatars are stored.
- **&lt;collection-xxx-name&gt;**  
  Folder in which all deviations, deviation descriptions and avatars for this
  collection are stored. Note that the first collections name is always
  `Favourites`
- **avatars**  
  Folder in which all avatars of the creators of the deviations in this
  collection are stored.
- **descriptions**  
  Folder in which all descriptions of the deviations in this collection are
  stored.
- **imgs**  
  Folder in which any images in the descriptions are stored.

## License

DeviantArt Downloader is released under the [MIT license](LICENSE.md).
