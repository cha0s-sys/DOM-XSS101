#### [ Description ] : These vulnerabilities source the payload from a component of the address bar, usually the fragment, and use javascript sinks to trigger DOM based XSS.


#### [ Location.hash ]
 
#### 1.Location.hash - assign - assign
#### 2.Vulnerable Code : 
 <script>
var payload = window.location.hash.substr(1);window.location.assign(payload);
 </script>
#### 3: source : window.location.hash.substd(1) 
//This source extracts the fragments part from the URL and define as variable payload(The portion after the # sign):


####  sink   : window.location.assign(payload) 
// This sink is use to redirect the browser to a new URL defined by the payload variable :

#### 4: Exploit : So we Can Exploit Open Redirect and DOM XSS by using this source and sink :
#### 5: POC ::

//https://public-firing-range.appspot.com/address/location.hash/assign#javascript:alert(1);//

//https://public-firing-range.appspot.com/address/location.hash/assign#//evil.com
