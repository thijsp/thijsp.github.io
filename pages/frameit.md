---
layout: basic
title: Frame-it
permalink: "/frameit/"
meta_title: "Thijs Peirelinck | Frame-it"
bootstrap: true
meta_description: "Privacy-friendly tool to create a border around images, as typically seen on Instagram."
---
## Fill in frame properties

<form action='{{ site.apiurl }}/frameit-external-multiple' method="POST" enctype="multipart/form-data">
	<div class="row">
		<div class="col-md-6">
			<label for="ratio">Ratio:</label><br>
			<select class="form-select" name="ratio" id="ratio">
				<option value="sq">Square (1:1)</option>
				<option value="45">Insta Vertical (4:5)</option>
				<option value="54">Insta Horizontal (5:4)</option>
				<option value="vert">Insta Story (9:16)</option>
				<option value="32"> Horizontal (3:2)</option>
        		<option value="4:5 pano_crop"> Vertical Insta Pano Crop</option>
				<option value="5:4 pano_crop"> Horizontal Insta Pano Crop</option>
			</select>
		</div>
		<div class="col-md-6">
			<label for="resolution">Quality:</label><br>
			<select class="form-select" name="resolution" id="resolution">
				<option value="best">Best</option>
				<option value="4k">4K</option>
				<option value="hd">Full HD</option>
			</select>
			<div id="QualityHelp" class="form-text" style="color: #d7dade">This is not an upscaling tool - if your picture's quality is bad, don't expect good results.</div>
		</div>
	</div>
	<br>
	<div class="row">
		<div class="col-md-6">
			<label for="background">Background color:</label><br>
			<input class="form-control form-control-color custom" id="background" name="background" type="color" value="#ffffff">
		</div>
		<div class="col-md-2">
			<label for="collage"> Collage: </label><br>
			<input type="checkbox" id="collage" name="collage" value="collage" style="transform: scale(1.5)">
		</div>
    	<div class="col-md-2">
			<label for="Black Border"> Black Border: </label><br>
			<input type="checkbox" id="blackborder" name="blackborder" value="blackborder" style="transform: scale(1.5)">
		</div>
	    <div class="col-md-2">
		    <label for="Rounded Corner"> Rounded: </label>
		    <br />
		    <input type="checkbox" id="rounded_corner" name="rounded_corner" value="rounded_corner" style="transform: scale(1.5)" />
	    </div>
	</div>
	<br>
	<div class="col-12">
		<label for="margin" >Border width: </label><br>
		<input class="form-range mb-3" type="range" value="5" style="width:100%" id="margin" name="margin" min="0" max="100">
	</div>
	<br>
	<div class="col-12">
		<input type="hidden" name="MAX_FILE_SIZE" value="30000" />
		<label for="myfile">Image(s):</label><br>
		<input class="form-control" type="file" id="myfile" name="image" accept="image/jpg,image/jpeg" multiple>
		<div id="fileHelp" class="form-text" style="color: #d7dade">We'll never save your image on the server.</div>
	</div>
	<br>
	<div class="col-12">
		<input class="btn btn-primary mb-3" type="submit" value="Create Frame" style="width:100%">
	</div>
</form> 

### Hosting this tool costs time and money
{% include extensions/donate.html donate_text="feel free to support this tool" %}
<br>
{% include extensions/share-buttons.html mail_subject="Frame-it" mail_body="Check out this privacy-friendly tool to create frames around your images: "%}