################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32G4xx_HAL_Driver/Src/subdir.mk
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
Test_CAN_NG474RE.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Test_CAN_NG474RE.list \

OBJCOPY_BIN += \
Test_CAN_NG474RE.bin \


# All Target
all: Test_CAN_NG474RE.elf secondary-outputs

# Tool invocations
Test_CAN_NG474RE.elf: $(OBJS) $(USER_OBJS) C:\Users\Slawek\STM32CubeIDE\workspace_1.3.0_testowy\Test_CAN_NG474RE\STM32G474RETX_FLASH.ld
	arm-none-eabi-gcc -o "Test_CAN_NG474RE.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Slawek\STM32CubeIDE\workspace_1.3.0_testowy\Test_CAN_NG474RE\STM32G474RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Test_CAN_NG474RE.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Test_CAN_NG474RE.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Test_CAN_NG474RE.list"
	@echo 'Finished building: $@'
	@echo ' '

Test_CAN_NG474RE.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Test_CAN_NG474RE.bin"
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
