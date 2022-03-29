# insta-follow-request-remove-script

- Open below link

https://www.instagram.com/accounts/access_tool/current_follow_requests

- Past below code in browser console 
```
var i = 0;
var unfollow = "global";
var final = "global";
var link = ["link", "link2"];
var proWindow = [""]
proWindow.length = 0
link.length = 0;
function sleep(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
  }
var ids = document.querySelectorAll(".-utLf");
for (i = 0; i < ids.length; i++) {
  //  for (i = ids.length-1; i !=0; i--) {
    link.push('https://www.instagram.com/' + ids[i].innerText + '/');
    console.log(link[i]);
    proWindow[i] = window.open(link[i]);
    await sleep(6000);
//}
//for(i=0;i<ids.length;i++)
try {
    unfollow = proWindow[i].document.querySelector("button._8A5w5");
    unfollow.click();
    final = proWindow[i].document.querySelector(".aOOlW");
    final.click();
    await sleep(1000);
}

catch(e) {
   console.log(e);
}
    proWindow[i].close();

    }
    
   console.log("Completed"); 
   ```
