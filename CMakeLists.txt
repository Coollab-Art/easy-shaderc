set(CMAKE_POLICY_DEFAULT_CMP0077 NEW) # Allows us to override options https://cmake.org/cmake/help/latest/policy/CMP0077.html

set(SHADERC_SKIP_INSTALL true)
set(SHADERC_SKIP_TESTS true)
set(SHADERC_SKIP_EXAMPLES true)
set(SHADERC_ENABLE_SHARED_CRT true)
set(SPIRV_HEADERS_SKIP_EXAMPLES true)
set(SPIRV_HEADERS_SKIP_INSTALL true)
add_subdirectory(SPIRV-Headers EXCLUDE_FROM_ALL)
add_subdirectory(SPIRV-Tools EXCLUDE_FROM_ALL)
add_subdirectory(glslang EXCLUDE_FROM_ALL)
add_subdirectory(shaderc EXCLUDE_FROM_ALL)
add_library(easy_shaderc::shaderc ALIAS shaderc)

# ---------------------
# ---Licenses---
# ---------------------
install(FILES "glslang/LICENSE.txt" DESTINATION "license/glslang")
install(FILES "shaderc/LICENSE" DESTINATION "license/shaderc")
install(FILES "SPIRV-Headers/LICENSE" DESTINATION "license/SPIRV-Headers")
install(FILES "SPIRV-Tools/LICENSE" DESTINATION "license/SPIRV-Tools")