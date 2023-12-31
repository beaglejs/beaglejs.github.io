https://tldp.org/HOWTO/Software-Building-HOWTO.html

https://moi.vonos.net/linux/beginners-installing-from-source/

v. LFS 및 표준
LFS의 구조는 가능한 한 Linux 표준을 따릅니다. 기본 표준은 다음과 같습니다.

POSIX.1-2008.

파일 시스템 계층 표준(FHS) 버전 3.0

Linux 표준 베이스(LSB) 버전 5.0(2015)

LSB에는 코어, 데스크탑, 런타임 언어 및 이미징의 네 가지 개별 사양이 있습니다. 코어 및 데스크탑 사양의 일부는 아키텍처에 따라 다릅니다. Gtk3와 Graphics라는 두 가지 평가판 사양도 있습니다. LFS는 이전 섹션에서 설명한 IA32(32비트 x86) 또는 AMD64(x86_64) 아키텍처에 대한 LSB 사양을 따르려고 합니다.

[참고] 참고
많은 사람들이 이러한 요구 사항에 동의하지 않습니다. LSB의 주요 목적은 독점 소프트웨어가 호환 시스템에 설치되고 실행될 수 있도록 하는 것입니다. LFS는 소스 기반이므로 사용자는 원하는 패키지를 완벽하게 제어할 수 있습니다. LSB에서 지정한 일부 패키지를 설치하지 않도록 선택할 수도 있습니다.

"처음부터" LSB 인증 테스트를 통과하는 완전한 시스템을 만드는 것이 가능하지만, LFS 책의 범위를 벗어나는 많은 추가 패키지 없이는 이를 수행할 수 없습니다. 이러한 추가 패키지에 대한 설치 지침은 BLFS에서 찾을 수 있습니다.

LSB 요구 사항을 충족하려면 LFS에서 제공하는 패키지가 필요합니다.
LSB 코어:

Bash, Bc, Binutils, Coreutils, Diffutils, 파일, Findutils, Gawk, Grep, Gzip, M4, Man-DB, Ncurses, Procps, Psmisc, Sed, Shadow, Tar, Util-linux, Zlib

LSB 데스크탑:

없음

LSB 런타임 언어:

펄, 파이썬

LSB 이미징:

없음

LSB Gtk3 및 LSB 그래픽(평가판 사용):

없음

LSB 요구 사항을 충족하려면 BLFS에서 제공하는 패키지가 필요합니다.
LSB 코어:

At, Batch(At의 일부), Cpio, Ed, Fcrontab, LSB-Tools, NSPR, NSS, PAM, Pax, Sendmail(또는 Postfix 또는 Exim), 시간

LSB 데스크탑:

Alsa, ATK, Cairo, Desktop-file-utils, Freetype, Fontconfig, Gdk-pixbuf, Glib2, GTK+2, Icon-naming-utils, Libjpeg-turbo, Libpng, Libtiff, Libxml2, MesaLib, Pango, Xdg-utils, Xorg

LSB 런타임 언어:

Libxml2, Libxslt

LSB 이미징:

CUPS, 컵 필터, Ghostscript, SANE

LSB Gtk3 및 LSB 그래픽(평가판 사용):

GTK+3

LSB 요구 사항을 충족하려면 LFS 또는 BLFS에서 제공되지 않는 패키지가 필요합니다.
LSB 코어:

없음

LSB 데스크탑:

Qt4(단, Qt5는 제공됨)

LSB 런타임 언어:

없음

LSB 이미징:

없음

LSB Gtk3 및 LSB 그래픽(시험 사용):

없음

----

표준을 따른다.

POSIX.1-2008.

Filesystem Hierarchy Standard (FHS) Version 3.0

Linux Standard Base (LSB) Version 5.0 (2015)