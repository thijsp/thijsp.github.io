---
layout: basic
title: Frame-it
permalink: "/frameit/"
meta_title: "Thijs Peirelinck | Frame-it"
bootstrap: true
---
## Fill in frame properties

<form action='https://frame-it.thijspeirelinck.be/external' method="POST" enctype="multipart/form-data">
	<div class="row">
		<div class="col-md-3">
			<label for="ratio">Ratio:</label><br>
			<select class="form-select form-select-sm" name="ratio" id="ratio">
				<option value="sq">Square (1:1)</option>
				<option value="45">Insta Vertical (4:5)</option>
				<option value="vert">Insta Story (9:16)</option>
			</select>
		</div>
		<div class="col-md-3">
			<label for="resolution">Quality:</label><br>
			<select class="form-select form-select-sm" name="resolution" id="resolution">
				<option value="best">Best</option>
				<option value="4k">4K</option>
				<option value="hd">Full HD</option>
			</select>
		</div>
	</div>
	<br><br>
	<div class="col-6">
		<label for="background">Background color:</label><br>
		<input class="form-control form-control-color" id="background" name="background" type="color" value="#ffffff"><br><br>
	</div>
	<div class="col-6">
		<input type="hidden" name="MAX_FILE_SIZE" value="30000" />
		<label for="myfile">Image:</label><br>
		<input class="form-control form-control-sm" type="file" id="myfile" name="image" accept="image/jpg,image/jpeg">
		<div id="fileHelp" class="form-text">We'll never save your image on the server.</div>
	</div>
	<br><br>
	<input class="btn btn-primary mb-3" type="submit" value="Create Frame">
</form> 