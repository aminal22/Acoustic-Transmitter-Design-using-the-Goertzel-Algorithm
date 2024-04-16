################################################################################
# Automatically-generated file. Do not edit!
################################################################################

SHELL = cmd.exe

CG_TOOL_ROOT := D:/ti_v6_2/ccsv6/tools/compiler/c6000_7.4.18

GEN_OPTS__FLAG := 
GEN_CMDS__FLAG := 

ORDERED_OBJS += \
"./Vectors_intr.obj" \
"./c6713dskinit.obj" \
"./main.obj" \
"../C6713dsk.cmd" \
$(GEN_CMDS__FLAG) \
-llibc.a \
-l"D:/ti_v6_2/CCCStudio_v3.1/C6000/cgtools/lib/rts6700.lib" \
-l"D:/ti_v6_2/CCCStudio_v3.1/C6000/csl/lib/csl6713.lib" \
-l"D:/ti_v6_2/CCCStudio_v3.1/C6000/dsk6713/lib/dsk6713bsl.lib" \

-include ../makefile.init

RM := DEL /F
RMDIR := RMDIR /S/Q

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir_vars.mk
-include subdir_rules.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(S62_DEPS)),)
-include $(S62_DEPS)
endif
ifneq ($(strip $(C64_DEPS)),)
-include $(C64_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(SV7A_DEPS)),)
-include $(SV7A_DEPS)
endif
ifneq ($(strip $(S55_DEPS)),)
-include $(S55_DEPS)
endif
ifneq ($(strip $(C67_DEPS)),)
-include $(C67_DEPS)
endif
ifneq ($(strip $(CLA_DEPS)),)
-include $(CLA_DEPS)
endif
ifneq ($(strip $(C??_DEPS)),)
-include $(C??_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
ifneq ($(strip $(S??_DEPS)),)
-include $(S??_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(C62_DEPS)),)
-include $(C62_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(ASM_UPPER_DEPS)),)
-include $(ASM_UPPER_DEPS)
endif
ifneq ($(strip $(K_DEPS)),)
-include $(K_DEPS)
endif
ifneq ($(strip $(C43_DEPS)),)
-include $(C43_DEPS)
endif
ifneq ($(strip $(INO_DEPS)),)
-include $(INO_DEPS)
endif
ifneq ($(strip $(S67_DEPS)),)
-include $(S67_DEPS)
endif
ifneq ($(strip $(SA_DEPS)),)
-include $(SA_DEPS)
endif
ifneq ($(strip $(S43_DEPS)),)
-include $(S43_DEPS)
endif
ifneq ($(strip $(OPT_DEPS)),)
-include $(OPT_DEPS)
endif
ifneq ($(strip $(PDE_DEPS)),)
-include $(PDE_DEPS)
endif
ifneq ($(strip $(S64_DEPS)),)
-include $(S64_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(C55_DEPS)),)
-include $(C55_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXE_OUTPUTS += \
TP4_Goertzel.out \

EXE_OUTPUTS__QUOTED += \
"TP4_Goertzel.out" \

BIN_OUTPUTS += \
TP4_Goertzel.hex \

BIN_OUTPUTS__QUOTED += \
"TP4_Goertzel.hex" \


# All Target
all: TP4_Goertzel.out

# Tool invocations
TP4_Goertzel.out: $(OBJS) $(CMD_SRCS) $(GEN_CMDS)
	@echo 'Building target: $@'
	@echo 'Invoking: C6000 Linker'
	"D:/ti_v6_2/ccsv6/tools/compiler/c6000_7.4.18/bin/cl6x" -mv6700 --abi=coffabi -g --define=CHIP_6713 --diag_wrap=off --diag_warning=225 --display_error_number --mem_model:data=far --asm_listing -z -m"TP4_Goertzel.map" --stack_size=0x100 -i"D:/ti_v6_2/ccsv6/tools/compiler/c6000_7.4.18/lib" -i"D:/ti_v6_2/ccsv6/tools/compiler/c6000_7.4.18/include" --reread_libs --diag_wrap=off --display_error_number --warn_sections --xml_link_info="TP4_Goertzel_linkInfo.xml" --absolute_exe --rom_model -o "TP4_Goertzel.out" $(ORDERED_OBJS)
	@echo 'Finished building target: $@'
	@echo ' '

TP4_Goertzel.hex: $(EXE_OUTPUTS)
	@echo 'Invoking: C6000 Hex Utility'
	"D:/ti_v6_2/ccsv6/tools/compiler/c6000_7.4.18/bin/hex6x"  -o "TP4_Goertzel.hex" $(EXE_OUTPUTS__QUOTED)
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXE_OUTPUTS__QUOTED)$(BIN_OUTPUTS__QUOTED)
	-$(RM) "c6713dskinit.d" "main.d" 
	-$(RM) "Vectors_intr.obj" "c6713dskinit.obj" "main.obj" 
	-$(RM) "Vectors_intr.d" 
	-@echo 'Finished clean'
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

