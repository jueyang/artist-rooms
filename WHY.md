### It all started with an object

It all started with an object I saw from the [collection metadata](https://github.com/tategallery/collection) of the Tate Gallery. I was intrigued by the `subjects` field, which appears to be the curitorial description and categorization of an artwork, presented along with the title, artist(s), and many other attributes:

https://twitter.com/jue_yang/status/500309650097831936

![](http://f.cl.ly/items/3z1p3O0S032s3L0Q3K0P/Screen%20Shot%202014-09-01%20at%207.28.06%20PM.png)

_Universal concepts_, what a term. There's something curious and poetic. What is a universal concept by the vision of an archivist? And what artworks belong to that concept in the eyes of a curator? At once I wanted to see all that was associcated with such poetry, but, as I soon discovered with more in-depth investigation about the data, it was difficult. The `subjects` field was not structured conveniently for comparison and grouping of the artworks.

So the quest began.

After a [brief study](https://github.com/jueyang/into-the-tate/blob/play/bin/README.m) of the data I converted the subjects into three flat look-up files. The schematics were clearer, yet something was missing. The important piece of the visual knowledge - the image reprsentation of the art itself - was only captured in the form of URLs.

This would not be a problem if I were doing an quantitative analysis of the metadata, such as the acquisition year of artworks, or the number of contributors they had. But my quest was not about quantifying art. Rather I was trying to fill in the blanks of a curitorial description with flesh, an archival skeleton that would be empty, and too abstract, without images. Words can descibe and interpret art, but (visual) art is not tangible until it is seen.

So the quest continued.

The download of the images took a couple of hours with cURL. Even though no image exceeded a few dozen kilobytes, the agglomeration of over 70,000 files added up. It became clear that I wouldn't be able to fit the artworks in a browser all at once, at least not with front-end-only solutions (which is mostly where my realm of web knowledge resides so far.) I picked the Artist Rooms archive for the most pragmatic reason: the size of its files (both words and images) was the smallest among all the acession-number-based metadata.

With a focused group of content, I made a new subject look-up file, each subject associated with an array of the respective Artist Rooms artworks and their images. That json file became the start for the this site.

With the visual presentation and the interactions of an idea coming to life in the browser, I used d3 to map the data to the screen. I felt at home.
