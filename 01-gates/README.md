# Lab 1: Michal Papaj

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![rovnice](https://user-images.githubusercontent.com/124675666/218318471-af339bef-ec4b-4332-915a-1d56af60e261.jpg)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
    f_orig_o <= (not(b_i) and a_i) or (c_i and not(b_i or not(a_i)));
    f_nand_o <= not(not(not(b_i)and a_i) and not(not(b_i) and (c_i and a_i)));
    f_nor_o  <= not(b_i or not(a_i)) or not(not(c_i) or (b_i or not(a_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

   | **c** | **b** |**a** | **f_ORIG** | **f_(N)AND** | **f_(N)OR** |
   | :-: | :-: | :-: | :-: | :-: | :-: |
   | 0 | 0 | 0 | 0 | 0 | 0 |
   | 0 | 0 | 1 | 1 | 1 | 1 |
   | 0 | 1 | 0 | 0 | 0 | 0 |
   | 0 | 1 | 1 | 0 | 0 | 0 |
   | 1 | 0 | 0 | 0 | 0 | 0 |
   | 1 | 0 | 1 | 1 | 1 | 1 |
   | 1 | 1 | 0 | 0 | 0 | 0 |
   | 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![grafy](https://user-images.githubusercontent.com/124675666/218319499-b8b603ca-c7c6-4715-acde-648800b09200.jpg)
   First Distributive law: in rows nand and nor

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/x/6vfm)
