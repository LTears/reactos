remove_definitions(-D_WIN32_WINNT=0x502)
add_definitions(-D_WIN32_WINNT=0x600)

add_definitions(-DUNICODE -D_UNICODE -D__NTOSKRNL__ -D_NTOSKRNL_ -D_NTSYSTEM_)

list(APPEND SOURCE
    fsrtl.c
    rtl.c)

add_library(ntoskrnl_vista ${SOURCE})
add_dependencies(ntoskrnl_vista bugcodes xdk)
