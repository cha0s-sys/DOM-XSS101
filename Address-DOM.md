#Location.hash

1.Location.hash - assign - assign
2.Vulnerable Code : 
<script>
var payload = window.location.hash.substr(1);window.location.assign(payload);
</script>
3: source : window.location.hash.substd(1)
   sink   : window.location.assign(payload)

4: Exploit :   
