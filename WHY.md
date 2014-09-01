It all started with an object I saw from the [collection metadata](https://github.com/tategallery/collection) of the Tate Gallery:

https://twitter.com/jue_yang/status/500309650097831936

_Universal concepts_, what an intriguing term. At once I wanted to see all the artworks associcated with such poetry. But I soon discovered, by looking more in-depth at the data, that the `subjects` field to be used was not structured conveniently for comparison and grouping of the artworks. So the quest began.

After I converted the subjects into three flat json files (for the [three schematic levels](https://github.com/jueyang/into-the-tate/blob/play/bin/README.md), respectively) I realized an important ingredient of the knowledge of the artwork is missing - the image reprsentation of the art itself is only captured in the form of URLs.

This would not be a problem if I were doing an quantitative analysis of the metadata, such as the acquisition year of artworks, or the number of contributors they had. But my quest was not about quantifying art. Rather I was trying to fill in the blank of a curitorial description, which would be too abstract without images. Words can descibe and interpret art, but (visual) art is not tangible until it is seen. So the quest continued.

The download of the images took a couple of hours with cURL. Even though no image exceeded a few dozen kilobytes, the agglomeration of over 70,000 files added up. It became clear that I wouldn't be able to fit the artworks in a browser all at once, at least not with front-end-only solutions. I picked the Artist Rooms archive for the most pragmatic reason: the size of its files (both words and images) was the smallest among the acession number-based metadata.

With a focused group of content, I made a new subject look-up file, each subject associated with an array of the respective Artist Rooms artworks and their images. That json file was the start for the frontend development - this site.

With the visual presentation and the interactions of an idea coming to life in the browser, I felt at home.
