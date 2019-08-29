<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#000">
<meta name="apple-mobile-web-app-status-bar-style" content="#000">
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<style>
body{
  background-color: #000;
}
#loader {
  position: absolute;
  left: 50%;
  top: 50%;
  z-index: 1;
  width: 150px;
  height: 150px;
  margin: -75px 0 0 -75px;
  border: 16px solid #f3f3f3;
  border-radius: 50%;
  border-top: 16px solid #3498db;
  width: 120px;
  height: 120px;
  -webkit-animation: spin 2s linear infinite;
  animation: spin 2s linear infinite;
}

@-webkit-keyframes spin {
  0% { -webkit-transform: rotate(0deg); }
  100% { -webkit-transform: rotate(360deg); }
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>
</head>
<body>
<script type="text/javascript">
$.get("https://cors-anywhere.herokuapp.com/https://izleknk.com/").then(function(data){
  window.location.href = 'https://'+$(data).find('#siteadresi').text();
});
// Yedek
setTimeout(function(){
$.get("https://jsonp.afeld.me/?url=https://izleknk.com/").then(function(data){
  window.location.href = 'https://'+$(data).find('#siteadresi').text();
}); }, 3000);
</script>
<div id="loader"></div>

</body>
</html>
