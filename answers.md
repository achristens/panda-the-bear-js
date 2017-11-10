Replace profile image:
    var profile = document.querySelector('.profile-image')
    undefined
    profile
    <img src=​"images/​self-portrait-grassbg.jpg" alt=​"Self Portrait" title=​"Self Portrait" class=​"profile-image">​

    profile.src = "https://placebear.com/400/400"
    "https://placebear.com/400/400"
    Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

Select the heading that says "Panda the Bear" and change it to your own name.
    var heading = document.querySelector('h1');
    undefined
    heading
    <h1 class=​"highlight">​Panda The Bear​</h1>​
    heading.innerText = "Abby Christens";
    "Abby Christens"


Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)
    var employmentHeading = document.querySelector("div#employment > h3 ")
    undefined
    employmentHeading.innerText = "Work History"
    "Work History"


Change the colour of the body.
    var body = document.querySelector("body")
    undefined
    body.style.background = "#2e2e2e"
    "#2e2e2e"

Change the colour of each element using the highlight class. Use a for loop to do this.
    var highlight = document.querySelectorAll('.highlight')
    highlight.forEach(function(each){each.style.backgroundColor = "#ecb7bf"})

Change the font family of the h1 to 'monospace'.
    var headings = document.querySelectorAll("h1");
    headings.forEach(function(heading){heading.style.fontFamily = 'monospace'})

Find a way to select the round icons in the sidebar and then change their colour.
    var roundIcons = document.querySelectorAll(".action-icon-bg");
    roundIcons.forEach(function(icon){ icon.style.backgroundColor = "#dedede"})

Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
    var formName = document.querySelector("#name")
    formName.placeholder = "Identify Yourself";

Change the placeholder attribute of the message field to "state your business".
    var formMessage = document.querySelector("#message")
    formMessage.placeholder = "state your business"

Give the name field a "value" attribute of "your nemesis".
    formName.value = "Your Nemesis"

Change the value attribute of the email field to "koalathebear@gmail.com".
    var emailForm = document.querySelector("#email")
    emailForm.value = "koalathebear@gmail.com"

Change the value of the submit button on the contact form to "En garde!".
    var submitButton = document.querySelector("#submit")
    submitButton.value = "En garde!"

We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
    submitButton.disabled = true;

We should help Panda protect their privacy by erasing their personal details from the sidebar.
  var sidebarContact = document.querySelectorAll(".bio-info-item")
  sidebarContact.forEach(function(item){ item.innerText = "" })



=================================================================================================================================
Removing Elements from the DOM

Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)
  var parent = document.querySelector('section > div')
  var skills = document.querySelectorAll(".bar-default")
  var timeTravel = skills[2]
  parent.removeChild(timeTravel);


Adding Elements to the DOM

That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().
    var image = document.querySelector('#right-image > img')
    var newImage = image.cloneNode();
    var portfolio = document.querySelector('.portfolio-container')
    portfolio.appendChild(newImage);

Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.
    for(i=0;i<10;i++){
    var image = document.querySelector('#right-image > img');
        var newImage = image.cloneNode();
        var portfolio = document.querySelector('.portfolio-container')
        portfolio.appendChild(newImage);
    }

Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

    var listItem = document.createElement('li');
    var leftSpan = document.createElement('span');
    var lastUpdated = document.createTextNode('Page last updated on');
    leftSpan.appendChild(lastUpdated);
    listItem.appendChild(leftSpan);
    var bioSection = document.querySelector('.bio-info')
    bioSection.appendChild(listItem)
    var rightSpan = document.createElement('span');
    var date = new Date()
    var dateHTML = document.createTextNode(date);
    rightSpan.appendChild(dateHTML)
    var lastItem = bioSection.lastChild
    lastItem.appendChild(rightSpan)
