# ollama-0.13.0_enableAmdMi50
Modify ollama source code to enable amd instinct mi50 gpu(Depend on rocm7.0.2.The method for install rocm7 is borrowed from the upgraded video on YouTube)
https://www.reddit.com/r/LocalLLaMA/comments/1o99s2u/rocm_70_install_for_mi50_32gb_ubuntu_2404_lts/

Build cmd:
cmake --preset "ROCm 7"
cmake –build –preset “ROCm 7”

Release program:
go build -tags=nolegacy -ldflags="-s -w -X main.Version=0.13.0"
