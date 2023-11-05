# ROUND ROBIN ARBITER

A round-robin arbiter is a digital circuit or algorithm used in computer systems to fairly allocate a shared resource among multiple requestors. It works in a sequential manner, granting access to each requestor in a cyclic order, ensuring fairness without favoring any one requestor. Round-robin arbiters are commonly used in scenarios like memory access in multi-processor systems and network packet scheduling, where multiple devices or entities contend for access to a common resource.

While round-robin arbitration provides fairness, it may not always be the most efficient or suitable method for every application. Some systems require more complex arbitration strategies to address specific requirements or priorities. Nonetheless, round-robin arbiters remain a fundamental concept in digital design for achieving equitable resource sharing.


<details><summary>Phase 1</summary>
   
__1. Create the files:__
   
![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/fd2e38ab-6ff5-409e-8580-45c13f37b907.png)

__2. Waveform (pre-synthesis):__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/b89d35b3-5f8a-4f57-907c-c7626f41768f.png)

YOSYS:

__3. Open yosys where the verilog files are present:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/77580f96-f90d-491f-bfba-d12a635edc60.png)


![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/6a7e3535-b118-4e58-aaef-ad46193da4c0.png)

synthesis:

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/56c30750-9cd8-41d2-b0b2-069546e5633f.png)


![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/3c32c520-f6ee-4076-9142-0fbc608016b4.png)

__4. ABC:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/5c2d69a9-6f1e-48e2-9ab8-018c8fc74cd8.png)

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/0d6e5721-f6c5-4f8d-9261-f97165ad9edb.png)

__5. show:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/b2cf5b41-26b7-47cc-b4d1-173670a26c15.png)

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/1e8a4701-1061-4240-9484-c525d7d7e8a2.png)

__6. Generating netlist:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/677c45e8-f673-41ba-a1d2-6fbcc1129a65.png)


![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/212d9c74-da12-4380-8401-399ea49386f5.png)

__7. Concise netlist file:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/d19ce7d8-fee7-4467-8d38-4a96c5d5cd00.png)

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/3e7acee3-425c-4121-bb0e-05fcef986cf0.png)

I used the original netlist file itself to generate the GLS waveform sinc eusing the concise file was not working properly

__8. GLS (Gate level synthesis) waveform:__

Use the generated netlist file to get the GLS waveform and compare with the pre-synthesis waveform

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/4ab29d70-ca7d-4351-a6cb-1307bfc8a7e3)

pre-synthesys waveform (for comparision):

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/b89d35b3-5f8a-4f57-907c-c7626f41768f.png)

The above warnings did not affect the waveforms.

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/13e5d330-81aa-4009-92fc-6669d7ac933a.png)

__The GLS and pre-synthesis waveform match.__

</details>


<details><summary>Phase 2</summary>
   
# Physical Design

<details><summary>Steps after Installation</summary>
   
__successful openlane installation:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/f0ce46f3-5c05-4f7e-84d9-1774112695cc)

__After installation__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/92c7fc06-0e9b-4285-819a-9a99bcf3894f)


__In a new tab:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/80051c9a-bf1b-4368-9dcb-2b4bcb39da6a)


![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/f6204385-38cf-48e9-b83e-41d1d36aee04)

__Modify config.json file in the design directory__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/26ba25bc-eb43-4386-b548-168d4e0dfa09)

</details>

<details><summary>Synthesis</summary>
   
__run_synthesis:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/d4960d44-e15c-4fbf-ad3f-93f4b8cdba43)

__summary report:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/a44ce181-a325-480c-96ec-cb35ae60f24c)

</details>


<details><summary>Floorplan</summary>

__run_floorplan:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/8fad6a53-85a4-4ab4-87df-d3153617f851)


![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/43699c2a-f66c-4dbc-9862-b6318e1939e7)

__floorplan:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/d730e5c0-eacb-49d8-9a36-58975927fded)

</details>


<details><summary>Placement</summary>

__run_placement:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/59ff45f6-5032-479c-929c-08e31ab2beba)

__placement:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/7da41c98-da20-46b7-a759-a2baee6ea0fd)

</details>


<details><summary>Clock Tree Sythesis & Routing</summary>
   
__run_cts:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/9532750a-d7f3-4c1f-b980-6e2f1335c9b1)

__gen_pdn:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/c38ebdcd-53da-49db-9298-fc6beb0398b1)

__Routing:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/c5cb7300-350d-4342-9352-0212fb4a4d76)

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/a0d7eaa5-6e25-45ee-ad04-b1045e276b8c)

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/35bc44b8-d99f-48a6-b591-66b37c909be1)

</details>

<details><summary>Errors & Resolution</summary>
   
__Errors faced:__

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/03ce3aea-aaaa-4325-9101-04c20bed7270)

__To resolve it:__

In the configuration files, go to floorplan.tcl

Increase the die area and run_floorplan again:

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/64763719-07a9-41f6-becc-ef0501704463)

</details>
</details>




















