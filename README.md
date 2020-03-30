This web application is to configure the behaviour and appearance of any horizontal web app without needing to release an app update or tinkering with the code.gh
 
This SDK is a tool that lets you change the appearance of your app without requiring users to download an app update. When using this SDK, you can configure the theme or the appearance of the elements of any web application without any impact on the functionality or the performance of the web app.

KEY CAPABILITIES
The SDK enables configuring the UI/UX elements with a tap of a button in the interface of the SDK. The colour, the size, the font, the icons even the background of the web application can be configured or themed easily without having to roll out an update or changing the code. The SDK is designed to be integrated with any web app making it a versatile tool. The SDK is capable of adding in more and more features in order to configure one or more UI/UX elements at the same time. The interface is minimal and user friendly to ensure that all the features can be easily used to correspondingly change the UI/UX elements of the web app.

WORKING
This SDK has a set of features or corresponding changes that can be done to any element in the UI. Every feature has a switch and when the required switch is enabled. The corresponding UI element changes its appearance or behaviour based on the given feature. Every element can be mapped with appropriate indexing that is any element can be remotely configured through the SDK. 

TO THE WEB DEVELOPER:
In order to integrate the SDK with any web app, the UI/UX elements of the corresponding features need to be given a class name or an ID same as the corresponding feature 'querySelector' command in the code snippet that resembles as follows:
<header id = head>
            <input type="text" placeholder="What do you want to do today?" id="item">
            <button id="add">
                <svg version="1.1" ></svg>
            </button>
        </header>

        <div class="container" id="body">
            <!-- Uncompleted tasks -->
            <ul class="todo" id="todo"></ul>

            <!-- Completed tasks -->
            <ul class="todo" id="completed"></ul>
        </div>

        <!-- JavaScripts -->
        <script src="resources/js/main.js"></script>
{Code snippet from index.html showing that every element has a specified ID or class name}

function fourthfuncon(){
      var temp = document.querySelector("#completed")
      for(var i = 0; i < temp.children.length; i++){
        temp.children[i].style.backgroundColor = '#FFB6C1';
      }
    }
       
  if (localStorage.getItem('d')=='on')
        fourthfuncon();
      
      
  function fourthfuncoff(){
      var temp = document.querySelector("#completed")
      for(var i = 0; i < temp.children.length; i++){
      temp.children[i].style.backgroundColor = '#FFFFFF';
        }
    }
    if (localStorage.getItem('d')=='off')
          fourthfuncoff();
{Code snippet from main.js showing that every querySelector command has a specified ID or class name corresponding to the required element to be configured}
If the ID/class name of the respective UI/UX elements are not the same as the in the 'queryselector' command in the index file, the required changes will not be made on the elemtents because no element with the specified ID exists in the web app. Also, if many elements are to be configured in the same feature or switch, the ID of all the required elements to be commonly configured must be the same.

The SDK is designed in a way that any number of UI/UX element can be configured. If a new element is added in the web app, or a set of new elements is added in the web app, the developer must specify a unique class or ID to the element. So that the SDK can access it using that specified ID or class name.

FURTHER SCOPE OF DEVELOPMENT:
A more general approach as to configuring all or a lot of common elements at the same time (using the same switch) will be more efficient and practical. So further development can be carried out to make this software development kit more versatile and user friendly. 
More features can be added by replicating the following snippet and making another variable in the LocalStorage that can be accessed and further configuration of the corresponding UI/UX element is carried out. 
The snippet to be replicated is as follows

if(chb[4].checked)
                {
                   localStorage.setItem('e', 'on');
                }
                if(!chb[4].checked)
                {
                   localStorage.setItem('e', 'off');
                }

Already existing code in sdk.js where variable ‘e’ is declared in the LocalStorage

if(chb[5].checked)
                {
                   localStorage.setItem('f', 'on');
                }
                if(!chb[5].checked)
                {
                   localStorage.setItem('f', 'off');
                }
The code to be replicated when another feature or switch is added to configure an element. Here a new variable ‘f’ is declared in the LocalStorage


LIMITATIONS AND SCOPE OF IMPROVEMENT
The SDK is very specific regarding configuring one feature or one UI/UX element at a time. This is a limitation that the SDK is not generally controlling or configuring the elements and bringing about changes to a collective group of elements i.e. changing the entire theme of the UI or changing the font of all the text in the web application. The SDK has a condition that prior to implementing, all the elements in the web app that have to be configured need to have unique class names or IDs.
