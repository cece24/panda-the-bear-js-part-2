1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

var profileImage = document.querySelector('.highlight img');

profileImage.src = 'https://placebear.com/400/400';


2. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

var skyPhoto = document.querySelector('#left-image img');

skyPhoto.src = 'https://placebear.com/325/225';


3. Select the heading that says "Panda the Bear" and change it to your own name.

var heading = document.querySelector('h1');

heading.innerText = 'Boop The Mao!';


4. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

var employmentHeader = document.querySelector('.info-inner-container:nth-child(2) h3');

employmentHeader.innerHTML = '<i class="icon-suitcase"></i> &nbsp; Experience';


5. Change the colour of the body.

document.body.style.background = 'grey';



6. Change the colour of each element using the highlight class. Use a for loop to do this.

var highlightElements = document.querySelectorAll('.highlight');

highlightElements.forEach(function(element) {
  element.style.backgroundColor = '#0ea3ec';
});


7. Change the font family of the h1 to 'monospace'.

var h1Header = document.querySelector('h1');

h1Header.style.fontFamily = 'monospace';


8. Find a way to select the round icons in the sidebar and then change their colour.

var roundIcons = document.querySelectorAll('.action-icon-bg');

for (var i=0; i < roundIcons.length; i++) {
  roundIcons[i].style.backgroundColor = 'grey';
};

<!-- or -->

roundIcons.forEach(function(icon) {
    icon.style.backgroundColor = 'grey';
});


9. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

var nameField = document.querySelector('input[name = "name"]');

nameField.placeholder = 'Identify yourself';


10. Change the placeholder attribute of the message field to "state your business".

var messageField = document.querySelector('#message');

messageField.placeholder = 'State your business';



11. Give the name field a "value" attribute of "your nemesis".

var nameField = document.querySelector('input[name = "name"]');

nameField.value = 'Your nemesis';


12. Change the value attribute of the email field to "koalathebear@gmail.com".

var emailField = document.querySelector('#email');

emailField.value = 'koalathebear@gmail.com';


13. Change the value of the submit button on the contact form to "En garde!".

var submitButton = document.querySelector('#submit');

submitButton.value = 'En garde!';


14. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

var submitButton = document.querySelector('#submit');

submitButton.disabled = true;


15. We should help Panda protect their privacy by erasing their personal details from the sidebar.

var personalDetails = document.querySelectorAll('.bio-info-value');

personalDetails.forEach(function(detail) {
    detail.style.display = 'none';
});
