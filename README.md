# ShiftRegister-
# AIM:

To implement SISO Shift Register using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

SISO shift Register

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

<img width="798" height="257" alt="image" src="https://github.com/user-attachments/assets/a03e3ffd-3087-4807-b5d5-84c31e0435ea" />

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next. Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

Procedure

# PROGRAM
always @(posedge clk or posedge rst)
begin
    if (rst) begin
        q <= 4'b0000;      
    end
    else begin
        q[0] <= q[3];      
        q[1] <= q[0];
        q[2] <= q[1];
        q[3] <= q[2];
    end
end


# Developed by: BUSHPIKA C
# RegisterNumber:25007434



RTL LOGIC FOR SISO Shift Register
<img width="1920" height="1080" alt="Screenshot 2025-12-16 000834" src="https://github.com/user-attachments/assets/3c8a3fc7-2cd6-4226-9f57-0fab4d5d37ad" />


TIMING DIGRAMS FOR SISO Shift Register
<img width="1060" height="607" alt="image" src="https://github.com/user-attachments/assets/d59eac5c-5a4c-4a45-a583-c9725cf8d54b" />

RESULTS


