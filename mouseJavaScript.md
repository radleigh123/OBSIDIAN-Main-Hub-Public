---
cssclass: no-m
aliases:
tags:
- JavaScript
---
## Mouse Position in [[JavaScript]] (x, y)
```HTML JavaScript
<p>X: <span id="x-value"></span></p>
<p>Y: <span id="y-value"></span></p>

<script type="text/javascript">
	window.addEventListener("mousemove", function (e) {
		document.getElementById("x-value").textContent = e.x;
		document.getElementById("y-value").textContent = e.y;
	});
</script>
```

# 

<br>

---
**Sources:**
- [Get Mouse Position in JavaScript ('x' and 'y') - JavaScript Tutorial For Beginners - YouTube](https://www.youtube.com/watch?v=P2i11xnrpNI)