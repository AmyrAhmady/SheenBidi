if(WIN32)
	add_definitions(
		-D_CRT_SECURE_NO_WARNINGS
		-DWIN32_LEAN_AND_MEAN
	)
endif()

file(GLOB_RECURSE sheen_bidi_source_list Source/*.c Source/*.h)

add_library(SheenBidi STATIC ${sheen_bidi_source_list})

target_include_directories(SheenBidi INTERFACE Headers PRIVATE Headers)
