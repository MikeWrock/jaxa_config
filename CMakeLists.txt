cmake_minimum_required(VERSION 3.22)
project(jaxa_config)

find_package(ament_cmake REQUIRED)

ament_package()

install(DIRECTORY launch DESTINATION share/${PROJECT_NAME}
  PATTERN "setup_assistant.launch" EXCLUDE)
  install(DIRECTORY config DESTINATION share/${PROJECT_NAME})
  install(DIRECTORY simulation_worlds DESTINATION share/${PROJECT_NAME})

install(DIRECTORY objectives DESTINATION share/${PROJECT_NAME})
install(DIRECTORY waypoints DESTINATION share/${PROJECT_NAME})
install(FILES .setup_assistant DESTINATION share/${PROJECT_NAME})
