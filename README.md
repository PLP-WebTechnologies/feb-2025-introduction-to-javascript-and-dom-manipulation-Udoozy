# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

  // Changing text content dynamically
        const changeTextButton = document.createElement('button');
        changeTextButton.innerText = "Change Text Content";
        document.body.appendChild(changeTextButton);

        changeTextButton.addEventListener('click', () => {
            const ol = document.querySelector('.container');
            ol.innerHTML = "<li>HTML</li><li>CSS</li><li>JavaScript</li><li>DOM Manipulation</li>";
        });

        // Modifying CSS styles via JavaScript
        const changeStyleButton = document.createElement('button');
        changeStyleButton.innerText = "Change Styles";
        document.body.appendChild(changeStyleButton);

        changeStyleButton.addEventListener('click', () => {
            document.body.style.backgroundColor = "lightblue";
            document.body.style.fontFamily = "Verdana, sans-serif";
            const img = document.getElementById("image");
            img.style.border = "5px solid black";
        });

        // Adding/removing an element (creating/removing a paragraph)
        const toggleElementButton = document.createElement('button');
        toggleElementButton.innerText = "Toggle Paragraph";
        document.body.appendChild(toggleElementButton);

        toggleElementButton.addEventListener('click', () => {
            const paragraph = document.getElementById("dynamic-paragraph");
            if (!paragraph) {
                const newParagraph = document.createElement('p');
                newParagraph.id = "dynamic-paragraph";
                newParagraph.innerText = "This paragraph was dynamically added!";
                document.body.appendChild(newParagraph);
            } else {
                paragraph.remove();
            }
        });

        // Button to trigger form submission behavior
        const submitButton = document.getElementById("submit");
        submitButton.addEventListener('click', () => {
            alert("Form submitted!");
