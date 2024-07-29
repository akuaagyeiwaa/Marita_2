# Marita_2
This is a test trial of my work
<html xmlns:tei="http://www.tei-c.org/ns/1.0">
   <head>
      <title>Marita or the Folly of Love</title>
      <style>
                    .persName { color: blue; cursor: pointer; text-decoration: underline; }
                    .tooltip {
                        display: none;
                        position: absolute;
                        background-color: white;
                        border: 1px solid black;
                        padding: 5px;
                        z-index: 1000;
                    }
                </style>
      <script>
                    document.addEventListener("DOMContentLoaded", function() {
                        document.querySelectorAll('.persName').forEach(function(element) {
                            element.addEventListener('click', function() {
                                let tooltip = document.getElementById('tooltip');
                                tooltip.textContent = 'Character: ' + element.textContent;
                                tooltip.style.display = 'block';
                                tooltip.style.left = (element.getBoundingClientRect().left + window.scrollX) + 'px';
                                tooltip.style.top = (element.getBoundingClientRect().bottom + window.scrollY) + 'px';
                            });
                        });
                        document.addEventListener('click', function(event) {
                            let tooltip = document.getElementById('tooltip');
                            if (!event.target.classList.contains('persName')) {
                                tooltip.style.display = 'none';
                            }
                        });
                    });
                </script>
   </head>
   <body>
      <div id="tooltip" class="tooltip"/>
      <h1>Marita or the Folly of Love</h1>
      <p>Author: A. Native</p>
      <div>
         <p>This is a story about <span class="persName" data-name="marita">Marita</span>.</p>
         <p>Marita met <span class="persName" data-name="john">John</span> at the market.</p>
      </div>
   </body>
</html>
