################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
BlackPill_KeyButton.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BlackPill_KeyButton.list \

OBJCOPY_BIN += \
BlackPill_KeyButton.bin \


# All Target
all: BlackPill_KeyButton.elf secondary-outputs

# Tool invocations
BlackPill_KeyButton.elf: $(OBJS) $(USER_OBJS) C:\ProjetosSTM32\BlackPill_KeyButton\STM32F411CEUX_FLASH.ld
	arm-none-eabi-gcc -o "BlackPill_KeyButton.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\ProjetosSTM32\BlackPill_KeyButton\STM32F411CEUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BlackPill_KeyButton.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BlackPill_KeyButton.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BlackPill_KeyButton.list"
	@echo 'Finished building: $@'
	@echo ' '

BlackPill_KeyButton.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "BlackPill_KeyButton.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
