## 1 在 SiFive 官网下载预编译好的 riscv 工具链，解压后添加环境变量

## 2 更改 C2So.py中所有 riscv32-unknown-elf 为 riscv64-unknown-elf

## 3 把改 C2SO.py 中所有 mkdir 改成 md

## 4 修改 ld 命令，指定 32 位 emulation ，否则会出现 `elf32-littleriscv' does not match `elf64-littleriscv'

    riscv64-unknown-elf-ld  -m elf32lriscv  -T link.ld ...