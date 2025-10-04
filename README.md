# week_2
### Pre-Synthesis Simulation

Run the following command to perform a pre-synthesis simulation:

```bash
iverilog -o output/pre_synth_sim/pre_synth_sim.out -DPRE_SYNTH_SIM \
-I src/include -I src/module \
src/module/testbench.v src/module/vsdbabysoc.v
cd output/pre_synth_sim
./pre_synth_sim.out

<img width="1269" height="623" alt="image" src="https://github.com/user-attachments/assets/1b607f67-0de5-4678-9738-76504d4bd3bf" />
