---
layout: basic
title: Frame-it
permalink: "/frameit/"
meta_title: "Thijs Peirelinck | Frame-it"
bootstrap: true
meta_description: "Privacy-friendly tool to create a border around images, as typically seen on Instagram."
---
## Fill in frame properties

<form action='https://frame-it.thijspeirelinck.be/external' method="POST" enctype="multipart/form-data">
	<div class="row">
		<div class="col-md-6">
			<label for="ratio">Ratio:</label><br>
			<select class="form-select" name="ratio" id="ratio">
				<option value="sq">Square (1:1)</option>
				<option value="45">Insta Vertical (4:5)</option>
				<option value="vert">Insta Story (9:16)</option>
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
	<div class="col-6">
		<label for="background">Background color:</label><br>
		<input class="form-control form-control-color custom" id="background" name="background" type="color" value="#ffffff">
	<br>
	</div>
	<div class="col-12">
		<input type="hidden" name="MAX_FILE_SIZE" value="30000" />
		<label for="myfile">Image:</label><br>
		<input class="form-control" type="file" id="myfile" name="image" accept="image/jpg,image/jpeg">
		<div id="fileHelp" class="form-text" style="color: #d7dade">We'll never save your image on the server.</div>
	</div>
	<br>
	<div class="col-12">
		<input class="btn btn-primary mb-3" type="submit" value="Create Frame" style="width:100%">
	</div>
</form> 

### Hosting this tool costs time and money
<div class="page-social relative">
	<a href="https://paypal.me/thijspeirelinck" target="_blank">
		<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-paypal" viewBox="0 0 16 16">
  		<path d="M14.06 3.713c.12-1.071-.093-1.832-.702-2.526C12.628.356 11.312 0 9.626 0H4.734a.7.7 0 0 0-.691.59L2.005 13.509a.42.42 0 0 0 .415.486h2.756l-.202 1.28a.628.628 0 0 0 .62.726H8.14c.429 0 .793-.31.862-.731l.025-.13.48-3.043.03-.164.001-.007a.351.351 0 0 1 .348-.297h.38c1.266 0 2.425-.256 3.345-.91.379-.27.712-.603.993-1.005a4.942 4.942 0 0 0 .88-2.195c.242-1.246.13-2.356-.57-3.154a2.687 2.687 0 0 0-.76-.59l-.094-.061ZM6.543 8.82a.695.695 0 0 1 .321-.079H8.3c2.82 0 5.027-1.144 5.672-4.456l.003-.016c.217.124.4.27.548.438.546.623.679 1.535.45 2.71-.272 1.397-.866 2.307-1.663 2.874-.802.57-1.842.815-3.043.815h-.38a.873.873 0 0 0-.863.734l-.03.164-.48 3.043-.024.13-.001.004a.352.352 0 0 1-.348.296H5.595a.106.106 0 0 1-.105-.123l.208-1.32.845-5.214Z"/>
		</svg>
	Feel free to support me - choose your amount
	</a> 
</div>