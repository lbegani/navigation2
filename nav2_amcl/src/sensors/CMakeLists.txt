add_library(sensors_lib SHARED
  laser/laser.cpp
  laser/beam_model.cpp
  laser/likelihood_field_model.cpp
  laser/likelihood_field_model_prob.cpp
)
target_link_libraries(sensors_lib pf_lib)

install(TARGETS
  sensors_lib
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  RUNTIME DESTINATION lib/${PROJECT_NAME}
)
