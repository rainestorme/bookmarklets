# Bookmarklets

## Bypasses

Ingot - Disable any extension easily!

```
javascript:(function () {var a = document.createElement('script');a.src = 'https://cdn.jsdelivr.net/gh/FogNetwork/Ingot/ingot.min.js';document.body.appendChild(a);}())
```

Porta-UV - Spawn an ultraviolet proxy window on-demand on any site!

```
javascript:(function()%7Bvar iframe %3D document.createElement("iframe")%3B%0Aiframe.style%3D"position%3Afixed%3Btop%3A0%3Bleft%3A0%3Bbottom%3A0%3Bright%3A0%3B width%3A100%25%3Bheight%3A100%25%3Bborder%3Anone%3Bmargin%3A0%3Bpadding%3A0%3Boverflow%3Ahidden%3Bz-index%3A999999%3B"%3B%0Aiframe.src%3D"https%3A%2F%2Fuv.piesoftwaredev.repl.co%2F"%3B%0Adocument.body.appendChild(iframe)%3B%7D)()%3B
```

GoGuardian Block Bypass - Will prevent your tabs from being closed by GoGuardian

```
javascript:(function() {window.onbeforeunload=function() {return false;}})()
```

Google Drive Cloak - A tab cloak to make any tab look like google drive

```
javascript:(function() {var link = document.querySelector("link[rel*='icon']") || document.createElement('link');link.type = 'image/x-icon';link.rel = 'shortcut icon';link.href = 'https://ssl.gstatic.com/docs/doclist/images/infinite_arrow_favicon_5.ico';document.title = 'My Drive - Google Drive';console.log(document.title);document.getElementsByTagName('head')[0].appendChild(link);})();
```

Vapor - A bookmarklet multitool

```
javascript:(function () {var a = document.createElement('script');a.src = 'https://cdn.jsdelivr.net/gh/FogNetwork/Vapor/vapor.min.js';document.body.appendChild(a);}())
```

## Enhancements

Zap Cheap Effects - Gets rid of deprecated html effects like the marquee and blink tags and replaces them with modern elements

```
javascript:(function(){var d=document; function K(N,w) { var nn = d.createElement(w), C = N.childNodes, i; for(i=C.length-1;i>=0;--i) nn.insertBefore(C[i],nn.childNodes[0]); N.parentNode.replaceChild(nn,N); } function Z(t,w) { var T = document.getElementsByTagName(t), j; for (j=T.length-1;j>=0;--j) K(T[j],w); } Z("blink", "span"); Z("marquee", "div"); })();
```

Hypothesis - A very nice-looking annotation and note-taking system for websites

```
javascript:(function(){window.hypothesisConfig=function(){return{showHighlights:true,appType:'bookmarklet'};};var d=document,s=d.createElement('script');s.setAttribute('src','https://hypothes.is/embed.js');d.body.appendChild(s)})();
```

Dark Mode Anywhere - A portable version of Dark Reader that works in a bookmarklet

```
javascript:(function()%7Bfunction callback()%7BDarkReader.enable(%7Bbrightness%3A 100%2Ccontrast%3A 90%2Csepia%3A 2%7D)%7Dvar s%3Ddocument.createElement("script")%3Bs.src%3D"https%3A%2F%2Fcdn.jsdelivr.net%2Fnpm%2Fdarkreader%404.9.39%2Fdarkreader.min.js"%3Bif(s.addEventListener)%7Bs.addEventListener("load"%2Ccallback%2Cfalse)%7Delse if(s.readyState)%7Bs.onreadystatechange%3Dcallback%7Ddocument.body.appendChild(s)%3B%7D)()
```

Adblock - Blocks a good amount of ads

```
javascript:(function(){function R(w){try{var d=w.document,j,i,t,T,N,b,r=1,C;for(j=0;t=["object","embed","applet","iframe"][j];++j){T=d.getElementsByTagName(t);for(i=T.length-1;(i+1)&&(N=T[i]);--i)if(j!=3||!R((C=N.contentWindow)?C:N.contentDocument.defaultView)){b=d.createElement("div");b.style.width=N.width; b.style.height=N.height;b.innerHTML="<del>"+(j==3?"third-party "+t:t)+"</del>";N.parentNode.replaceChild(b,N);}}}catch(E){r=0}return r}R(self);var i,x;for(i=0;x=frames[i];++i)R(x)})()
```

Music Player - Plays and finds music in a very hacky way by scraping google and ftp archives for directory listings with music.

```
javascript:var e,t,n=document.links,i=[],o=0;for(t in n){var a=n[t].toString().toUpperCase();0==a.indexOf("JAVASCRIPT:")||-1==a.indexOf(".MP3")&&-1==a.indexOf(".OGG")&&-1==a.indexOf(".WAV")&&-1==a.indexOf(".M4A")||i.push(n[t])}if(0==i.length)w(prompt("No songs detected on the current page. What type of music would you like to hear?","okgo"));else{var d=x("div","player","","",""),r=x("div","playing","","",""),p=x("div","progressbar","","",function(t){var n=t.clientX;n/=window.innerWidth,e.currentTime=e.duration*n}),l=x("div","progress","","","");p.appendChild(l),r.appendChild(p);var s=x("div","songname","","","");r.appendChild(s);var u=x("div","buttons","","","");u.appendChild(x("button","","|◀","",y)),u.appendChild(x("button","","||","",function(){e.paused?(e.play(),this.innerHTML="||"):(e.pause(),this.innerHTML="▶")})),u.appendChild(x("button","","▶|","",C)),u.appendChild(x("button","","⤭","",function(){o=Math.floor(Math.random()*i.length),f()})),u.appendChild(x("button","","⌕","",function(){w(prompt("What type of music would you like to hear?","okgo"))})),r.appendChild(u),d.appendChild(r);var c=x("ul","playlist","","","");for(songIndex in i){var h=decodeURIComponent(unescape(i[songIndex].href));c.appendChild(x("li","",h.substring(h.lastIndexOf("/")+1),songIndex,function(){o=parseInt(this.getAttribute("data")),f()}))}d.appendChild(c);var g=x("style","","","","");g.innerHTML=".player{position:absolute;bottom:0;left:0;right:0;background:grey;font-size:x-large;color:#87ceeb;text-shadow:0 1px 1px #000;font-family:courier;font-weight:700}.playing{width:100%;height:160px}.playlist{position:fixed;top:0;bottom:170px;width:100%;background:grey;box-sizing:border-box;margin:0;overflow:scroll}.progressbar{position:relative;height:40px;margin:10px;border-radius:20px;text-align:center;overflow:hidden;border:1px solid #555}.progress{position:relative;width:99%;height:40px;background:#87ceeb}.songname{height:40px;width:100%;text-align:center;white-space:nowrap}.buttons{height:60px;width:100%;text-align:center}.player button{background:0 0;border:none;font-size:40px;color:#87ceeb;text-shadow:0 1px 1px #000}",d.appendChild(g);var m=document.createElement("meta"),b=document.createAttribute("name");b.value="viewport",m.setAttributeNode(b),(b=document.createAttribute("content")).value="width=device-width, initial-scale=1",m.setAttributeNode(b),document.head.appendChild(m),document.body.innerHTML="",document.body.appendChild(d),(e=new Audio).addEventListener("ended",C,!1),v(),f(),navigator.mediaSession.setActionHandler("previoustrack",y),navigator.mediaSession.setActionHandler("nexttrack",C)}function f(){e.src=i[o],e.play();var t=decodeURIComponent(i[o].href);s.innerHTML=t.substring(t.lastIndexOf("/")+1),navigator.mediaSession.metadata=new MediaMetadata({title:s.innerHTML})}function x(e,t,n,i,o){var a=document.createElement(e);""!=t&&a.classList.add(t);var d=document.createAttribute("data");return d.value=i,a.setAttributeNode(d),a.appendChild(document.createTextNode(n)),a.onclick=o,a}function v(){l.style.width=e.currentTime/e.duration*100+"%",requestAnimationFrame(v)}function w(e){e&&window.open('https://www.google.com/search?q=intitle:"index.of" (wma|mp3|midi) '+e,"_self")}function y(){o>0?o--:o=i.length-1,f()}function C(){o<i.length-1?o++:o=0,f()}
```

Coolmath Hax - Skips the ads before a coolmathgames game and enables fullscreen for free

```
javascript:(function () {var script = document.createElement("script");script.src = "https://cdn.jsdelivr.net/gh/j-a-13/cmg-hacks/cmg-hacks/hacks.js";document.body.append(script);}())
```

### Desmos Enhancements

Clean Desmos - Cleans up the UI a bit

```
javascript:(function() {var appendtext = "nozoomButtons&nokeypad&nosettingsMenu&nobranding&noexpressionsTopbar";if ((window.location.href).indexOf("?") >= 0) {window.location.href = window.location.href + %27&%27+appendtext;} else {window.location.href = window.location.href + %27?%27+appendtext;}})();
```

Discord Theme - Makes Desmos look like Discord

```
javascript:(function() {var appendtext = "backgroundColor=4f5666&textColor=abb2bf";if ((window.location.href).indexOf("?") >= 0) {window.location.href = window.location.href + %27&%27+appendtext;} else {window.location.href = window.location.href + %27?%27+appendtext;}})();
```

SimulationFPS - Shows the FPS of the graph

```
javascript:(function() {var appendtext = "simulationFPS";if ((window.location.href).indexOf("?") >= 0) {window.location.href = window.location.href + %27&%27+appendtext;} else {window.location.href = window.location.href + %27?%27+appendtext;}})();
```

### Google Docs Enhancements

```
javascript:function linkster%28text%2Cdata%29%7Breturn %27<a href%3D%5C"%27%2Bdata%2B%27%5C">%27%2Btext%2B%27<%2Fa><br>%5Cn%27%3B%7D%3Bfunction jster%28url%29%7Bvar out%3D%27javascript%3A%28function%28%29%7B%27%3Bout%2B%3D%27var href%3Dwindow.location.href%3B%27%3Bout%2B%3D%27var d%3Dnew Date%28%29%3B%27%3Bout%2B%3D%27var curr_date%3Dd.getDate%28%29%3B%27%3Bout%2B%3D%27var curr_day%3Dd.getDay%28%29%3Bcurr_day%2B%2B%3B%27%3Bout%2B%3D%27if %28curr_day.toString%28%29.length%3D%3D1%29%7Bcurr_day%3D%5C%270%5C%27%2Bcurr_day.toString%28%29%3B%7D%3B%27%3Bout%2B%3D%27var curr_month%3Dd.getMonth%28%29%3Bcurr_month%2B%2B%3B%27%3Bout%2B%3D%27if %28curr_month.toString%28%29.length%3D%3D1%29%7Bcurr_month%3D%5C%270%5C%27%2Bcurr_month.toString%28%29%3B%7D%3B%27%3Bout%2B%3D%27var curr_year%3Dd.getFullYear%28%29%3B%27%3Bout%2B%3D%27var dstr%3Dcurr_year%2B%5C%27-%5C%27%2Bcurr_month%2B%5C%27-%5C%27%2Bcurr_date%3B%27%3Bout%2B%3D%27var url%3D%5C%27%27%2Burl%2B%27%5C%27%2Bdstr%3B%27%3Bout%2B%3D%27var o%3Dwindow.open%28%5C%27%5C%27%2C%5C%27_blank%5C%27%29%3B%27%3Bout%2B%3D%27o.location.href%3Durl%3B%27%3Bout%2B%3D%27%7D%29%28%29%3B%27%3Bout%2B%3D%27%27%3Breturn out%3B%7D%3B%28function%28%29%7Bvar href%3Dwindow.location.href%3Bvar str%3D%27<html><body><h2>URL%3A %27%2Bhref%2B%27<%2Fh2>%5Cn%27%3Bvar d%3Dnew Date%28%29%3Bvar curr_date%3Dd.getDate%28%29%3Bvar curr_day%3Dd.getDay%28%29%3Bcurr_day%2B%2B%3Bif %28curr_day.toString%28%29.length%3D%3D1%29%7Bcurr_day%3D%270%27%2Bcurr_day.toString%28%29%3B%7D%3Bvar curr_month%3Dd.getMonth%28%29%3Bcurr_month%2B%2B%3Bif %28curr_month.toString%28%29.length%3D%3D1%29%7Bcurr_month%3D%270%27%2Bcurr_month.toString%28%29%3B%7D%3Bvar curr_year%3Dd.getFullYear%28%29%3Bvar dstr%3Dcurr_year%2B%27-%27%2Bcurr_month%2B%27-%27%2Bcurr_date%3Bvar TemplateID%3D%271l05Zm9pa9XtunhyiraozYh0EJ1cRrKledaceSOjWkd8%27%3Bvar longre%3D%2F%5Ehttps%5C%3A%5C%2F%5C%2Fdrive%5C.google%5C.com%5C%2Fdrive%5C%2F%28u%5C%2F0%5C%2F%29%3Ffolders%2Fi%3Bif %28href.match%28longre%29%29%7Bvar re%3D%27folders%2F%28%5B%5E%5C%2F%5D%2B%29%27%3Bvar found%3Dhref.match%28re%29%3Bvar FOLDER_ID%3Dfound%5B1%5D%3Bstr%2B%3D%27<p>Google drive folder%3A %27%2BFOLDER_ID%2B%27<%2Fp>%5Cn%27%3Bstr%2B%3D%27<p>Source%3A %27%2Blinkster%28href%2C%27Google drive folder%27%29%2B%27<%2Fp>%5Cn%27%3Bstr%2B%3D%27<p>Please note%3A Adding titles to Google sheets via links does not work %28last tested March 2018%29. It is included here in case it starts working in the future.<%2Fp>%5Cn%27%3Bvar doctemplate%3D%27%27%3Bstr%2B%3D%27<h3>Draggable links - javascript %28adds dynamic date at time of click%3Btitle%3A X_date%29<%2Fh3>%5Cn%27%3Bstr%2B%3Dlinkster%28%27%2Bdoc%27%2Cjster%28%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNotes %27%29%29%3Bstr%2B%3Dlinkster%28%27%2Bsheet%27%2Cjster%28%27https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DSheet %27%29%29%3Bstr%2B%3Dlinkster%28%27%2Bpres%27%2Cjster%28%27https%3A%2F%2Fdocs.google.com%2Fpresentation%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DSlides  %27%29%29%3Bstr%2B%3Dlinkster%28%27%2Bdraw%27%2Cjster%28%27https%3A%2F%2Fdocs.google.com%2Fdrawings%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DDrawing  %27%29%29%3Bstr%2B%3Dlinkster%28%27%2BdocT%27%2Cjster%28%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F%27%2BTemplateID%2B%27%2Fcopy%3Fid%3D%27%2BTemplateID%2B%27%26copyCollaborators%3Dfalse%26copyComments%3Dfalse%26usp%3Ddocs_web%27%2B%27%26copyDestination%3D%27%2BFOLDER_ID%2B%27%26title%3DNotes %27%29%29%3Bstr%2B%3D%27<h3>Draggable links - plain html<%2Fh3>%5Cn%27%3Bstr%2B%3D%27<h4>Draggable links %28plain html%2C tite%3A New_X%29<%2Fh4>%5Cn%27%3Bstr%2B%3Dlinkster%28%27%2Bdoc%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNew_Notes%27%29%3Bstr%2B%3Dlinkster%28%27%2Bsheet%27%2C%27https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNew_Sheet%27%29%3Bstr%2B%3Dlinkster%28%27%2Bpres%27%2C%27https%3A%2F%2Fdocs.google.com%2Fpresentation%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNew_Slides %27%29%3Bstr%2B%3Dlinkster%28%27%2Bdraw%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdrawings%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNew_Drawing %27%29%3Bstr%2B%3Dlinkster%28%27%2BdocT%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F%27%2BTemplateID%2B%27%2Fcopy%3Fid%3D%27%2BTemplateID%2B%27%26copyCollaborators%3Dfalse%26copyComments%3Dfalse%26usp%3Ddocs_web%27%2B%27%26copyDestination%3D%27%2BFOLDER_ID%2B%27%26title%3DNotes %27%2Bdstr%29%3Bstr%2B%3D%27Template%3A %27%2Blinkster%28%27%28here%29%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F%27%2BTemplateID%2B%27%2Fedit%27%29%2B%27<br>%5Cn%27%3Bstr%2B%3D%27<h4>For use now%2C with current date%2C unchanging%3Btitle%3A X_%27%2Bdstr%2B%27%3A<%2Fh4>%5Cn%27%3Bstr%2B%3Dlinkster%28%27%2Bdoc%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DNotes %27%2Bdstr%29%3Bstr%2B%3Dlinkster%28%27%2Bsheet%27%2C%27https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DSheet %27%2Bdstr%29%3Bstr%2B%3Dlinkster%28%27%2Bpres%27%2C%27https%3A%2F%2Fdocs.google.com%2Fpresentation%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DSlides %27%2Bdstr%29%3Bstr%2B%3Dlinkster%28%27%2Bdraw%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdrawings%2Fcreate%3Fhl%3Den%26folder%3D%27%2BFOLDER_ID%2B%27%26title%3DDrawing %27%2Bdstr%29%3Bstr%2B%3Dlinkster%28%27%2BdocT%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F%27%2BTemplateID%2B%27%2Fcopy%3Fid%3D%27%2BTemplateID%2B%27%26copyCollaborators%3Dfalse%26copyComments%3Dfalse%27%2B%27%26copyDestination%3D%27%2BFOLDER_ID%2B%27%26title%3DNotes %27%2Bdstr%29%3Bstr%2B%3D%27Template%3A %27%2Blinkster%28%27%28here%29%27%2C%27https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F%27%2BTemplateID%2B%27%2Fedit%27%29%2B%27<br>%5Cn%27%3Bstr%2B%3D%27<h4>Folder download %28doesnt work in March 2018%2C apparently worked in 2014%29<%2Fh4>%5Cn%27%3Bstr%2B%3Dlinkster%28%27Download folder%27%2C%27https%3A%2F%2Fdrive.google.com%2Fuc%3Fexport%3Ddownload%26id%3D%27%2BFOLDER_ID%2B%27%27%29%3B%7Delse if %28href.match%28%2F%5Ehttps%5C%3A%5C%2F%5C%2Fdocs%5C.google%5C.com%2F%29%29%7Bstr%2B%3D%27<p>Google docs%2Fsheets%2Fslides<%2Fp>%5Cn%27%3Bstr%2B%3D%27<p>Source%3A %27%2Blinkster%28href%2C%27Google doc%2Fsheet%2Fslide%27%29%2B%27<%2Fp>%5Cn%27%3Bstr%2B%3D%27<p>Export%3A<%2Fp>%5Cn%27%3Bvar re%3D%27%2Fd%2F%28%5B%5E%5C%2F%5D%2B%29%27%3Bvar found%3Dhref.match%28re%29%3Bvar FILE_ID%3Dfound%5B1%5D%3Bvar formats%3D%5B%5D%3Bvar type%3D%27%27%3Bif %28href.match%28%27%2Fdocument%7Cspreadsheets%2F%27%29%29%7Bvar gid%3D%27%27%3Bvar gidx%3D%27%27%3Bif %28href.match%28%27%2Fdocument%2F%27%29%29%7Bformats%3D%5B%27doc%27%2C%27odt%27%2C%27rtf%27%2C%27pdf%27%2C%27txt%27%2C%27html%27%2C%27epub%27%5D%3Btype%3D%27document%27%3B%7Delse if %28href.match%28%27%2Fspreadsheets%2F%27%29%29%7Btype%3D%27spreadsheets%27%3Bformats%3D%5B%27xlsx%27%2C%27ods%27%2C%27pdf%27%2C%27csv%27%2C%27tsv%27%5D%3Bvar re%3D%2Fgid%3D%28%5Cd%2B%29%2Fi%3Bvar found%3Dhref.match%28re%29%3Bif %28found%29%7Bformats%3D%5B%27xlsx%27%2C%27ods%27%2C%27pdf%27%2C%27csv%27%2C%27tsv%27%5D%3Bgid%3D%27%28sheet%3A %27%2Bfound%5B1%5D%2B%27%29 %27%3Bgidx%3D%27%26%27%2Bfound%5B0%5D%3B%7Delse%7B%7Dfor %28var i%3D0%3Bi < formats.length%3Bi%2B%2B%29%7Bstr%2B%3Dlinkster%28%27Export Google %27%2Btype%2B%27 %27%2Bgid%2B%27as %27%2Bformats%5Bi%5D%2C%27https%3A%2F%2Fdocs.google.com%2F%27%2Btype%2B%27%2Fd%2F%27%2BFILE_ID%2B%27%2Fexport%3Fformat%3D%27%2Bformats%5Bi%5D%2Bgidx%29%3B%7Dformats%3D%5B%27xlsx%27%2C%27ods%27%2C%27pdf%27%5D%3Bgid%3D%27%28all sheets%29 %27%3Bgidx%3D%27%27%3B%7Dfor %28var i%3D0%3Bi < formats.length%3Bi%2B%2B%29%7Bstr%2B%3Dlinkster%28%27Export Google %27%2Btype%2B%27 %27%2Bgid%2B%27as %27%2Bformats%5Bi%5D%2C%27https%3A%2F%2Fdocs.google.com%2F%27%2Btype%2B%27%2Fd%2F%27%2BFILE_ID%2B%27%2Fexport%3Fformat%3D%27%2Bformats%5Bi%5D%2Bgidx%29%3B%7D%7Delse if %28href.match%28%27%2Fpresentation%2F%27%29%29%7Btype%3D%27presentation%27%3Bformats%3D%5B%27pptx%27%2C%27odp%27%2C%27pdf%27%2C%27txt%27%5D%3Bfor %28var i%3D0%3Bi < formats.length%3Bi%2B%2B%29%7Bstr%2B%3Dlinkster%28%27Export Google %27%2Btype%2B%27 as %27%2Bformats%5Bi%5D%2C%27https%3A%2F%2Fdocs.google.com%2F%27%2Btype%2B%27%2Fd%2F%27%2BFILE_ID%2B%27%2Fexport%2F%27%2Bformats%5Bi%5D%29%3B%7Dstr%2B%3D%27Additional formats jpg%2C png%2C svg require google apps script. https%3A%2F%2Fstackoverflow.com%2Fquestions%2F31662455%2Fhow-to-download-google-slides-as-images%27%3B%7Dif %28type%3D%3D%3D%27%27%29%7Bstr%2B%3D%27Sorry%2C this bookmarklet will only work on Google Drive%2FDocs%2FSheet%2FPresentations pages.%27%3B%7D%3B%7Delse%7Bstr%2B%3D%27Sorry%2C this bookmarklet will only work on Google Drive%2FDocs%2FSheet%2FPresentations pages.%27%3B%7D%3Bstr%2B%3D%27<p>To find out more%2C visit <a href%3D%5C%27https%3A%2F%2Fbjohas.de%2Fgo%2Fgoogle-docs-helper-bookmarklet%5C%27>https%3A%2F%2Fbjohas.de%2Fgo%2Fgoogle-docs-helper-bookmarklet<%2Fa>.<%2Fp>%27%3Bvar o%3Dwindow.open%28%27%27%2C%27_blank%27%29%3Bvar newdoc%3Do.document%3Bnewdoc.write%28str%29%3Bnewdoc.close%28%29%3B%7D%29%28%29%3B
```
