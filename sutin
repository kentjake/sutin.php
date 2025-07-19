<?php
function calculateSums($n) {
    $sumOfSquares = 0;
    $sumOfCubes = 0;

    for ($i = 1; $i <= $n; $i++) {
        $sumOfSquares += $i * $i;
        $sumOfCubes += $i * $i * $i;
    }

    return array($sumOfSquares, $sumOfCubes);
}

if ($_SERVER['REQUEST_METHOD'] === 'POST' && isset($_POST['number'])) {
    $n = intval($_POST['number']);

    if ($n < 1) {
        echo "Please enter a positive integer.";
    } else {
        list($squares, $cubes) = calculateSums($n);
        echo "The sum of Squares from 1 to $n is $squares.<br>";
        echo "The sum of Cubes from 1 to $n is $cubes.";
    }
} else {
    echo '<form method="post">';
    echo 'Enter the Upper Limit: <input type="number" name="number" required>'; 
    echo '<input type="submit" value="Calculate">';
    echo '</form>';
}
?>
