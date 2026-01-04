This is the target folder for retro-go.

Move it into the target folder of retro go and add the path to "Retro-Go\components\retro-go\targets\config.h"

#elif defined(RG_TARGET_RETRO_LE_GO_BOY)
#include "targets/retro-le-go-boy/config.h"


For a N8R8 the sdkconfig is allready set up and will also work for a N16R8, but to use the extra ram, change the followin in sdkconfig

CONFIG_ESPTOOLPY_FLASHSIZE_8MB=y
CONFIG_ESPTOOLPY_FLASHSIZE_16MB=n
CONFIG_ESPTOOLPY_FLASHSIZE="8MB"

to 

CONFIG_ESPTOOLPY_FLASHSIZE_8MB=n
CONFIG_ESPTOOLPY_FLASHSIZE_16MB=y
CONFIG_ESPTOOLPY_FLASHSIZE="16MB"
