#
# Makefile for the CMUCAL drivers.
#

# Object files in subdirectories

obj-y					+= cal-if.o
obj-$(CONFIG_PMUCAL)			+= pmucal_system.o pmucal_local.o pmucal_cpu.o pmucal_rae.o
obj-$(CONFIG_CMUCAL)			+= cmucal.o ra.o vclk.o pll_spec.o
obj-$(CONFIG_CMUCAL_DEBUG)		+= cmucal-debug.o
obj-$(CONFIG_ACPM_DVFS)			+= acpm_dvfs.o fvmap.o

ifndef CONFIG_SOC_EMULATOR8895
obj-$(CONFIG_SOC_EXYNOS8895)		+= exynos8895/cal_data.o
else
obj-$(CONFIG_SOC_EMULATOR8895)		+= emulator8895/cal_data.o
endif

subdir-ccflags-y += -Wno-sizeof-pointer-div
