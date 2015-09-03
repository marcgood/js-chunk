# js-chunk

function chunk(arr, size) {
  var mdArray = [];
  var row = 0;
  var col = 0;
  
  for (var i = 0; i < arr.length; i++) {
    mdArray[row][col] = arr.push(i);
    col++;
   if (col >= size) {
      col = 0;
      row++;
    }
  } 
  return mdArray;
}

chunk(['a', 'b', 'c', 'd'], 2);

// Split an array (first argument) into groups 
// the length of size (second argument) and 
// returns them as a multidimensional array.
// Should = to  [ [ 'a', 'b' ], [ 'c', 'd' ] ]
