#
# Copyright (C) 2018-2020 Intel Corporation
#
# SPDX-License-Identifier: MIT
#

if(TESTS_LKF)
  set(IGDRCL_SRCS_tests_gen11_lkf
      ${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
      ${CMAKE_CURRENT_SOURCE_DIR}/test_hw_info_config_lkf.cpp
      ${CMAKE_CURRENT_SOURCE_DIR}/test_device_caps_lkf.cpp
  )
  target_sources(igdrcl_tests PRIVATE ${IGDRCL_SRCS_tests_gen11_lkf})
  add_subdirectories()
  neo_copy_test_files(copy_test_files_lkf lkf)
  add_dependencies(unit_tests copy_test_files_lkf)
endif()
