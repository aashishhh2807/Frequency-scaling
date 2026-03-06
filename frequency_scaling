/*
# Filename:         frequency_scaling.v
# File Description: Frequency divider module to scale down 50 MHz input clock 
                    to generate approximately 3.125 MHz output clock.
# Global variables: None
*/

module frequency_scaling (
    input clk_50M,              // clk_50M: 50 MHz input clock signal
    output reg clk_3125KHz      // clk_3125KHz: output clock divided to ~3.125 MHz
);

initial begin
    clk_3125KHz = 0;            // Initialize output clock to 0
end

// counter: 3-bit counter used to divide the clock
reg [2:0] counter = 0;

// Divide clock inside always block
always @ (posedge clk_50M) begin
    /*
    Purpose:
    ---
    This always block implements frequency division. 
    It uses a 3-bit counter to toggle the clk_3125KHz signal 
    whenever the counter rolls over.
    */

    if (!counter) 
        clk_3125KHz = ~clk_3125KHz;   // Toggle output clock when counter resets to 0

    counter = counter + 1'b1;         // Increment counter (wraps around after 7)
end

endmodule

