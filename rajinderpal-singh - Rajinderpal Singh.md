# Developer – Winter of Code (WoC) 2020
---
##### **Rajinderpal Singh**
## DSC-X : [OMG-Frames](https://sairish2001.github.io/omgframestesting.github.io/)

OMG-Frames aims to Generate Badges for the events that happens for across the Student Clubs, or any other events.My work is to create a Frontend for the entire project mainly Dashboard.
>**Apart from my work, I added new features which I thought to be in for better user experience.**

I am **[Rajinderpal Singh](https://github.com/sairish2001/)** ,an undergraduate student from **[Guru Nanak Dev University,Amritsar,](http://www.gndu.ac.in/)** as part of Winter of Code.This project was mentored by **[Anubhav Singh](https://github.com/xprilion/)**.

## Contributions
Contributions are outlined as follows:

 - 20 [commits](https://github.com/dsc-x/omg-frames/commits/develop) (approx.) are made into the develop branch of OMG-Frames

- Total of 3 Pull Requests made and got merged in develop branch.

    - First Pull Request
 ![First Pull Request](https://i.imgur.com/QR3CiKv.png) [#PR-6](https://github.com/dsc-x/omg-frames/pull/5)

    - Second Pull Request ![Second Pull Request](https://i.imgur.com/EaHvExN.png) [#PR-8](https://github.com/dsc-x/omg-frames/pull/8)

    - Total ![Total](https://i.imgur.com/LAaiWWz.png)

- Created 2 Issues in API Repository.
    - Fogot Password? API wanted [{#14}](https://github.com/dsc-x/omg-frames-api/issues/14)
    - Delete Frame API [{#11}](https://github.com/dsc-x/omg-frames-api/issues/11)

- Closed 2 Issues, by working on it.
    - Dashboard UI [{#3}](https://github.com/dsc-x/omg-frames/issues/3)
    - Performance issue in `gallery.html` page [{#9}](https://github.com/dsc-x/omg-frames/issues/9)
- Created 3 issues in omg-frames Repository
    - Implement update frame API [{#11}](https://github.com/dsc-x/omg-frames/issues/11)
    - Design a Favicon [{#12}](https://github.com/dsc-x/omg-frames/issues/12)
    - Make Share button Working [{#13}](https://github.com/dsc-x/omg-frames/issues/13)
- 10 (approx.) New Features

## New Features
- Created Frontend
    - [Bootstrap Framework](https://getbootstrap.com/) for responsive website 
    - [index.html](https://github.com/dsc-x/omg-frames/blob/develop/index.html), [dashboard.html](https://github.com/dsc-x/omg-frames/blob/develop/dashboard.html), [gallery.html](https://github.com/dsc-x/omg-frames/blob/develop/gallery.html), [forgotpassword.html](https://github.com/dsc-x/omg-frames/blob/develop/forgotpassword.html), [reset.html](https://github.com/dsc-x/omg-frames/blob/develop/reset.html)
    - CSS files for each page [{css/}](https://github.com/dsc-x/omg-frames/tree/develop/css)
    
    - [{JS/}](https://github.com/dsc-x/omg-frames/tree/develop/js) files([main.js](https://github.com/dsc-x/omg-frames/blob/develop/js/main.js),[imageedit.js](https://github.com/dsc-x/omg-frames/blob/develop/js/imageedit.js), [loginsignup.js](https://github.com/dsc-x/omg-frames/blob/develop/js/loginsignup.js)), the `main.js` contains all the required functions, the `imageedit.js` contains implementation of crop feature into dashboard, and `loginsignup.js` contains all functions which has link with Backend in someway, along with all functions for AJAX request.
- Functionality added [{see working}](https://sairish2001.github.io/omgframestesting.github.io/)
    - Crop feature [Croppie.js](https://foliotek.github.io/Croppie/). Now user can crop it's Picture after selecting.

    - [Customized Croppie.js](https://github.com/dsc-x/omg-frames/blob/develop/js/croppie.js) for showing instant result on canvas (oninput/onchange)
    
    - **Generate Strong Password** (12 characters long, includes alphabets, numbers, special characters), it generates a strong password and insert automatically into password field [{ function generatepassword() }](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/main.js#L197)
    ![generatepassword](https://i.imgur.com/8ruldPM.png)
    
    - Fullscreen mode, now user can experience fullscreen feature.[{ function enablefullscreen() }](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/main.js#L224)

    - User can see it’s Account information by clicking on My Account button in navbar (email, name, organization,role).
    
    - Colored custom popups for displaying response message after fetching from API request, just call `alertpopup(message,'open',colorofpopup);`.Red(`#dc3545`) on error, Green(`#28a745`) on success.[{ function alertpopup() }](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/main.js#L186)
    ![popups](https://i.imgur.com/9qBVSu7.png)

    - `loader()` function, to show/hide loading animation, just call `loader(‘show’)` or `loader(‘hide’)`[{ function loader() }](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/main.js#L88)
    
    - Light/Dark  Mode (index.html, dashboard.html, gallery.html), set mode in any page, will be applied to all pages automatically.
    ![lightdark](https://i.imgur.com/gwKAX24.jpg)
    
    - Show/Hide Password.[{ function showpassword() }](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/main.js#L210) in Login/SignUp form.
    
    - Form validation [(jQuery form validation)](https://jqueryvalidation.org/) with custom error messages and color 
    
    - [Download or Delete](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L190) Saved frames by hovering on fetched frames in gallery.html.
    ![gallerypage](https://i.imgur.com/j8Bm0R1.jpg)

    - Customized Bootstrap’s buttons, input field’s classes according to wireframe design.

    - Changed SVG logo to PNG (by making it’s background transparent) [{logo.png}](https://github.com/dsc-x/omg-frames/blob/develop/images/logo.png)                                
    - Changed Black color to white of logo for dark mode.[{logodark.png}](https://github.com/dsc-x/omg-frames/blob/develop/images/logodark.png)
    
    - As per requirement, user cannot use dashboard or visit gallery **without logging in**.
    
    - Created other required functions for proper working of project [{ js/ }](https://github.com/dsc-x/omg-frames/tree/develop/js)
        - `createordestroybutton()` for creating and destroying **Login/Logout button**.
        
        - `dashboardandgallerybutton()` for creating/destroying **View Dashboard and Gallery button** if Logged in and **Get Started button** if not Logged in.
        
        - Other functions for toggle closing/opening of Content.[{ main.js }](https://github.com/dsc-x/omg-frames/blob/develop/js/main.js)
        
        - Many More

    - Implemented All available API’s [{ loginsignup.js }](https://github.com/dsc-x/omg-frames/blob/develop/js/loginsignup.js)
        - [Login](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L117)
        - [Sign Up](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L68)
        - [Save Frame](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L246)
        - [Get Frame](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L219)
        - [Delete Frame](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L162)
        - [Send-reset-email](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L280)
        - [Update-password](https://github.com/dsc-x/omg-frames/blob/6c1e9c40dfcd8e21980094d9291784da1c7b6612/js/loginsignup.js#L309)

## Future Scope
Here is a list for future developers. 
- Use [`frabric.js`](http://fabricjs.com/) for live editing on  canvas.
- Make frames fully customized so that user can change Event Text(Attendee, Speaker,etc.) , and can also change logo.
- Other editing features like Brightness, Contrast,etc. along with filters(for filters I suggest [CSSgram](https://una.im/CSSgram/)).

- Drag,Transform, contents inside canvas.

- Enable user to download the frame in different Resolutions

Feel free to come up with new ideas yourself.

## Acknowledgments
I would like to express my gratitude to [Anubhav Singh](https://github.com/xprilion) for his patient guidance and thanks for going through all my PR's.
I would also like to thank [Awantika Nigam](https://github.com/awantika10) and [Arnab Sen](https://github.com/arnabsen1729),they are the main source of configuring bugs regarding new Pull Request. It has been a great experience working at OMG-Frames!.


WoC with DSC-X was a warm and unforgettable experience for me. Everytime I talk of Open Source, OMG-Frames will be remembered fondly.
