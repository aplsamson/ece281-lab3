# Lab 3: Thunderbird Turn Signal

VHDL for ECE 281 [Lab 3](https://usafa-ece.github.io/ece281-book/lab/lab3.html)

Targeted toward Digilent Basys3. Make sure to install the [board files](https://github.com/Xilinx/XilinxBoardStore/tree/2018.2/boards/Digilent/basys3).

Tested on Windows 11.

---

## Build the project

You can simply open `thunderbird.xpr` and Vivado will do the rest!

## GitHub Actions Testbench

The workflow uses the [setup-ghdl-ci](https://github.com/ghdl/setup-ghdl-ci) GitHub action
to run a *nightly* build of [GHDL](https://ghdl.github.io/ghdl/).

The workflow uses GHDL to analyze, elaborate, and run the entity specified in the `.github/workflows/testbench.yml`.

```yaml
env:
  TESTBENCH_ENTITY: myfile
```

If successful then GHDL will quietly exit with a `0` code.
If any of the `assert` statements fail **with** `severity error` then GHDL will cease the simulation and exit with non-zero code; this will also cause the workflow to fail.

## Documentation
C3C Simon Janssen and I worked as partners to problem solve and write our report. He specifically helped me fix my next-state equations. C3C Jake Marbach helped me to write my test functions. He did this by explaining the delay and what I was trying to assert. Then I just referenced ICE4 and some other labs.


## DEMO: https://usafa0-my.sharepoint.com/:v:/g/personal/c26andres_samson_afacademy_af_edu/Edx8Q8dGHY9DtzSclfsr6usB6cmrTWgqpAQVDoT6p4ocfw?e=R7qf15
