#!/bin/bash

input_dir=$1
output_dir=$2
output_tar=$3

mkdir $output_dir
n=1
spliter=_

list_paths=$(find "$input_dir" -type f)

for file in $list_paths 
do
    name=$(basename "$path")
    cp $path $output_dir/"$n$spliter$name"
    n=$((n+1))
done

tar -cvf $output_tar $output_dir
