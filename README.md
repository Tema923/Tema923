function rotateRight90 (matrix) {
  let result = [];
  for (let i = matrix.length - 1; i >= 0; i--) {
    for (let j = 0; j < matrix[i].length; j++) {
      if (!result[j]) {
        result[j] = [];
      }
      result[j].push(matrix[i][j]);
    }
  }
  return result;
}

let matrix = [
	[1, 2, 3],
	[4, 5, 6],
	[7, 8, 9],
];
matrix.forEach((arr) => console.info([...arr]));

let newMatrix = rotateRight90(matrix);
console.info("\n");
newMatrix.forEach((arr) => console.info([...arr]));
