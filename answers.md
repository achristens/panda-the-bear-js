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

We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

We should help Panda protect their privacy by erasing their personal details from the sidebar.
