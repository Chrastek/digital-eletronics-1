# Lab 2: INSERT_YOUR_FIRSTNAME INSERT_YOUR_LASTNAME

### 2-bit comparator

1. Karnaugh maps for other two functions of 2-bit comparator:

   Greater than:

   ![bvicea](https://user-images.githubusercontent.com/124675666/219621612-75571a42-b2b4-4982-a7c8-e4b679347502.png)

   Less than:

   ![bmenea](https://user-images.githubusercontent.com/124675666/219621597-7600d611-1056-4fbe-8712-a0d5437ea0de.png)

2. Mark the largest possible implicants in the K-map and according to them, write the equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![image](https://user-images.githubusercontent.com/124675666/219632398-c8a952da-6fc4-46ca-8941-096e4b663492.png)

### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx??**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started";

        -- First test case ...
        -- 08 last two digits of id - a=0000,b=1000
        s_b <= "1000"; s_a <= "0000"; wait for 100 ns;
        -- ... and its expected outputs
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '1') and
                (s_B_less_A    = '0'))
        -- If false, then report an error
        -- If true, then do not report anything
        report "Input combination 1000, 0000 FAILED" severity error;


        -- WRITE OTHER TEST CASES HERE
        s_b <= "0000"; s_a <= "0000"; wait for 100 ns;
        s_b <= "0000"; s_a <= "1111"; wait for 100 ns;
        s_b <= "1111"; s_a <= "0000"; wait for 100 ns;
        

        -- Report a note at the end of stimulus process
        report "Stimulus process finished";
        wait; -- Data generation process is suspended forever
    end process p_stimulus;
```

2. Link to your public EDA Playground example:

   [[https://www.edaplayground.com/...](https://www.edaplayground.com/...)](https://www.edaplayground.com/x/6gmg)
