
# Retail QR Code![Build Status](http://devtools1.risevision.com:8080/job/Storage-Client-BranchPush/badge/icon)

## Introduction

The Retail QR Code The Retail QR Code Template was created to promote a product while offering a QR code to scan for a coupon takeaway. A preview of the template can be seen here: http://rise-vision.github.io/content-retail-qrcode/index.html

##Steps to run the Retail QR Code Template:##

1. Fork or download the entire content-retail-qrcode repository.  
![alt tag](images/readme-step1.jpg)

2. Modify the files within the content-retail-qrcode folder directory to fit your needs (see below on how to modify specific elements).  
![alt tag](images/readme-step2.jpg)

3. Host the entire “content-retail-qrcode” folder directory in rise vision storage or your web hosting service.  
![alt tag](images/readme-step3.jpg)

4. Copy the link to the index.html file where you have it hosted and insert the url into a schedule. (you can also add this link to the url gadget within a presentation)  
![alt tag](images/readme-step4.jpg)


##Directions to Modify the Retail QR Code Template:##

####Changing the Animated Background Image
The background image is loaded by using the Rise Storage Web Component.
To change the image open index.html, locate the following code and modify the rise-storage tag to reflect your company id, folder and image name:

```
<div id="background">
	<rise-storage companyId="395c64e5-2930-460b-881e-009aabb157df" folder="content-retail-qrcode" fileName="retail-qrcode-bg.jpg"></rise-storage>
  <img id="storage-image" src="" />
  <script>
    var storage = document.querySelector("rise-storage"),
      image = document.querySelector("#storage-image");

    storage.addEventListener("rise-storage-response", function(e) {
      image.setAttribute("src", e.detail[0]);
    });
  </script>
</div>
```

The components folder is an assortment of dependices needed for the rise storage web component to work.

For more information on how to utilze rise storage web component. Please refer to the readme.md within the following repo:
https://github.com/Rise-Vision/web-component-rise-storage

The style of the animation is done within css/style-main.css file. Look for the keyframes called ```@-webkit-keyframes "slidein"```.

####Changing the Quote Text
Open index.html, the quote content is nested within the div ```<div id="quote-container">``` Modify the text within the span tags to meet your needs. 

The style of the quote content is controlled within css/style-main.css. Look for the comment called ```Quote Content```.

####Changing the QR Code
Open index.html, locate the following code and modify the src url of the source tag to the path of your qr code graphic.:

```
<img id="qrcode" src="images/qrcode.png">
```

The animation is done within css/qrcode-animation.css file. Look for the keyframes called ```@-webkit-keyframes "scan"``` and ```@-webkit-keyframes "pulse"```.
 
 
####Changing the QR Code Destination Page
When a user scans the qr code they will be taken to the coupon.html page. The style of this page is controlled by the css/coupon.css. 
If you would like it to continue to take people to this page do not change the qr graphic. 

####Miscellaneous Items
The text size and various other elements within css files use viewport sizing.
This is a way to dynamically size elements without the use of media queries.
For more information I suggest this article: http://css-tricks.com/viewport-sized-typography/

## Built With
actual tools used
- HTML
- CSS
- Javascript

Retail QR Code Template works in conjunction with [Rise Vision](http://www.risevision.com), the [digital signage management application](http://rva.risevision.com/) that runs on [Google Cloud](https://cloud.google.com).

At this time Chrome is the only browser that this project and Rise Vision supports.

## Submitting Issues
If you encounter problems or find defects we really want to hear about them. If you could take the time to add them as issues to this Repository it would be most appreciated. Please Identify the specific template that has the issue and follow the following format where applicable:

**Reproduction Steps**

1. did this
2. then that
3. followed by this (screenshots / video captures always help)

**Expected Results**

What you expected to happen.

**Actual Results**

What actually happened. (screenshots / video captures always help)

## Contributing
All contributions are greatly appreciated and welcome! If you would first like to sound out your contribution ideas please post your thoughts to our [community](http://community.risevision.com), otherwise submit a pull request and we will do our best to incorporate it.

### Suggested Contributions
- Alternative ways to animate background
- Alternative ways to engage users to scan qr code
- i18n Language Support

## Resources
If you have any questions or problems please don't hesitate to join our lively and responsive community at http://community.risevision.com.

If you are looking for user documentation on Rise Vision please see http://www.risevision.com/help/users/

If you would like more information on developing applications for Rise Vision please visit http://www.risevision.com/help/developers/.

 If you have any questions or problems please don't hesitate to join our lively and responsive community at http://community.risevision.com.
 
**Additional Content Templates can be found here: https://github.com/Rise-Vision/content-templates**

**Facilitator**

[Mathew Meiers](https://github.com/mmeiers "Mathew Meiers")
