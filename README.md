# photoshop-emailerizr
Takes HTML and images exported from Photoshop and makes them actually usable as HTML emails.

First...

* Generate an HTML file plus images/*.jpg from Photoshop

Prep

* Download bugfixes.css and doctype
* Insert doctype at top of html
* Create style.css
* Insert link to bugfixes.css and style.css into html head
* Clean unrecognised characters (ETX) and escape HTML entities

Edit

* Edit style.css to your heart's content

Build

* Create output folder
* Copy html to _tmp.html
* Inline CSS
* Remove link tags
* Copy _tmp.html to output/index.html
* Remove _tmp.html

Platform specific

* Campaign monitor
    * Copy output to output_cm
	* Zip output_cm/index.html and output_cm/images
* dotMailer
	* Curse their families
    * Copy output to output_dm
	* Move *.jpg from output_dm/images to output
	* Remove instances of "images/" from index.html
	* Remove output_cm/images

 