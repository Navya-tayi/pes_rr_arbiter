# ROUND ROBIN ARBITER

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

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/4ab29d70-ca7d-4351-a6cb-1307bfc8a7e3)

The above warnings did not affect the waveforms.

![image](https://github.com/Navya-tayi/pes_rr_arbiter/assets/79205242/13e5d330-81aa-4009-92fc-6669d7ac933a.png)

##__The GLS and pre-synthesis waveform match.__

Code Credits:
https://www.youtube.com/watch?v=X6oJn7r9-8s (Arjun-Narula)




