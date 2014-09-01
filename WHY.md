It all started with an object I saw from the [collection metadata](https://github.com/tategallery/collection) of the Tate Gallery:

https://twitter.com/jue_yang/status/500309650097831936

_Universal concepts_, what an intriguing term. At once I wanted to see all the artworks associcated with such poetry. But I soon discovered, by looking more in-depth at the data, that the `subjects` field to be used was not structured conveniently for comparison and grouping of the artworks. So the quest began.

After I converted the subjects into three flat json files (for the three schematic levels respectively) I realized an important ingredient of the knowledge of an artwork is only available as a url from the metadata. The image reprsentation of the art itself is missing.

This would not be a problem if I were doing an quantitative analysis of the metadata, such as the acquisition year of artworks, or the number of contributors it had. But my quest was not about quantifying art. Rather I was trying to fill in the blank of a curitorial description that would be empty without images. Words can descibe and interpret art, but (visual) art is not tangible until it is seen. So the quest continued.

The download of the images took a couple of hours with cURL. Even though no image exceeded a few dozen kilobytes, the agglomeration of over 70,000 files added up. It became clear that I wouldn't be able to fit the artworks in a browser all at once, at least not with front-end-only solutions. I picked the Artist Rooms archive for the most pragmatic reason: the size of its files (words and images along) was the smallest among the acession number-based metadata.

Now, with a focused group of content, I made a new subject look-up file, each subject associated with the respective Artist Rooms artworks and their images. That json file was the start of front-end, the visual presentation of such the idea, and the interactions.

But I felt at home now.