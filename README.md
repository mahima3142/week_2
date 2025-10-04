# week_2
### Pre-Synthesis Simulation

Run the following command to perform a pre-synthesis simulation:

```bash
iverilog -o output/pre_synth_sim/pre_synth_sim.out -DPRE_SYNTH_SIM \
-I src/include -I src/module \
src/module/testbench.v src/module/vsdbabysoc.v
cd output/pre_synth_sim
./pre_synth_sim.out
