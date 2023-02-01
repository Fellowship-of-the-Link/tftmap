# Manually creating permanent versions on this wiki

We are currently playing with concepts like permanent versions and trying to combine the best aspects of wikis and blogs - see [[Wiki practice meets blogging]].

This guide was extracted from the above post for reasons of readability. It sets out how to create a new permanent version of a blog post, so that:

* the current version always occupies the same URL, and yet can evolve
* it links to the previous permanent version, which links forward and backward to the permanent version before that, which in turn links forward and back to permanent version before *that*...

The key to managing this lies in the "Revision notes" section at the bottom of each page, which should always include a version control section. 

In the **very first version** of any "versioned" page this version control section should contain something like this:

* this is version: current
* here is the current version: \[\[filename\]\]  
  *(aware that including a link to itself looks odd, but as this is copied each time a new major version is created it will save a lot of time)*
* previous version: n/a

When it is time to update the current file, duplicate the file, creating \[\[filename-1\]\], and:

* move it into the permanent versions subfolder
* add a "snapshot warning" at the top of the page pointing to version control section
* edit its version control section (*italic* = manual edits)
	* this is version: *1*
	* here is the current version: \[\[filename\]\]  
	* previous version: n/a
* when editing the current file, edit its version control section (*italic* = manual edits)
		* this is version: current
		* here is the current version: \[\[filename\]\]  
		* previous version: version 1:  \[\[filename-1\]\]

When it is time to update the current file again, simply repeat:

* duplicate the current file, creating \[\[filename-2\]\], and 
	* move it into the permanent versions subfolder
	* add a "snapshot warning" at the top of the page pointing to version control section
	* edit its version control section (*italic* = manual edits)
		* this is version: *2*
		* here is the current version: \[\[filename\]\]  
		* previous version: version 1: [[The Way of the Wiki meets blogging 1]]
	* edit the current file
		* this is version: current
		* here is the current version:  \[\[filename\]\]  
		* previous version: version 2:  \[\[filename-2\]\]

Therefore each major update of the file requires creating a copy of the current file and making a total of 3 simple edits across the two files.

Why go to all this trouble? See [[Wiki practice meets blogging]] (the current version, of course).

---

## Revision Notes

* (29/01/2023) extracted and generalised the content of this file from [[Wiki practice meets blogging]] to make it more readable.