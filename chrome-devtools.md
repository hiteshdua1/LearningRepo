# Chrome Devtools

I will cover each chrome Devtools feature in 3 parts

> - How to enable/access specific feature ?
> - What it does ?
> - Why should I bother using, SaxoTrader Example(If any)?

- ## Paint Flashing

  #### How ?

  - Open Developers console <Duh?>
  - go to element panel , press `ctrl + shft + p`
  - type `Dom Rendering`
  - Enable **Paint Flashing**

  #### What ?

  - With this option switched on Chrome will flash the screen green whenever painting happens.

  #### Why ?

  - If you’re seeing the whole screen flash green, or areas of the screen that you didn’t think should be painted, then you should dig in a little furthe. Helps me debug unnecessary render cycles and fix bugs.

- ## Capture Screenshot

  #### How ?

  - You can type in screenshot into the Command Menu (shortcut: Cmd + Shift + P) and any of the following options:

  #### What ?

  - With this you can capture screenshots without a browser extension, options :
    - Capture full size screenshot
    - Capture screenshot - will download an image of your website based on what is in the visible viewport
    - Capture node screenshot - will download an image of selected dom node
    - Capture area screenshot - will let select the area and then capture it's screenshot.

  #### Why ?

  - During design discussions you could use this to directly capture screenshots. Obviously we have snagIt (\$49.95), but I am like to save money.

- ## Copy

  #### How ?

  - ~~Open Developers console <?>~~
  - go to network tab
  - right click on request
  - `copy` -> `copy response`
  - Voila, copies to clipboard
  - Another one, typing copy([variable name]) in developers console will copy it's content to clipboard

  #### What ?

  - Just a mentos thing, dimag ki batti jalade\*.

  #### Why ?

  - Network request copy -> just to see if the data is correct or not, debugging bro.
  - `copy command` While walking over the breakpoints, you encounter a variable which is big json and you want to see it's response, just copy it to clipboard and then paste to editor and search, Aloha Momement ;)
  - **Example** : Helped me find specific property if it was being returned in a JSON or not.

- ## Monitor Events

  #### How ?

  - in console window type `monitorEvents(object [, events]).`

  #### What ?

  - It captures all the events for the selected DOM node.

  #### Why ?

  - Helps you filter out the relevent events and helps you debug their order and inspect which all events are being fired for that element.
  - **Example** : Helped me tackle cypress test cases where the event order helped mefix a highchart tooltip not showing. (We were not firing a mouseOut event)

* ## Network Filters

  ### How ?

  - Open the network tab and use filter search box

  ### What ?

  - Helps you filter down network request based on your specific filter term down to exactly what you want to find.

  ### WHY ?

  - Using specific keyworks like : - `status-code:200` to find resources with a status code response of 200.
    status-code:200 to find resources with a status code response of 200. - You can negate a query by prepending a '-'
  - domain, mime-type, scheme, set-cookie-domain, set-cookie-value, has-response-header

## Others

- Console.table()

  - **Example** :
    - console.table(["apples", "oranges", "bananas"]);
    - `console.table($state.instrumentDocuments['47624-CfdOnIndex-KIIDs,PRIIP_KIDs'])`
    - `console.table($config)`

- document.designMode = 'on'

- Js Snippets

  - Saves custom snippet instead of typing to console.
  - Then use that to create bookmarklet
    - `javascript:console.table(Array.from($('.instrument')).map(ele=>{return ele.innerText}))`

- style-rule-toolbar

- Break On
  - Subtree modifications
  - Attributes modifications
  - Node removal
  - **Example** : Who is removing the dom , check from stack trace once debugger is stopped.
