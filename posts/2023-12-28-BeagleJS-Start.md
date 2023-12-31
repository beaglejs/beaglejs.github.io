---
layout: 'index'
view: 'post'
permalink: '/posts/2023/12/28/BeagleJS-Start.html'
opengraph:
    site:
        name: 'BeagleJS'
        url: '/'
date: '2023/12/28 13:58:00'
title: 'BeagleJS Start'
description: ""
category: Start
tags: ['BeagleJS', 'Start']
---

우선 BeagleJS 를 위한 리눅스를 빌드하는 것으로 한다. 현재 내가 사용하는 운영체제는 윈도우즈로 가상 머신을 이용하여 빌드를 한다. 라이브 CD는 우분투 서버 버전으로 도전한다.

1. Linux From Scratch

i. Foreword
My journey to learn and better understand Linux began back in 1998. I had just installed my first Linux distribution and had quickly become intrigued with the whole concept and philosophy behind Linux.

There are always many ways to accomplish a single task. The same can be said about Linux distributions. A great many have existed over the years. Some still exist, some have morphed into something else, yet others have been relegated to our memories. They all do things differently to suit the needs of their target audience. Because so many different ways to accomplish the same end goal exist, I began to realize I no longer had to be limited by any one implementation. Prior to discovering Linux, we simply put up with issues in other Operating Systems as you had no choice. It was what it was, whether you liked it or not. With Linux, the concept of choice began to emerge. If you didn't like something, you were free, even encouraged, to change it.

I tried a number of distributions and could not decide on any one. They were great systems in their own right. It wasn't a matter of right and wrong anymore. It had become a matter of personal taste. With all that choice available, it became apparent that there would not be a single system that would be perfect for me. So I set out to create my own Linux system that would fully conform to my personal preferences.

To truly make it my own system, I resolved to compile everything from source code instead of using pre-compiled binary packages. This “perfect” Linux system would have the strengths of various systems without their perceived weaknesses. At first, the idea was rather daunting. I remained committed to the idea that such a system could be built.

After sorting through issues such as circular dependencies and compile-time errors, I finally built a custom-built Linux system. It was fully operational and perfectly usable like any of the other Linux systems out there at the time. But it was my own creation. It was very satisfying to have put together such a system myself. The only thing better would have been to create each piece of software myself. This was the next best thing.

As I shared my goals and experiences with other members of the Linux community, it became apparent that there was a sustained interest in these ideas. It quickly became plain that such custom-built Linux systems serve not only to meet user specific requirements, but also serve as an ideal learning opportunity for programmers and system administrators to enhance their (existing) Linux skills. Out of this broadened interest, the Linux From Scratch Project was born.

This Linux From Scratch book is the central core around that project. It provides the background and instructions necessary for you to design and build your own system. While this book provides a template that will result in a correctly working system, you are free to alter the instructions to suit yourself, which is, in part, an important part of this project. You remain in control; we just lend a helping hand to get you started on your own journey.

I sincerely hope you will have a great time working on your own Linux From Scratch system and enjoy the numerous benefits of having a system that is truly your own.

--
Gerard Beekmans
gerard@linuxfromscratch.org

나. 머리말
Linux를 배우고 더 잘 이해하기 위한 나의 여정은 1998년에 시작되었습니다.
저는 방금 첫 번째 Linux 배포판을 설치했고 Linux 뒤에 있는 전체 개념과 철학에 빠르게 흥미를 느꼈습니다.

단일 작업을 수행하는 방법에는 항상 여러 가지가 있습니다. Linux 배포판에 대해서도 마찬가지입니다. 수년에 걸쳐 매우 많은 것이 존재했습니다. 일부는 여전히 존재하고 일부는 다른 것으로 변형되었지만 다른 일부는 우리 기억 속으로 밀려났습니다. 그들은 모두 대상 고객의 요구에 맞게 다른 방식으로 작업을 수행합니다. 동일한 최종 목표를 달성하는 방법은 매우 다양하기 때문에 더 이상 하나의 구현에 제한을 받을 필요가 없다는 것을 깨닫기 시작했습니다. Linux를 발견하기 전에는 선택의 여지가 없었기 때문에 다른 운영 체제의 문제를 참았습니다. 당신이 좋아하든 원하지 않든 그것은 바로 그런 것이었습니다. Linux에서는 선택의 개념이 등장하기 시작했습니다. 마음에 들지 않는 것이 있으면 자유롭게 바꿀 수 있었고 심지어 격려를 받아 변경할 수도 있었습니다.

나는 여러 배포판을 시도했지만 어느 것도 결정할 수 없었습니다. 그것들은 그 자체로 훌륭한 시스템이었습니다. 더 이상 옳고 그름의 문제가 아니었습니다. 그것은 개인적인 취향의 문제가 되었습니다. 선택의 폭이 넓어지면서 나에게 딱 맞는 단일 시스템은 없다는 것이 분명해졌습니다. 그래서 나는 내 개인적인 취향에 완전히 맞는 나만의 Linux 시스템을 만들기 시작했습니다.

진정한 나만의 시스템으로 만들기 위해 미리 컴파일된 바이너리 패키지를 사용하는 대신 소스 코드에서 모든 것을 컴파일하기로 결심했습니다. 이 "완벽한" Linux 시스템은 인식된 약점 없이 다양한 시스템의 장점을 갖습니다. 처음에는 그 생각이 다소 부담스러웠습니다. 나는 그러한 시스템이 구축될 수 있다는 생각에 계속 전념했습니다.

순환 종속성, 컴파일 시간 오류 등의 문제를 정리한 후 마침내 맞춤형 Linux 시스템을 구축했습니다. 당시의 다른 Linux 시스템과 마찬가지로 완벽하게 작동하고 완벽하게 사용할 수 있었습니다. 하지만 그것은 내가 직접 만든 작품이었습니다. 이런 시스템을 직접 구축했다는 자체가 매우 만족스러웠습니다. 더 나은 유일한 방법은 각 소프트웨어를 직접 만드는 것이었습니다. 이것이 차선책이었습니다.

내 목표와 경험을 Linux 커뮤니티의 다른 구성원과 공유하면서 이러한 아이디어에 대한 지속적인 관심이 있다는 것이 분명해졌습니다. 이러한 맞춤형 Linux 시스템은 사용자의 특정 요구 사항을 충족할 뿐만 아니라 프로그래머와 시스템 관리자가 자신의 (기존) Linux 기술을 향상시킬 수 있는 이상적인 학습 기회로도 사용된다는 사실이 금방 명백해졌습니다. 이러한 폭넓은 관심 속에서 Linux From Scratch Project가 탄생했습니다.

이 Linux From Scratch 책은 해당 프로젝트의 핵심입니다. 자신만의 시스템을 설계하고 구축하는 데 필요한 배경 지식과 지침을 제공합니다. 이 책에서는 시스템이 올바르게 작동하도록 하는 템플릿을 제공하지만, 지침을 자신에게 맞게 자유롭게 변경할 수 있으며 이는 부분적으로 이 프로젝트의 중요한 부분입니다. 귀하는 통제권을 유지합니다. 우리는 당신이 자신의 여정을 시작할 수 있도록 도움의 손길을 빌려줄 뿐입니다.

나는 진심으로 당신이 자신만의 Linux From Scratch 시스템을 작업하면서 즐거운 시간을 보내고 진정한 자신만의 시스템을 갖는 데서 오는 수많은 이점을 누리기를 진심으로 바랍니다.

--
제라드 비크먼스
gerard@linuxfromscratch.org

ii. Audience
There are many reasons why you would want to read this book. One of the questions many people raise is, “why go through all the hassle of manually building a Linux system from scratch when you can just download and install an existing one?”

One important reason for this project's existence is to help you learn how a Linux system works from the inside out. Building an LFS system helps demonstrate what makes Linux tick, and how things work together and depend on each other. One of the best things this learning experience can provide is the ability to customize a Linux system to suit your own unique needs.

Another key benefit of LFS is that it gives you control of the system without relying on someone else's Linux implementation. With LFS, you are in the driver's seat. You dictate every aspect of your system.

LFS allows you to create very compact Linux systems. With other distributions you are often forced to install a great many programs you neither use nor understand. These programs waste resources. You may argue that with today's hard drives and CPUs, wasted resources are no longer a consideration. Sometimes, however, you are still constrained by the system's size, if nothing else. Think about bootable CDs, USB sticks, and embedded systems. Those are areas where LFS can be beneficial.

Another advantage of a custom built Linux system is security. By compiling the entire system from source code, you are empowered to audit everything and apply all the security patches you want. You don't have to wait for somebody else to compile binary packages that fix a security hole. Unless you examine the patch and implement it yourself, you have no guarantee that the new binary package was built correctly and adequately fixes the problem.

The goal of Linux From Scratch is to build a complete and usable foundation-level system. If you do not wish to build your own Linux system from scratch, you may nevertheless benefit from the information in this book.

There are too many good reasons to build your own LFS system to list them all here. In the end, education is by far the most important reason. As you continue your LFS experience, you will discover the power that information and knowledge can bring.

ii. 청중
이 책을 읽고 싶은 데에는 여러 가지 이유가 있습니다. 많은 사람들이 제기하는 질문 중 하나는 "기존 Linux 시스템을 다운로드하여 설치할 수 있는데 왜 처음부터 Linux 시스템을 수동으로 구축해야 하는 번거로움을 겪어야 합니까?"입니다.

이 프로젝트가 존재하는 중요한 이유 중 하나는 Linux 시스템이 내부에서 어떻게 작동하는지 배울 수 있도록 돕는 것입니다. LFS 시스템을 구축하면 무엇이 Linux를 작동하게 하는지, 그리고 사물이 어떻게 함께 작동하고 서로 의존하는지를 보여주는 데 도움이 됩니다. 이 학습 경험이 제공할 수 있는 가장 좋은 것 중 하나는 자신의 고유한 요구 사항에 맞게 Linux 시스템을 사용자 정의할 수 있다는 것입니다.

LFS의 또 다른 주요 이점은 다른 사람의 Linux 구현에 의존하지 않고 시스템을 제어할 수 있다는 것입니다. LFS를 사용하면 운전석에 앉을 수 있습니다. 귀하는 시스템의 모든 측면을 지시합니다.

LFS를 사용하면 매우 컴팩트한 Linux 시스템을 만들 수 있습니다. 다른 배포판에서는 사용하지도 이해하지도 못하는 수많은 프로그램을 설치해야 하는 경우가 많습니다. 이러한 프로그램은 자원을 낭비합니다. 오늘날의 하드 드라이브와 CPU에서는 자원 낭비가 더 이상 고려 사항이 아니라고 주장할 수도 있습니다. 그러나 때로는 시스템 크기로 인해 여전히 제약을 받는 경우도 있습니다. 부팅 가능한 CD, USB 스틱 및 임베디드 시스템을 생각해 보십시오. LFS가 도움이 될 수 있는 영역입니다.

맞춤형 Linux 시스템의 또 다른 장점은 보안입니다. 소스 코드에서 전체 시스템을 컴파일하면 모든 것을 감사하고 원하는 모든 보안 패치를 적용할 수 있습니다. 다른 사람이 보안 허점을 수정하는 바이너리 패키지를 컴파일할 때까지 기다릴 필요가 없습니다. 패치를 검사하고 직접 구현하지 않는 한 새 바이너리 패키지가 올바르게 빌드되고 문제가 적절하게 해결된다는 보장이 없습니다.

Linux From Scratch의 목표는 완전하고 사용 가능한 기초 수준 시스템을 구축하는 것입니다. 자신만의 Linux 시스템을 처음부터 구축하고 싶지 않더라도 이 책의 정보를 활용하면 도움이 될 것입니다.

여기에 모두 나열하기에는 자신만의 LFS 시스템을 구축해야 할 이유가 너무 많습니다. 결국 가장 큰 이유는 교육이다. LFS 경험을 계속하면서 정보와 지식이 가져올 수 있는 힘을 발견하게 될 것입니다.


iii. LFS 타겟 아키텍처
LFS의 주요 대상 아키텍처는 AMD/Intel x86(32비트) 및 x86_64(64비트) CPU입니다. 한편, 이 책의 지침은 일부 수정을 거쳐 Power PC 및 ARM CPU에서도 작동하는 것으로 알려져 있습니다. 이러한 대체 CPU 중 하나를 활용하는 시스템을 구축하려면 다음 페이지의 전제 조건 외에 주요 전제 조건은 이전 LFS 설치, Ubuntu, Red Hat/Fedora, SuSE 또는 기타 배포판과 같은 기존 Linux 시스템입니다. 해당 아키텍처를 목표로 하는 것입니다. (32비트 배포판은 64비트 AMD/Intel 컴퓨터에 설치하여 호스트 시스템으로 사용할 수 있습니다.)

32비트 시스템에 비해 64비트 시스템에서 구축할 때 얻는 이점은 매우 적습니다. 예를 들어 Core i7-4790 CPU 기반 시스템에서 4개의 코어를 사용하는 LFS-9.1의 테스트 빌드에서 다음 통계가 측정되었습니다.

아키텍처 빌드 시간 빌드 크기
32비트 239.9분 3.6GB
64비트 233.2분 4.4GB
보시다시피, 동일한 하드웨어에서 64비트 빌드는 32비트 빌드보다 단지 3% 더 빠르며 22% 더 큽니다. LFS를 LAMP 서버나 방화벽으로 사용할 계획이라면 32비트 CPU이면 충분할 수 있습니다. 반면, BLFS의 여러 패키지는 이제 빌드 및/또는 실행을 위해 4GB 이상의 RAM이 필요합니다. LFS를 데스크탑으로 사용하려는 경우 LFS 작성자는 64비트 시스템 구축을 권장합니다.


iv. 전제조건
LFS 시스템을 구축하는 것은 간단한 작업이 아닙니다. 문제를 해결하고 나열된 명령을 올바르게 실행하려면 Unix 시스템 관리에 대한 특정 수준의 기존 지식이 필요합니다. 특히, 최소한 명령줄(셸)을 사용하여 파일과 디렉터리를 복사 또는 이동하고, 디렉터리와 파일 내용을 나열하고, 현재 디렉터리를 변경하는 방법을 이미 알고 있어야 합니다. 또한 Linux 소프트웨어를 사용하고 설치하는 방법도 알고 있어야 합니다.

LFS 책은 최소한 이 기본 수준의 기술을 가정하기 때문에 다양한 LFS 지원 포럼은 이러한 영역에 대해 많은 도움을 제공하지 않을 것입니다. 그러한 기본 지식에 관한 귀하의 질문은 답변되지 않을 가능성이 높습니다(또는 단순히 LFS 필수 사전 읽기 목록을 참조하게 될 것입니다).

LFS 시스템을 구축하기 전에 다음 기사를 읽어 보시기 바랍니다.

소프트웨어 구축-HOWTO https://tldp.org/HOWTO/Software-Building-HOWTO.html

이것은 Linux에서 "일반" Unix 소프트웨어 패키지를 구축하고 설치하는 방법에 대한 포괄적인 안내서입니다. 이 책은 오래 전에 작성되었지만 여전히 소프트웨어를 구축하고 설치하는 데 사용되는 기본 기술에 대한 좋은 요약을 제공합니다.

소스에서 설치하기 위한 초보자 가이드 https://moi.vonos.net/linux/beginners-installing-from-source/

이 가이드는 소스 코드에서 소프트웨어를 구축하는 데 필요한 기본 기술과 기술에 대한 좋은 요약을 제공합니다.

LFS의 결과인 기본 64비트 빌드는 "순수한" 64비트 시스템입니다. 즉, 64비트 실행 파일만 지원합니다. "multi-lib" 시스템을 구축하려면 많은 애플리케이션을 두 번(32비트 시스템용으로 한 번, 64비트 시스템용으로 한 번) 컴파일해야 합니다. 이는 기본 Linux 시스템에 필요한 최소한의 지침을 제공하려는 교육 목표를 방해하기 때문에 LFS에서는 직접 지원되지 않습니다. 일부 LFS/BLFS 편집자는 https://www.linuxfromscratch.org/~thomas/multilib/index.html에서 액세스할 수 있는 LFS의 다중 라이브러리 포크를 유지 관리합니다. 그러나 그것은 고급 주제입니다.

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

> 표준을 따른다.
> 
> POSIX.1-2008.
> 
> Filesystem Hierarchy Standard (FHS) Version 3.0
> 
> Linux Standard Base (LSB) Version 5.0 (2015)

vi. Rationale for Packages in the Book
The goal of LFS is to build a complete and usable foundation-level system—including all the packages needed to replicate itself—and providing a relatively minimal base from which to customize a more complete system based on the user's choices. This does not mean that LFS is the smallest system possible. Several important packages are included that are not, strictly speaking, required. The list below documents the reasons each package in the book has been included.

Acl

This package contains utilities to administer Access Control Lists, which are used to define fine-grained discretionary access rights for files and directories.

Attr

This package contains programs for managing extended attributes on file system objects.

Autoconf

This package supplies programs for producing shell scripts that can automatically configure source code from a developer's template. It is often needed to rebuild a package after the build procedure has been updated.

Automake

This package contains programs for generating Make files from a template. It is often needed to rebuild a package after the build procedure has been updated.

Bash

This package satisfies an LSB core requirement to provide a Bourne Shell interface to the system. It was chosen over other shell packages because of its common usage and extensive capabilities.

Bc

This package provides an arbitrary precision numeric processing language. It satisfies a requirement for building the Linux kernel.

Binutils

This package supplies a linker, an assembler, and other tools for handling object files. The programs in this package are needed to compile most of the packages in an LFS system.

Bison

This package contains the GNU version of yacc (Yet Another Compiler Compiler) needed to build several of the LFS programs.

Bzip2

This package contains programs for compressing and decompressing files. It is required to decompress many LFS packages.

Check

This package provides a test harness for other programs.

Coreutils

This package contains a number of essential programs for viewing and manipulating files and directories. These programs are needed for command line file management, and are necessary for the installation procedures of every package in LFS.

DejaGNU

This package supplies a framework for testing other programs.

Diffutils

This package contains programs that show the differences between files or directories. These programs can be used to create patches, and are also used in many packages' build procedures.

E2fsprogs

This package supplies utilities for handling the ext2, ext3 and ext4 file systems. These are the most common and thoroughly tested file systems that Linux supports.

Expat

This package yields a relatively small XML parsing library. It is required by the XML::Parser Perl module.

Expect

This package contains a program for carrying out scripted dialogues with other interactive programs. It is commonly used for testing other packages.

File

This package contains a utility for determining the type of a given file or files. A few packages need it in their build scripts.

Findutils

This package provides programs to find files in a file system. It is used in many packages' build scripts.

Flex

This package contains a utility for generating programs that recognize patterns in text. It is the GNU version of the lex (lexical analyzer) program. It is required to build several LFS packages.

Gawk

This package supplies programs for manipulating text files. It is the GNU version of awk (Aho-Weinberg-Kernighan). It is used in many other packages' build scripts.

GCC

This is the Gnu Compiler Collection. It contains the C and C++ compilers as well as several others not built by LFS.

GDBM

This package contains the GNU Database Manager library. It is used by one other LFS package, Man-DB.

Gettext

This package provides utilities and libraries for the internationalization and localization of many packages.

Glibc

This package contains the main C library. Linux programs will not run without it.

GMP

This package supplies math libraries that provide useful functions for arbitrary precision arithmetic. It is needed to build GCC.

Gperf

This package produces a program that generates a perfect hash function from a set of keys. It is required by Udev .

Grep

This package contains programs for searching through files. These programs are used by most packages' build scripts.

Groff

This package contributes programs for processing and formatting text. One important function of these programs is to format man pages.

GRUB

This is the Grand Unified Boot Loader. It is the most flexible of several boot loaders available.

Gzip

This package contains programs for compressing and decompressing files. It is needed to decompress many packages in LFS.

Iana-etc

This package provides data for network services and protocols. It is needed to enable proper networking capabilities.

Inetutils

This package supplies programs for basic network administration.

Intltool

This package contributes tools for extracting translatable strings from source files.

IProute2

This package contains programs for basic and advanced IPv4 and IPv6 networking. It was chosen over the other common network tools package (net-tools) for its IPv6 capabilities.

Kbd

This package produces key-table files, keyboard utilities for non-US keyboards, and a number of console fonts.

Kmod

This package supplies programs needed to administer Linux kernel modules.

Less

This package contains a very nice text file viewer that allows scrolling up or down when viewing a file. Many packages use it for paging the output.

Libcap

This package implements the userspace interfaces to the POSIX 1003.1e capabilities available in Linux kernels.

Libelf

The elfutils project provides libraries and tools for ELF files and DWARF data. Most utilities in this package are available in other packages, but the library is needed to build the Linux kernel using the default (and most efficient) configuration.

Libffi

This package implements a portable, high level programming interface to various calling conventions. Some programs may not know at the time of compilation what arguments are to be passed to a function. For instance, an interpreter may be told at run-time about the number and types of arguments used to call a given function. Libffi can be used in such programs to provide a bridge from the interpreter program to compiled code.

Libpipeline

The Libpipeline package supplies a library for manipulating pipelines of subprocesses in a flexible and convenient way. It is required by the Man-DB package.

Libtool

This package contains the GNU generic library support script. It wraps the complexity of using shared libraries into a consistent, portable interface. It is needed by the test suites in other LFS packages.

Libxcrypt

This package provides the libcrypt library needed by various packages (notably, Shadow) for hashing passwords. It replaces the obsolete libcrypt implementation in Glibc.

Linux Kernel

This package is the Operating System. It is the Linux in the GNU/Linux environment.

M4

This package provides a general text macro processor useful as a build tool for other programs.

Make

This package contains a program for directing the building of packages. It is required by almost every package in LFS.

Man-DB

This package contains programs for finding and viewing man pages. It was chosen instead of the man package because of its superior internationalization capabilities. It supplies the man program.

Man-pages

This package provides the actual contents of the basic Linux man pages.

Meson

This package provides a software tool for automating the building of software. The main goal of Meson is to minimize the amount of time that software developers need to spend configuring a build system. It's required to build Systemd, as well as many BLFS packages.

MPC

This package supplies arithmetic functions for complex numbers. It is required by GCC.

MPFR

This package contains functions for multiple precision arithmetic. It is required by GCC.

Ninja

This package furnishes a small build system with a focus on speed. It is designed to have its input files generated by a higher-level build system, and to run builds as fast as possible. This package is required by Meson.

Ncurses

This package contains libraries for terminal-independent handling of character screens. It is often used to provide cursor control for a menuing system. It is needed by a number of the packages in LFS.

Openssl

This package provides management tools and libraries relating to cryptography. These supply cryptographic functions to other packages, including the Linux kernel.

Patch

This package contains a program for modifying or creating files by applying a patch file typically created by the diff program. It is needed by the build procedure for several LFS packages.

Perl

This package is an interpreter for the runtime language PERL. It is needed for the installation and test suites of several LFS packages.

Pkgconf

This package contains a program which helps to configure compiler and linker flags for development libraries. The program can be used as a drop-in replacement of pkg-config, which is needed by the building system of many packages. It's maintained more actively and slightly faster than the original Pkg-config package.

Procps-NG

This package contains programs for monitoring processes. These programs are useful for system administration, and are also used by the LFS Bootscripts.

Psmisc

This package produces programs for displaying information about running processes. These programs are useful for system administration.

Python 3

This package provides an interpreted language that has a design philosophy emphasizing code readability.

Readline

This package is a set of libraries that offer command-line editing and history capabilities. It is used by Bash.

Sed

This package allows editing of text without opening it in a text editor. It is also needed by many LFS packages' configure scripts.

Shadow

This package contains programs for handling passwords securely.

Sysklogd

This package supplies programs for logging system messages, such as those emitted by the kernel or daemon processes when unusual events occur.

Sysvinit

This package provides the init program, the parent of all the other processes on a running Linux system.

Udev

This package is a device manager. It dynamically controls the ownership, permissions, names, and symbolic links of device nodes in the /dev directory when devices are added to or removed from the system.

Tar

This package provides archiving and extraction capabilities of virtually all the packages used in LFS.

Tcl

This package contains the Tool Command Language used in many test suites.

Texinfo

This package supplies programs for reading, writing, and converting info pages. It is used in the installation procedures of many LFS packages.

Util-linux

This package contains miscellaneous utility programs. Among them are utilities for handling file systems, consoles, partitions, and messages.

Vim

This package provides an editor. It was chosen because of its compatibility with the classic vi editor and its huge number of powerful capabilities. An editor is a very personal choice for many users. Any other editor can be substituted, if you wish.

Wheel

This package supplies a Python module that is the reference implementation of the Python wheel packaging standard.

XML::Parser

This package is a Perl module that interfaces with Expat.

XZ Utils

This package contains programs for compressing and decompressing files. It provides the highest compression generally available and is useful for decompressing packages in XZ or LZMA format.

Zlib

This package contains compression and decompression routines used by some programs.

Zstd

This package supplies compression and decompression routines used by some programs. It provides high compression ratios and a very wide range of compression / speed trade-offs.

1.1. LFS 시스템 구축 방법
LFS 시스템은 이미 설치된 Linux 배포판(예: Debian, OpenMandriva, Fedora 또는 openSUSE)을 사용하여 구축됩니다. 기존 Linux 시스템(호스트)은 새로운 시스템을 구축하는 데 컴파일러, 링커, 셸 등 필요한 프로그램을 제공하는 출발점으로 사용됩니다. 이러한 도구를 포함하려면 배포판 설치 중에 "개발" 옵션을 선택하십시오.

[참고] 참고
Linux 배포판을 설치하는 방법에는 여러 가지가 있으며 기본값은 일반적으로 LFS 시스템 구축에 적합하지 않습니다. 상업용 배포 설정에 대한 제안 사항은 https://www.linuxfromscratch.org/hints/downloads/files/partitioning-for-lfs.txt를 참조하세요.

컴퓨터에 별도의 배포판을 설치하는 대신 상용 배포판의 LiveCD를 사용할 수도 있습니다.

이 책의 2장에서는 새로운 LFS 시스템이 컴파일되고 설치될 새로운 Linux 기본 파티션과 파일 시스템을 생성하는 방법을 설명합니다. 3장에서는 LFS 시스템을 구축하기 위해 어떤 패키지와 패치를 다운로드해야 하는지, 그리고 이를 새로운 파일 시스템에 저장하는 방법을 설명합니다. 4장에서는 적절한 작업 환경 설정에 대해 설명합니다. 4장에서는 5장과 그 이후 작업을 시작하기 전에 알아야 할 몇 가지 중요한 문제를 설명하므로 주의 깊게 읽으십시오.

5장에서는 크로스 컴파일 기술을 사용하여 호스트 시스템에서 새 도구를 분리하는 초기 도구 체인(binutils, gcc 및 glibc) 설치에 대해 설명합니다.

6장에서는 방금 구축한 크로스 툴체인을 사용하여 기본 유틸리티를 크로스 컴파일하는 방법을 보여줍니다.

7장은 그런 다음 새로운 도구를 사용하여 LFS 시스템을 만드는 데 필요한 나머지 모든 도구를 구축하는 "chroot" 환경으로 들어갑니다.

호스트 배포에서 새 시스템을 분리하려는 이러한 노력은 과도해 보일 수 있습니다. 이것이 수행되는 이유에 대한 전체 기술 설명은 툴체인 기술 노트에 제공됩니다.

8장에서는 본격적인 LFS 시스템이 구축됩니다. chroot 환경이 제공하는 또 다른 이점은 LFS가 구축되는 동안 호스트 시스템을 계속 사용할 수 있다는 것입니다. 패키지 컴파일이 완료될 때까지 기다리는 동안 평소처럼 컴퓨터를 계속 사용할 수 있습니다.

설치를 마무리하기 위해 9장에서는 기본 시스템 구성을 설정하고, 10장에서는 커널과 부트로더를 생성합니다. 11장에는 이 책 이후에도 계속해서 LFS 경험을 할 수 있는 정보가 담겨 있습니다. 이 장의 단계가 구현되면 컴퓨터는 새로운 LFS 시스템으로 부팅할 준비가 됩니다.

이것은 간단히 말해서 프로세스입니다. 각 단계에 대한 자세한 정보는 다음 장에 나와 있습니다. LFS 모험을 시작하면 지금 복잡해 보이는 항목이 명확해지고 모든 것이 제자리에 있게 될 것입니다.

이 장에서는 LFS 구축에 필요한 호스트 도구를 확인하고, 필요한 경우 설치합니다. 그런 다음 LFS 시스템을 호스팅할 파티션이 준비됩니다. 파티션 자체를 생성하고 여기에 파일 시스템을 생성한 후 마운트하겠습니다.

------------

2.2. 호스트 시스템 요구 사항
2.2.1. 하드웨어
LFS 편집자들은 시스템 CPU에 최소 4개의 코어가 있고 시스템에 최소 8GB의 메모리가 있을 것을 권장합니다. 이러한 요구 사항을 충족하지 않는 이전 시스템도 여전히 작동하지만 패키지를 빌드하는 데 걸리는 시간은 문서에 나온 것보다 훨씬 길어집니다.

2.2.2. 소프트웨어
호스트 시스템에는 표시된 최소 버전의 다음 소프트웨어가 있어야 합니다. 이는 대부분의 최신 Linux 배포판에서는 문제가 되지 않습니다. 또한 많은 배포판에서는 소프트웨어 헤더를 종종 "<패키지 이름>-devel" 또는 "<패키지 이름>-dev" 형식으로 별도의 패키지에 배치한다는 점에 유의하세요. 배포판에서 제공하는 경우 이를 설치하십시오.

나열된 소프트웨어 패키지의 이전 버전은 작동할 수 있지만 테스트되지 않았습니다.

Bash-3.2(/bin/sh는 bash에 대한 기호 링크 또는 하드 링크여야 함)

Binutils-2.13.1(2.41보다 큰 버전은 테스트되지 않았으므로 권장되지 않음)

Bison-2.7(/usr/bin/yacc는 bison에 대한 링크이거나 bison을 실행하는 작은 스크립트여야 합니다)

Coreutils-7.0

Diffutils-2.8.1

Findutils-4.2.31

Gawk-4.0.1(/usr/bin/awk는 gawk에 대한 링크여야 함)

C++ 컴파일러, g++를 포함한 GCC-5.1(13.2.0보다 큰 버전은 테스트되지 않았으므로 권장되지 않음) C++ 컴파일러가 호스트된 프로그램을 구축할 수 있도록 C 및 C++ 표준 라이브러리(헤더 포함)도 있어야 합니다.

Grep-2.5.1a

Gzip-1.3.12

리눅스 커널-4.14

커널 버전 요구 사항이 있는 이유는 5장과 8장에서 glibc를 빌드할 때 해당 버전을 지정하므로 이전 커널에 대한 해결 방법이 활성화되지 않고 컴파일된 glibc가 약간 더 빠르고 작아지기 때문입니다. 2023년 6월 기준으로 4.14는 커널 개발자가 여전히 지원하는 가장 오래된 커널 릴리스입니다.

호스트 커널이 4.14 이전 버전인 경우 커널을 최신 버전으로 교체해야 합니다. 이에 대해 두 가지 방법을 사용할 수 있습니다. 먼저, Linux 공급업체가 4.14 이상의 커널 패키지를 제공하는지 확인하세요. 그렇다면 설치해 보시기 바랍니다. 공급업체에서 허용되는 커널 패키지를 제공하지 않거나 이를 설치하지 않으려는 경우 직접 커널을 컴파일할 수 있습니다. 커널 컴파일 및 부트 로더 구성(호스트가 GRUB를 사용한다고 가정)에 대한 지침은 10장에 있습니다.

UNIX 98 PTY(의사 터미널)를 지원하려면 호스트 커널이 필요합니다. Linux 4.14 또는 최신 커널을 탑재한 모든 데스크톱 또는 서버 배포판에서 활성화해야 합니다. 사용자 정의 호스트 커널을 구축하는 경우 커널 구성에서 CONFIG_UNIX98_PTYS가 y로 설정되어 있는지 확인하세요.

M4-1.4.10

Make-4.0

패치-2.5.4

Perl-5.8.8

파이썬-3.4

Sed-4.1.5

타르-1.22

텍스인포-5.0

Xz-5.0.0

[중요] 중요
이 책에 포함된 지침을 사용하여 LFS 시스템을 구축하려면 위에서 언급한 심볼릭 링크가 필요합니다. 다른 소프트웨어(예: dash, mawk 등)를 가리키는 Symlink는 작동할 수 있지만 LFS 개발 팀에서 테스트하거나 지원하지 않으며 지침에서 벗어나거나 일부 패키지에 추가 패치가 필요할 수 있습니다.

호스트 시스템에 적절한 버전이 모두 있는지, 프로그램을 컴파일할 수 있는지 확인하려면 다음 명령을 실행하세요.

비글 JS 시작하는 사람이 접근할 수 있는 프로젝트를 만들자.

1. CTRL + ALT + F1 을 통하여 인스톨 화면에서 쉘 화면으로 전환

2. 운영체제 업데이트

```sh
sudo apt update
sudo apt upgrade
```

시간이 조금 걸리네...
실패가 많아서 설치하지 위의 작업은 수행하지 않는다.

3. GIT 에서 다운로드

git clone https://github.com/beaglejs/hi.git














