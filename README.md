# JSGetParentTraversing
JavaScript jQuery get parent from child traversing  

```HTML
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js"></script>

<script>
 $(document).ready(function(){
   
  let getKey = jQuery('#child1');

     console.log( getKey.parent() );
     console.log( '---------------' );
     console.log( getKey.parents() );
     console.log( '---------------' );
     console.log( getKey.children() );

 });
</script> 
</head>
<body>

  <div id="main">
    <div id="xyz">
      <div id="child1">1</div>  
    </div>
    <div>2</div>  
    <div>3</div> 
  </div>

 <!-- THIS IS NOT VISIBLE TO CONSOLE LOG BECAUSE NO CHILD SELECTED ! -->
  <div id="vvmain">
    <div id="ddxyz">
      <div id="xsschild1">1</div>  
    </div>
    <div>2</div>  
    <div>3</div> 
  </div>

</body>
</html>
```

```JS
// Result console.log
S.fn.init [div#xyz, prevObject: S.fn.init(1)] //  PARENT FOUND [ NOT PARENTS | without "S" ]
  0 : div#xyz
  length : 1
 prevObject :  S.fn.init(1)
  0 : div#child1
  length : 1
  > [[Prototype]] : Object(0)
 [[Prototype]] : Object(0)
 
index.html:12 --------------- // HAVING [ child1 as we SELECT the CHILD finding it's PARENTS ! ]
S.fn.init(4) [div#xyz, div#main, body, html, prevObject: S.fn.init(1)]
 0 :  div#xyz
 1 :  div#main
 2 :  body
 3 :  html
 length : 4
 > prevObject : S.fn.init [div#child1]
> [[Prototype]] :  Object(0)

index.html:14 --------------- // HAVING NO SELECTED NO PARENTS FOUND! 
S.fn.init [prevObject: S.fn.init(1)]
 length : 0
 prevObject : S.fn.init [div#child1] 
 > [[Prototype]] : Object(0)
```

Also filter();

<br /> Traversing: https://api.jquery.com/category/traversing/filtering/
<br /> https://api.jquery.com/filter/#filter-selector

<br /> https://api.jquery.com/next/#next-selector
<br /> https://api.jquery.com/nextAll/#nextAll-selector
<br /> https://api.jquery.com/nextUntil/#nextUntil-selector-filter
<br /> https://api.jquery.com/nextUntil/#nextUntil-element-filter

<br /> https://api.jquery.com/first/#first
<br /> https://api.jquery.com/first-child-selector/#first-child1

<br /> https://api.jquery.com/prev/#prev-selector
<br /> https://api.jquery.com/prevUntil/#prevUntil-selector-filter
<br /> https://api.jquery.com/prevAll/#prevAll-selector
<br /> https://api.jquery.com/next-adjacent-selector/#next-adjacent1

<br /> https://api.jquery.com/children/#children-selector
<br /> https://api.jquery.com/only-child-selector/#only-child1
<br /> https://api.jquery.com/nth-child-selector/#nth-child1
<br /> https://api.jquery.com/first-child-selector/#first-child1

<br /> https://api.jquery.com/last/#last
<br /> https://api.jquery.com/nth-last-of-type-selector/#nth-last-of-type1
<br /> https://api.jquery.com/last-child-selector/#last-child1
<br /> https://api.jquery.com/last-selector/#last1

