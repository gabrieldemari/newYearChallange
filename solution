<?php

// Complete the minimumBribes function below.
function minimumBribes($q) {
    $bribe = 0;
    $chaotic = false;
    $n = count($q);
    for($i = 0; $i < $n; $i++){
        if($q[$i]-($i+1) > 2){
            $chaotic = true;
            break;
        }
        for ($j = max(0, $q[$i]-2); $j < $i; $j++){
            if ($q[$j] > $q[$i]){
                $bribe++;
            }
        }
    }
    if($chaotic){
        echo "Too chaotic \n";
    }
    else{
        echo "$bribe\n";
    }
}
$stdin = fopen("php://stdin", "r");

fscanf($stdin, "%d\n", $t);

for ($t_itr = 0; $t_itr < $t; $t_itr++) {
    fscanf($stdin, "%d\n", $n);

    fscanf($stdin, "%[^\n]", $q_temp);

    $q = array_map('intval', preg_split('/ /', $q_temp, -1, PREG_SPLIT_NO_EMPTY));

    minimumBribes($q);
}

fclose($stdin);
