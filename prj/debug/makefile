################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include library/usb/subdir.mk
-include library/fat_sd/option/subdir.mk
-include library/fat_sd/subdir.mk
-include cmsis/device/subdir.mk
-include cmsis/core/subdir.mk
-include cmsis/STM32F10x_StdPeriph_Driver/src/subdir.mk
-include bsp/bsp_usb_otg/src/subdir.mk
-include bsp/subdir.mk
-include app/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_FLASH += \
usb_host_dock.hex \

SECONDARY_LIST += \
usb_host_dock.lst \

SECONDARY_SIZE += \
usb_host_dock.siz \


# All Target
all: usb_host_dock.elf secondary-outputs

# Tool invocations
usb_host_dock.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: ARM Yagarto Windows GCC C++ Linker'
	arm-none-eabi-g++ -T"..\prj\stm32f105rb_flash.ld" -L"C:\Users\Hz\git\usb_host_dock\library\usb" -Wl,-Map,usb_host_dock.map -mcpu=cortex-m3 -mthumb -g3 -gdwarf-2 -o "usb_host_dock.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

usb_host_dock.hex: usb_host_dock.elf
	@echo 'Invoking: ARM Yagarto Windows GNU Create Flash Image'
	arm-none-eabi-objcopy -O ihex usb_host_dock.elf  "usb_host_dock.hex"
	@echo 'Finished building: $@'
	@echo ' '

usb_host_dock.lst: usb_host_dock.elf
	@echo 'Invoking: ARM Yagarto Windows GNU Create Listing'
	arm-none-eabi-objdump -h -S usb_host_dock.elf > "usb_host_dock.lst"
	@echo 'Finished building: $@'
	@echo ' '

usb_host_dock.siz: usb_host_dock.elf
	@echo 'Invoking: ARM Yagarto Windows GNU Print Size'
	arm-none-eabi-size  --format=berkeley usb_host_dock.elf
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(SECONDARY_FLASH)$(CXX_DEPS)$(S_UPPER_DEPS)$(SECONDARY_LIST)$(SECONDARY_SIZE)$(C++_DEPS)$(ASM_DEPS)$(CC_DEPS)$(CPP_DEPS)$(EXECUTABLES)$(C_UPPER_DEPS) usb_host_dock.elf
	-@echo ' '

secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_LIST) $(SECONDARY_SIZE)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
