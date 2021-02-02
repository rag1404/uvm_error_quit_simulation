# uvm_error_quit_simulation
A program to demonstrate different ways to quit simulation based on UVM_ERROR !

````systemverilog
# Example 1
1) We have 2 UVM_ERROR messages inside the test and 1 in comp_c component.
2) First, lets use the command line +UVM_MAX_QUIT_COUNT=<int> to stop the simulation.
3) In this case, lets add +UVM_MAX_QUIT_COUNT=2 to run_options.
4) We will see the test finishes after two errors.

# Example 2
1) Let's use the same example 
2) lets use this in the command line +uvm_set_action=uvm_test_top.*,_ALL_,UVM_ERROR,UVM_DISPLAY|UVM_EXIT
3) Inside test_top if you see UVM_ERROR, go ahead and display the error and stop the simulation.

````  
 
  
  
  
