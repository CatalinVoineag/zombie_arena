cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(zombie_arena)

set(SFML_INCLUDE_DIR "./SFML/include")
set(SFML_LIBRARY_DIR "./SFML/build/lib")

add_executable(
	${PROJECT_NAME}
	main.cpp
	Player.cpp
	CreateBackground.cpp
	TextureHolder.cpp
	Zombie.cpp
	CreateHorde.cpp
	Bullet.cpp
	Pickup.cpp
)

link_directories(SFML_LIBRARY_DIR)
include_directories(SFML_INCLUDE_DIR)

find_package(SFML 2.5.1 COMPONENTS system window graphics network audio)

target_link_libraries (zombie_arena sfml-graphics sfml-window sfml-system sfml-audio)
