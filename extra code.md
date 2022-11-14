<!-- <div class="options">
            <button id="bold" class="option-button format">
              <i class="fa-solid fa-bold fa-lg"></i>
            </button>
            <button id="italic" class="option-button format">
              <i class="fa-solid fa-italic fa-lg"></i>
            </button>
            <button id="underline" class="option-button format">
              <i class="fa-solid fa-underline fa-lg"></i>
            </button>
            <button id="strikethrough" class="option-button format">
              <i class="fa-solid fa-strikethrough fa-lg"></i>
            </button>

            <button id="insertUnorderedList" class="option-button">
              <i class="fa-solid fa-list fa-lg"></i>
            </button>
            <button id="undo" class="option-button">
              <i class="fa-solid fa-rotate-left fa-lg"></i>
            </button>
            <button id="redo" class="option-button">
              <i class="fa-solid fa-rotate-right fa-lg"></i>
            </button>
            <button id="createLink" class="adv-option-button">
              <i class="fa fa-link fa-lg"></i>
            </button>

            <button id="justifyLeft" class="option-button align">
              <i class="fa-solid fa-align-left fa-lg"></i>
            </button>
            <button id="justifyCenter" class="option-button align">
              <i class="fa-solid fa-align-center fa-lg"></i>
            </button>
            <button id="justifyRight" class="option-button align">
              <i class="fa-solid fa-align-right fa-lg"></i>
            </button>
            <button id="justifyFull" class="option-button align">
              <i class="fa-solid fa-align-justify fa-lg"></i>
            </button>
            <select id="fontName" class="adv-option-button"></select>
            <select id="fontSize" class="adv-option-button"></select>
            <div class="input-wrapper">
              <input type="color" id="foreColor" class="adv-option-button" />
              <label for="foreColor">Font Color</label>
            </div>
            <div class="input-wrapper">
              <input type="color" id="backColor" class="adv-option-button" />
              <label for="backColor">Highlight Color</label>
            </div>
          </div> -->

// let optionsButtons = document.querySelectorAll(".option-button");
// let advancedOptionButton = document.querySelectorAll(".adv-option-button");
// let fontName = document.getElementById("fontName");
// let fontSizeRef = document.getElementById("fontSize");
// let writingArea = document.getElementById("text-input");
// let linkButton = document.getElementById("createLink");
// let alignButtons = document.querySelectorAll(".align");
// let spacingButtons = document.querySelectorAll(".spacing");
// let formatButtons = document.querySelectorAll(".format");
// let scriptButtons = document.querySelectorAll(".script");

// let btn = document.querySelector(".btn");
// //List of fontlist
// let fontList = [
// "Arial",
// "Verdana",
// "Times New Roman",
// "Garamond",
// "Georgia",
// "Courier New",
// "cursive",
// "Poppins",
// ];
// //Initial Settings
// const initializer = () => {
// //function calls for highlighting buttons
// //No highlights for link, unlink,lists, undo,redo since they are one time operations
// highlighter(alignButtons, true);
// highlighter(spacingButtons, true);
// highlighter(formatButtons, false);
// highlighter(scriptButtons, true);
// //create options for font names
// fontList.map((value) => {
// let option = document.createElement("option");
// option.value = value;
// option.innerHTML = value;
// fontName.appendChild(option);
// });
// //fontSize allows only till 7
// for (let i = 1; i <= 7; i++) {
// let option = document.createElement("option");
// option.value = i;
// option.innerHTML = i;
// fontSizeRef.appendChild(option);
// }
// //default size
// fontSizeRef.value = 3;
// };
// //main logic
// const modifyText = (command, defaultUi, value) => {
// //execCommand executes command on selected text
// document.execCommand(command, defaultUi, value);
// };
// //For basic operations which don't need value parameter
// optionsButtons.forEach((button) => {
// button.addEventListener("click", () => {
// modifyText(button.id, false, null);
// });
// });
// //options that require value parameter (e.g colors, fonts)
// advancedOptionButton.forEach((button) => {
// button.addEventListener("change", () => {
// modifyText(button.id, false, button.value);
// });
// });
// //link
// linkButton.addEventListener("click", () => {
// let userLink = prompt("Enter a URL");
// //if link has http then pass directly else add https
// if (/http/i.test(userLink)) {
// modifyText(linkButton.id, false, userLink);
// } else {
// userLink = "http://" + userLink;
// modifyText(linkButton.id, false, userLink);
// }
// });
// //Highlight clicked button
// const highlighter = (className, needsRemoval) => {
// className.forEach((button) => {
// button.addEventListener("click", () => {
// //needsRemoval = true means only one button should be highlight and other would be normal
// if (needsRemoval) {
// let alreadyActive = false;
// //If currently clicked button is already active
// if (button.classList.contains("active")) {
// alreadyActive = true;
// }
// //Remove highlight from other buttons
// highlighterRemover(className);
// if (!alreadyActive) {
// //highlight clicked button
// button.classList.add("active");
// }
// } else {
// //if other buttons can be highlighted
// button.classList.toggle("active");
// }
// });
// });
// };
// const highlighterRemover = (className) => {
// className.forEach((button) => {
// button.classList.remove("active");
// });
// };
// // window.onload = initializer();

// // var noPrintElements = [];

width: 600px;
.options {
background-color: #ffffff;
padding: 20px 30px;
border-radius: 10px;
display: flex;
flex-wrap: wrap;
justify-content: center;
align-items: center;
gap: 30px;
button {
padding-top: 3px;
height: 28px;
width: 28px;
display: grid;
place-items: center;
border-radius: 3px;
border: none;
background-color: #ffffff;
outline: none;
color: #020929;
cursor: pointer;
}
button:hover {
background-color: lightblue;
}
select {
padding: 7px;
border: 1px solid #020929;
border-radius: 3px;
.options label,
.options select {
font-family: "Poppins", sans-serif;
}
}
.input-wrapper {
display: flex;
align-items: center;
gap: 8px;
padding: 20px 13px;
input[type="color"] {
-webkit-appearance: none;
-moz-appearance: none;
appearance: none;
background-color: transparent;
width: 40px;
height: 28px;
border: none;
cursor: pointer;
}
input[type="color"]::-webkit-color-swatch {
border-radius: 15px;

                    }
                    input[type="color"]::-moz-color-swatch {
                      border-radius: 15px;

                    }
                  }
                }
              }
                div:empty:before {
                content:attr(data-placeholder);
                color:gray;
                font-size: 5;

              }
              #text-input {
               background-color: #ffffff;
               line-height: 20px;
                  padding: 20px;
                min-height: 40vh;
                border-radius: 10px;
                width: 95%;

              }
              #text-input:hover{
                border: 1px solid black;
              }
              .active {
                background-color: #e0e9ff;
              }
