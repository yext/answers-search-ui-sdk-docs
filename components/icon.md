---
title: Icon
order: 16
component: true
appliesTo: Both
apiProperties:
  - property: iconName
    type: string
    description: Use one of the predefined icons in the Answers Search UI Library
  - property: iconUrl
    type: string
    description: Sets the icon to reference an image URL. Overrides icon name.
  - property: classNames
    type: string
    description: Adds class names to the icon. Multiple classnames should be space-delimited. 
---

## Background

The icon component is typically created by other components, but it can also be used as a standalone component. 


## Basic Configuration
```html
<div class='icon-container'></div>
```

```js
ANSWERS.addComponent('IconComponent', {
  container: '.icon-container',
  iconName: 'pantheon',
});
```

## Built-In Icons

The following is a list of names for the icons that are supported by default. You can reference these names when a component has an attribute to set the icon (this includes the search bar, universal results and no results).


<table style="min-width: 12rem;">
  <thead>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <th>Name</th>
      <th>Icon</th>
    </tr>
  </thead>
  <tbody>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>briefcase</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M20 7h-4V5c0-1.11-.89-2-2-2h-4c-1.11 0-2 .89-2 2v2H4c-1.11 0-1.99.89-1.99 2L2 20c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V9c0-1.11-.89-2-2-2zm-6 0h-4V5h4v2z"></path></svg> </div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>calendar</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M18.111 13.2H12v6h6.111v-6zM16.89 0v2.4H7.11V0H4.667v2.4H3.444c-1.356 0-2.432 1.08-2.432 2.4L1 21.6C1 22.92 2.088 24 3.444 24h17.112C21.9 24 23 22.92 23 21.6V4.8c0-1.32-1.1-2.4-2.444-2.4h-1.223V0H16.89zm3.667 21.6H3.444V8.4h17.112v13.2z"></path></svg> </div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>callout</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M21.99 4c0-1.1-.89-2-1.99-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h14l4 4-.01-18z"></path></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>chevron</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"> <g fill-rule="evenodd" transform="translate(-1 -8)"><path d="m2.6417004 8-1.1417004 1.0575 3.70850202 3.4425-3.70850202 3.4425 1.1417004 1.0575 4.8582996-4.5z"/></g></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>close</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M7 8l9.716 9.716m0-9.716L7 17.716" stroke="currentColor" stroke-width="2"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>directions</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M23.649 11.154L12.846.35a1.195 1.195 0 00-1.692 0L.35 11.154a1.195 1.195 0 000 1.692L11.154 23.65a1.195 1.195 0 001.692 0L23.65 12.846c.468-.456.468-1.212 0-1.692zm-9.254 3.853v-3.001H9.593v3.6h-2.4v-4.8c0-.66.54-1.2 1.2-1.2h6.002V6.604l4.2 4.2-4.2 4.202z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>document</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M4 6H2v14c0 1.1.9 2 2 2h14v-2H4V6zm16-4H8c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm-1 9H9V9h10v2zm-4 4H9v-2h6v2zm4-8H9V5h10v2z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>elements</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M13,15 L13,17 L21,17 L21,19 L13,19 L13,21 L11,21 L11,15 L13,15 Z M9,17 L9,19 L3,19 L3,17 L9,17 Z M9,15 L7,15 L7,13 L3,13 L3,11 L7,11 L7,9 L9,9 L9,15 Z M21,11 L21,13 L11,13 L11,11 L21,11 Z M17,3 L17,5 L21,5 L21,7 L17,7 L17,9 L15,9 L15,3 L17,3 Z M13,5 L13,7 L3,7 L3,5 L13,5 Z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>email</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12,-3.55271368e-15 C8.81712,-3.55271368e-15 5.7648,1.26468 3.5148,3.5148 C1.2648,5.76492 3.55271368e-15,8.81736 3.55271368e-15,12 C3.55271368e-15,15.18264 1.26468,18.2352 3.5148,20.4852 C5.76492,22.7352 8.81736,24 12,24 C15.18264,24 18.2352,22.73532 20.4852,20.4852 C22.7352,18.23508 24,15.18264 24,12 C24,8.81736 22.73532,5.7648 20.4852,3.5148 C18.23508,1.2648 15.18264,-3.55271368e-15 12,-3.55271368e-15 Z M17.28,7.92 L12,11.87064 L6.72,7.92 L17.28,7.92 Z M18,15.64776 C18,15.7743216 17.9446872,15.894312 17.85,15.976824 C17.7543744,16.059324 17.6278128,16.096824 17.503128,16.0799496 L6.479928,16.0799496 C6.352428,16.0940122 6.224928,16.0499496 6.13212,15.961824 C6.0402456,15.8727624 5.9914944,15.7471368 5.9999328,15.618696 L5.9999328,9.047736 L5.9999328,8.441184 L7.9536768,9.90744 L11.6398368,12.67224 C11.839524,12.8681784 12.1601568,12.8681784 12.3598368,12.67224 L17.8939968,8.51736 L17.9849352,8.44986 L17.9858726,8.45079768 C17.9914978,8.48548488 17.9952478,8.52111048 17.9971226,8.55579768 L17.9971226,15.6386777 L18,15.64776 Z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>gear</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12 10c-1.1 0-2 .9-2 2s.9 2 2 2 2-.9 2-2-.9-2-2-2zm7-7H5a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2V5a2 2 0 00-2-2zm-1.75 9c0 .23-.02.46-.05.68l1.48 1.16c.13.11.17.3.08.45l-1.4 2.42c-.09.15-.27.21-.43.15l-1.74-.7c-.36.28-.76.51-1.18.69l-.26 1.85c-.03.17-.18.3-.35.3h-2.8c-.17 0-.32-.13-.35-.29l-.26-1.85c-.43-.18-.82-.41-1.18-.69l-1.74.7c-.16.06-.34 0-.43-.15l-1.4-2.42a.353.353 0 01.08-.45l1.48-1.16c-.03-.23-.05-.46-.05-.69 0-.23.02-.46.05-.68l-1.48-1.16a.353.353 0 01-.08-.45l1.4-2.42c.09-.15.27-.21.43-.15l1.74.7c.36-.28.76-.51 1.18-.69l.26-1.85c.03-.17.18-.3.35-.3h2.8c.17 0 .32.13.35.29l.26 1.85c.43.18.82.41 1.18.69l1.74-.7c.16-.06.34 0 .43.15l1.4 2.42c.09.15.05.34-.08.45l-1.48 1.16c.03.23.05.46.05.69z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>info</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12 8.4A1.2 1.2 0 1012 6a1.2 1.2 0 000 2.4zM12 0c6.624 0 12 5.376 12 12s-5.376 12-12 12S0 18.624 0 12 5.376 0 12 0zm0 18c.66 0 1.2-.54 1.2-1.2V12c0-.66-.54-1.2-1.2-1.2-.66 0-1.2.54-1.2 1.2v4.8c0 .66.54 1.2 1.2 1.2z"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>kabob</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><circle cx="1.5" cy="1.5" r="1.5"/><circle cx="1.5" cy="5.5" r="1.5"/><circle cx="1.5" cy="9.5" r="1.5"/></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>light_bulb</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M11.585 31.056l8.38-.493v-.986l-8.38.493zM11.585 33.028L15.775 35l4.19-1.972V31.55l-8.38.493v.986zm6.926-.407l-2.736 1.29-2.13-1.004 4.866-.286zM15.775 7.394c-4.63 0-8.38 3.205-8.38 8.38 0 5.177 4.19 6.902 4.19 12.818v.493l8.38-.493c0-5.916 4.19-8.188 4.19-12.817a8.38 8.38 0 00-8.38-8.38zm5.617 13.48c-1.025 1.837-2.174 3.892-2.381 6.786l-6.44.38c-.129-3.01-1.29-5.021-2.32-6.808-.493-.8-.928-1.636-1.299-2.5h13.556c-.325.708-.704 1.403-1.116 2.142zm1.479-3.128H8.627a7.793 7.793 0 01-.247-1.971c0-4.353 3.042-7.395 7.395-7.395a7.394 7.394 0 017.394 7.395 6.739 6.739 0 01-.3 1.971h.002zM26.62 15.282h4.93v1h-4.93zM23.094 7.756l2.091-2.091.698.697-2.092 2.092zM15.282 0h1v4.93h-1zM5.666 6.362l.697-.697 2.091 2.091-.697.697zM0 15.282h4.93v1H0z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>link</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M2.28 12A3.723 3.723 0 016 8.28h4.8V6H6c-3.312 0-6 2.688-6 6s2.688 6 6 6h4.8v-2.28H6A3.723 3.723 0 012.28 12zm4.92 1.2h9.6v-2.4H7.2v2.4zM18 6h-4.8v2.28H18A3.723 3.723 0 0121.72 12 3.723 3.723 0 0118 15.72h-4.8V18H18c3.312 0 6-2.688 6-6s-2.688-6-6-6z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>magnifying_glass</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M16.124 13.051a5.154 5.154 0 110-10.308 5.154 5.154 0 010 10.308M16.114 0a7.886 7.886 0 00-6.46 12.407L0 22.06 1.94 24l9.653-9.653A7.886 7.886 0 1016.113 0"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>mic</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12 15c1.66 0 2.99-1.34 2.99-3L15 6c0-1.66-1.34-3-3-3S9 4.34 9 6v6c0 1.66 1.34 3 3 3zm5.3-3c0 3-2.54 5.1-5.3 5.1S6.7 15 6.7 12H5c0 3.41 2.72 6.23 6 6.72V22h2v-3.28c3.28-.48 6-3.3 6-6.72h-1.7z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>office</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12 7V3H2v18h20V7H12zM6 19H4v-2h2v2zm0-4H4v-2h2v2zm0-4H4V9h2v2zm0-4H4V5h2v2zm4 12H8v-2h2v2zm0-4H8v-2h2v2zm0-4H8V9h2v2zm0-4H8V5h2v2zm10 12h-8v-2h2v-2h-2v-2h2v-2h-2V9h8v10zm-2-8h-2v2h2v-2zm0 4h-2v2h2v-2z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>pantheon</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M9.947 16.598h.252V9.412h-.252a.432.432 0 01-.23-.065c-.07-.043-.106-.093-.106-.15L9.15 7.82v-.15c0-.044.028-.08.084-.109a.691.691 0 01.105-.086.254.254 0 01.146-.043H13.6c.056 0 .104.015.146.043.042.03.091.058.147.086a.271.271 0 01.063.108c.014.043.007.093-.02.15l-.42 1.378a.374.374 0 01-.147.15.37.37 0 01-.19.065h-.251v7.186h.252a.37.37 0 01.189.065c.07.043.119.093.147.15l.42 1.378c.027.028.034.071.02.129a.275.275 0 01-.063.129 1.364 1.364 0 00-.147.086.254.254 0 01-.146.043H9.485a.254.254 0 01-.146-.043.691.691 0 01-.105-.086c-.056-.029-.084-.072-.084-.13v-.128l.461-1.377c0-.058.035-.108.105-.151a.432.432 0 01.231-.065zm5.792 0h.252V9.412h-.252a.432.432 0 01-.23-.065.374.374 0 01-.148-.15l-.42-1.377c-.027-.029-.034-.072-.02-.13a.275.275 0 01.063-.129c.056-.028.105-.057.146-.086a.254.254 0 01.147-.043h4.114c.055 0 .104.015.146.043a.691.691 0 01.105.086c.056.03.084.072.084.13v.129l-.42 1.377a.374.374 0 01-.146.15.432.432 0 01-.231.065h-.21v7.186h.21a.43.43 0 01.23.065c.07.043.12.093.148.15l.42 1.378v.15c0 .043-.029.08-.085.108a.691.691 0 01-.105.086.254.254 0 01-.146.043h-4.114a.254.254 0 01-.147-.043 1.364 1.364 0 00-.146-.086.271.271 0 01-.063-.108c-.014-.043-.007-.093.02-.15l.42-1.377a.374.374 0 01.147-.151.432.432 0 01.231-.065zm-11.794-.086h.252V9.498h-.252a.334.334 0 01-.21-.065.386.386 0 01-.126-.193l-.42-1.377a.248.248 0 01-.02-.172.854.854 0 01.063-.173c.028-.057.07-.1.126-.129a.365.365 0 01.168-.043h4.07c.057 0 .113.015.169.043a.278.278 0 01.126.13.854.854 0 01.062.172.248.248 0 01-.02.172l-.42 1.377a.386.386 0 01-.126.193.334.334 0 01-.21.065h-.21v7.014h.21c.084 0 .154.029.21.086a.673.673 0 01.126.172l.42 1.378a.248.248 0 01.02.172.854.854 0 01-.062.172.278.278 0 01-.126.129.365.365 0 01-.168.043H3.526a.365.365 0 01-.168-.043.278.278 0 01-.126-.13.854.854 0 01-.063-.171.248.248 0 01.02-.172l.42-1.378a.673.673 0 01.126-.172.281.281 0 01.21-.086zM1.763 6.658a.717.717 0 01-.504-.194.644.644 0 01-.21-.495v-.43a.73.73 0 01.105-.387.68.68 0 01.273-.259C4.309 3.402 6.54 2.276 8.121 1.515 9.702.755 10.493.361 10.493.332c.531-.258.972-.366 1.322-.323.35.043.734.165 1.154.366l8.31 4.518c.14.058.245.144.315.259a.73.73 0 01.105.387v.43c0 .201-.07.366-.21.495a.717.717 0 01-.504.194H1.763zm-.714 13.34a.54.54 0 01.168-.387.516.516 0 01.378-.172h19.642c.168 0 .308.057.42.172a.541.541 0 01.168.387v.818a.522.522 0 01-.168.408.605.605 0 01-.42.151H1.595a.551.551 0 01-.378-.15.522.522 0 01-.168-.41v-.817zm21.405 2.022c.14 0 .266.058.378.173a.592.592 0 01.168.43v.818a.541.541 0 01-.168.387.516.516 0 01-.378.172L.546 23.957a.516.516 0 01-.378-.172.541.541 0 01-.168-.387v-.818a.59.59 0 01.168-.43.516.516 0 01.378-.173l21.908.043z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>person</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M9 9c2.486 0 4.5-2.014 4.5-4.5S11.486 0 9 0a4.499 4.499 0 00-4.5 4.5C4.5 6.986 6.514 9 9 9zm0 2.25c-3.004 0-9 1.508-9 4.5v1.125C0 17.494.506 18 1.125 18h15.75c.619 0 1.125-.506 1.125-1.125V15.75c0-2.992-5.996-4.5-9-4.5z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>phone</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M4.827 10.387a20.198 20.198 0 008.786 8.786l2.934-2.933c.36-.36.893-.48 1.36-.32a15.21 15.21 0 004.76.76c.733 0 1.333.6 1.333 1.333v4.654C24 23.4 23.4 24 22.667 24 10.147 24 0 13.853 0 1.333 0 .6.6 0 1.333 0H6c.733 0 1.333.6 1.333 1.333 0 1.667.267 3.267.76 4.76.147.467.04.987-.333 1.36l-2.933 2.934z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>pin</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="m9.375 0c-3.52446429 0-6.375 2.817-6.375 6.3 0 4.725 6.375 11.7 6.375 11.7s6.375-6.975 6.375-11.7c0-3.483-2.8505357-6.3-6.375-6.3zm.00000018 8.55000007c-1.25678576 0-2.27678579-1.008-2.27678579-2.25s1.02000003-2.25 2.27678579-2.25c1.25678572 0 2.27678582 1.008 2.27678582 2.25s-1.0200001 2.25-2.27678582 2.25z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>receipt</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M14.606 9.5c-.671-.515-1.591-.833-2.606-.833 1.015 0 1.935.318 2.606.833zm-7.985 0H1.655A1.66 1.66 0 010 7.833V3.667C0 2.747.741 2 1.655 2h20.69A1.66 1.66 0 0124 3.667v4.166A1.66 1.66 0 0122.345 9.5h-4.966V22H6.621V9.5h2.773H6.62zm10.758-1.667h4.966V3.667H1.655v4.166h4.966v-2.5h10.758v2.5z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>star</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M8.991 0C4.023 0 0 4.032 0 9s4.023 9 8.991 9C13.968 18 18 13.968 18 9s-4.032-9-9.009-9zm3.816 14.4L9 12.105 5.193 14.4l1.008-4.329-3.357-2.907 4.428-.378L9 2.7l1.728 4.077 4.428.378-3.357 2.907z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>support</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M12,0 C5.376,0 0,5.376 0,12 C0,18.624 5.376,24 12,24 C18.624,24 24,18.624 24,12 C24,5.376 18.624,0 12,0 Z M13,19 L11,19 L11,17 L13,17 L13,19 Z M15.07,11.25 L14.17,12.17 C13.45,12.9 13,13.5 13,15 L11,15 L11,14.5 C11,13.4 11.45,12.4 12.17,11.67 L13.41,10.41 C13.78,10.05 14,9.55 14,9 C14,7.9 13.1,7 12,7 C10.9,7 10,7.9 10,9 L8,9 C8,6.79 9.79,5 12,5 C14.21,5 16,6.79 16,9 C16,9.88 15.64,10.68 15.07,11.25 Z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>tag</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M17.469 8.622l-8.1-8.1A1.789 1.789 0 008.1 0H1.8C.81 0 0 .81 0 1.8v6.3c0 .495.198.945.531 1.278l8.1 8.1c.324.324.774.522 1.269.522a1.76 1.76 0 001.269-.531l6.3-6.3A1.76 1.76 0 0018 9.9c0-.495-.207-.954-.531-1.278zM3.15 4.5c-.747 0-1.35-.603-1.35-1.35 0-.747.603-1.35 1.35-1.35.747 0 1.35.603 1.35 1.35 0 .747-.603 1.35-1.35 1.35z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>thumb</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M15.273 1H5.455c-.906 0-1.68.55-2.008 1.342L.153 10.097A2.19 2.19 0 000 10.9v2.2c0 1.21.982 2.2 2.182 2.2h6.883L8.03 20.327l-.033.352c0 .451.186.869.48 1.166L9.633 23l7.178-7.249a2.16 2.16 0 00.644-1.551v-11c0-1.21-.982-2.2-2.182-2.2zm0 13.2l-4.735 4.774L11.75 13.1H2.182v-2.2l3.273-7.7h9.818v11zM19.636 1H24v13.2h-4.364V1z"></svg></div></td>
    </tr>
    <tr style="display: flex; justify-content: space-between; align-items: center;">
      <td>window</td>
      <td><div style="max-height: 2rem; max-width: 2rem;"><svg xmlns="http://www.w3.org/2000/svg"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"></svg></div></td>
    </tr>
  </tbody>
</table>
