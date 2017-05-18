dtb-$(CONFIG_ARCH_THUNDER) += thunder-88xx.dtb
dtb-$(CONFIG_ARCH_VEXPRESS) += rtsm_ve-aemv8a.dtb foundation-v8.dtb
dtb-$(CONFIG_ARCH_XGENE) += apm-mustang.dtb
dtb-$(CONFIG_MODEL_FLAT) += exynos8890-herolte_kor_all_00.dtb exynos8890-herolte_kor_all_01.dtb \
			exynos8890-herolte_kor_all_02.dtb exynos8890-herolte_kor_all_03.dtb \
			exynos8890-herolte_kor_all_04.dtb exynos8890-herolte_kor_all_08.dtb \
			exynos8890-herolte_kor_all_09.dtb
dtb-$(CONFIG_MODEL_EDGE) += exynos8890-hero2lte_kor_all_00.dtb exynos8890-hero2lte_kor_all_01.dtb \
			exynos8890-hero2lte_kor_all_03.dtb exynos8890-hero2lte_kor_all_04.dtb \
			exynos8890-hero2lte_kor_all_08.dtb exynos8890-hero2lte_kor_all_09.dtb

targets += dtbs

DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif
targets += $(DTB_LIST)

dtbs: $(addprefix $(obj)/, $(DTB_LIST))

clean-files := dts/*.dtb *.dtb
