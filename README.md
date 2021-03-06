Artist Rooms
============

### Why

[It all started with an object](https://github.com/jueyang/artist-rooms/blob/gh-pages/WHY.md).

### How

Metadata from Tate Gallery: 
- https://github.com/tategallery/collection

Tools used for this project:

- Python: create indices for `subjects` associated with each artwork
- Wrapped in Bash scripts:
  - cURL: download thumbnails for the collection
  - imagemagick: resize and crop thumbnails into fitting size
  - openssl: base64 encode images to associated them within the json object
- d3.js: put data into browser

Detailed process and thoughts can be found in:
- https://github.com/jueyang/into-the-tate/tree/play/bin

Resulting files are in:
- https://github.com/jueyang/into-the-tate/tree/play/processed
