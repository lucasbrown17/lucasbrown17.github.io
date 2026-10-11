---
layout: default
title: CV
permalink: /cv/
---

<div id="cv-viewer"><p id="cv-msg">Loading CV…</p></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script>
(function () {
  var msg = document.getElementById("cv-msg");
  var box = document.getElementById("cv-viewer");
  var url = "{{ 'lucas_brown_cv_robots.pdf' | relative_url }}";

  if (typeof pdfjsLib === "undefined") {
    msg.textContent = "PDF.js did not load from the CDN (blocked or offline).";
    return;
  }

  pdfjsLib.GlobalWorkerOptions.workerSrc =
    "https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js";

  pdfjsLib.getDocument(url).promise.then(async function (pdf) {
    msg.remove();
    var dpr = window.devicePixelRatio || 1;
    for (var n = 1; n <= pdf.numPages; n++) {
      var page = await pdf.getPage(n);
      var base = page.getViewport({ scale: 1 });
      var vp = page.getViewport({ scale: (box.clientWidth / base.width) * dpr });
      var canvas = document.createElement("canvas");
      canvas.width = vp.width;
      canvas.height = vp.height;
      canvas.style.cssText = "width:100%;display:block;margin-bottom:1rem;";
      box.appendChild(canvas);
      await page.render({ canvasContext: canvas.getContext("2d"), viewport: vp }).promise;
    }
  }).catch(function (err) {
    msg.textContent = "Could not load " + url + ": " + err.message;
  });
})();
</script>