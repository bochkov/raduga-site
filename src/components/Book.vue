<template>
  <div style="margin: 0px;">
    <iframe id="my-iframe-id" src style="border: 0;" width="100%" scrolling="no"></iframe>
  </div>
</template>

<script>
export default {
  created: function() {
    var myEventMethod = window.addEventListener
      ? "addEventListener"
      : "attachEvent";
    var myEventListener = window[myEventMethod];
    var myEventMessage =
      myEventMethod == "attachEvent" ? "onmessage" : "message";
    myEventListener(
      myEventMessage,
      function(e) {
        if (e.data === parseInt(e.data)) {
          document.getElementById("my-iframe-id").height = e.data + "px";
        }
      },
      false
    );
    function getParameterByName(name) {
      name = name.replace(/[[]/, "[").replace(/[\]]/, "]");
      var regex = new RegExp(
          "[?" + "\u0026" + "]" + name + "=([^" + "\u0026" + "#]*)"
        ),
        results = regex.exec(location.search);
      return results === null
        ? ""
        : decodeURIComponent(results[1].replace(/\+/g, " "));
    }
    // ]]>
    document.addEventListener("DOMContentLoaded", function() {
      var url;
      if (document.body.clientWidth > 767) {
        url =
          "//hostelraduga-book.otelms.com/bookit/step1/?inline=true" +
          "\u0026" +
          "datein=" +
          getParameterByName("datein") +
          "\u0026" +
          "dateout=" +
          getParameterByName("dateout") +
          "\u0026" +
          "lang=" +
          getParameterByName("lang");
      } else {
        url =
          "//hostelraduga-book-m.otelms.com/bookit/step1/?inline=true" +
          "\u0026" +
          "datein=" +
          getParameterByName("datein") +
          "\u0026" +
          "dateout=" +
          getParameterByName("dateout") +
          "\u0026" +
          "lang=" +
          getParameterByName("lang");
      }
      document.getElementById("my-iframe-id").src = url;
    });
  }
};
</script>

<style>
</style>