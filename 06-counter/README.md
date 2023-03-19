# Lab 6 INSERT_YOUR_FIRSTNAME INSERT_YOUR_LASTNAME

### Bidirectional counter

1. Listing of VHDL code of the completed process `p_cnt_up_down`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines

```vhdl
    --------------------------------------------------------
    -- p_cnt_up_down
    -- Clocked process with synchronous reset which implements
    -- n-bit updown counter.
    --------------------------------------------------------
    p_cnt_up_down : process (clk) is
  begin

    if rising_edge(clk) then
      if (rst = '1') then           -- Synchronous reset
        sig_cnt <= (others => '0'); -- Clear all bits
      elsif (en = '1') then         -- Test if counter is enabled
        if (cnt_up = '1') then
            sig_cnt <= sig_cnt + 1;
        elsif (cnt_up = '0') then
            sig_cnt <= sig_cnt - 1;   
        end if;     
      end if;
    end if;

  end process p_cnt_up_down;
```

2. Screenshot with simulated time waveforms. Test (a) reset, (b) counter direction, (c) enable. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![image](https://user-images.githubusercontent.com/124675666/226162570-3f04aa91-1107-4b0c-a129-9f2bbcbeab34.png)

### Two counters

1. Image of the top layer structure including both counters, ie a 4-bit bidirectional counter from Part 4 and a 12-bit counter with a 10 ms time base from Experiments on your own. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

   ![obr](https://user-images.githubusercontent.com/124675666/226164766-5f8ecb3f-9955-44d4-882e-3da51f6da490.png)

