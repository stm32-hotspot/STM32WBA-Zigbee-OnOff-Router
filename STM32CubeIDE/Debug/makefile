################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Utilities/subdir.mk
-include Middlewares/STM32_WPAN/LinkLayer/subdir.mk
-include Drivers/STM32WBAxx_HAL_Driver/subdir.mk
-include Drivers/CMSIS/subdir.mk
-include Drivers/BSP/STM32WBAxx_Nucleo/subdir.mk
-include Common/WPAN/Startup/subdir.mk
-include Common/WPAN/Modules/SerialCmdInterpreter/subdir.mk
-include Common/WPAN/Modules/RTDebug/subdir.mk
-include Common/WPAN/Modules/RFControl/subdir.mk
-include Common/WPAN/Modules/MemoryManager/subdir.mk
-include Common/WPAN/Modules/Log/subdir.mk
-include Common/WPAN/Modules/BasicAES/subdir.mk
-include Common/WPAN/Modules/subdir.mk
-include Common/WPAN/Interfaces/subdir.mk
-include Application/User/System/Interfaces/subdir.mk
-include Application/User/System/Config/LowPower/subdir.mk
-include Application/User/System/Config/Debug_GPIO/subdir.mk
-include Application/User/Startup/subdir.mk
-include Application/User/STM32_WPAN/Target/subdir.mk
-include Application/User/STM32_WPAN/App/subdir.mk
-include Application/User/Core/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Zigbee_OnOff_Router_Demo
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Zigbee_OnOff_Router_Demo.elf \

MAP_FILES += \
Zigbee_OnOff_Router_Demo.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Zigbee_OnOff_Router_Demo.list \


# All Target
all: main-build

# Main-build Target
main-build: Zigbee_OnOff_Router_Demo.elf secondary-outputs

# Tool invocations
Zigbee_OnOff_Router_Demo.elf Zigbee_OnOff_Router_Demo.map: $(OBJS) $(USER_OBJS) C:\Users\petr\ david\STM32CubeIDE\WBA_ZB_1_6_1\Zigbee_OnOff_Router_Demo\STM32CubeIDE\STM32WBA65RIVX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Zigbee_OnOff_Router_Demo.elf" @"objects.list" $(USER_OBJS) -Wl,--start-group $(LIBS) -Wl,--end-group -mcpu=cortex-m33 -T"C:\Users\petr david\STM32CubeIDE\WBA_ZB_1_6_1\Zigbee_OnOff_Router_Demo\STM32CubeIDE\STM32WBA65RIVX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Zigbee_OnOff_Router_Demo.map" -Wl,--gc-sections -static -L../../Middlewares/ST/STM32_WPAN/link_layer/ll_cmd_lib/lib -L../../Middlewares/ST/STM32_WPAN/mac_802_15_4/lib -L../../Middlewares/ST/STM32_WPAN/zigbee/clusters -L../../Middlewares/ST/STM32_WPAN/zigbee/stack -z noexecstack --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Zigbee_OnOff_Router_Demo.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Zigbee_OnOff_Router_Demo.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Zigbee_OnOff_Router_Demo.elf Zigbee_OnOff_Router_Demo.list Zigbee_OnOff_Router_Demo.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
