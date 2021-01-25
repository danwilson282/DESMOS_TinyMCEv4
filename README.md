# DESMOS_TinyMCEv4
DESMOS plugin for TinyMCE

This plugin will allow you to insert a screenshot of a DESMOS graph or equation into TinyMCE V4.Once imported, both will behave as images and can be formatted in the usual way. You have full access to all the DESMOS calculator settings, and can change the canvas size before taking the snapshot.

Instructions:
1) Copy the desmos folder into the plugins subfolder of TinyMCE
2) Enable the plugin using the following lines of code between the <HEAD> headers of your HTML page
  
  
  <script src="js/tinymce/tinymce.min.js" referrerpolicy="origin"></script>
  <script src="https://www.desmos.com/api/v1.5/calculator.js?apiKey=dcb31709b452b1cf9dc26972add0fda6"></script>

  <script>
  tinymce.init({ 
selector: "textarea",  // change this value according to your HTML
            //toolbar: "image, paste, formula, save, table",
            toolbar: "desmos",
            plugins: "desmos",
            menubar: "insert ,edit, chart, tools",
            paste_data_images: true
});
  </script>
