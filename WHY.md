### It all started with an object

It all started with an object that I saw from the [collection metadata](https://github.com/tategallery/collection) of the Tate Gallery. [I was intrigued](https://twitter.com/jue_yang/status/500309650097831936) by the `subjects` field, which appeared to be the curatorial description of an artwork:

![](http://f.cl.ly/items/3z1p3O0S032s3L0Q3K0P/Screen%20Shot%202014-09-01%20at%207.28.06%20PM.png)

_Universal concepts_, what a term. There's something curious and poetic: what is a Universal Concept to an archivist? How could it surprise me (or bore me, I can't be sure)? What artworks belong to that concept in the eyes of a curator?

At once I wanted to see all that was associcated with such poetry, but, as I soon discovered with a more in-depth data investigation, it was difficult; the `subjects` field was not structured conveniently for comparison and grouping of the artworks.

## And the quest began

After a [brief study](https://github.com/jueyang/into-the-tate/blob/play/bin/README.md) of the data I converted the subjects into three flat look-up files. The schematics were clearer, yet something was missing; the important piece of the visual knowledge -- the image reprsentation of the art itself -- was only captured in the form of URLs.

This would not be a problem if I were doing a quantitative analysis of the metadata, such as the acquisition year of artworks, or the number of contributors they had. But my quest was not about quantifying the art market or the museum practice. Rather, I was trying to fill in the blanks of this curatorial description -- a skeleton that would be empty, and too abstract, without images as flesh. Words can descibe and interpret art, but (visual) art is not tangible until it is seen.

## So the quest continued

The download of the images took a couple of hours with `cURL`. Even though no image exceeded a few dozen kilobytes, the agglomeration of over 70,000 files added up. It became clear that I wouldn't be able to fit the artworks in a browser all at once, at least not with front-end-only solutions (which is mostly where my realm of web knowledge resides for the time being.) I picked the Artist Rooms archive for the most pragmatic reason: the size of its files (both words and images) was the smallest among all the acession-number-based metadata.

With a focused group of content, I made a new subject look-up file, each subject associated with an array of the respective Artist Rooms artworks and their images, whose JSON file became the start of this site.

To bring the interactions into the browser, I used d3. I felt at home. The rest was about honest portrayal of the information I'd thought about, the visual manifestation of an idea, which some might refer to as design.

But you see, design had started at the first sight of an object, flat and abstract.
