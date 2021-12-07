## list files
hadoop fs -ls

## copy frpm local
hadoop fs -copyFromLocal \<file_path\>
## copt to local
hadoop fs -copyToLocal \<file_path\>

## copy
hadoop fs -cp \<from_path\> \<to_path\> 

## remove file
hadoop fs -rm \<file_path\>