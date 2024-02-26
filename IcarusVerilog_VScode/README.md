# Icarus-Verilog + дополнения VSCode

Это памятка по созданию среды разработки прошивок под FPGA в дистрибутивах GNU Linux. Используемый дистрибутив - Manjaro Linux версии 23.1.1, FPGA board Terasic DE10-Lite Altera MAX10.

## Icarus Verilog
*Icarus Verilog* — компилятор языка описания аппаратуры Verilog. Используется для симуляции и верификации проектов. Для загрузки используем менеджер пакетов Manjaro - *pamac*. В терминале вводим следующую команду:
```
pamac install iverilog
```

## Установка необходимых дополнений для VSCode   

### Verilog-HDL/SystemVerilog/Bluespec SystemVerilog

Для комфортной работы с Verilog нам потребуется дополнение, обеспечивающее подсветку синтаксиса языка, форматирование, linting и snippets. Будем использовать **Verilog-HDL/SystemVerilog/Bluespec SystemVerilog** оно не единственное возможное и требует несколько сторонних программ для работы, но это лучшее из того что есть на сегодняшний день. Скачиваем его прямо из *marketplace* в *VSCode*:

![Task: Verilog-HDL/SystemVerilog/Bluespec SystemVerilog](srcImg/VerilogHDL_SystemVerilog_BluespecSystemVerilog.png)  

#### Syntax Highlighting  
Поддерживается подсветка синтаксиса для:
- Verilog-HDL
- SystemVerilog
- Bluespec SystemVerilog
- VHDL
- Vivado UCF constraints
- Synopsys Design Constraints
- Verilog Filelists (dot-F files)
- Tcl

#### Formatting  
Сtags. Он даст минимальный autocomplete. Загружаем:
```
pamac install ctags 
```

#### Linting  
**Verilog › Linting › Iverilog: Run At File Location** - *YES*
![Task: Verilog › Linting › Iverilog: Run At File Location ](srcImg/Extensions_Linting_Iverilog_RunAtFileLocation.png)  

**Verilog › Linting: Linter** - **iverilog**
![Task: Verilog › Linting: Linter ](srcImg/Extensions_Verilog_Linting_Linter.png)  


#### Snippets 
языковой сервер svls. Добавит предупреждений на кривом коде
Для загрузки используем помощник *Aur* - *yay*
```
yay -S svls
```

Для этого жмём *Ctrl + ,* нужно заполнить такие настройки: **Verilog: Language Server** - *svls*
![Task: Verilog: Language Server - svls ](srcImg/Extensions_LanguageServer_svls.png)  

### WaveTrace
![WaveTrace](srcImg/WaveTrace.png)  

### Verilog Testbench Runner
![Task: Verilog Testbench Runner ](srcImg/Verilog_Testbench_Runner.png)  
