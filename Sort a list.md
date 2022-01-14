<!DOCTYPE html> 
<html> 
<title>Sort a HTML List Alphabetically</title> </BR>
<body> </BR>

<p>Click the button to sort the list alphabetically:</p> </BR>
<button onclick="sortList()">Sort</button> </BR>

<ul id="id01"></BR>
  <li>Oslo</li></BR>
  <li>Stockholm</li></BR>
  <li>Helsinki</li></BR>
  <li>Berlin</li></BR>
  <li>Rome</li></BR>
  <li>Madrid</li></BR>
</ul></BR>

<script></BR>
function sortList() {</BR>
  var list, i, switching, b, shouldSwitch;</BR>
  list = document.getElementById("id01");</BR>
  switching = true;</BR>
  /* Make a loop that will continue until
  no switching has been done: */</BR>
  while (switching) {</BR>
    // start by saying: no switching is done:</BR>
    switching = false;</BR>
    b = list.getElementsByTagName("LI");</BR>
    // Loop through all list-items:</BR>
    for (i = 0; i < (b.length - 1); i++) {</BR>
      // start by saying there should be no switching:</BR>
      shouldSwitch = false;</BR>
      /* check if the next item should
      switch place with the current item: */</BR>
      if (b[i].innerHTML.toLowerCase() > b[i + 1].innerHTML.toLowerCase()) {</BR>
        /* if next item is alphabetically
        lower than current item, mark as a switch
        and break the loop: */</BR>
        shouldSwitch = true;</BR>
        break;</BR>
      }</BR>
    }</BR>
    if (shouldSwitch) {</BR>
      /* If a switch has been marked, make the switch
      and mark the switch as done: */</BR>
      b[i].parentNode.insertBefore(b[i + 1], b[i]);</BR>
      switching = true;</BR>
    }</BR>
  }</BR>
}</BR>
</script></BR>

</body></BR>
</html></BR>
