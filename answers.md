Removing Elements from the DOM

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

var timeTravelBar = document.querySelector('.bar-default:nth-of-type(4)');

timeTravelBar.remove();


Adding Elements to the DOM

1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

var pikachuDrawing = document.querySelector('#right-image img');

var copyOfPikachuDrawing = pikachuDrawing.cloneNode();

var portfolioContainer = document.querySelector('.portfolio-container');

portfolioContainer.appendChild(copyOfPikachuDrawing);

or

portfolioContainer.insertAdjacentHTML('beforeend', '<img src="images/pikachu-drawing.jpg" alt="Pikachu" title="Pikachu">');


2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

var pikachuDrawing = document.querySelector('#right-image img');

var copyOfPikachuDrawing = pikachuDrawing.cloneNode();

var portfolioContainer = document.querySelector('.portfolio-container');

for (var i=0; i < 10; i++) {
    portfolioContainer.insertAdjacentHTML('beforeend', '<img src="images/pikachu-drawing.jpg" alt="Pikachu" title="Pikachu">');
}

or

for (var i=0; i < 10; i++) {
    portfolioContainer.appendChild(copyOfPikachuDrawing.cloneNode());
}


3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

var listItem = document.createElement('li');

var leftSpan = document.createElement('span');

var lastUpdated = document.createTextNode('Last Updated');

leftSpan.appendChild(lastUpdated);

listItem.appendChild(leftSpan);

var bioInfoList = document.querySelector('.bio-info');

bioInfoList.appendChild(listItem);

var rightSpan = document.createElement('span');

var updateText = document.createTextNode(Date());

rightSpan.appendChild(updateText);

listItem.appendChild(rightSpan);
