CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT (GOBO)

FILE(GLOB FILES sources/bin/ge*)
INSTALL (PROGRAMS ${FILES} DESTINATION bin)
INSTALL (DIRECTORY sources/library DESTINATION eiffel/gobo)
INSTALL (DIRECTORY sources/tool DESTINATION eiffel/gobo)
INSTALL (DIRECTORY sources/misc DESTINATION eiffel/gobo)
INSTALL (DIRECTORY sources/doc DESTINATION eiffel/gobo)


SET (CPACK_PACKAGE_NAME "Gobo")
SET (CPACK_PACKAGE_VENDOR "Gobosoft")
SET (CPACK_PACKAGE_CONTACT "ebezault@gobosoft.com")
SET (CPACK_PACKAGE_VERSION_MAJOR 3)
SET (CPACK_PACKAGE_VERSION_MINOR 9)
SET (CPACK_DEBIAN_PACKAGE_MAINTAINER "Guillaume Chauvet <gchauvet@zatarox.com>")
SET (CPACK_PACKAGE_DESCRIPTION_SUMMARY "Provide to the Eiffel community with free and portable Eiffel tools and libraries.")
SET (CPACK_PACKAGE_DESCRIPTION "One of the main concerns of Gobo Eiffel is to provide you with Eiffel libraries and tools that are portable across various Eiffel compilers available on the market. That way, you can still use your favorite Eiffel compiler while taking advantage of the goodies included in this package.")
SET (CPACK_DEBIAN_PACKAGE_DEPENDS "libgc-dev gcc")
SET (CPACK_DEBIAN_PACKAGE_SECTION "devel")
SET (CPACK_DEBIAN_PACKAGE_VERSION ${CPACK_PACKAGE_VERSION}+ubuntu1)

INCLUDE(CPack)
