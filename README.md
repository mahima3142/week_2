# week_2
### Pre-Synthesis Simulation

Run the following command to perform a pre-synthesis simulation:

```bash
iverilog -o output/pre_synth_sim/pre_synth_sim.out -DPRE_SYNTH_SIM \
-I src/include -I src/module \
src/module/testbench.v src/module/vsdbabysoc.v
cd output/pre_synth_sim
./pre_synth_sim.out
```
<img width="1269" height="623" alt="image" src="https://github.com/user-attachments/assets/1b607f67-0de5-4678-9738-76504d4bd3bf" />

### post-Synthesis Simulation

Run the following command to perform a pre-synthesis simulation:

```bash
iverilog -DFUNCTIONAL -DUNIT_DELAY=#1 -o ./output/post_synth_sim.out ./src/gls_model/primitives.v ./src/gls_model/sky130_fd_sc_hd.v ./output/vsdbabysoc_net.v ./src/module/avsdpll.v ./src/module/avsddac.v ./src/module/testbench.v
```

Debug the errors

```bash
./post_synth_sim.out
```
GTKwave dump:

<img width="1257" height="795" alt="image" src="https://github.com/user-attachments/assets/5f151a80-a3cd-40ed-b1c1-4cb288c79537" />
