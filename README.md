# GDScript Syntax Benchmarks

Speed comparisons of various syntax alternatives within the GDScript language (Godot game engine).  All code is within [benchmarks.gd](benchmarks.gd), including funcs referenced in results table.

__SEE THE END OF THIS README FOR THE RESULTS TABLE__


## To Run Tests Yourself

* Open the project in Godot
* Click the lone node in the Scene/Node panel
* Click the unchecked box in the Inspector for the exported variable 'Click To Run'
* Wait several seconds for the tests to run (Godot editor may appear frozen during this time)

The script is a 'tool' and clicking this exported variable will trigger a setget function which actually runs the tests.  The results will be printed in the standard output and written to your disk as README.md (clobbering the existing README.md)

## Contributors

Please only add [benchmarks.gd](benchmarks.gd) to your commits.  This entire readme file is automaticaly generated by the script, so please do not commit changes to the readme itself.  Thanks!

## Results

```Godot version: 2.1.7-rc (official)```

         concat_str  *** 101% faster than ***  format_str      (0.180 vs 0.362 msec)
         float_cast  ***   0% faster than ***  float_inter     (0.023 vs 0.023 msec)
       format_stemp  ***   0% faster than ***  format_dtemp    (0.204 vs 0.205 msec)
        format_cast  *** 688% faster than ***  format_stemp    (0.026 vs 0.205 msec)
          dict_loop  ***  37% faster than ***  dict_loopkeys   (4.354 vs 5.980 msec)
            dict_in  ***  11% faster than ***  dict_has        (0.066 vs 0.073 msec)
           callfunc  ***  73% faster than ***  call_funcref    (0.077 vs 0.133 msec)
       call_funcref  ***  58% faster than ***  call_callv      (0.134 vs 0.212 msec)
          call_call  ***  31% faster than ***  call_callv      (0.160 vs 0.209 msec)
           int_incr  ***   0% faster than ***  int_increq      (0.047 vs 0.047 msec)
         dictwr_var  ***  37% faster than ***  dictwr_point    (0.116 vs 0.159 msec)
      dictwr_string  ***  10% faster than ***  dictwr_point    (0.147 vs 0.161 msec)
       dictread_var  ***  31% faster than ***  dictread_point  (0.090 vs 0.118 msec)
    dictread_string  ***   0% faster than ***  dictread_point  (0.120 vs 0.120 msec)
        array_index  ***  42% faster than ***  array_append    (0.062 vs 0.088 msec)
       array_append  ***   5% faster than ***  array_pushback  (0.081 vs 0.085 msec)
         array_size  *** 154% faster than ***  array_len       (0.048 vs 0.122 msec)
        array_izero  ***  11% faster than ***  array_front     (0.045 vs 0.050 msec)
         array_ineg  ***   4% faster than ***  array_back      (0.047 vs 0.049 msec)
           var_func  ***   6% faster than ***  var_script      (0.035 vs 0.037 msec)
         var_script  ***  14% faster than ***  var_self        (0.037 vs 0.042 msec)
       iter_for_int  ***   1% faster than ***  iter_for_range  (0.342 vs 0.344 msec)
           iter_for  ***  48% faster than ***  iter_while      (0.029 vs 0.043 msec)
            matches  ***   3% faster than ***  ifs             (0.068 vs 0.070 msec)
     array_appendrw  *** 385% faster than ***  parray_appendrw (0.121 vs 0.587 msec)
       dontcallfunc  *** 209% faster than ***  callfunc        (0.023 vs 0.071 msec)
       inteval_auto  ***  48% faster than ***  inteval         (0.031 vs 0.046 msec)
     arrayeval_auto  ***  49% faster than ***  arrayeval       (0.070 vs 0.104 msec)
      dicteval_auto  ***  42% faster than ***  dicteval        (0.064 vs 0.091 msec)
      nulleval_auto  ***  61% faster than ***  nulleval        (0.033 vs 0.053 msec)
