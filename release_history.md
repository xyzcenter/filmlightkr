Baselight Release 5.2.12393 (2019-10-03)

베이스라이트 릴리즈 5.2.12393 버전 (2019-10-03)

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

DVI-to-SDI Convertors
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners performing that function are supported. At Baselight 5.3
Generation V systems will have to either be upgraded to the Baselight
Ultra High Definition option (see data sheet) which includes an AJA
Kona 4 PCIe card or revert to GPU DVI output. Earlier generation
systems will be constrained to a GPU DVI output only.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

New Features Since Baselight 5.2.12381
======================================

* Added support for reading ProRes encoded MXFs from the ALEXA Mini LF
  camera [bug 52776]
  알렉사 미니 LF 카메라로부터 프로레스로 엔코딩된 MXF 파일 읽기를 지원합니다. 

Bug Fixes Since Baselight 5.2.12381
===================================

* Fixed a failure in the bl-render commandline when omitting the
  "-filetype" parameter [bug 52795]

* Fixed ARRIRAW MXF failures in thumbnails and on systems with limited
  GPU memory [bug 52833]
  제한된 GPU 메모리로 인해서 썸네일과 시스템에서 ARRIRAW MXF 실패되는 부분 수정

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------
Baselight Release 5.2.12381 (2019-09-26)

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

DVI-to-SDI Convertors
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners performing that function are supported. At Baselight 5.3
Generation V systems will have to either be upgraded to the Baselight
Ultra High Definition option (see data sheet) which includes an AJA
Kona 4 PCIe card or revert to GPU DVI output. Earlier generation
systems will be constrained to a GPU DVI output only.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

New Features Since Baselight 5.2.12356
======================================

Dolby Vision
돌비비젼
------------


* Added support for Dolby Vision v4.0 in Analysis, Trim, Software CMU
  and XML export.
  분석, 트림, 소프트웨어 CMU, XML추출 등의 돌비비젼 버전4.0 지원 기능을 추가했습니다. 

  v4.0 Analysis adds an "L3 Mid Offset" option. v4.0 Trim adds
  additional advanced trim controls and six-vector secondary controls.
  버전 4.0의 분석(Analysis)기능에는 L3 미들 오프셋 옵션이 추가되었습니다. 트림에서는 추가적인 향상된 트림 컨털과 6벡터 세컨더리 컨트롤이 가능합니다. 

  v4.0 behaviour is enabled from Scene Settings View. Note that
  switching a scene between different CMU versions will delete all
  existing Dolby Vision Analysis and Trim strips [bug 50761]
  4.0 방식에서는 씬설정뷰가 가능합니다. 참고로 다른 CMU버전으로 씬을 스위칭할 경우 모든 돌비비젼 분석 및 트림스트립이 삭제됩니다. 



Toggle Previous Operator
이전 오퍼레이터로 스위칭 =
------------------------

* Added the ability to toggle between the current and the previous
  operator for quick and easy adjustment of two operators.
  현재와 이전 오퍼레이터사이에서 빠르고 쉽게 두 오퍼레이터 적용이 가능하도록 토글(스위칭)이 가능하게 되었습니다. 
  

  'Toggle Previous Operator' is available on the Select menu, the "="
  key, Chalk and on the Blackboard 2 and Slate default layouts.
  선택 메뉴에서 '이전 오퍼레이터로 스위칭'을 가능하게 할 경우 "=" 키나 블랙보드2/슬레이트 기본 레이아웃에서 선택가능합니다. 

  For Blackboard 1 and Blackboard Classic, operators can be toggled by
  holding Inside/Outside followed by any operator to the right of the
  Inside/Outside button [bug 51940]
  블랙보드1이나 블랙보드 클래식에서는 인사이드/아웃사이드 버튼을 누른 상태에서 인사이드/아웃사이드 버전의 오른쪽의 어떤 오퍼레이터로 스위칭할 수 있습니다. 



Final Cut Pro X XML Conform and Modify
파이널 컷 프로 X XML 컨펌 및 수정
--------------------------------------

* Added support for conforming Final Cut Pro X .fcpxml files, and
  modifying them to reference new media rendered from Baselight.
  파이널 컷 프로 X의 fcpxml 파일 지원 기능을 추가했으며, 베이스라이트로 부터 랜더된 새로운 레퍼런스 이미지 기반으로 xml을 수정할 수 있습니다. 

  Conform is supported from FCPXML files in the same manner as AAFs,
  XMLs, etc. Supported effects include dissolves, transforms and
  retimes.
  AAF나 XML등과 같은 방식으로 FCPXML로 부터 컨펌을 지원합니다. 디좉브, 트랜스폼, 리타임과 같은 이펙트를 지원합니다. 

  To update an FCPXML with rendered graded media:
  - Perform a Timeline Sort using the "FCP XML Rendering" tab
  - Select the "Movies, Video+Audio" tab in the Render View, choose
    File Type as a Quicktime Movie, and check the "Modify FCPXML"
    button
  - The updated FCPXML file will be written to the specified location
    once the render is finished [bug 18628]
  FCPXML과 같이 랜더된 색보정 데이터는 
  


Input Methods
입력방식
-------------

* On Linux, X11 Input Methods (see the desktop System->Preferences->
  Input Method menu) can now be used to enter non-ASCII characters
  into text fields in the application.
  리눅스에서 X11 입력방식(데스크탑의 시스템->설정->입력방식메뉴(Input Method menu)에서) 
  어플리케이션의 텍스트 영역에서 비 ASCII 캐릭터를 사용할 수 있게 되었습니다.  

  For example this permits using the AltGr modifier key for European
  characters like "ß", or by using a more complex input method for
  CJK characters.
  예를 들면, "ß" 유럽캐릭터를 위해서 AltGr(오른쪽Alt) 수정키를 사용하여 작성할 수 있거나 CJK(중국일본한국)캐릭터를 위한 복잡한 입력방식을 사용을 허용합니다. 

  This can be used for Burnins or Text strips when a suitable font is
  chosen for the text, or when entering filenames - but note that the
  characters may not be shown in the user interface [bug 51875]
  이는 적절한 폰트가 텍스트 또는 파일이름 입력을 우해서 선택된 경우, 번인 또는 텍스트 스트립을 
  사용할 수 있게 합니다. 그렇지만 유저 인터페이스에서는 캐릭터가 보이지 않습니다. 


Miscellaneous
기타기능
-------------

* Updated to Blackmagic RAW SDK 1.4. This adds support for the
  Blackmagic Pocket Cinema Camera 6K [bug 51786]
  블랙매직 로우 SDK 1.4가 업데이트 되었습니다. 블래매직 포켓 시네마 카메라 6K위한 기능 지원입니다. 

* Added option to disable active grade tooltips on the timeline.
  Right-click on the timeline to toggle "Display Active Grade Tooltip"
  [bug 52255]
  타임라인에서 활성화된 색보정 툴팁을 비활성화 할 수 있는 옵션을 추가했습니다. 타임라인에서 마우스 우클릭하여 "Display Active Grade Tooltip(활성화된 색보정 툴팁 보기)"를 스위치하여 비활성화 할 수 있습니다. 

* Updated the Sony XAVC Encoder to version 1.1.11. This improves
  parallel processing [bug 52305]
  소니 XAVC 엔코더의 1.1.11 버전으로 업데이트 했습니다. 이는 병렬 프로레싱을 개선시킵니다. 


* Movie formats that do not have integrated audio, e.g. 'DCI MXF' and
  'IMF MXF', are now available under the 'Movies Video+Audio' tab in
  the render panel. Renders for these filetypes can now be setup to
  output audio to a separate file [bug 39852]
  무비포맷에서 오디오가 포함되지 않은 예를 들면 DCI MXF와 IMF MXF의 경우 랜더 패널에서 
  Movie (Video+Audio)에서 랜더가 됩니다. 이와 같은 파일 타입의 랜더에서는 출력된 오디오의 분리된 파일형태의 설정을 할수 있습니다. 

* Modify AAF now allows clips to be split in the Baselight timeline
  before updating an AAF with Baselight grades; these splits are
  reflected in the updated AAF [bug 26315]
  

* Updated bl-openclip to support Open Clip files expressed with
  relative paths [bug 52373]

* Improved the detection of sequence versioning patterns during a
  conform to avoid as much as possible any ambiguity [bug 52102]

* FLUX Manage now shows "Grade Data" information when media has
  embedded BLG, CDL or LUT grades, and new filter tiles allow
  filtering based on this information [bug 52049]
  플럭스매니지(Flux Manage)에서는 미디어에 임베디드된 BLG, CDL, LUT 색보정 데이터에서 색보정 데이터 정보를 보여주며, 새로운 필터 타일에서는 이 정보기반으로 필터링을 가능하게 합니다.  

* Additional metadata, including per-frame metadata, is now shown for
  non-HEVC Canon MXF movies [bug 51755]
  프레임별 메타데이터를 포함한 추가 메타데이터가 있는 비 HEVC 캐논 MXF 무비 파이르 볼 수 있게 지원합니다. 


* Added Transform operator Customise menu option for enabling & 
  disabling 'Show Input' on tracker strips created for stabilisation
  [bug 52715]

* Allowed a sequence of images or a movie to be potentially part of
  several Open Clip files during a conform [bug 52603]

Bug Fixes Since Baselight 5.2.12356
===================================

* The sequence of Panorama encoders has been reordered to match
  the GUI layout. Each encoder has a reset button added underneath
  in order to be used on a Blackboard [bug 52217]

* The controls for Grid Warp control points have been moved to the 
  left-hand side of the Blackboard layout in order to be more clear
  [bug 52165]

* In the Colour Temperature operator, the default minimum and maximum 
  values of Old Temp have been changed to 3200K and 9800K
  respectively [bug 51529]

* Fixed crash in Base Grade graph pop-up menu [bug 52107]

* Fixed incorrect undo text in the edit menu, after an edit that
  didn't actually change anything [bug 52288]

* Fixed 50fps timecode calculation in some edge case sequences
  [bug 51836]

* Fixed crash when updating certain Premiere XML files [bug 50286]

* Fixed occasional crash in Layer View when toggling large matte
  view when a scene is closed [bug 52085]

* Correct timecode is now added to IMF Audio MXFs. This applies both
  to audio files rendered as part of IMF packages and audio files
  rendered using the "IMF Audio" filetype [bug 52348]

* Fixed the reported resolution and decoded image area of Nikon D4
  NEF-files to match the decode of other software such as Finder and
  Photoshop. Previously, the image was shifted to the right with loss
  of image data on the right hand side. This change affects any
  existing scenes using Nikon D4 NEF-files [bug 52310]

* Fixed an issue where audio OpAtom MXF files could fail to read a few
  audio samples at the end of the file. This could cause audible
  clicks at strip boundaries at some frame rates [bug 52284]

* Fixed potential crash when clicking on/selecting existing Despot 
  operator rectangles after a Despot strip had been split/temporally
  offset [bug 17238]

* Fixed issue where not all Color Correction effects would be removed
  from clips when updating an AAF with Baselight grades [bug 50844]

* Fixed an issue where highlights in DNG and Photo RAW files could
  change colour when changing the 'Always Decode At Max Quality'
  toggle button. The 'Always Decode At Max Quality' option is no
  longer shown for these files, as they're always decoded at max
  quality to avoid this issue. Existing sequence strips will retain
  the old behaviour [bug 52236]

* Fixed an issue where switching Chalk layouts would cause buttons
  to disappear [bug 52430]

* Fixed an issue that prevented 'Sequence + Audio File' renders from
  scenes with a Dolby Vision mastering display set in the scene
  settings [bug 52435]

* Fixed an issue that could cause renders of the filetype 'DCI Audio'
  to fail with an internal error when the scene working rate was not
  24fps [bug 52442]

* The default highlight reconstruction threshold in the DNG Params
  operator has been improved, which fixes issues with magenta or
  washed out highlights for some DNG-files [bug 52336]

* Layer View now remembers which stacks were shown when restarting
  [bug 52037]

* Fixed an issue that caused volumes to be temporarily unavailable 
  [bug 52513]

* Fixed rare crash when attempting to view the stack of a current shot
  within the Gallery [bug 52538]

* Associate OP-Atom audio files with the appropriate video sequences
  during conform [bug 49986]

* Fixed occasional crash in Text operator [bug 51180]

* Fixed an issue when an Open Clip file had relative path versions in
  its own directory [bug 52389]

* Fixed a bug in the Sequence Operation UI with the version drop down
  displaying incorrectly "Not a known version" [bug 52371]

* Fixed a potential bug when scanning the versions of a sequence
  versioning pattern and not being able to disambiguate a given
  version Id [bug 52417]

* Fixed an issue with "Strip Auto Select On" when moving to a new shot
  and not selecting a strip in an equivalent substack as the previous
  selected strip when it was possible [bug 51762]

* Fixed an issue that could prevent some crash reports from being sent
  to FilmLight [bug 52093]

* Fixed issue whereby some AAFs would fail to load [bug 52203]

* Fixed issue with Media Import Rules View and read only scenes 
  [bug 52580]

* Fixed an issue with IMF CPLs where the IntrinsicDuration and
  SourceDuration entries for the video track in HDR IMF-packages was
  incorrectly set to 0 [bug 52589]

* Added additional metadata in the picture essence descriptor of IMF
  MXFs. This fixes XML-schema validation issues for IMF-package CPLs
  [bug 52590]

* Fixed issue where database backup diagnostic would fail on systems
  set with a non-English default language [bug 52605]

* Changed colour space assigned to Rec.709 QuickTime movies based on
  metadata; previously it used "Rec.709 Camera: ~1.95 Gamma /
  Rec.709", now it uses "Rec.1886: 2.4 Gamma / Rec.709" [bug 52604]

* Fixed tooltip text for "Rec.2020: ST 2084 PQ / Rec.2020 / 108 nits"
  and "Dolby: ST 2084 PQ / P3 D65 / 4000 nits" colour spaces
  [bug 52005]

* Fixed problems with Media Import Rules View and read-only scenes
  [bug 52580]

* Fixed an issue where audio could fail to render with a warning about
  source data not containing the required samples [bug 52124]

* Fixed issue where numeric keypad bumps would lag in Film Grade 
  [bug 52619]

* Fixed an issue where attempting to submit a render with duplicate
  filenames would produce an incorrect error message [bug 51884]

* Fixed network connection issues when a 'share' volume was defined
  within a zone in volume.cfg [bug 52650]

* Fixed thumbnail issues with RMF media [bug 52666]

* Fixed errors when pasting a Dolby Vision Trim strip into a scene
  that has no Dolby Vision Mastering Display set [bug 52663]

* Fixed some Matchbox shaders not appearing in the Shader dialog
  [bug 52628]

* Improved appearance of Paint strokes while drawing additional
  strokes [bug 52488]

* The extraviewingconditions file is no longer used [bug 52221]

* Improved error message when using unsupported timecode rates when
  exporting CMX EDLs [bug 52012]

* Some GPU errors, notably out-of-memory, are now reported rather than
  causing a crash [bug 51208]

* Fixed errors caused by changing workspace while dragging [bug 50171]

* Improved the decode speed of some codecs using planar Y'CbCr in
  QuickTime and MXF containers. This improves the performance of Grass
  Valley HQX in particular [bug 24375]

* Fixed crash after changing the preference database during
  application startup [bug 52437]

* Improved error messages from database connection errors [bug 52542]

* Fixed multi-paste not applying the colourspace when pasting from 
  BLGs [bug 51473]

* Fixed a bug after a conform with Open Clip, where missing versions
  in the Sequence operator's versions drop down could potentially have
  a wrong name [bug 52582]

* Fixed a bug in the manual selection of movies/sequences per event 
  in EDL-import view [bug 52601]

* Fixed crash in some uses of the Paint operator [bug 51075]

* Fixed a potential crash while detecting sequence versioning after 
  inserting media from FLUX Manage [bug 52560]

* Fixed %C being lost from Sequence filenames after manual edits are
  made [bug 52748]

* Fixed a rendering artefact when metadata-driven burnin text is
  empty [bug 52402]

* Fixed a potential crash when upgrading 4.4m1 jobs where every scene
  in the job is unable to be upgraded [bug 51820]

* Fixed an occasional crash in flit service when local-to-local
  copy is cancelled [bug 52683]

* Fixed crash when dynamically generated burnin text is empty
  [bug 52761]

* Fixed OFX GPU memory errors [bug 52759]

* Fixed error changing a Sequence to use new media, when there was no
  original media, for example due to conforming with "Setup for Tape
  Ingest" [bug 52757]

* Fix crash where Scene Detect is running in one scene and swapping to
  another cursor in a different scene [bug 52740]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------

Baselight Release 5.2.12356 (2019-09-24)

Bug Fixes Since Baselight 5.2.12304
===================================

* Fixed data corruption when copying files to some SAN volumes with
  FLUX Manage or fl-cp [bug 52723]

* Fixed image corruption in "Default"-mode Video Grade operators when
  using the version 418 nvidia driver [bug 52421]

* Fixed image corruption in some Looks when using the version 418
  nvidia driver [bug 52626]

--------------------------------------------------------------------------
Baselight Release 5.2.12304 (2019-09-09)
베이스라이트 릴리즈 5.2.12304 (2019-09-09)


Important Notes
===============

Compatibility With 5.1
5.1 버전과의 호환성 
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.
새로운 이미지 트랜스폼 설정으로 인해서(자세한 내용은 아래 리스트 참조), 5.2에서 새로운 씬을 저장할 경우 5.1 버전에서는 더 이상을 열리지 않습니다. 

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.
호환성을 위해서 베이스라트, 데이라이트, 플럭스 스토어에는 원격으로 지속적인 이미지 디코딩 작업을 하기위해서 5.2 버전 릴리즈가 설치되어 있어야 합니다. 

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.
버전 5.2에서 BLG파일을 추출한 경우 베이스라이트 에이션을 포함한 5.1버전 제품에서는 사용할 수 없습니다. 

Baselight FOUR and EIGHT 베이스라이트 4(Four)/ 8 (Eight)
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.
베이스라이트 5.2 버전이 베이스라이트 4/8 시스템을 지원하는 마지막 버전이 됩니다. 베이스라이트 5.3버전에서는 설치되거나 실행할 수 없습니다. 

DVI-to-SDI Convertors
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners performing that function are supported. At Baselight 5.3
Generation V systems will have to either be upgraded to the Baselight
Ultra High Definition option (see data sheet) which includes an AJA
Kona 4 PCIe card or revert to GPU DVI output. Earlier generation
systems will be constrained to a GPU DVI output only.

Baselight CONFORM 베이스라이트 컨펌 
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]
macOS 10.14 모하비에서 베이스라이트 컨펌 설치와 실행을 지원합니다. MacOS 10.9, 10.10, 10.11 은 더이상 지원하지 않습니다. 

Bug Fixes Since Baselight 5.2.12238
버그개선 
===================================

* Fixed image corruption after changing to a different nvidia driver version [bug 52421]
다른 엔비디아 드라이버 버전으로 변경시 이미지가 깨지는 문제 개선

* Fixed connection errors when /etc/hosts contains multiple entries
  for the same hostname [bug 52485]

* Fixed licensing errors when a bonding interface is present
  [bug 35262]

* Fixed Debug menu being shown on the menu bar [bug 52547]
메뉴바에 디버그 메뉴가 보이는 문제 수정

* Fixed being ability to access decode parameters in Media Import
  Rules View [bug 52579]

* Fixed issue where various default values were disabled for
  different grading operators [bug 52553]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------




Baselight Release 5.2.12238 (2019-08-22)
베이스라이트 릴리즈 5.2.12238 (2019-08-22)


Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

DVI-to-SDI Convertors
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners performing that function are supported. At Baselight 5.3
Generation V systems will have to either be upgraded to the Baselight
Ultra High Definition option (see data sheet) which includes an AJA
Kona 4 PCIe card or revert to GPU DVI output. Earlier generation
systems will be constrained to a GPU DVI output only.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

New Features Since Baselight 5.2.12057
======================================

FilmLight Image Transfer 
필름라이트 이미지 전송
------------------------

* The new FilmLight Image Transfer (FLIT) service accelerates copying of media using FLUX Manage or fl-cp. 
새로운 필름라이트 이미지전소(FLIT, 플릿) 서비스는 플럭스 매지니또는 fl-cp 복사 프로그램르 사용하여 미디어를 복사하는데 가속화시킵니다. 

  FLIT automatically uses the fastest network link (or pair of links) connecting the source and destination systems, and will use almost all the network capacity, if the storage is fast enough.
플릿(FLIT)는 소스와 대상 시스템을 연결하는 가장 빠른 네트워크 링크(또는 쌍으로 된 링크)를 자동으로 사용하며, 스토리지가 충분히 빠른 경우 거의 모든 네트워크 용량을 사용합니다. 


  When writing image sequences to FilmLight storage, FLIT uses the most efficient layout for fast playback.
이미지 시퀀스(소스)를 필름라이트 스토리지에 쓸 경우 플릿는 빠른 재생을 위한 가장 효율적인 레이아웃을 사용합니다. 


  Files copied using FLIT are unmodified by the copy (unlike image files in certain formats copied using older FilmLight tools).
플릿을 (이전의 필름라이트 툴을 사용하여 특정 포맷의 이미지 파일과는 달리) 사용하여 복사한 파일은 복사로 인해서 수정되지 않습니다. 



  FLIT can copy files with restrictive permissions which can only be read or written as a result of extended group membership (unlike older FilmLight tools).
플릿는(이전 필름라이트 툴과 달리) 확장된 그룹 멤버쉽결과로 제한적은 권을 가지고 읽거나 쓸수 있습니다. 


  FLIT can copy files between locations that are not both accessible to one single machine, for example from a removable drive on one  system to a removable drive on another system [bug 49593]
플릿은 하나의 단일 시스템에서 둘다 액세스할 수 있는 위치간의 파일을 복사할 수 있습니다. 예. 한시스템의 이동식 드라이브에서 다른 시스템의 이동식 드라이브로 이동

Sequence Versioning 
시퀀스 버전닝
-------------------

* Added support for Sequence Versioning, which allows a Sequence
  operator to switch between different versions of the input media. It
  also allows the Sequence operator to scan for new versions of the
  input media and, optionally, switch to a new current version. This
  means that the user can quickly update a scene to reflect new
  versions of the input media with needing to conform or manually load
  media using FLUX Manage.

  Sequence Versioning comes in two forms:
   - Open Clip Versioning: Open Clip files are XML files (the format
     was developed by Autodesk) which refer to multiple versions of
     the media representing a clip. A separate Open Clip file is
     generated for each shot which requires sequence versioning and is
     then modified as new versions arrive. Baselight detects changes
     in Open Clip files and then scans for any new media referenced by
     the Open Clip. The simple file format makes them very easy to
     generate and update by 3rd-party tools, meaning that updating
     Baselight scenes to reflect new versions can be completely
     automated by using Open Clip files to reflect, say, the contents
     of a post house's asset database.

   - Filename Versioning: In this type of versioning, Baselight looks
     for sub-strings in file names which look like version numbers
     (e.g "_v1" or ".V34") and replaces them with the new %V
     substitution. Then, when scanning for new versions, it detects
     all media which matches this template. The simplicity of this
     scheme makes it very easy to integrate in pipelines between VFX
     and finishing - the rendered VFX media simply need to be produced
     with a consistent naming scheme in which versioned filenames
     diffe only in version numbers [bug 27173]

* Reflecting the fact that there are two types of Sequence Versioning,
  there are two sets of versioning-related settings in the EDL Import
  panel:
   - Open Clip versioning: To conform using Open Clip files, switch on
     the "Use Open Clip" toggle in the "Media" section. Then, in the
     drop-down to the right of the button, select the directory
     containing the Open Clip files which refer to the media being
     conformed. Finally, if you're confident that *all* the media to
     be conformed should be referenced by an Open Clip file, switch on
     the "Restrict" toggle, which ensures that media not referenced by
     Open Clip will ignored when scanning for media.

     It is still necessary to set one or more search directories to be
     scanned for media. At the very least, the search directories
     should contain the media representing the current version of each
     shot.

     Then, conform as normal. If any of the filenames of media in the
     search directory match filenames in Open Clip files, any Sequence
     operators generated will be sequence-versioned and pointed at the
     matching Open Clip file.

   - Filename versioning: If "Use Open Clip" is switched off, then the
     "Sequence Versioning" option becomes available. In it, select
     "Detect Versions in Paths and/or Filenames" to enable filename
     versioning. With it enabled, Baselight will look for version
     numbers in matching media and if they are found, any Sequence
     operators generated will be sequence-versioned, with the
     appropriate %V substitutions.

* It is also possible to add sequence versioned media from FLUX
  Manage. Simply inserting media which contains version numbers will
  produce the "Sequence Versioning" dialog which allows the user to
  decide whether or not to use sequence versioning in the Sequence
  operators inserted.

  Known issues:
   - It isn't currently possible to insert Open Clip files using FLUX
     Manage, other than via the "Browse for New Sequence" button in
     the Sequence operator UI.
   - The FLUX Manage UI is not currently sequence versioning aware -
     it doesn't treat Open Clip (.clip) files as image files and only
     detects version numbers in the filenames when inserted into the
     timeline.

* If a Sequence operator is versioned, the Sequence UI changes to
  reflect this:
   - If the sequence is Open Clip-versioned, the "File Name" edit
     field will contain the path to an Open Clip (.clip) file, rather
     than a path to image media.
   - If the sequence is filename-versioned, the "File Name" edit field
     will contain a template with one or more %V substitutions.
   - A "Version" drop-down appears containing the versions of the
     input media detected so far. The current version's version name
     will be drawn in green. For Open Clip versioning, if a version
     couldn't be found, the filename of the version will be shown in
     grey, rather than blue.

   - In the "Actions" menu, two additional options appear:
      - Change to Current Sequence Version: If selected, then the
        Sequence's version is changed to be the current version in the
        Open Clip or the filename version with the highest number.
      - Check for New Sequence Versions: Pops up a dialog which scans
        for new versions of the input media.

     Both of these actions work with grouped grading switched on,
     making it easy to update versions of multiple Sequence operators
     in one go.

* To scan for updated versions of *all* the shots in the scene, the
  "Check for New Sequence Versions" action has been added to the
  "Baselight" menu. Selecting it pops up a dialog which will scan for
  new media and will also provide the following options:
   - Add Category to Updated Shots: If "Yes", then the user can add a
     category to those shots which have new versions.
   - Create Tab in Shots View: If the previous setting is "Yes", then
     the user has the option of creating a Shots view tab which will
     show those shots which have new versions.
   - Set Current Version in Updated Sequence: If "Yes", all Sequence
     operators with new versions will be modified to point to the
     current version. Without this, the current version of all
     sequences will be left alone.

* To force a check for new sequence versions when the scene is opened,
  a new "Check for Sequence Version Changes" option has been added to
  the "General" tab in the Scene Settings view.

* To assist in creating and updating Open Clip files, the bl-openclip
  command line tool has been added. Usage information is available by
  running the tool with no arguments.

IMF Packages
IMF패키지
------------

* Added support for writing IMF packages of type Application 2e. The
  The DCP tab in the render panel has changed name from 'DCP' to 'DCP
  / IMF'. The type selector in this tab now contains the following IMF
  package options:
어플리케이션 2e 유형의 IMF패키지 생성지원이 추가되었습니다. 랜더 패널안의 DCP탭이 ‘DCP’에서 ‘DCP/IMF’로 변경되었습니다. IMF 패캐지 옵션에는 다음과 같은 선택이 가능합니다. 

  - IMF: Application 2e: This option will create a package compliant with SMPTE 2067-21.
IMF: 어플리케이션 2e: 이 옵션은 SMPTE 2067-1을 준수하는 패키지를 만듭니다. 

    The video encoding is selectable between IMF profile or Broadcast
    Contribution profile JPEG 2000 with or without subsampling. The
    same set of video codec parameters that are available when
    rendering these profiles to the 'J2C' or 'IMF MXF' filetypes are
    available for this package type.
비디오 엔코딩은 서브샘플링이 있거나 없는 IMF 프로파일이나 브로드캐스트 컨트리뷰션 프로파일 JPEG2000을 선택할 수 있습니다. J2C나 IMF MXF 파일유형과 같은 랜더링이 가능한 패키지를 사용할때 같은 비디오 코덱 변수 세트를 선택할 수 있습니다. 

    Audio is optional and can be either 48kHz or 96kHz 24-bit PCM.
    Audio codec parameters can be used to set the language tag and the
    applied Multi Component Audio (MCA) tags are fully configurable
    using the audio codec parameters dialog in the render panel. The
    same set of audio codec parameters that are available when
    rendering the 'IMF Audio' filetype is available for this package
    type.

    The render panel will show an entry for 'IMF Colour Tag' in the
    'Video' selector when selecting this package type. The IMF Colour
    Tag entry contains a text field which shows which tag will be
    applied, if any. It also has a 'Change...' button to assist in
    setting up output for the different colorimetry systems.

    MaxCLL/MaxFALL metadata can be added by enabling the analysis of
    these values in the render panel.
랜더패널에 이러한 분석을 활성화하면 MaxCLL/MaxFALL 메타데이터를 추가할 수 있습니다. 

  - IMF: Application 2e with Dolby Vision Mezzanine: As above but the
    video file will be a Dolby Vision Mezzanine MXF with embedded
    Dolby Vision metadata. This option only appears if a Dolby Vision
    mastering display has been set in the scene settings. This package
    type will not display the 'IMF Colour Tag' entry in the 'Video'
    selector. The available colour spaces are restricted to the
    relevant Dolby mastering spaces and the bitdepth is locked to
    12-bit.

    Analysis of MaxCLL/MaxFALL is always performed for this package
    type and metadata will be added to the created CPL.

  - IMF: Netflix SDR: This option is a subset of the "IMF: Application
    2e" package type, with the available resolutions and codec options
    locked to match the SDR packages defined in Netflix Originals
    Delivery Specification version OC-3-2. The colour space must be
    Rec.1886: 2.4 Gamma / Rec.709, and the frame rate must be one of
    23.976 / 24 / 25 / 29.97 / 30 / 50 / 59.94 / 60 for packages to be
    compliant.

  - IMF: Netflix HDR: This option is a subset of the "IMF: Application
    2e with Dolby Vision Mezzanine" package type, with the available
    resolutions and codec options locked to match the HDR packages
    defined in Netflix Originals Delivery Specification version
    OC-3-2. The colour space must be ST 2084 PQ / P3 D65, and the
    frame rate must be one of 23.976 / 24 / 25 / 29.97 / 30 / 50 /
    59.94 / 60 for packages to be compliant.

  All IMF package types will present an 'IMF' selector in the render
  panel that allows configuration of the package title, content kind,
  content version, issuer, originator and created file names. The
  package title will be copied to the annotation field in the created
  ASSETMAP, CPL, PKL and OPL files.

  The available DCP packages types are 'DCP: Interop' and 'DCP:
  SMPTE'. Wether to include audio was previously part of the DCP
  package type selection, but is now configured using the 'Enable
  Audio' toggle in the render panel [bug 26866]

* Added a new filetype called "IMF Audio". It allows 48kHz and 98kHz
  24-bit PCM audio to be written to AS-02 MXF containers. MCA audio
  channel labels and soundfield group labels can be configured using
  the codec parameters dialog in the render panel. By default, the
  audio channel layout tags will be used to label individual channels
  where possible. Soundfield groups for stereo (ST), 5.1 (51) and 7.1
  (71) channel audio will be applied if the output tags L+R,
  L+R+C+LFE+Ls+Rs or L+R+C+LFE+Ls+Rs+Lrs+Rrs are
  present. E.g. 'ST(L+R)' will be used for 2ch audio with output tags
  Left + Right.

  The 'MCA Configuration' entry in the codec parameters for this file
  type accepts the following audio channel labels:
     L               : Left
     R               : Right
     C               : Center
     LFE             : Low Frequency Effects
     Ls              : Left Surround
     Rs              : Right Surround
     Lss             : Left Side Surround
     Rss             : Right Side Surround
     Lrs             : Left Rear Surround
     Rrs             : Right Rear Surround
     Lc              : Left Center
     Rc              : Right Center
     Cs              : Center Surround
     HI              : Hearing Impaired
     VIN             : Visually Impaired-Narrative
     M1              : Mono One
     M2              : Mono Two
     Lt              : Left Total
     Rt              : Right Total
     Lst             : Left Surround Total
     Rst             : Right Surround Total
     S               : Surround
     -               : No label
     NSC001 - NSC128 : Numbered Source Channel

  The available soundfield group labels are:
     51   : 5.1
     71   :  7.1DS
     SDS  : 7.1SDS
     61   : 6.1
     M    : 1.0 Monaural
     ST   : Standard Stereo
     DM   : Dual Mono
     DNS  : Discrete Numbered Sources
     30   : 3.0
     40   : 4.0
     50   : 5.0
     60   : 6.0
     70   : 7.0DS
     LtRt : Lt-Rt
     51Ex : 5.1EX
     HA   : Hearing Accessibility
     VA   : Visual Accessibility

  MCA configuration is specified using a comma separated list of audio
  channel labels and soundfield group labels. Soundfield group labels
  define the audio channels that belong to the group by a comma
  separated list of audio channel labels within parentheses.

  Labels are applied in the order they occur in the configuration
  string. For example, to explicitly tag a L+R stereo configuration,
  set the MCA configuration entry to 'ST(L+R)'. This will add the
  audio channel label 'L' to the first channel, and 'R' to the
  second. Both are then wrapped in the soundfield group label 'ST'.

  A more complex MCA configuration example could look like
  'ST(L,R),DNS(NSC001,NSC002),-,VIN'. This will label channels 1-2 as
  being the left and right channel of a stereo configuration. Channel
  3-4 will be labeled as numbered source channels 1 & 2 and wrapped in
  a soundfield group label of the "Discrete Numbered Sources"
  type. Channel 5-6 will be untagged and tagged "Visually
  Impaired-Narrative" respectively. Neither channel 5 nor 6 will be
  part of a soundfield group label.

  If there are more channels than tags, remaining channels will be
  untagged. This means that a single '-' can be used to disable MCA
  tagging completely.

  The codec parameters for language, title, title version, content
  kind and element kind will set the corresponding MCA tags for spoken
  language, title, title version, etc, in each defined soundfield
  group label [bug 26866]

Miscellaneous
-------------

* The command-line copying tool fl-cp has been rewritten to use the
  fluxc command to enqueue copies in the Operations Queue and then to
  monitor their progress [bug 50601]

* Updated the Sony RAW SDK to version 3.3.0, which adds support
  for reading X-OCN 4K 2.39:1 bitstreams [bug 51227]
소니 RAW(로우) SDK 버전 3.3.0 지원 : 이를 통해서 X-OCN(소니 고유 로우 포맷)의  4K 해상도 2.39:1 비율(4096x1716)을 지원


* Added support for reading additonal metadata from Sony MXF-files,
  including Cooke protocol lens metadata [bug 51855] 
소니 MXF파일에서 쿠크 렌즈 메타데이터기록되어 있을 경우 읽을 수 있어서 편리하게 표준/와이드/광각을 사용했는지 확인이 가능

* Improved metadata-based input colour space selection for EXR files
  which were written by Baselight/Daylight [bug 51808]

* QuickTime colour space tags ('nclc' and 'gama') are now used to
  assist metadata-based input colour space selection [bug 51981]

* The interpretation of QuickTime colour space tags ('nclc' and
  'gama') are now shown as metadata in FLUX Manage [bug 51987]

* Added support for reading Avid DNxUncompressed MXF files [bug 51554]

* In Render View, when using a Render Frame Rate which is different
  from the scene's Working Frame Rate, "Frames To Render" now always
  shows frame numbers at the Working Frame Rate, and text alongside
  "Render Frame Rate" now indicates the frames that will be rendered
  at the Render Frame Rate [bug 38602]

* Added options in Setup editor for choosing 48, 50 and 60fps timeline
  timecodes [bug 52015]

* Updated to ARRIRAW SDK v5.5. This adds support for the ALEXA Mini LF
  camera [bug 52385]

* Added "Document Library" to the Help menu, which opens the Document
  Library page of the FilmLight website [bug 52145]

* Updated to DNxHD/DNxHR SDK version 2.5.2. This includes bug fixes
  [bug 52326]

* Added support for RTX 2080 Ti graphics card, using the 418.56 driver
  [bug 51764]

* Fixed an issue that affects the browsing of movies with frame rates 
  that are greater than 255 [bug 52039]

Bug Fixes Since Baselight 5.2.12057
===================================

* Improved Texture Highlight help text [bug 50241]

* Fixed an issue with Sony MXF-files where the format frame rate
  would be used instead of the capture frame rate [bug 51373]

* Added a note about Looks to FilmLight's scene template tooltip 
  [bug 51752]

* Added a customise option in the Shape operator to set a default 
  intershape operation [bug 51528]

* Increased the default exposure of Photo RAW files with one stop when
  blending highlights. This makes exposure match better when switching
  between the two highlight handling modes 'Blend' and 'Clip' in the
  Photo RAW Parameters operator [bug 51753]

* Fixed hang in Shots View when trying to substitute a column value
  into itself [bug 51710]

* Fixed incorrect display and behaviour of selected shots button in
  Media Import Rules View [bug 51766]

* Fixed issue where bypassing all wasn't correctly updating in Layer
  View [bug 51926]

* Fixed indication of gamma curve EOTF in Render View Colour Space
  Tagging menu [bug 51956]

* Fixed Smart Paste pasting onto source stack creating strange gaps
  in stack [bug 52026]

* Fixed crash when conforming using 'static text' in a Media Import 
  Rule with 'Setup for tape ingest' [bug 51311]

* Fixed sorting of some Shots View columns not working after editing
  them after a conform [bug 51800]

* Fixed Media Import Rules View not enabling/disabling correctly
  [bug 52019]

* Fixed crash in Layer View when updating selections [bug 51892]

* In the Text operator shortened escape strings, such as '%F' for
  %{TimelineFrame}, now update correctly [bug 52072]

* Fixed failures on some Baselight FOUR/EIGHT systems, typically seen
  when accessing a file system mounted on the io node [bug 52066]

* Fixed a crash when loading a font file that doesn't specify a style
  name [bug 52108]

* Fixed 50fps timecode calculation in some edge case sequences
  [bug 51836]

* Fixed issue in layer number selector whereby the thumbnails were
  too large [bug 51805]

* Layer names shown in the Layer View are now clipped correctly when
  resizing and the name doesn't fit the thumbnail [bug 51763]

* Fixed issue in Gallery causing comments to disappear when they
  become too long [bug 51525]

* Fixed issue where Layer View controls would be disabled when
  Cuts View was not shown [bug 52276]

* Fixed delays caused where a badly-configured DNS takes a long time
  to give a negative response [bug 52064]

* Fixed crash in bl-conform when source directories were not 
  expressed using volume names [Bug 51934]

* Allow selection of timecode framerate format when conforming 50fps
  AAFs [bug 52007]

* Fixed bug where explicit layer paste on Slate could leave the paste
  operation in progress [bug 52339]

* Fixed missing SignalRange entry in Dolby Vision XML [bug 52361]

* Fixed crash when changing keyer type in a layer [bug 52394]

* Fixed error on Dolby Vision View if it is opened before a scene is
  open [bug 52424]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------


Baselight Release 5.2.12057 (2019-07-19)

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

Bug Fixes Since Baselight 5.2.12039
===================================

* Fixed crash related to cached strips encountered in some situations
  [bug 46466]

* Fixed unresponsiveness on macOS [bug 52071]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------



Baselight Release 5.2.12039 (2019-07-15)

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS 10.9, 10.10 or 10.11 are no longer supported [bug 50131]

New Features Since Baselight 5.2.11913
======================================

Layer View
레이어 뷰
----------

* Along with a new look, Layer View can now follow both the current cursor and the DBS cursor.

  Layers can be easily drag and dropped between the current cursor and DBS cursor.

  Added the ability to change between viewing the current cursor, DBS cursor, or both cursors.

  Renamed 'Show Matte' to 'Large Matte' to better reflect its function.

  Resizing the view has been made consistent to keep text readable.

  Multiple layers can now be selected within a layer stack using Control and/ or Shift keys; allowing for multiple layers to be drag and dropped.

  A temporary floating Layer View from Cuts View now moves correctly when moving the DBS and layers can be properly selected using a Blackboard or Slate.

  Layer View titles for cursor stacks now better reflect what is selected.

  When dragging layers, the provided information for what is being
  dragged and what will occur when you drop the layers at the current
  destinaton has been made more accurate.

  Layers can now be selected in Gallery shots via the layer View,
  allowing multiple layer drag and drop from the Gallery [bug 49421]

* Added a button in Layer View when showing both Current and DBS
  cursor stacks to swap their positions [bug 50891]

* Layer names are now shown for easier location of layers and there is
  an option within Layer View to hide layer names [bug 50906]

Dolby Vision
돌비비젼
------------

* Added option to perform Dolby Vision analysis at the poster frames
  of all selected strips, to enable a draft preview render to be
  produced quickly [bug 49863]

* Target displays that are as bright or brighter than the mastering
  display do not use Software CMU, so their colour spaces are no
  longer offered in Cursor View or Render View [bug 51515]

Miscellaneous 기타
-------------

* Changed Master, Red, Green, Blue, Luma (Y) Curve Grade axis labeling
  from 10 bit values to normalised 0->1 values [bug 50696]

* Added a toggle button to the selection menu for obeying playback
  filtering; enabling strip and stack selection to obey the current
  playback filter [bug 50579]

* Added a diagnostic test for the SDI card temperature to the Video
  submenu [bug 50205]

* Avid MXF "Disk Label" metadata is now shown [bug 51538]

* The installer on Linux now uses more efficient 'xz' compression
  [bug 51540]

* Mastering Colour Space information is now stored in QuickTime movies
  (in the new mdcv atom), and this metadata is also read from such
  movies [bug 51652]

* MaxCLL/MaxFALL analysis is now stored in QuickTime movies (in the
  new clli atom), and this metadata is also read from such movies. A
  new option on Render View allows this data to only be stored in the
  movies without also writing a sidecar XML file [bug 51652]

* When rendering to OpenEXR using a display-referred colour space, the
  colourimetry of the space is now stored in the file [bug 51659]

* The "Colour Space Tagging" menu on Render View, which is shown when
  rendering to QuickTime movies, now shows the tags that will be
  written to the output files [bug 51671]

* Added FLUX Manage filter tiles "Has image channel", "Has image
  track", "Image channels" and "Image tracks" to assist filtering of
  multi-channel OpenEXR files [bug 51447]

* Mastering Colour Space information is now read from metadata in MXF
  movies [bug 51566]

* Added Histogram waveform to Base Grade. Right-click on the waveform
  to switch between the two waveforms. Base Grade will retain the last
  used waveform settings on restart [bug 37225]

* Updated to RED SDK 7.0.8. This contains fixes as follows:
레드 SDK 7.0.8이 업데이트되었습니다. 다음과 같이 개선이 포함됩니다. 
  - REDWideGamutRGB output incorrectly had gamut mapping applied
    in IPP2; this fix may cause very saturated colours to change
  - HLG rendering artifacts
  - memory leak
  - missing audio for incomplete DSMC clips [bug 51660]


* Improved the ability for an OFX plugin to request a large amount of
  GPU memory [bug 50245]

* Added support for reading audio from OpAtom MXF-files. This adds
  support for audio MXF-files written by Avid [bug 51380]

* Added support for rendering Dolby Vision Mezzanine MXF files. This
  file type contains JPEG 2000 compressed image data and frame wrapped
  Dolby Vision XML. The available JPEG 2000 profiles are "IMF
  Profile", "IMF Profile YCC 422", "Broadcast Contribution Profile"
  and "Broadcast Contribution Profile YCC 422" with the same encoding
  options as for the IMF MXF filetype, except for bit depth which is
  locked to 12-bit.

  The "Dolby Vision Mezzanine MXF" filetype only appears if a Dolby
  Vision mastering display has been set inte the scene settings. The
  available colour spaces are restricted to the relevant Dolby
  mastering spaces.

  The ASDCP library has been updated from version 2.7.19 to version
  2.10.32. This fixes partition version and index rate metadata issues
  in AS-02 MXF-files, as used with the "IMF MXF" filetype.

  Mastering Colour Space information is now stored in Dolby Vision
  Mezzanine and IMF MXF movies using SMPTE mastering display labels
  [bug 48053]

* Added support for creating Dolby Vision ISXD MXF files. This file
  type is an IMF compliant metadata only track based on SMPTE RDD 47.
  The "Dolby Vision ISXD MXF" filetype only appears if a Dolby Vision
  mastering display has been set inte the scene settings.

  Dolby Vision ISXD MXF does not contain image data, but images are
  still rendered to perform MaxCLL/MaxFALL analysis. Available colour
  spaces are restricted to the relevant Dolby mastering spaces
  [bug 51417]

* fl-diag will now suggest an upgrade of the nvidia driver on
  compatible systems; doing this will enable Blackmagic RAW and ProRes
  RAW support [bug 51336]

* Added support for 3x1 tiled output for DVI/HDMI/DisplayPort video
  output configurations [bug 51480]

* Improved Zoom/Pan behaviour. It is now possible to zoom in close to
  a particular subject in the image in bird's eye mode. This frees the
  need to pan the image to readjust its centre [bug 51108]

Bug Fixes Since Baselight 5.2.11913
===================================

* Fixed bug in Curve Grade's Saturation vs Lightness curve which
  prevented setting saturation values greater than 1 [bug 45428]

* Changed Curve Grade axis labeling from 10 bit values to normalised
  0->1 values [bug 50696]

* Ensured that clips with variable retimes from AAFs have appropriate
  static retimes in the case that variable retimes are not applied
  [bug 51275]

* Fixed an issue reading MXF-files with index partitions written
  before the corresponding essence partitions [bug 51084]

* Fixed an issue where double-frame timecode in MXF-files was
  incorrectly calculated if the timecode edit rate was different to
  the frame rate [bug 51374]

* Reduced amount of RAM required when opening very large scenes
  [bug 51353]

* Improved scene load times when using extremely large job databases
  [bug 51576]

* Improved job export times when using extremely large job databases
  [bug 51590]

* Relaxed out of memory threshold to prevent out of memory killer
  thread from killing Baselight prematurely [bug 51278]

* Fixed a rare remote grading notification has mismatch error
  [bug 51094]

* Removed some legacy settings from the Decode Parameters Tab within
  Media Import Rules View [bug 51239]

* Fixed incorrect labels being shown for the R3D Params "Highlight
  Roll Off" control. The image is not affected by this change, just
  the on-screen labels [bug 51445]

* Fixed an issue that caused renders to 8-bit IMF MXF to produce
  broken images [bug 51456]

* Fixed Transform Alarm Overlay to work with transform strips that
  have "Flip" or "Flop" enabled [bug 48397]

* Network card config diagnostic now warns if no link speed has been
  found [bug 50985]

* Fixed crash closing application when licence has expired [bug 51212]

* Fixed crash when using Playback Filtering when the cursor is beyond
  the end of the timeline [bug 51612]

* Fixed crash in Text operator when editing text field during playback
  [bug 51224]

* Improved speed of updating Shots View highlights [bug 51550]

* Increased RAM requirements in diagnostics when running on Gen VII
  hardware [bug 51343]

* Fixed colour space identification of ARRI QuickTime files as LogC
  [bug 51575]

* Fixed crash when applying Media Import Rules [bug 51643]

* Fixed crash when inserting many Text operators [bug 51308]

* Improved speed of Media Import Rules View response to selection
  changes [bug 51648]

* Fixed crash when inserting a Text operator into a scene with certain
  working colour spaces [bug 51635]

* Fixed crash upon importing certain AAFs [bug 51627]

* Fixed issue where drag & drop was possible into Gallery
  [bug 51613]

* Fixed issue where temporary Layer Views could be open during
  playback with Lock Scroll to Cursor Position enabled [bug 51065]

* Fixed issue where thumbnails within Layer View were being rebuilt
  unnecessarily [bug 50888]

* Fixed crash when replacing layers through Layer View that are below
  the render line. It is now impossible to paste below the render line
  through Layer View drag and drop [bug 50817]

* Fixed crash when opening a temporary Layer View for a shot and
  navigating using the Blackboard or Slate [bug 28126]

* The Cursor View clip alarm now uses more accurate thresholds for
  alarms based on the viewing colour space [bug 51357]

* Improved test for running applications when starting Baselight or
  Daylight on Linux [bug 51440]

* Fixed rare crash when changing workspaces [bug 50188]

* Characters '&', '<' and '>' now display correctly when used in a
  Text operator [bug 51592]

* Fixed reporting of disk activity information shown in
  fl-systemmonitor and System Monitor View [bug 51636]

* Fixed issue where Graticule would round a manually entered entry to
  a wrong value [bug 51561]

* Fixed "OfxImageClipPropConnected" property when an OFX plugin has
  optional inputs [bug 51410]

* Fixed failures and crashes when working with old scenes that use the
  legacy "Log", "Linear", "Video" and/or "Video (Full Range)" colour
  spaces [bug 51599]

* Fixed crash in Reference when using tracks/channels, e.g. from an
  EXR Sequence added in an older build [bug 51615]

* Fixed crash when opening Layer View with no available width
  [bug 51688]

* Fixed various issues in Dolby Vision XML output, including animated
  trim under a Dissolve [bug 51476]

* Fixed incorrect Dolby Vision analysis when the analysed stack is not
  at the bottom of the timeline [bug 51582]

* Fixed incorrect timecode rate reported for some media (e.g. 50fps
  timecode reported as 50@25fps) [bug 51370]

* 1x1 Stereo Difference Layout now uses a grey level equivalent to 0.5
  linear in the viewing colour space, to improve usage on PQ displays
  [bug 51654]

* Fixed Shots View columns incorrectly becoming read only [bug 51666]

* Fixed crash when clicking "Current" conform tab after cancel conform
  [bug 51307]

* Fixed an issue where rendering very short QuickTime movies with
  AAC-encoded audio could crash [bug 51649]

* Fixed identification of OpenEXR channels in sequences that have
  handles without the full set of channels [bug 51031]

* Fixed bug when moving keyframes of shapes with custom inner/outer
  curves enabled [bug 51697]

* Fixed crash when switching between scenes with different containers,
  prior to FLUX Manage View being opened [bug 51333]

* Fixed problem when applying a filter for a Media Import Rule that
  caused Shots View to display incorrectly [bug 51715]

* Fixed inability to stop playback using mouse or keyboard when Big
  Metadata View is in use [bug 42433]

* Timecode is now set correctly when rendering IMF MXF movies. The
  timecode rate must match the frame rate of the file or the timecode
  will be ignored [bug 48053]

* Added support for Wacom Intuos Pro M tablet [bug 44170]
와콤 인튜어스 프로 M 타블렛 지원 추가
* Fixed the QuickTime colour space tag written when rendering to sRGB
  [bug 51682]

* Fixed hang when interacting with some OFX plugins [bug 51589]

* Images in PDF Reports are now JPEG compressed, resulting in far
  smaller file sizes for reports containing images and thumbnails
  [bug 51653]
PDF리포트의 이미지가 압축된 JPEG가 가능하게 되어 리포트에 포함되는 썸네일이미지가 작게되었습니다.


* Fixed crash when doing a multipaste from an edl [bug51482]

* Fixed an issue in the index service that caused it to consume memory
  [bug 51692]
인덱스 서비스에서 소모되는 메모리관련 이슈 해결

* Fixed misreporting of 8GB DIMMs in fl-diag "Installed RAM" test
  [bug 51925]

* Fixed an issue that could cause some sequences to appear missing in 
  FLUX Manage [bug 51932]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* AAC-encoded audio may not sync correctly when reading MP4-files
  created by Adobe Premiere. Typically the offset is around a frame
  in either direction [bug 51199]

--------------------------------------------------------------------------
Baselight Release 5.2.11913 (2019-06-13)
베이스라이트 릴리즈5.2.11913 (2019-06-13)

Important Notes
===============

Compatibility With 5.1
5.1 버전과의 호환성 
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.
새로운 이미지 트랜스폼 설정으로 인해서(자세한 내용은 아래 리스트 참조), 5.2에서 새로운 씬을 저장할 경우 5.1 버전에서는 더 이상을 열리지 않습니다. 

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.
호환성을 위해서 베이스라트, 데이라이트, 플럭스 스토어에는 원격으로 지속적인 이미지 디코딩 작업을 하기위해서 5.2 버전 릴리즈가 설치되어 있어야 합니다. 

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.
버전 5.2에서 BLG파일을 추출한 경우 베이스라이트 에이션을 포함한 5.1버전 제품에서는 사용할 수 없습니다. 

Baselight FOUR and EIGHT 베이스라이트 4(Four)/ 8 (Eight)
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.
베이스라이트 5.2 버전이 베이스라이트 4/8 시스템을 지원하는 마지막 버전이 됩니다. 베이스라이트 5.3버전에서는 설치되거나 실행할 수 없습니다. 

Baselight CONFORM 베이스라이트 컨펌 
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]
macOS 10.14 모하비에서 베이스라이트 컨펌 설치와 실행을 지원합니다. MacOS 10.9, 10.10, 10.11 은 더이상 지원하지 않습니다. 

New Features Since Baselight 5.2.11854
베이스라이트 5.2.11854 이후 새로운 기능 
======================================

* Added option to the Metadata section on Render View to allow control
  over the frame rate metadata stored in DPX, OpenEXR and JPEG 2000
  files [bug 51164]
랜더뷰(Render View)에서 메타데이터(Metadata)옵션을 추가하여 DPX, OpenEXR, JPEG 2000 파일에서 프레임레이트의 메타데이터를 제어할 수 있습니다.


Bug Fixes Since Baselight 5.2.11854
===================================

* Fixed loading of control surface button layouts [bug 51338]

* Fixed issue that caused some per-frame metadata from movie files to
  be ignored [bug 51506]

* Improved behaviour when attempting to start Baselight on a system
  using the 418.56 nvidia driver when there is insufficient free GPU
  memory [bug 51396]

* Fixed crash when using ARRIRAW media with other RAW media on a
  system with limited GPU memory [bug 51556]

* Fixed database warning from 'index' service on the first install of 
  Baselight [bug 51651]

* Fixed crash when working with dissolves in stereo scenes [bug 51655]

* Fixed crash in Multi-Paste [bug 51578]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* Image corruption has been seen on RTX 6000 GPUs when using some
  GPU-enabled OFX plugins [bug 51505]
일부 GPU 가능한 OFX 플러그인을 사용할때 RTX6000 GPU에서는 손상된 이미지를 볼 수 있습니다. 


Baselight Release 5.2.11854 (2019-05-30)
베이스라이트 릴리즈 5.2.11854

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.

Baselight FOUR and EIGHT
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

New Features Since Baselight 5.2.11761
======================================

ARRI BLG Support
아리(ARRI) BLG 지원
----------------

* Baselight and Daylight now support the reading of BLG data stored in
  ARRI media. This allows preliminary grades that are created on set
  using Prelight to be applied automatically when the media is
  imported into Daylight or Baselight, without the need for additional
  BLG files.
이제 베이스라이트(Baselight)와 데이라이트(Daylight)에서 아리 미디어에 저장된 BLG 데이터를 읽을 수 있습니다. 미디어를 데이라이트(Daylight)나 베이스라이(Baselight)트에 넣을때 프리라이트(Prelight)로 미리 만들어온 룩(그레이드)를 자동으로 적용할 수 있으며, 추가적인 BLG 파일이 필요하지 않습니다.


  This feature can be enabled in the Sequence Overrides tab of the
  Media Import Rules View. Settings in the Apply Embedded BLG dropdown
  allow embedded BLGs to be always applied, never applied, or for a
  dialog to give the option upon sequence insertion. The rule will be
  applied to BLGs inserted both from FLUX Manage, and during conform
  from an EDL.  Compatible media types are ARRIRAW sequences,
  Quicktime movies and MXFs, shot on ARRI cameras [bug 45943]
이 기능은 미디어 임포트 규칙 보기(Media Import Rules Vie입)의 시퀀스 우선기능(Sequence Overrides)을 가능하게 합니다. 임베디드 BLG 드롭다운 적용에서의 설정은 임베디드 BLG를 항상 적용하거나, 적용하지 않거나, 시퀀스 입력시 옵션을 줄 수 있는 창을 만들수 있습니다. 이 규칙은 플럭스 매니지나 EDL 컨펌시 둘 다에서 BLG 입력을 적용할 수 있습니다. 호환가능한 미디어 유형은 ARRI 카메라들로 촬영된 ARRIRAW 시퀀스, 퀵타임 무비(Mov), MXF입니다. 






Base Grade Bumps 
베이스 그레이드 범프
----------------

* Numeric keypad bumps, previously available for Film Grade, are now
  also available on Base Grade, with the following tweaks and changes:

숫자 키패드 범프, 이전에는 필름그레이드가 가능했는데, 이제는 베이스그레이드 또한 가능하게 되었습니다. 트윅과 변경은 다음과 같습니다. 

  To enable these bumps, set the numeric keypad mode to "Grading",
  under:
  범프를 가능하게 할려면, 숫자키패드 모드를 '그레이딩(Grading)'으로 설정합니다. 
      "Edit" -> "Numeric Keypad Mode".

  Each zone can be bumped through a set of parameters called a Vector
  Bump. Unlike Film Grade, the individual channel bump keys,
각 영역은 벡터 범프라고 불리우는 변수값들의 세트를 통해서 값을 올릴 수 있습니다. 
필름그레이드와는 달리 각 채널별 범프키가 적용됩니다.


      R|G|B Up & Down and C|M|Y Up & Down,
      R|G|B 업 앤 다운, C|M|Y 업 앤 다운,

  have been generalised to a single set of keys:

      Left|Middle|Right Up & Down.

  The behaviour of each bump per channel can be customised. This can
  be done by editing the default Vector Bump values, under:

      "Customise" -> "Default Values and Bumps".

  By default, all groups with Vector Bumps have their bump values set
  to R|G|B, which have been fitted against the Munsel hues. Balance,
  has two additional Vector Bumps, one set to C|M|Y, and the other to
  Exposure|Flare|Saturation.

  The newly availble keys which were reserved for C|M|Y bumps in Film
  Grade, have now been assigned as switches to different groups.
  These keypad mappings can also be customised, under:

      "Customise" -> "Configure Bump Keypad Keys".

  Switching between groups will show a yellow glow around the
  currently selected group as an indicator.

  The overall bump buttons and the keyframe toggle button retain the
  same functionality, based on currently selected group.

  The table below illustrates the new numeric keypad functions for
  Base Grade bumps.
아래의 표처럼 베이스그레이드 범프의 새로운 키패드 기능을 보여줍니다. 

   Keypad (키패드)        | Function (기능)
   ------------------------------------------
   Num Lock, /, * | Bump Left|Middle|Right Up 
   7, 8, 9        | Bump Left|Middle|Right Down
   4, 5, 6        | Bump Keypad Mapping (4, 5, 6)
   1, 2, 3        | Bump Keypad Mapping (1, 2, 3)
   -              | Keyframe Toggle
   +              | Bump Overall Up
   Enter          | Bump Overall Down 
   0, .           | N/A

   Keypad (키패드)        | Function (기능)
   ------------------------------------------
   Num Lock, /, * | 범프 왼쪽|중간|오른쪽 업 
   7, 8, 9        | 범프 왼쪽|중간|오른쪽 다운 
   4, 5, 6        | 범프 키패드 매핑 (4, 5, 6)
   1, 2, 3        | 범프 키패드 매핑 (1, 2, 3)
   -              | 키프레임 토글
   +              | 범프 전체 업
   Enter          | 범프 전체 다운 
   0, .           | N/A (적용없음)





   Groups that can be bumped through the numeric keypad can also be
   used to bump on Blackboard and Slate [bug 39320]

Graticule Generator 
격자 생성기 
-------------------

* Added a graticule generator to the Cursor view. When enabled, it
  starts by drawing a small box overlay at the centre of the
  screen.
커서보기(Cursor view)에 격자생성기를 추가했습니다. 사용하도록 설정하면, 화면 중앙에 작은 박스가 겹쳐서 보이게 됩니다. 


  The two sliders in the Cursor view adjust the width and the
  height of the box. The box is always centred during the
  horizontal and vertical adjustments. It is also possible to set
  the size of the graticule box manually using the corresponding
  edit boxes for each dimension.
커서뷰 격자생성기의 두개의 슬라이더는 박스의 가로와 세로를 조정합니다. 수평과 수직 조정중에 박스는 항상 중앙에 위치하여 있습니다. 격자 X, Y 박스 수치를 직접 넣어서 수동으로 격자 박스의 사이즈를 조절할 수 있습니다. 


  Blackboard controls:
블랙보드에서 조작

  The graticule generator can also be controlled using a Blackboard.
  A new combo button named "Graticule" has been added to the "Cursor"
  button category in Chalk. Simply drag this onto a spare button
  to map it to the desk.
블랙보드에서도 격자생성기를 제어할 수 있습니다. 

  The "Graticule" button works as follows:
  1) Toggle graticule on/off
     A single press toggles the graticule state between enabled and
     disabled.
  2) Show/Hide graticule panel
     If pressed and held, a graticule panel will be displayed allowing
     control of the graticule size using the corresponding encoders.
     When released, the graticule panel will disappear
     [bug 16584]

Miscellaneous (기타)
-------------

* Added the ability to set categories on media to Media Import Rules
  View [bug 49655]

* Added the ability to enable input strip caching with Media Import
  Rules [bug 49323]

* Added the ability to control Stack Colour Space with Media Import
  Rules [bug 49654]

* Added the ability to create new Galleries to the Gallery View
  [bug 34128]

* Made 'Apply x Rules to y Shots' button obey shot selection
  [bug 50231]

* Updated to DNxHD/DNxHR SDK version 2.4.2.31. This includes bug fixes
  [bug 50846]

* Added support for RTX 2080 and RTX 6000 graphics cards, using the
  418.56 driver [bug 51104]
418.56 드라이버를 사용하여, RTX 2080 및 RTX 6000 그래픽 카드 추가 지원

* Added a button to the Media Import Rules View to allow rules to
  be applied either to all shots in a scene or selected shots only
  [bug 51203]

Bug Fixes Since Baselight 5.2.11761
===================================

* Fix a crash while resetting the Zoom/Pan of a display image with
  panorama projection enabled [bug 50662]

* Fix an issue where on changing the Zoom/Pan settings of a scene with
  multiple views at different shots, the image would disappear
  [bug 50592]

* Improved the decode performance of temporally compressed movie files
  when navigating the timeline and creating thumbnais simultaneously
  [bug 49528]

* Fixed an issue where resetting the Audio operator would have no
  effect [bug 50731]

* Hide handles in Curve Grade when "Auto Handles" mode is enabled
  [bug 50694]

* Most types of temporally compressed material in MXF or QuickTime
  containers will now use additonal CPU resources to perform the
  decode. This improves the decode speed of e.g. XAVC Long and XDCAM
  encoded files [bug 50010]

* Allowed access to File Metadata of the form abcd.efg [bug 50536]

* Shots that are part of a dissolve are no longer considered graded
  [bug 49068]

* Fixed issues with Truelight selection in Media Import Rules View
  [bug 50230]

* Fixed crash in Gallery when closing a tab whereby another tab
  contains the same scene [bug 50583]

* Fixed an issue that caused an invalid aspect ratio to be set in
  XDCAM essence when written to Sony MXF [bug 50836]
Sony MXF에 기록할때, XDCAM 에센스에 잘못된 화면비를 설정하는 문제 해결

* Retimes are removed from the input strip when updating an AAF with
  Baselight grades [bug 50842]

* When importing .edl files we now accept a ':' following ASC_SOP and
  ASC_SAT specifiers [bug 50792]

* Fixed an issue where DNG files from Panasonic V35LT cameras were not
  correctly identified as Panasonic CinemaDNG [bug 50914]

* Fixed a crash when deleting a custom column that is being used for
  filtering [bug 50981]

* Fixed issue whereby a colour pick for a colour well that is not
  currently displayed could lead to a hang [bug 50775]

* Fixed issue with painting though a matte with mulitple paint layers
  [bug 50999]

* Fixed issue where some CDL groups would show incorrect text on
  Blackboard and Slate [bug 50628]

* Fixed issue whereby updating an AAF with Baselight grades would
  sometimes fail [bug 36213]

* The "Maximum hotspot grab range" preference setting is now in the
  "Display" tab. The setting is now aware of the display monitor
  resolution, in order to make it easier to work with control points
  with high resolution displays [bug 48809]

* Fixed an issue where Media Import Rules were not being correctly
  applied to both inputs to a dissolve [bug 50456]

* Removed the limit on the number of search directories in the EDL 
  Import View and in bl-conform [bug 50968]

* Fixed issue preventing multipaste from .ale files for which there
  are multiple possible timecode formats [bug 50515]

* Fixed issue with variable retimes from Premiere XMLs in mixed
  framerate projects [bug 50863]

* Changed the hotspot for scrolling through shots whilst performing
  a drag to be consistent with the size of the view [bug 50758]

* Fixed issue with paint layer source mode not being passed to 
  strips created by cutting stacks or copy and paste actions
  [bug 51115]

* Improved speed of Shots View filtering [bug 50250]

* Fixed Text issue where many keyframes would be dropped if keyframe
  striping was disabled and the transform was edited during playback
  [bug 51131]

* Fixed an issue that could cause audio decode from movie files using
  frame-wrapped audio to be slow. This affected e.g. XAVC encoded
  MXF-files [bug 50528]

* Fixed issue where the grade would 'jump' when the trackball was 
  touched in Base Grade and Video Grade, for certain trackball
  positions [bug 50872]

* Fixed crash when recalling from scratch pad to group grade selection
  [bug 50366]

* Fixed an issue where MPEG-4 encoded QuickTime and MP4 movie files
  could decode frames in the wrong order. This fix can also slightly
  alter the look of this media in sequence strips inserted or
  refreshed after this fix [bug 51294]

* Fixed an issue where Area Tracker and Area Tracker Perspective
  wouldn't track in low exposure contexts or with slight occlusions
  [bug 50807]

* Fixed clamping applied in Shader operators which limited pixel
  values to +/- 10,000 [bug 51114]

* Fix a crash when when conforming with some audio files [bug 51293]

* Fixed clip alarm not indicating too-bright colours for some viewing
  colour spaces [bug 51133]

* Improved handling of non-ASCII text pasted between Baselight and
  other Linux applications [bug 50858]

* When writing OpenEXR files, "Tape" metadata is now stored as
  "reelName" to improve compatibility with other software [bug 37445]

* Fixed a matte insertion issue. It was not possible to insert a matte
  on the second channel when a matte was selected [bug 51195]

* Fixed a crash in Media Import Rules View when clicking on "Apply
  Rules to Shots" button [bug 50643]

* Fixed incorrect "no conversion" message on Colour Space Journey View
  when the Sequence has a Video LUT and/or a Y'CbCr matrix [bug 50740]

* Adaptec diagnostic now reports controller firmware version
  [bug 50770]

* Changed behaviour when applying Media Import Rules during EDL
  import and FLUX Manage insert, to consider all new shots
  [bug 51203]

* Fixed bug which could cause some FCP 7 XMLs generated via a
  "Modify XML" workflow to not load back into Baselight [bug 50903]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Sony RAW media added to scenes in Baselight 4.4m1.9217 or earlier
  may now fail to decode at half resolution. A workaround is to enable
  Max Quality decoding on the cursor and/or Sequence [bug 46625]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* Image corruption has been seen on RTX 6000 GPUs when using some
  GPU-enabled OFX plugins [bug 51505]
일부 GPU 가능한 OFX 플러그인 사용시 RTX 6000 GPU 사용지 이미지 오류 문제  


Baselight Release 5.2.11761 (2019-05-07)
베이스라이트 릴리즈 5.2.11761 버전 

Important Notes
===============

Compatibility With 5.1
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.
새로운 이미지 트랜스폼 설정으로 인해서(자세한 내용은 아래 리스트 참조), 5.2에서 새로운 씬을 저장할 경우 5.1 버전에서는 더 이상을 열리지 않습니다. 

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.
호환성을 위해서 베이스라트, 데이라이트, 플럭스 스토어에는 원격으로 지속적인 이미지 디코딩 작업을 하기위해서 5.2 버전 릴리즈가 설치되어 있어야 합니다. 

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions.
버전 5.2에서 BLG파일을 추출한 경우 베이스라이트 에이션을 포함한 5.1버전 제품에서는 사용할 수 없습니다. 

Baselight FOUR and EIGHT 베이스라이트 4(Four)/ 8 (Eight)
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.
베이스라이트 5.2 버전이 베이스라이트 4/8 시스템을 지원하는 마지막 버전이 됩니다. 베이스라이트 5.3버전에서는 설치되거나 실행할 수 없습니다. 

DVI-to-SDI Convertors
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners used to perform that function are supported. From
Baselight 5.3, Generation V systems will have to either be upgraded to
the Baselight Ultra High Definition option (see data sheet) which
includes an AJA Kona 4 PCIe card, or revert to GPU DVI output. Earlier
generation systems will be constrained to GPU DVI output only.
베이스라이트5.2 버전이 DVI-to-SDI 컨버터나 컴바이너를 지원하는 마지막 버전이 될 것입니다. 베이스라이트 5.3 부터는 5세대 시스템의 경우 AJA Kona 4 PCIe 카드가 포함된 베이스라이트 UHD 옵션으로 업그레이드 하거나 GPU DVI 출력으로 변환해야 합니다. 이전 세대 시스템의 경우 GPU DVI 출력만 가능합니다. 

Baselight CONFORM 베이스라이트 컨펌 
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]
macOS 10.14 모하비에서 베이스라이트 컨펌 설치와 실행을 지원합니다. MacOS 10.9, 10.10, 10.11 은 더이상 지원하지 않습니다. 

New Features Since Baselight 5.2.11675
======================================

* You can now use the individual start/end timecodes from "Source TC"
  and "Record TC" variables in expressions by suffixing the variable
  name with '[0]' and '[1]' array index operators.
 [0]과[1] 인덱스 오퍼레이터를 소스 타임코드(Source TC)나 레코드 타임코드(Record TC) 변수로 부터 각각의 시작/끝 타임코드를 사용할 수 있습니다. 
 
  For example, you can use '%{Source TC[0]}' to get the start source
  timecode of a shot in an expression [bug 51162]
소스 타임코드와 레코딩 타임코드 변수표현식안에 [0],[1]의 인덱스 연산자를 붙이면 개별적인 시작/종료 타임코드를 사용할 수 있습니다. 
예를 들면,  %{Source TC[0]} 이면 촬영소스의 시작 타임코드를 가져올 수 있습니다. 




Bug Fixes Since Baselight 5.2.11675
===================================

* Fixed occasional crash in Text operator when no strip is selected
  during playback [bug 51116]

* Fixed crash when dynamically generated burnin text is empty
  [bug 50603]

* Fixed bug where using %{Source TC} in expressions would result
  in an empty string [bug 51162]

* Fixed failure to start application on a system using an older nvidia
  driver [bug 51161]

* Added a missing MXF tag that prevented some flavours of AVC-Intra
  from being decoded [bug 51196]

* Fixed crash with protected strips inside a matte channel [bug 50412]

* Fixed failure to use Dolby Vision Software CMU when rendering more
  than 500 frames [bug 51269]

* Fixed excessive memory use when rapidly opening & closing scenes
  [bug 51288]
  빠르게 씬을 열고 닫을때 과도한 메모리 사용을 수정함. 

* Fixed issues opening Chalk Layout files created by earlier versions
  of Chalk [bug 51125]

Known Issues
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]

* On some systems, an interaction between third-party SDKs can cause
  Baselight rendering to hang when decoding Sony RAW media, if it has
  previously decoded ARRIRAW media in the same session (either in the
  timeline or in a queued render). If this happens you will need to
  kill and restart Baselight [bug 49010]

* There can be a pause of several seconds the first time a Blackmagic
  RAW frame is decoded. This is due to issues in the Blackmagic RAW
  SDK, which we hope will be addressed in a future release [bug 49057]

--------------------------------------------------------------------------

Baselight Release 5.2.11675 (2019-04-09)
베이스라이트 릴리즈 5.2.11675 버전 

Important Notes 중요 내용 
===============

Compatibility With 5.1
5.1 버전과의 호환성 
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.
새로운 이미지 트랜스폼 설정으로 인해서(자세한 내용은 아래 리스트 참조), 5.2에서 새로운 씬을 저장할 경우 5.1 버전에서는 더 이상을 열리지 않습니다. 

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.
호환성을 위해서 베이스라트, 데이라이트, 플럭스 스토어에는 원격으로 지속적인 이미지 디코딩 작업을 하기위해서 5.2 버전 릴리즈가 설치되어 있어야 합니다. 

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions. 
버전 5.2에서 BLG파일을 추출한 경우 베이스라이트 에이션을 포함한 5.1버전 제품에서는 사용할 수 없습니다. 

Baselight FOUR and EIGHT 베이스라이트 4(Four)/ 8 (Eight)
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.
베이스라이트 5.2 버전이 베이스라이트 4/8 시스템을 지원하는 마지막 버전이 됩니다. 베이스라이트 5.3버전에서는 설치되거나 실행할 수 없습니다. 

DVI-to-SDI Convertors DVI-to-SDI 컨버터
---------------------

Baselight 5.2 is also the last version for which DVI-to-SDI Convertors
or Combiners used to perform that function are supported. From
Baselight 5.3, Generation V systems will have to either be upgraded to
the Baselight Ultra High Definition option (see data sheet) which
includes an AJA Kona 4 PCIe card, or revert to GPU DVI output. Earlier
generation systems will be constrained to GPU DVI output only.

베이스라이트5.2 버전이 DVI-to-SDI 컨버터나 컴바이너를 지원하는 마지막 버전이 될 것입니다. 베이스라이트 5.3 부터는 5세대 시스템의 경우 AJA Kona 4 PCIe 카드가 포함된 베이스라이트 UHD 옵션으로 업그레이드 하거나 GPU DVI 출력으로 변환해야 합니다. 이전 세대 시스템의 경우 GPU DVI 출력만 가능합니다. 

Baselight CONFORM 베이스라이트 컨펌 
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]
macOS 10.14 모하비에서 베이스라이트 컨펌 설치와 실행을 지원합니다. MacOS 10.9, 10.10, 10.11 은 더이상 지원하지 않습니다. 

New Features Since Baselight 5.2.11644 
베이스라이트 5.2.11644 이후 새로운 기능 
======================================

* Added support for reading Apple ProRes RAW camera media [bug 47832]
애플 ProRes RAW 카메라 미디어 읽기 지원 

* Added support for reading Blackmagic RAW camera media. Note that
  this functionality is not available on Linux systems using older
  NVIDIA drivers (versions 290, 304 or 319) [bug 49057]
블랙매직 RAW 카메라 미디어 읽기 지원. 엔비디아 그래픽카드 버전 (290, 304, 319) 의 레가시 버전을 사용하는 리눅스 시스템의 경우 지원하지 않습니다. 

Bug Fixes Since Baselight 5.2.11644 
베이스라이트 5.2.11644 이후 버그개선  
===================================

* Fixed issues with Truelight selection in Truelight strip [bug 50195]

* Fixed colour space conversion applied to OFX input images used in
  the UI [bug 50847]

* Fixed a potential crash when pressing the filter button on a media
  row in EDL Import View [bug 51067]

* Fixed issue that caused Consolidate not to trim the head of movies
  [bug 51063]

* Fixed behaviour of the Sequence Input Colour Space menu during
  playback, and when Grouped Grading is enabled while Shots View is
  open [bug 50788]

* Fixed "Scene Timecode" not appearing among the conform settings
  in the EDL Import View [bug 51102]

Known Issues 알려진 이슈들 
============

* When running on a Baselight TWO/FOUR/EIGHT system whose UI host has
  a NVS 450 graphics card, many of the new operators in Baselight 5
  currently cause thumbnail errors in Cuts View and elsewhere. This
  issue will be addressed in a future Baselight 5 release. Please
  contact FilmLight Support if you wish to discuss upgrading the
  graphics card in your UI host [bug 40279]

* Saturated areas in Photo RAW files can acquire a colour tint when
  adjusting the exposure slider in the Photo RAW Parameters operator
  while blending highlights [bug 44769]

* Baselight and Daylight are known to hang on macOS 10.13 High Sierra
  when run on older (2012 and mid-2014) MacBook Pro machines with
  nvidia graphics [bug 44949, bug 48343]

* Canon RAW media added to scenes in Baselight 5.1.10836 or earlier
  using the tone curve setting "Canon Log" may now fail to decode with
  an error message stating "Invalid function parameter". Changing the
  tone curve will allow images to decode, but will change their look
  [bug 50371]

* On first installation on macOS Mojave (10.14) setup of the vol
  service will fail due to macOS security enhancements. In order to
  work around this issue it is necessary to manually run the command
  'sudo fl-service setup vol' and authorise Terminal to administer the
  computer [bug 50732]
MacOS 모하비(10.14)에서 첫번째 설치후 볼륨서비스는 macOS의 보안강화로 인해서 실패됩니다. 이러한 문제를 해결하기 위해서 'sudo fl-service setup vol'명령어를 수동으로 실행할 필요가 있을 수 있으며, 이때 관리자 인증받은 터미널에서 진행해야 합니다.

* On some systems, an interaction between third-party SDKs can cause
  Baselight rendering to hang when decoding Sony RAW media, if it has
  previously decoded ARRIRAW media in the same session (either in the
  timeline or in a queued render). If this happens you will need to
  kill and restart Baselight [bug 49010]
일부 시스템에서, 써드파티 SDK간의 상호작용으로 인해서 베이스라이트 랜더링이 응답없는 현상이 발생할 수 있스니다. 소니 RAW 미디어를 디코팅할 때 만일 이전의 ARRIRAW 미디어 디코딩이 같은 세션일 있을 경우(타임라인 또는 같은 렌더큐 상황). 이러할 경우 베이스라이트를 강제종료후 다시 시작해야 합니다.  

* There can be a pause of several seconds the first time a Blackmagic
  RAW frame is decoded. This is due to issues in the Blackmagic RAW
  SDK, which we hope will be addressed in a future release [bug 49057]
블랙매직 RAW 프레임을 처음 디코딩할때 몇초간 멈출 수 있습니다. 이는 블랙매직 RAW SDK로 인해서 이며, 앞으로 나올 SDK에서 개선되길 바라고 있습니다.

--------------------------------------------------------------------------

Baselight Release 5.2.11644 (2019-04-02)
베이스라이트 릴리즈 5.2.11644버전

New Features Since Baselight 5.2.11581 베이스라이트 5.2.11581 이후 새로운 기능
======================================

* Added the capability to cycle through groups that contain the 
  current shot. With a keyboard, Alt + '+' and Alt + '-' will cycle
  forwards and backwards (resp.) through the groups that contain the
  shot. The same can be achieved on a Blackboard with the 'Cycle Fwd'
  and 'Cycle Back' buttons in the Group menu [bug 50611]
현재 샷이 포함된 그룹내에서 순환할 수 있는 기능이 추가되었습니다. 키보드 사용시, Alt +, Alt -를 통해서 샷이 포함된 그룹내에서 앞으로 뒤로 순환이동할 수 있습니다. 블랙보드를 사용시에 그룹메뉴에서 Cycle Fwd와 Cycle Back 버튼을 사용하시면 동일한 결과를 얻을 수 있습니다. 

Multi Directory Conform 멀티 디렉토리 컨펌 
-----------------------

* The EDL Import view has been updated to support up to 7 different
  media directories. The media conform settings (source directories,
  sub directories, filenames, and included file types) have moved
  above the conform setting list into a specific media section. For
  each media directory, a filtering dialog can be used (by pressing
  the filter button) to test location and filename patterns or file
  types and visualize the scanning result in a thumbnail view. Once
  the result is satisfactory, it can be applied to the selected media
  directory [bug 29103]
EDL 임포트 뷰는 최대 7개의 다른 미디어 디렉토리를 지원하도록 업데이트 되었습니다. 미디어 컨펌 설정들(소스 디렉토리, 서브 디렉토디, 파일이름, 파일타입)은 컨펌설정 리스트 위의 미디어소스 섹션으로 이동되었습니다. 각각의 미디어 디렉토리에 필터버튼을 누르면 필터창이 나오며 디렉토리, 파일이름패턴, 파일타입으로 스캔하여 적용할수 있는 썸네일뷰를 사용할수 있습니다. 스캔한 결과가 만족스러우면 해당 미디어 디렉토리에 적용할 수 있습니다. 



Bug Fixes Since Baselight 5.2.11581 베이스라이트 5.2.11581 이후 버그개선
===================================

* Boost Contrast missing controls mapped to Blackboard 2 [bug 48067]

* Boost Colour works with LUT export [bug 50523]

* Fixed error in Denoise pick that could scramble the picked
  region for small non-square picks with speedfx. Does not affect
  existing Denoise, just new picks [bug 50511]

* Updated the Sony XAVC Encoder to version 1.1.10. This fixes a crash
  when multiple encoders are intialised with different format
  types. It also improves picture quality for XAVC Long HDR HLG
  [bug 49996] 
소니 XAVC 엔코더 버전 1.1.10 지원. 

* In FCP7 XML import, reversed clips with a different framerate to the
  timeline and a speed change have the correct offset [bug 49578]

* In AAF import, the ordering of Avid FrameFlex and a flip or flop on
  a clip has been corrected [bug 49653]

* Fixed update of Comments field in Shots View in response to
  "Toggle Strip Category" [bug 49242]

* Added the Input DRT options to the DBS apply with "Layer 0 Ops"
  [bug 50134]

* Fixed issue with copy and pasting Grid Warps of different dimensions
  [bug 50482]

* Fixed floating licence issues in Baselight CONFORM [bug 48160]

* Slate diagnostic now reports firmware version [bug 39596]

* Fix potential division by zero bug in Relight3D UI [bug 50498]

* OFX and Shader strips are now grouped under "Plugins" on the Insert
  menu [bug 50549]
인서트(Insert)메뉴에 OFX와 쉐이더(Shader) 스트립은 플러그인 아래에 함께 있습니다. 
인서트 > 플러그인 (새로 생김) > 쉐이더 (단축키 있음. Shift+Y)

* Changed the default tone curve used for decoding Canon CRM files
  from 'Canon Log' to 'Canon Log 3'. This avoids a decode problem when
  not using the automatic input colour space [bug 50371]
캐논로그 에서 캐논로그3로 캐논CRM 파일의 디코딩시 기본 톤커브값이 변경되었습니다. 이는 자동 입력 컬러스페이스를 사용하지 않았을 경우 디코딩 문제를 피하기 위함입니다. 

* Fixed behaviour of Link Files option in Consolidate when using
  multi-part movie files [bug 50565]

* Fixed crash in colour space parser when the current directory has
  been deleted [bug 50520]

* Added support for OFX "OfxParamPropGroupOpen" [bug 50574]

* Fixed vertical spacing of empty text lines [bug 50483]

* NVMe storage diagnostics now accepts 1 controller for Generation VI
  Baselight ONE systems [bug 50440]

* Fixed bug which could cause a crash when pressing the Gridwarp
  button "Hide Overlays on Edit" during playback [bug 50459]

* Fixed issue with Paste where the tracker strip was being removed
  in replace mode even when Paste Protect Mattes was on [bug 50570]

* Fixed an issue that could cause slow performance of temporally
  compressed MXFs around frame 400. This affected e.g. XAVC Long
  encoded files [bug 50606]

* In CDL grade, bump amount for contrast, saturation and power can
  now be set [bug 33384]

* Added fix message for users when Adaptec RAID test in fl-diag warns,
  "Adaptec RAID manager is running..." [bug 46136]

* Audio stem searches now also find files without a digit at the end
  of the filename base stem [bug 50653]

* Rendering with with "Analyse MaxCLL/MaxFALL" will now fail when
  an inappropriate Render Colour Space is chosen [bug 50491]
부적절한 랜더 컬러스페이스를 선택한 경우 MaxCLL/MaxFALL분석 랜더가 실패합니다. 

* Fixed crash when exporting an ALE, caused by missing sound timecode
  [bug 50581]

* Fixed failure to copy to/from cloud media volumes that are exported
  by systems not in cloud.cfg and/or local DNS [bug 50622]

* OFX plugins are now correctly "unloaded" when the application is
  quit [bug 50547]

* Fixed "internal error" message when accessing movie files using an
  account with an extremely long list of numeric supplemental group
  ids [bug 47494]

* Improved speed of presenting initial file scans in FLUX Manage View
  [bug 38500]

* Fixed loss of Dolby Vision Target Display information from Dolby
  Vision Trim strips when loading a Baselight 5.1 scene [bug 50644]

* A scene can now be changed between "Software CMU (v2.9)" and
  "Hardware CMU (v2.9)" without its Dolby Vision strips being deleted
  [bug 50638]

* Fixed an issue where inverting projection in Panorama could while
  playing could cause a crash [bug 50458]

* Enable scene detect to run on multiple selected shots or on the 
  currently selected shot [bug 35112]

* Ensure "Group Grade All Keyframes" is temporarily disabled while
  adjusting Stereo Grade parameters [bug 50641]

* Improved stability when using OFX plugins on macOS [bug 50726]

* Fixed crash in the Text operator when renaming a colour space upon
  scene load [bug 50752]

* Fixed crash loading galleries [bug 50859]

* Fixed wrong source and destination selection during a copy and paste
  operation (with DBS and the blackboard/Slate) [bug 50616]

* Fixed a crash that could occur when copying files by drag and drop 
  actions on indexed volumes [bug 50637]

* Fixed an issue that could cause both audio and video decode of
  temporally compressed MXFs to fail, typically with a message stating
  'Bad index at position' [bug 50920]

--------------------------------------------------------------------------

Baselight Release 5.2.11581 (2019-03-19)
베이스라이트 릴리즈 5.2.11581버전

Bug Fixes Since Baselight 5.2.11483
===================================

* Fixed failure of Dolby Vision Analysis in some stacks containing a
  Blend operator [bug 50274]

* Fixed issue causing single layer selections to remain when moving
  cursor to a new stack [bug 50757]

* Fixed incorrect Dolby Vision analysis when using Dual Colour Spaces
  Layout with Viewing Space 2 selected [bug 50778]

* Fixed an issue with file browsing and conforming with some media 
  types that could cause the operation to fail [bug 50478]

--------------------------------------------------------------------------

Baselight Release 5.2.11483 (2019-02-27)
베이스라이트 릴리즈 5.2.11483버전

New Features Since Baselight 5.2.11383
======================================

Baselight CONFORM
-----------------

Installing and running on macOS 10.14 Mojave is now supported. macOS
10.9, 10.10 or 10.11 are no longer supported [bug 50131]

Three-Point Insertion 쓰리포인트 인서트
---------------------

* Insertion of a single sequence from FLUX Manage View can now use
  "three-point insertion", taking account of In and Out marks and gaps
  on the timeline to control where the strip is placed on the
  timeline. 
FLUX Manage View에서 단일 시퀀스를 삽입하면 타임 라인의 시작(인점) 및 종료(아웃점) 표시와 간격(갭)을 고려하여 타임 라인에 스트립이 배치되는 위치를 제어하는 "3점 삽입(3point insertion)"을 사용할 수 있습니다.

  - If there are In and Out marks on the timeline, then the
    sequence is inserted between the marks.
  - If there is an In mark on the timeline, then the sequence is
    inserted starting at the mark.
  - If there is an Out mark on the timeline, then the sequence is
    inserted to the left of the mark.
  - If there are no In/Out marks on the timeline but the cursor is in
    a gap between two stacks, then the sequence is inserted into the
    gap.
  - Otherwise the sequence is inserted at the cursor's location.
- 타임라인에 인/아웃 마크가 있을 경우, 마크사이로 시퀀스가 삽입됩니다. 
- 타임라인에 인 마크만 있을 경우, 마크에서부터 시퀀스가 삽입되기 시작합니다. 
- 타임라인에 아웃 마크만 있을 경우, 마크의 왼쪽부터 시퀀스가 삽입되기 시작합니다. 
- 타임라인에 인/아웃 마크가 없지만 두 스택사이의 간격사이에 커서가 있을 경우 시퀀스가 간격사이에 삽입됩니다. 
- 그렇지 않을 경우, 시퀀스는 커서의 위치에 삽입됩니다. 

  The FLUX Manage View Mark In/Out controls continue to determine the
  length of the sequence which is inserted.
플럭스 매니지 뷰의 마크 인/아웃 컨트롤은 삽입된 시퀀스의 길이를 계속적으로 결정하게 됩니다. 

  Four-point insertion (where there are In and Out marks or a gap, and
  also the sequence has been marked both In and Out) is not supported. 
  4점 삽입(인/아웃마크 또는 간격, 시퀀스의 인/아웃)은 지원하지 않습니다. 

  This behaviour applies when the Insert button is pressed or a
  sequence thumbnail is double-clicked.
이러한 동작은 삽입버튼을 누르거나 시퀀스 썸네일을 두번 클릭할 경우 적용됩니다. 

  The old behaviour (where insertion always occurs at the cursor) can
  be restored using the Options button above the Insert button on FLUX
  Manage View.

  In and Out marks can be added to the timeline from the Marks menu,
  the keyboard shift+[ and shift+], Blackboard 1 Mark In/Out buttons,
  or Blackboard 2 and Slate ctrl+Prev/Next Frame buttons [bug 48421]

  New commands to navigate to the In/Out marks on the timeline have
  been added to the Marks menu [bug 50322]

* Similarly, strip insertion from the Insert menu now also takes
  account of In and Out marks and gaps on the timeline.

  - If there is a selected strip, then the strip is inserted below (or
    above) it, as before.
  - If there are In or Out marks on the timeline, then the strip is
    inserted at or between the mark(s).
  - If the cursor is in a gap between two stacks, then the strip is
    inserted into the gap.
  - Otherwise the strip is inserted at the cursor, with a default
    length of 100 frames.

  An option on the Insert menu controls whether insertion at marks or
  gaps happens regardless of whether a strip is selected [bug 48421]

Miscellaneous 기타 
-------------

* The EDL Import window now gives the option to apply a set of
  categories to all imported sequences [bug 46449]

* An OpenEXR sequence will now default to using a track named 'rgba'
  rather than the first track in the file [bug 50024]

* An OpenEXR sequence whose first frame has different tracks or
  channels from the remaining frames is now treated as if every frame
  has the tracks and channels of the remaining frames [bug 45964]

* When not in "Ripple" or "Rolling" edit modes, Paste Strips at Cursor
  now bounces existing strips overlapping the paste location out of
  the way, rather than failing [bug 50014]

* There is now an option in Multi Paste to copy the source layer 0
  strip categories. These can be appended to or replace the
  destination layer 0 categories. Also categories can be excluded from
  the copy [bug 28968, bug 50147]

* To allow more flexibility in how the scene's start timecode is
  set/used in EDL Import, the following changes have been made:
   - The "Overwrite Start Timecode" EDL Import setting has now been
     renamed "Scene Timecode".
   - The "No" option has been renamed "Leave Unchanged".
   - The "Yes" option has been renamed "Overwrite Start Timecode".
   - The "Position Events Using Existing Scene Timecode" has been
     added. When this option is selected, rather than simply placing
     the new events at the current cursor location, they will be
     placed in the scene using their record timecode and The existing
     timecode of the scene. This is useful for conforming EDLs
     representing a partial update of an existing edit - e.g an EDL
     representing updated VFX shots [bug 49886]

* Client View can now be set to start automatically when Baselight
  starts [bug 50129]

* In 1x1 stereo display mode, when a shape strip is selected the 
  overlays for both that shape strip & the matching other eye's shape
  strip are drawn in the appropriate output. In this mode interactions
  with the overlays (eg. dragging control points) are disabled on the
  image itself, however shape positions can still be adjusted from the
  desk/trackballs [bug 46385]

* Added control modifier support to middle trackball when moving
  shapes horizontally in a stereo scene (with grouped grading
  enabled). When activated, rather than moving the other eye's shape
  in the opposite direction (adjusting convergence), both eye's shapes
  will move in the same direction (adjusting position) [bug 46385]

* Media Import Rules now support Metadata mapping of arbitrary text.
  An additional submenu "Text" has been added to the "From" column of
  the Media Import Rules Metadata Mapping tab. This menu allows text
  to be created, edited and deleted for use in rules. Substitution
  codes supported in these text entries are as follows:
미디어 임포트 룰에서 임의의 텍스트의 메타데이터 매핑을 지원합니다. 추가적은 서브메뉴"TEXT"에서는 미디어 임포트 룰의 메타데이터 매핑 툴의 "From"이라는 컬럼이 추가되었습니다. 이 메뉴는 룰안에서 텍스트를 생성하거나 편집 또는 삭제할 수 있습니다. 이 텍스트항목에서 지원되는 대체코드는 다음과 같습니다. 

  %L Clip Name 클립네임
  %O Comment 코멘트
  %E Event Number 이벤트 넘버
  %D Sequence Filename 시퀀스 파일이름
  %N Tape Name 테잎 이름
  %Z Insert Name - name as if inserted from FLUXmanage. 만일 플럭스매니지에서 인스트한 경우 이름

  Using these options in conjunction with setting the "To" column to
  "Name" allows the name of the input strip to be controlled
  [bug 49675, bug 49656]

* Creating (and deleting) shapes in an existing shape strip now obeys 
  grouped grading in a stereo scene (creating/deleting matching shapes
  in the other eye) [bug 50300]

* A click in the timecode display area of the timeline now moves the
  current cursor to the click position [bug 33142]

* Added new grouped grading option to the "Edit" menu: "Grouped Grade
  All Keyframes". This controls how the currently selected operator
  behaves with grouped grading enabled when that operator contains
  keyframes.

  If enabled (together with grouped grading), when a change is made to
  one of the operator's keyframes, the same relative change is applied
  to all the other keyframes. If disabled, only the keyframe at the
  current time will be modified.

  In a stereo scene, if the current operator has a matching operator
  for the other eye (and "Grouped Grade Both Eyes" is enabled), then
  this also applies to keyframes on the other eye's operator.

  Note: The new "Grouped Grade All Keyframes" option replaces the
  shape specific "Apply Transform Modifications To All Keyframes"
  option [bug 50406]

* Added "Group Grade Both Eyes" to Chalk actions under the stereo 
  section. This will toggle the group grade both eyes setting
  [bug 50387]

* When choosing an EXR channel or track in the Reference operator or
  Layer setup dialog, a thumbnail of each channel/track is now shown
  [bug 50257]

* Added ARRI Look Library Scene Looks to FilmLight's website, as an 
  additional download package [bug 46007]

* Added "Apple: ~2.2 Gamma / P3 D65" colour space to be used 
  with newer Apple displays [bug 49961]

* Added -left, -right and -both flags to bl-shots to select which 
  stereo track(s) to include in the XML output generated when the
  -xml option is selected [bug 50270]

* Updated the Sony RAW SDK to version 3.2.0, which adds support for
  reading X-OCN XT as well as 6K 16:9 and 6K 2.39:1 bitstreams
  [bug 50232]

* Added v5 User Guide [bug 50375]
버전5 유저가이드 추가

Bug Fixes Since Baselight 5.2.11383 
===================================

* Fixed FLUX Manage thumbnail failures for some multi-channel OpenEXR
  sequences [bug 50024]

* In shape strips, the "Lock Y Positions" toggle setting is now obeyed
  when dragging/moving control points (as well as transform boxes)
  [bug 49956]

* Fixed bug in "Overwrite Start Timecode" in EDL Import view where it
  didn't offset the start timecode properly if the conform wasn't done
  at the beginning of the timeline [bug 49866]

* Fixed failure when grabbing stacks using multi-channel and/or
  multi-view OpenEXR files to a gallery [bug 50076]

* Fixed filtering UI being shown in 1x1 Shots Layout [bug 50078]

* Fixed Shots View filtering not saving or updating correctly
  [bug 50103]

* Fixed multi-pasting metadata to include both eyes in stereo scenes
  [bug 50199]

* Fixed issues with overlays sometimes drawing incorrectly when
  playing across strips of different types [bug 46385]

* Fixed bug which could result in the "Grouped Grade Both Eyes" menu
  option from being incorrectly (automatically) disabled after using
  the Stereo Grade operator [bug 50323]

* Fixed bug where transform overlays were being incorrectly displayed 
  during playback when disabled [bug 50337]

* Ensure layer strips with no grade changes that have explicit caching
  enabled are actually cached [bug 50354]

* Fixed stereo bug where the matte mode (Overlay/Inverse Overlay)
  would sometimes only be applied to the current eye, rather than
  both eyes [bug 50262]

* Fixed inverted custom curve matte un-inverting when opacity is
  set to zero [bug 50185]

* Fixed changing the colour of a stereo-split strip [bug 50383]

* Fixed stereo bug where creating a new tracker from a stereo split 
  strip would not insert the tracker inside the existing split
  tracker strip, where it should [bug 50423]

* Fixed an issue where 3X10 DPX files written by Scanity software
  could be misinterpreted as 1X10 [bug 49926]

* Fixed reading of 10-bit DPX files that uses packing value 2 (type B)
  [bug 50018]

* AES3 emphasis metadata is now written correctly when rendering to
  Sony MXF. This fixes an issue where these files could be flagged as
  having metadata errors in the Sony format verification tools
  [bug 49957]

* Fixed an issue where the audio waveform view did not work with audio
  from encrypted DCPs where the KDM was set in the DCP Params strip
  [bug 49763]

* Fixed an issue decoding some large RAW files on specific
  hardware configurations [bug 50023]

* Fixed an issue where Baselight would fail to start up and report
  'No comms from host' [bug 34409]

* Fixed an issue where timecodes with rate larger than 30fps in MXF
  containers would always be interpreted as double-frame
  timecode. This also solves a problem where these timecodes could be
  flagged as drop-frame when they were not [bug 50081]

* Fixed an issue where inserting media from local volumes gave the
  option to change the scene container [bug 42204]

* Fixed an issue where the incorrect coding equations label could be
  written to IMF MXFs, along with various minor improvements:
  - Avaliable colour primaries and transfer function tags are now
    written, even when none of the IMF-specified colorimetry systems
    are used.
  - Coding equations tags are no longer written when rendering RGB
    essence.
  - The dialog available to assist configuring the render panel to
    produce IMF-spec colorimetry systems now also shows an option for
    the Y'CbCr matrix to use [bug 49337]

* Fixed issue where source file was deleted if source and destination
  were the same while copying in FLUX Manage View via symlinks
  [bug 49795]

* Improved UI for Stereo Geometry Fix [bug 49379]

* Reduced the number of warnings about Grouped Grading when making
  adjustments to Stereo Geometry Fix [bug 49378]

* Fixed failure to create a per-job gallery when the opened scene uses
  a basic Working Format [bug 50002]

* Improved warning on Render View when using Full to Legal Video LUT
  with a legacy ProRes deliverable [bug 49919]

* Fixed crash when attempting to copy an unreadable folder by dropping
  it on a folder in FLUX Manage [bug 49756]

* Fixed crash when using Source Alpha on an OFX operator [bug 49781]

* Fixed crash in Smart Paste when pasting input strip and there is
  copy protection on [bug 49776]

* Fixed an issue whereby certain Slate buttons were resetting strips
  unexpectedly [bug 49702]

* File and Folder patterns now supported for index and non-index 
  use [bug 49846]

* Fixed an issue with printing the SDI temperature to the terminal 
  [bug 49147]

* Fixed issue with Relight3D overlay interfearing with certain
  stereo display setups [bug 49829]

* Fixed interaction problem in Relight3D with material that has
  camera matrices stored in a certain format [bug 49666]

* Improved interaction with Light Intensity and Light Target Distance
  slider in Relight3D [bug 49844]

* Improved slate/blackboard button interaction to indicate what
  current interaction mode is active for Relight3D [bug 49840]

* Improved desk encoder precision for Target Distance, Cone and
  Hot spot angle for Relight3D [bug 49833]

* Fixed an issue that could cause the File System Index to fail to 
  update metadata for sequences [bug 50118]

* Consolidate now accounts for temporal and time-remapping operators
  under each Sequence, to ensure that every frame which is needed by
  the scene is copied [bug 49662]

* Fixed issue that meant burnin metadata could be incorrect in a stack
  using a temporal OFX effect (e.g. NeatVideo) [bug 50009]

* Fixed an issue that could cause the File System Index to be updated
  more frequently than it should [bug 50114]

* Fixed an issue with missing symlinks when using the File System 
  Index [bug 49949]

* Fixed issue with switching paint strips losing the erase brush 
  settings [bug 49864]

* Fixed a low-level metadata inconsistency when rendering Avid OP-Atom
  MXFs. These files can now be AMA linked in Avid [bug 49478]

* Fixed issue in Paint with desk encoders leaving a delta open when
  switch to a different strip [bug 49989]

* Improved display of active Media Import Rules to only report rules
  that do something as being active [bug 50145]

* Fixed font-specific outline text rendering errors [bug 50210]

* Network diagnostic now accepts interfaces which are faster than
  expected [bug 50237]

* Fixed issue where pop-up showing the active grades in a strip
  were not displaying correctly [bug 50266]

* Fixed a crash when user colour space cannot be parsed [bug 50312]

* Added support for Pro Tools audio stem naming and fixed issue with 
  deleting audio stems when performing another search, with a new
  option to reset all stems [bug 43545]

* Fixed crash in EDL Import when finalizing a conform with a gap in
  the timeline [bug 50186]

* Added "Display Pixel Offset" customise option for Grid Warp and new
  options to reset control points to the default grid or to the
  'other' grid [bug 48732]

* Turning on "Display Pixel Offset" in Grid Warp will highlight any
  displaced control points with an outer ring, in order to quickly
  see which control points have been modified [bug 48655]

* Improved the efficiency of data transfers to the Slate control
  panel. This fixes issues seen when the panel is connected via a
  USB extender. The change requires updated Slate firmware; please
  contact FilmLight support for further information [bug 50090]

* Fixed an issue that prevented MXF-files with multiple partitions of
  CBE essence from being read correctly [bug 50360]

* Fixed bug which could cause a crash when adjusting a transform from
  the trackballs during playback [bug 13552]

* Fixed bug causing a crash during Timeline Sort [bug 50398]

* Fixed an issue that prevented some MXF-files with missing essence
  descriptor metadata from being opened [bug 50395]

* Fixed an issue where incorrect image metadata in MXF-headers could
  cause broken decode of thumbnails and images in the affected files
  [bug 50400]

* Fixed an issue where UUIDs generated by different processes started
  at nearly the same time were insufficiently randomised. This
  affected the IDs generated by fl-kdmtool in particular [bug 50377]

* Improved spacing of text drawn on macOS Retina displays [bug 43230]

* Fixed failure when copying sequences from remote media [bug 49777]

* Fixed warning when compiling some Matchbox Shaders [bug 49807]

* Fixed UHD setups to default to use Rec.2020 matrix [bug 49914]

* Timecodes from ARRIRAW files now have a fixed frame rate [bug 50082]

* Fixed crash in bl-conform when setting containers [bug 50214]

* Fixed crash in Colour Panel [bug 50275]

* Fixed crash when loading a scene with a Text strip referencing a
  non-existant font [bug 50247]

* Fixed performance issues related to colour space menus [bug 49369]

* Made re-selection of the current param strip from a multi-selection
  consistent [bug 49624]

* Fixed issue causing keyframes of audio sequences to be loaded
  incorrectly [bug 49141]

* Fixed potential crash on scene load after using cloned curves in
  shapes [bug 50439]

* Adaptec RAID disk diagnostics now report disk serial numbers and
  locations [bug 31830]

* Fixed various issues with MaxCLL/MacFALL analysis, including when
  rendering to a local path and when rendering movies with audio. The
  per-frame analysis data is now written as floating-point, for
  greater clarity when the analysis numbers are very small [bug 50479]

* Paint and Text now deal with missing and renamed colour spaces
  correctly [bug 49938]

* Corrected the Timeline offset for Grid Warps undergoing a Timeline
  Sort [bug 50481]

* Fixed "too many open files" errors when using a floating licence
  server [bug 49958]

* Improved perfomance issues when browsing folders containing movie
  files, particularly on 3rd-party storage [bug 50198]

* Fixed crash when changing the Y'CbCr matrix on some varieties of
  Sequence [bug 50518]

--------------------------------------------------------------------------

Baselight Release 5.2.11383 (2019-01-30)
베이스라이트 릴리즈 5.2.11383버전

Bug Fixes Since Baselight 5.2.11313
===================================

* Fixed Dolby Vision Software CMU behaviour when using a Dolby Vision
  Viewing/Rendering Colour Space with a maximum brightness higher than
  any Dolby Vision Trim set for the shot (e.g. rendering a 1000-nit
  deliverable when there is only a 100-nit trim) [bug 50035]

* Fixed failure to recognise movie and/or audio files when browsing a
  large directory in FLUX Manage [bug 50039]

* Fixed problem where opening the Media Import Rules View after
  opening a scene would remove any rules from the scene [bug 50087]

* Fixed crash in EXR writing, encountered for example when grabbing
  certain resolutions of EXR files to a gallery [bug 50085]

* Fixed crash when using Input Format in a Media Import Rules filter
  [bug 50088]

* Fixed problem where importing an EDL caused Media Import Rules to
  be applied to all shots in the scene [bug 50108]

* Fixed an issue where HD resolution DNxHR 444 written to Quicktime
  would display black or green frames when viewed in Avid or on MacOS
  [bug 49771]

* Fixed issue with scratchpad not storing keyframes [bug 50184]

* Fixed issue which would prevent undo/redo/scene close etc. from
  working after deselecting a panorama operator [bug 50124]

* Fixed crash rendering scenes with denoise and burnins [bug 50192]

* Fixed crash on startup on macOS when using SDI output hardware
  [bug 50144]

* Fixed crash on macOS when disconnecting a removable drive
  [bug 49708]

* Fixed a failure to import jobs with a very large number of tags
  [bug 50157]

* Fixed crash clicking on a colour well in the Preferences window when
  no scene is open [bug 50263]

--------------------------------------------------------------------------

Baselight Release 5.2.11313 (2019-01-15)
베이스라이트 릴리즈 5.2.11313버전

Important Notes 중요 내용 
===============

Compatibility With 5.1
5.1 버전과의 호환성 
----------------------

Due to changes listed below, notably the new Image Transform Settings,
scenes saved in 5.2 will no longer open in 5.1.
새로운 이미지 트랜스폼 설정으로 인해서(자세한 내용은 아래 리스트 참조), 5.2에서 새로운 씬을 저장할 경우 5.1 버전에서는 더 이상을 열리지 않습니다. 

So as to ensure consistent image decoding access to remote Baselight,
Daylight or FLUX Store systems also require a 5.2 release installed.
호환성을 위해서 베이스라트, 데이라이트, 플럭스 스토어에는 원격으로 지속적인 이미지 디코딩 작업을 하기위해서 5.2 버전 릴리즈가 설치되어 있어야 합니다. 

BLG files exported from 5.2 cannot be used by 5.1 products, including
Baselight Editions. 
버전 5.2에서 BLG파일을 추출한 경우 베이스라이트 에이션을 포함한 5.1버전 제품에서는 사용할 수 없습니다. 

Baselight FOUR and EIGHT 베이스라이트 4(Four)/ 8 (Eight)
------------------------

Baselight 5.2 is the last version that is supported on Baselight FOUR
and Baselight EIGHT systems. Baselight 5.3 and later will not install
or run on such systems.
베이스라이트 5.2 버전이 베이스라이트 4/8 시스템을 지원하는 마지막 버전이 됩니다. 베이스라이트 5.3버전에서는 설치되거나 실행할 수 없습니다. 

Baselight CONFORM 베이스라이트 컨펌
-----------------

Running on macOS 10.9, 10.10 or 10.11 is no longer supported
MacOS 10.9, 10.10, 10.11 은 더이상 지원하지 않습니다. 


New Features Since Baselight 5.1.11140
베이스라이트 5.2.11140 이후 새로운 기능 
======================================

Texture Highlight Operator 텍스쳐 하이라이트 오퍼레이터 
--------------------------

* Added new Texture Highlight operator. This can be used to reduce
  modulation (contrast) in higher frequencies to avoid unnatural sharp
  highlights. This is a common problem for HDR deliveries where bright
  specular highlights produce an over-sharp image. The operator can
  also be used to smooth out small clipped highlights. It is designed
  to be applied in scene-referred colour grading workflows and is
  colour space aware [bug 46352]
새로운 하이라이트 질감관리(텍스쳐 하이라이트;Texture Highlight) 오퍼레이터가 추가되었습니다.
부자연스럽게 예리한 하이라이트를 피하기 위해 고주파수(하이 프리퀀시)에서 변조 (콘트라스트)를 감소시키는 데 사용할 수 있습니다. 지나치게 밝게 반사된 하리라이트가 과도하게 선명한 이미지를 만들게 되는 HDR 딜리버리의 일반적인 문제가 있는데, 이 오퍼레이터는 적게 클립된 하이라이트를 통해서 부드럽게 만들수 있씁니다. 씬참조(Scene Referred)기반의 컬러그레이딩 워크플로우에 적용되도록 설계되었으며, 컬러스페이스르 인식합니다.

Panorama 파노라마
--------

* Baselight now includes a new tool called "Panorama" that enables
  common Baselight viewing and grading operations on 360 degree
  panoramic images.

  This tool is able to:

  - Given a user defined scene working format, activate a cursor based
    "Panorama Viewing Mode" that allows camera navigation about the
    projected scene.

  - Grade a particular region of interest in the scene directly in
    Panorama mode using a "Panorama Sandwich", free from the
    characteristic distortions of a 360 LatLong texture.

  Panorama Scene Setup 파노라마 씬 설정 
  --------------------
  To enable Baselight's Panorama functionality, material needs to be
  tagged as being panoramic.

  This is done by creating a new format of the appropriate resolution
  with the new "Projection" setting set to "Panorama" and then setting
  the Input Format of a Sequence to this format. The new format
  resolution should have the same pixel aspect ratio as the sequence
  dimensions to avoid distortion artefacts.

  The Working Format and Viewing Format of the scene should also be
  set to this same panorama format.

  Panorama Viewing Mode 파노라마 뷰잉모드
  ---------------------
  If the Viewing Format of current cursor is a panorama format, then
  the corresponding "Panorama" toggle button in the Cursor View is
  also enabled.

  This button switches between two viewing modes - rectangular
  (default) and panorama. When toggled on, the image is rendered in a
  spherical manner. The usual pan and zoom mouse controls are now
  reinterpreted as rotations around the scene and as changes in the
  camera field of view respectively.

  Toggling back into the normal rectangular format returns the mouse
  controls to the normal pan and zoom mode.

  - Mouse middle button: With the middle button pressed, mouse
    movements rotate the camera vertically and horizontally around the
    screen.

  - Ctrl + Mouse middle button: The Ctrl modifier lets the mouse
    middle button change the camera field of view.

  - Ctrl + Mouse wheel: The default camera height is at the centre of
    the sphere (cf. Fig 1).
    The combination Ctl + Mouse wheel allows the camera height to be
    adjusted inside the Panorama Viewer (cf. Fig 2). This control
    helps adjusting the panorama image if the original physical camera
    was not exactly at the centre of the scene.

          **   **
       *     .     *
     *       .       *
    *        .        *
    *        o-->     *
    *        .        *
     *       .       *
       *     .     *
          **   **
    Figure 1 - Default camera vertical position.

          **   **
       *     .     *
     *       o-->    *
    *        .        *
    *        .        *
    *        .        *
     *       .       *
       *     .     *
          **   **
    Figure 2 - Change the camera vertical position.

  - Alt + Mouse wheel: The combination Alt + Mouse wheel allows a
    cutoff correction at the bottom of the sphere (cf. Fig 3). A black
    circle appears at the bottom of the projected view indicating the
    point at which the truncation is applied.

    (NOTE) Not all footage corresponds to a complete spherical view of
    the world. Some images are truncated at the bottom to hide
    physical camera support equipment which might otherwise be visible
    in the scene.

    Wrongly assuming the physical camera view to be perfectly
    spherical results in a compressed image at the poles of the
    panorama projection. This can be detected by visual inspection of
    the projected image and noticing a merging artefact of the texture
    at the bottom of the sphere.

          **   **
       *     .     *
     *       .       *
    *        .        *
    *        o-->     *
    *        .        *
     * ************* *
    Figure 3 - Change the sphere bottom cutoff.

  Panorama Sandwich 파노라마 샌드위치 
  -----------------
  Due to the large amount of distortion, most Baselight tools like
  Shapes, Trackers, Paint etc don't work well when applied directly to
  panoramic (LatLong) images - a tool to remove the distortion is
  required. This tool is the "Panorama Sandwich".

  The Panorama Sandwich is a pair of Panorama projection strips. The
  first strip projects the LatLong image onto a spherical surface. The
  second strip inverts the operation and maps the projected texture
  back into the original LatLong image. Any grading applied between
  these two operators will be restricted to the region in the LatLong
  texture the camera is looking at.

  (NOTE) The projection necessarily magnifies the region of the
  LatLong image into the viewing format resolution. Conversely, the
  inverse projection will minify the projected texture back into the
  LatLong image. Both of these projections will involve a filtering
  step applied by the renderer and may therefore affect the projected
  region of the LatLong image.

  A Panorama Sandwich is constructed by inserting two consecutive
  Panorama operators and enabling the "Invert Projection" mode of the
  second one. The later will synchronise the camera state with the
  former and apply the invert projection at the correct position in
  the LatLong image. Inside this pair, any grading will be restricted
  to the area at which the camera of the top Panorama strip is
  looking. This is made easy by the "Smart Panorama" macro (Shift+J),
  which conveniently creates a "Panorama Sandwich" beneath the current
  selection and sets the projection state of each Panorama strip
  accordingly. For convenience, Smart Panorama copies the camera state
  of the current cursor, as long as it is in "Panorama" mode.

  - Details of the settings of the Panorama operator:

    - Camera View Controls
      "Left/Right View"  : Rotate the camera view horizontally.
      "Down/Up View"     : Rotate the camera view vertically.
      "Field of View"    : Change the camera field of view.
      "Camera Home View" : Reset the camera state.
      "Camera Control"   : Display an camera control overlay which
      allows its control using the mouse. The mouse controls are
      the same as in Viewing Mode.
      "Extended Ranges"  : Increase the range of camera rotations.

    - Camera Position Controls
      "Camera" : Change the camera vertical position.
      "Dome"   : Change the sphere bottom cutoff value.

      "Invert Projection" : Set the strip mode to invert the
      projection back onto the original LatLong texture. This will
      disable the strip controls and will set the strip to look up for
      its Panorama partner strip to read its camera state.

    - As well as using sliders and overlays to control the camera,
      Panorama also supports using the Blackboard/Slate trackballs and
      encoders using the following mappings:

      "Middle trackball"      : Rotate the camera view.
      "Middle trackball ring" : Change the camera field of view.

      "Up/Down enconder"   : Rotate the camera vertically.
      "Left/Right encoder" : Rotate the camera horizontally.
      "Zoom encoder"       : Change the camera field of view.
      "Camera encoder"     : Change the camera vertical position.
      "Dome encoder"       : Change the sphere buttom cutoff value.

Layer Blending 레이어 블랜딩 
--------------

* Added new popup panel used to simplify the configuration of a
  layer's blend-related options.
레이어의 블랜드와 연관된 옵션 구성을 단순화하여 사용되는 새로운 팝업패널을 추가되었습니다.

  Previously, these options were set via a few (opaque) buttons and
  menu options. Now, they've been collected together in a single
  graph- style display, accessed from the "graph" icon button next to
  a layer's blend type dropdown.

  This graph has nodes illustrating:

  - Where the layer's grade operators are applied
  - Where the blend operation is applied
  - Where the final mix is applied

  How these nodes relate to each other can also be configured via this
  panel. For example, in a default layer the grade ops are applied and
  then fed directly to the final mix. However, you can move the grade
  ops over to the "Blend Type" node's input simply by clicking the
  'tick' above the node itself.

  There are also node menus and buttons for setting the sources for
  various inputs/nodes, blend mode selection etc [bug 32897]

* Added new layer blend mode "Texture Blend". This allows you to
  restrict the grading operations in a layer to the lower or higher
  frequencies of an image.

  To grade lower frequencies:

  - Select "Texture Blend" as the blend type.
  - Set the result blending amount slider to ~50%.

  To grade higher frequencies:

  - Select "Texture Blend" as the blend type.
  - Popup the blend configuration panel and move the layer's grade
    operators to the other input of the blend node (by clicking on
    the grey tick).
  - Set the panel's "Mix" slider (or the result blending slider) to
    ~50% [bug 48277]

* Added nine new blend modes (to inside/outside layers and explicit
  blend strips) to match later versions of Adobe Photoshop:
최신 버전의 Adobe Photoshop과 맞추기 위해서 9개의 새로운 블랜드 모드(인사이드/아웃사이드 레이어와 블랙드 스트립)를 추가되었습니다.  
    Linear Burn 리니어 번
    Darker Colour 다커 컬러
    Lighter Colour 라이터 컬러
    Vivid Light 비비드 라이트
    Linear Light 리니어 라이트
    Pin Light 핀 라이트
    Hard Mix 하드 믹스
    Exclusion 익스클루션 
    Divide 디바이드 

* Reversed the sense of "Colour Dodge" and "Colour Burn" to match
  Adobe Photoshop [bug 41614]

* Changed the "Soft Light" algorithm to match Adobe Photoshop
  [bug 41614]

* The "Subtract" algorithm is now a simple subtraction (A - B) to
  match later versions of Adobe Photoshop [bug 41614]

* Changed the ordering and spacing of the blend mode drop-down in the
  Inside/Outside Layer and Blend parameter UIs to match Adobe
  Photoshop.

MaxCLL/MaxFALL Analysis MaxCLL/MaxFALL 분석
-----------------------

* Added the ability to analyse rendered frames and produce MaxCLL
  (content light level) and MaxFALL (frame average light level)
  numbers for the entire deliverable, and/or CLL and FALL numbers for
  each rendered frame.

  The deliverable analysis numbers are recorded in the render
  operation's log in the queue, and are written to an XML file in
  standard <md:Picture> format that also includes the colour space
  parameters for the Mastering Colour Space, if set [bug 33887]

Relight Operator 리라이트 오퍼레이터 
----------------

* The Relight operator is a new spatial grading operator that works
  with additional world position and normal information to allow the
  casting of virtual lights within the 3D space that is represented by
  the image. The virtual light uses physically-based lighting and
  surface material appearance equations to compute a contribution of
  this virtual light that then can be mixed with the input image in
  various ways.

  To make this operator work, the stack needs to be set up in a
  certain way so that the operator receives the correct input
  information. If the world position and normal passes are al stored
  in a single large OpenEXR sequence or similar multi-track image
  format, the simplest way to achieve this is to use the "Smart Insert
  Relight3D" macro, which is available in the "Insert" menu. It uses
  an internal dictionary of OpenEXR track names that represent the
  corresponding compositing channels. If none of these track names can
  be found in the sequence it will ask the user to specify the name of
  the track with the option to be added to the internal dictionary at
  the same time.

  Alternatively, to set up the stack manually, it needs have the
  following order:
    Input (Raw Sequence or grading stack)
    Reference to the normal surface data or an image sequence
    Reference to the world position data or an image sequence
    Relight3D operator

  You must ensure that for both the surface normal data and world
  position data there are no colour space conversions which could
  modify the data and distort the results. The easiest way to do this
  is to ensure that the "Ignore Colour Conversion" toggle is set in
  the Reference strips.

  Similarly, you should ensure that the working format of the scene is
  set to be the same as the format of the OpenEXR sequence being
  relit. This is required to prevent resizing of the normal and world
  position inputs, which can cause odd lighting effects.

  Once the stack has been set up correctly and the operator has been
  inserted successfully, the first thing the operator will ask you to
  do is to define the global unit size. Often with computer generated
  imagery, the size of the world and the scale of the units (mm, cm,
  meters, inches, feet) are not well defined or not clear. This
  information tends to be lost once it has reached the later stageof
  production. Unfortunately, this can lead to very confusing setups
  where an object might appear very small or very large in the image
  but its actual size in terms of 3D unit world scale could be tiny or
  enormous. To balance this out and to make setting the later lighting
  parameters easier, you can set the global scene scale. This can be
  done by just dragging a line in the image viewer from one point
  representing a part to the scene to another part. While doing the
  actual size of one unit will be displayed next to it. If you do not
  want to define a unit scale simply off click "Pick Scale Distance"
  button and the global scale stays 1.0. The global scale can also be
  changed at any time by either click on the "Pick Scale Distance"
  again or change the "World Global Scale" value manually in the user
  interface. If the scene contains multiple different sequences with
  roughly the same unit scale the current active scale can be stored
  as default for all future Relight3D operators via the "Customise"
  menu.

  Placing a light source is typically done in the Display View. Simply
  click on the position in the image you want to be lit and the light
  will automatically move to a point along the normal from the clicked
  point. The distance along the normal is specified by the "Target
  Distance".

  This works very well if only a diffuse contribution of the light is
  required. Making a specular highlight appear at the same point is a
  bit trickier as it depends not only on the light direction but also
  the virtual camera viewing direction. One has to shift the light
  facing direction to match up with the virtual camera viewing
  direction. To help to achieve this, there is a second click-mode
  that can be engaged by changed by changing the "Diffuse Hotspot at
  Mouse Position" setting to "Specular Highlight at Mouse Position".
  When engaged, the light will be positioned to ensure a specular
  highlight at the point clicked. For convenience, holding "Shift"
  when dragging will engage the alternative click mode during the
  drag. The specular highlight colour is determined by the light
  colour which is white by default. It can be changed in the user
  interface by selecting a colour from the colour wheel or
  alternatively a colour can be picked from the image by holding
  Control (Cmd on the Mac) and clicking in the image viewer at the
  same time. This is very useful when needing to match the specular
  colour of existing lights in the scene.

  The surface material in the Relight3D operator is based on a mixture
  of a Lambertian diffuse appearance model plus a Cook Torrance
  specular model on top of that. This allows the emulation of
  materials ranking from very matte surfaces (e.g. matte wall paint
  and fabrics) to semi-glossy (e.g. plastic, skin) to highly glossy
  surfaces, (e.g. untreated metals). The material parameters can be
  influenced by three settings in the UI: The "Diffuse Amount"
  determines how much diffuse/lambertian reflection the surface should
  exhibit. The "Specular Amount" determines how much specular/glossy
  reflection the surface should exhibit and finally the "Roughness"
  determines how rough/smooth the surface and therefore indirectly how
  glossy the surface should be. A high roughness values leads to a
  more diffuse-acting surface while low roughness lead to a nearly
  perfect mirror-like surface. As mentioned previously, the specular
  colour is determined by the light colour. However, the diffuse
  material colour is determined by the "Colour Source" and "Colour
  Use" options in the UI. By default, these are set to "Raw Input" and
  "Use Colour Source" respectively. This means the operator takes the
  pixel colour from the raw input images as the underlying diffuse
  material colour. This is not necessarily ideal as the raw image
  colour already contains baked-in lighting information so the whole
  process acts as a multiplier, which can look strange on occasion.
  Therefore, the other option is to "Use Colour Channel Input" this
  will allow to use an additional track in the OpenEXR (if available)
  as the per-pixel diffuse material colour instead. Alternatively, if
  everything is to be lit by a single unique diffuse material colour,
  "Use Colour Source" can be switched to "Use Single Colour" and an
  additional colour well will appear in the UI, allowing the diffuse
  colour to be specified.

  At the moment the Relight3D operator supports three different light
  types:
    - Omnidirectional Point Light: An infinitely small light that
      casts light in all directions with the same strength.
    - Directional Spot Light: An infinitely small spot light that
      only casts light within a given spotlight cone anle. The maximum
      intensity occurs within the "Hotspot Cone" and falls off to
      nothing at the "Spotlight Cone".
    - Area Light: A rectangular light that casts light onto surfaces
      lying in front of the rectangle. It is possible to set the width
      and height of the rectangle, making it useful when needing to
      mimic real lights in a scene (e.g. strip lights or tube lights).
      Be aware, however, that increasing the surface area also will
      increase the total flux of the light at the same time.

  Area lights are always physically accurate and therefore always use
  an inverse square falloff, which means that doubling the distance of
  the light from a surface will result in the surface receiving only a
  quarter of the previous intensity. For area lights, this parameter
  (labelled as "Quadratic" in the "Falloff" drop down) cannot be
  changed. For point lights and spot lights there is no such
  restriction - the falloff can be changed to either "Linear" or even
  "None". Switching off light falloff is useful when simulating
  distance objects like the sun.

  The "Apply Type" control determines how the result from the virtual
  light should be mixed with the raw input image:
   - Add the lighting result to the input image, simulating adding
     an additional light to the scene.
   - Multiply the lighting result with input image.
   - Subtract the lighting result from input image.
   - Replace the input image with the lighting result

  Out of the box, the Relight3D operator tries to extract the virtual
  camera position data from the metadata stored in the OpenEXR
  sequence. This data is required for computing the virtual viewing
  direction that is needed for the specular lighting contributions. If
  no such metadata can be retrieved from the OpenEXR sequence, the
  operator will try to solve the camera position automatically based
  on the 3D information stored in the normal and world position
  tracks. This process is not guaranteed to come up with a successful
  solution, but should work most of the time. In some rare cases the
  camera data stored in the OpenEXR sequence might be incorrect - if
  this is the case, there is the option to "Ignore Stored Camera Data"
  to force a solve of the camera position instead.

  The world position and normal inputs only contain a single value per
  pixel. Unfortunately, this can potentially introduce sharp/jaggy
  edges in the lighting result, especially if the light lies at a
  grazing angle to a surface. To soften this effect, the Relight3D
  operator allows one to use the "Edge Smoothing" slider to smooth
  edges and high frequency areas of the lighting result before it gets
  mixed with the input image.

  Rather than manipulating the light position in the Display View, the
  light position, light direction and some other lighting parameters
  can also be controlled using the "Point Cloud" tab. The controls of
  the point cloud views are identical to the ones that can be found in
  MatteXYZ.

  A control surface like Blackboard/Slate/Tangent Wave etc can be used
  to control certain light parameters via the trackballs and rings.
  When a control surface is available, the overlay in the image view
  will look slightly different, providing additional hints for the
  trackball controls. The trackballs are mapped to do following
  operations:
   - The left trackball controls the orientation of the light. On the
     image viewer, this is symbolised by the two rings close to the
     light widget. The red ring represents the directional change that
     is will occur when rolling the trackball horizontally. Rolling
     left is symbolised by a darker red and rolling right is
     symbolised by a lighter red. The green ring represents the
     directional change that is going to happen when rolling the
     trackball vertically. Rolling up is symbolised by a lighter green
     and rolling down by a darker green. Additionally, pressing one of
     the "Axis Lock" buttons will restrict the movement to one axis
     when moving the trackballs. The trackball movements represent the
     movements on a sphere that surrounds the light position. At the
     extreme positions of the sphere (the poles) only one axis will
     have a real affect on the light direction. The left ring controls
     the light distance.
   - The middle trackball controls the X/Y position of the light on
     the screen. The middle ring moves the light into/out of the
     screen.
   - The right trackball controls the area light size. The right ring
     controls the light intensity.

Upgrading of 4.4m1 Jobs and Scenes
----------------------------------

* Previously, Baselight 5 required a special installation of 4.4m1 to
  be able to read and upgrade old scenes and jobs. This it no longer
  required - Baselight can now import and upgrade 4.4m1 scenes
  directly.

  You can now also upgrade a single 4.4m1 scene "on the fly". Select
  it in the Job Manager and open it. Baselight will prompt you for a
  v5 job so it can make an upgraded copy of the scene.

* The bl-upgrade command-line tool usage flags have changed. It can
  now create a new job when upgrading. It can also rename the 4.4m1
  job so that the v5 job has the same name as the original. Run
  "bl-upgrade -i" for full instructions.

  When upgrading 4.4m1 jobs, scenes will be auto-unlocked whenever it
  is safe to do so.

  Baselight 5 is not able to recover autosave edits from 4.4m1 scenes.
  If this is required, open the scene in a copy of 4.4m1 first,
  recover the unsaved edits and save. Once that has been done,
  Baselight 5 will be able to read the scene [bug 39321]

Text Operator 텍스트 오퍼레이터 
-------------

* The Text operator has been substantially updated, allowing a much
  greater flexibility and creativity in the positioning and motion of
  text in a scene.

  This includes the following improvements over previous versions:

  - Support for transforms and perspective planes with the Text
    operator itself, in a manner similar to Shape and Paint
  - Support for trackers, including perspective tracking
  - Colour space aware colour picking
  - Significant performance improvements, particularly for large text
  - Improvements in the handling of extreme transforms [bug 46958]

Y'CbCr Matrices  Y'CbCr 매트리스 
---------------

* The matrix (also known as "coding equations") used to convert
  between RGB and Y'CbCr when:
  - reading Y'CbCr-encoded input media
  - writing Y'CbCr-encoded output media
  - displaying images via 4:2:2 SDI
  can now be switched between Rec.709, Rec.601 and Rec.2020.

  The Sequence operator allows the input matrix to be chosen; by
  default this is determined using the metadata obtained from the
  input media itself.

  The Render View allows the output matrix to be chosen; by default
  this is determined using the colour primaries of the render colour
  space.

  The Setup editor allows the display matrix to be chosen; you should
  set this to match the Y'CbCr-to-RGB matrix used by your display
  device.

  The Colour Space Journey View indicates which matrices are used by
  Sequence operators and SDI output.

  Sequences and deliverables in older scenes are unaffected, and will
  use the incorrect matrix for Rec.2020 media unless they are manually
  changed [bug 45891]

Image Transform Settings 이미지 트랜스폼 설정 
------------------------

* Five new image transform modes have been added:

  - Circle Average. This is good for reducing an image by 3:1 or
    greater. The averages are a soft-edged circles that touch at the
    diagonals. It is sharp, but blurs the centre of a starburst chart
    where other options may give aliasing.

  - Square Average. This is not as good as the Circle sampling. It is
    a bit sharper but may alias on diagonal features.

  - Fixed Simon. This uses a fixed set of weights similar to "Cubic"
    but a bit sharper.

  - Adaptive. This is like the old "Adaptive" mode but adds a blur if
    Sharpness < 1.0. This was desired because the "Adaptive" filter
    cannot handle low Sharpness values with large reductions
    [bug 46004]

  - Sharp Edge. This is a specialised mode that can be used for
    resizing titles or images containing other sharp features
    [bug 33630]

* Image transform modes menus now show only the most useful items; use
  the Shift key to see the whole list. There are tooltips for each
  mode if you hover the mouse over the menu.

Media Import Rules 미디어 임포트 룰
------------------

* A Media Import Rules View has been added. This view allows the
  setting up of rules that are applied whenever media is inserted into
  a scene. The rules are specified in the same way as Shots View
  filters are specified. When a rule matches a shot a number of
  actions can be taken:
  - File specific metadata can be mapped to a column in the scene
  - Decode parameters can be overridden
  - Certain parameters from the sequence operator can be overridden

  The view can be accessed via the Views menu or via shortcut buttons
  in the EDL Import and FLUX Manage views [bug 33033]

File System Indexing - beta functionality 파일시스템 인덱싱 - 베타 기능 
-----------------------------------------

  When enabled, Linux Baselight systems will maintain an index of the
  local images volume that is continually updated as new material is
  introduced to or removed from the volume.

  This feature will improve the speed of conform and other file system
  browsing operations. This feature is in beta test, and the
  configuration and operation is covered in the separate
  'file_system_index.beta.txt' file in the 'baselight/doc' folder.

Display And Timeline Cache 디스플레이와 타임라인 캐시
--------------------------

* Added support for 12-bit Integer RGB caches [bug 49395]
12비트 정수 RGB 캐시 지원 

* Caching at 10-bit Integer RGB or 8/10-bit Integer 4:2:2 Y'CrCb can
  now store data uncompressed or encoded in Apple ProRes [bug 49395]
10비트 정수 RGB 또는 8/10비트 정수 4:2:2  Y'CrCb  캐시를 무압축 또는 Apple ProRes 4444 방식으로 저장할 수 있음. 

IMF Rendering IMF랜더링 
-------------

* Added support for writing IMF profile JPEG 2000 codestream (J2C)
  files. 2K, 4K and 8K variants of single-tile (lossy) profile and
  reversible profile, as defined in ISO 15444-1:2016 (amendment 8),
  are supported. Mainlevel 0-11 is supported for every profile, and
  sublevel 0-9 is supported for lossy profiles. Reversible profile is
  always encoded at sublevel 0 (no bitrate constraint). The mainlevel
  specifies a maximum sample rate and a maximum sublevel:
JPEG2000 코드스트림(J2C) 방식의 IMF 프로파일 쓰기를 지원합니다. 2K, 4K, 8K 의 다양한 단일 타일프로그렘과 

   - Mainlevel 0:       Unspecified | Unspecified
   - Mainlevel 1:     65 MSamples/s | Max sublevel 1
   - Mainlevel 2:    130 MSamples/s | Max sublevel 1
   - Mainlevel 3:    196 MSamples/s | Max sublevel 1
   - Mainlevel 4:    260 MSamples/s | Max sublevel 2
   - Mainlevel 5:    520 MSamples/s | Max sublevel 3
   - Mainlevel 6:   1200 MSamples/s | Max sublevel 4
   - Mainlevel 7:   2400 MSamples/s | Max sublevel 5
   - Mainlevel 8:   4800 MSamples/s | Max sublevel 6
   - Mainlevel 9:   9600 MSamples/s | Max sublevel 7
   - Mainlevel 10: 19200 MSamples/s | Max sublevel 8
   - Mainlevel 11: 38400 MSamples/s | Max sublevel 9
  The sample rate is determined by the image format and the frame
  rate; sample rate = width x height x (components per pixel) x
  (frames per second). Each sublevel specifies a maximum bitrate:
   - Sublevel 0: Unspecified
   - Sublevel 1: 200 MBits/s
   - Sublevel 2: 400 MBits/s
   - Sublevel 3: 800 MBits/s
   - Sublevel 4: 1600 MBits/s
   - Sublevel 5: 3200 MBits/s
   - Sublevel 6: 6400 MBits/s
   - Sublevel 7: 12800 MBits/s
   - Sublevel 8: 25600 MBits/s
   - Sublevel 9: 51200 MBits/s
  This information is also available in the render panel, in the
  dropdown selector for each type of level. NB: The sublevel selector
  has no effect when using reversible profile. 2K, 4K or 8K profile is
  automatically set based on the rendered resolution. 2K up to a
  maximum resolution of 2048x1556, 4K up to 4096x3112 and 8K up to
  8192x6224. Higher resolutions than 8K can not be rendered using IMF
  profile.

  Support for writing Broadcast Contribution profile JPEG 2000
  codestream (J2C) files has also been added. All three Broadcast
  Contribution profiles defined in ISO 15444-1:2016 (amendment 8) are
  available; single-tile, multi-tile and multi-tile reversible. Level
  ranges from 0-11 are supported for single-tile and multi-tile
  profiles, while multi-tile reversible is always level 7. Each level
  specifies a maximum sample rate and a maximum bitrate. The rates for
  each level of single-tile and multi-tile profile are:
   - Level 0 :      Unspecified | Unspecified
   - Level 1 :    65 MSamples/s |   200 MBits/s
   - Level 2 :   130 MSamples/s |   200 MBits/s
   - Level 3 :   195 MSamples/s |   200 MBits/s
   - Level 4 :   260 MSamples/s |   400 MBits/s
   - Level 5 :   520 MSamples/s |   800 MBits/s
   - Level 6 :  1200 MSamples/s |  1600 MBits/s
   - Level 7 :  2400 MSamples/s |  3200 MBits/s
   - Level 8 :  4800 MSamples/s |  6400 MBits/s
   - Level 9 :  9600 MSamples/s | 12800 MBits/s
   - Level 10: 19200 MSamples/s | 25600 MBits/s
   - Level 11: 38400 MSamples/s | 51200 MBits/s
  This information is also available in the render panel, where the
  desired level is selected. Multi-tile reversible profile level 7 has
  a maximum sampling rate of 520 MSamples/s and no bitrate limit. NB:
  The level selector has no effect when using multi-tile reversible
  profile.

  The ASDCP library has been updated from version 1.12.51 to version
  2.7.19. This adds the capability to write AS-02 MXF-files, as used
  with IMF. It also fixes an issue where the SubDescriptors label
  written to DCI compatible MXF-files was incorrect.

  The string "JPEG2000" has been replaced with "JPEG 2000" in error
  messages and codec descriptions [bug 41312]

* SMPTE ST 2067-20/21 defines 7 different colorimetry systems, COLOR.1
  to COLOR.7, that an IMF picture track MXF can be tagged with. The
  render panel will show an entry for 'IMF Colour Tag' in the 'Video'
  selector when rendering to the IMF MXF file type. Tags will be
  applied when valid files are created. The IMF Colour Tag entry
  contains a text field which shows which tag will be applied, if any.
  It also has a 'Change...' button to assist in setting up output for
  the different colorimetry systems.

    - COLOR.3 will be tagged when:
      Using a matching colour space, e.g.
       + "Rec.709 Camera: ~1.95 Gamma / Rec.709"
       + "Rec.1886: 2.4 Gamma / Rec.709"
      Using a bitdepth of 8 or 10 bits.
      Using RGB (legal or full) or YCC 422 (legal) values.
    - COLOR.4 will be tagged when:
      Using a matching colour space, e.g.
       + "sRGB: ~2.2 Gamma / Rec.709"
      Using a bitdepth of 8 or 10 bits.
      Using YCC 422 and legal range values.
    - COLOR.5 will be tagged when:
      Using a matching colour space, e.g.
       + "Rec.2020: 2.4 Gamma / Rec.2020"
      Using a bitdepth of 10 or 12 bits.
      Using RGB (legal or full) or YCC 422 (legal) values.
    - COLOR.6 will be tagged when:
      Using a matching colour space, e.g.
       + "Dolby: ST 2084 PQ / P3 D65"
      Using a bitdepth of 10, 12 or 16 bits.
      Using RGB legal or full range values.
    - COLOR.7 will be tagged when:
      Using a matching colour space, e.g.
       + "Rec.2084: ST 2084 PQ / Rec.2020"
      Using a bitdepth of 10, 12 or 16 bits.
      Using RGB (legal or full) or YCC 422 (legal) values.

  Legal range values can be created by using a video LUT. The IMF
  colour tags are read and used for selecting the colour space from
  metadata on read [bug 41931]

File Formats 파일 포맷 
------------

* Additional metadata is now read from JPEG 2000 files (J2C, JP2,
  etc). Files with a defined JPEG 2000 profile will have a 'Profile'
  metadata entry naming the profile, as well as any level and sublevel
  if applicable. Up to two comments will be read from files with
  embedded comments into metadata entries named 'Comment' and
  'Comment2'. JPEG 2000 encoded MXF-files with valid JPEG 2000
  subdescriptors now also have a 'Profile' metadata entry with profile
  and level information.

  Rendered files will now contain information about software version,
  profile, level and compression ratio as applicable in an embedded
  comment. Files encoded using GPU JPEG 2000 acceleration will contain
  two comments, the first identifying the compression SDK, the second
  containing the information added by the software [bug 31956]

* Added an option to not clip highlights in DNG files. For new
  sequences, the default highlight handling is now 'Unclipped' rather
  than 'Clipped'. The highlight handling can be controlled via the DNG
  Params operator. A slider to control highlight reconstruction is
  also available when using 'Unclipped' [bug 32481]

* Four additional colour spaces are now recognised from NCLC-atom
  metadata when reading QuickTime movies; 'Rec.2100: HLG 1.2 Gamma /
  Rec.2020 / 1000 nits', 'Rec.1886: 2.4 Gamma / Rec.709', 'CGI: Linear
  / Rec.709' and 'sRGB: ~2.2 Gamma / Rec.709'. Range will also be
  picked up from the ACLR-atom when reading files using DNx codecs
  [bug 47377]

* Added support for reading Panasonic Varicam LT and EVA1 RAW
  CinemaDNG files using the V-Log colour space [bug 37851]

* Added Sensor Rate metadata for ARRIRAW media [bug 48693]

* ARRIRAW aperture metadata is now shown as a T-stop rather than an
  f-stop [bug 48389]

* Apple ProRes codecs always work with legal-range data. Previously a
  hidden scaling was done, and renders had to provide full-range data.
  For consistency and transparency this scaling is no longer applied,
  and image data sent to an Apple ProRes codec should be made
  video-legal using a Video LUT.

  This change also enables non-standard Apple ProRes movies to be
  created with full-range image data, should this be required.

  PLEASE NOTE: Deliverables in existing scenes, and deliverables
  created using older scene templates, will continue to use the old
  ranging behaviour. If you perform renders to Apple ProRes using the
  bl-render commandline, you will need to use the new "-v 1" option to
  retain the old ranging behaviour [bug 26117]

User Interface 유저인터페이스 
--------------

* Popup menus (from the menu bar, or popup controls, or right-click
  menus) can now be filtered using the keyboard while the menu is
  open. For example, in a Formats menu, type "p" to show only formats
  with a "p" in their name. Press Escape to clear the filtering
  [bug 48821]

* A popup tooltip will appear on a layer strip when the mouse is
  hovering over it, showing all the active grades within that layer.
  Popup info will not distinguish between inside/outside grades, if
  there are any [bug 34105]

* The size and position of most file- and scene/job-choosing dialogs
  is now remembered the next time they are opened [bug 29598]

* Custom (user-supplied) DRTs are now indicated with a user icon on
  menus, in the same manner as custom colour spaces [bug 46338]

* The brightness of some displayed elements (picked colours, pane
  descriptions, snapshot descriptions and fps) now matches the
  brightness set for the pane indicators, which prevents them being
  too bright on an HDR display [bug 46149]

Blackboard / Slate / Chalk 블랙보드/ 슬레이트/ 초크 
--------------------------

* Chalk for Blackboard 2 and Slate has been updated to be faster
  and more user-friendly:
  - when a modifier key (e.g. Control, Shift, Alt) is pressed, the
    display on the Chalk GUI and on the desk will update to more
    accurately reflect what would be displayed in the application
    under the same modifiers
  - every layout modification is now undo/redo compatible.
    This includes adding, duplicating, deleting and renaming
    buttons and Slate Layouts, adding and removing Actions to
    and from buttons, and renaming (but not deleting) layouts.
  - while Chalk is open, the standard undo/redo keyboard shortcuts
    can be used for layout modifications - Ctrl+Z to undo and
    Ctrl+Shift+Z to Redo (⌘+Z, ⌘+Shift+Z on Mac OS), and pressing
    Backspace or Delete on the keyboard will remove the selected
    button from the desk
  - it is now possible to rename a Custom Button [bug 47864]

* Added "Lock Y Position" and "Find Stereo Correspondence" buttons to
  Slate. These appear on the Home layout at the far left on the
  second-from-top row when a Shape strip is selected [bug 46514]

* Added desk controls on Slate for 17 operators: Blank, Camera Shake,
  DSpot, Erode/Dilate, Dissolve, EXR Exposure, Sander, Median, Motion
  Blur, Reference, Stereo Colour Matching, Switch, Threshold, and the
  Spirit grading operators (Spirit Noise Reduction, Spirit Primary,
  Spirit Six Vector and Spirit Spatial) [bug 46697]

* Added a "Pick" button to Blackboard, Blackboard 2 and Slate desks.
  This mirrors the "Pick" toggle in the BaseGrade user interface. It
  will appear next to 'Ext Rng' in the operator-specific area of the
  desk when the BaseGrade operator is selected [bug 45489]

* Added a "Balance Exposure" button to Blackboard, Blackboard 2 and
  Slate desks. This mirrors the "Balance Exposure" toggle in the Film
  Grade user interface. It will appear next to 'Ext Rng' in the
  operator-specific area of the desk when the Film Grade operator is
  selected [bug 35455]

* Added Actions for "Smart Dissolve" and "Smart Dissolve Shot" in
  Chalk [bug 34845]

* Added an Action for "Insert Layer Above" in Chalk [bug 46742]

* On Blackboard 2 and Slate, layer and operator buttons now appear
  hatched, when the operator or layer to which they correspond is
  bypassed, like on the main user interface [bug 46529]

* Added a control point bump feature to Grid Warp. When working on
  Grid Warp with a Blackboard or Slate, pressing the control key
  will toggle the arrow keys to bump keys. The default pixel bump
  amount can be set in the Grid Warp customise menu [bug 48573]

SDK Updates SDK업데이트 
-----------

* Updated to Sony XAVC encoder SDK version 1.1.8, which improves image
  quality when encoding XAVC Long GOP formats and brings minor
  improvements to encoding speed and quality [bug 47547]
소니 XAVC 엔코더 SDK 버전 1.1.8 지원. XAVC Long GOP 포맷의 이미지 퀄리지 향상

* Updated to DNxHD/DNxHR SDK version 2.3.7.46. This includes bug fixes
  [bug 48244]
 DNxHD/DNxHR SDK 버전 2.3.7.46 지원 

* Updated to Canon RAW SDK version 2.2R2. This includes a bug fix
  addressing incorrect exposure of clips with a specific ISO Speed or
  Gain [bug 49413]
캐논 RAW SDK 버전 2.2R2지원. 특정 ISO 스피트 또는 게인의 클립의 노출값이 정확하지 않는 버그 수정

* Updated to OpenEXR SDK version 2.2.1. There are no user-visible
  changes as a result [bug 46009]
OpenEXR SDK 버전 2.2.1 지원 

* Updated to FFMPEG SDK version 3.4.2. This SDK is used to read and
  write various video codecs in MXF and QuickTime containers. This
  update adds support for reading additional codecs, as well as minor
  speed and quality improvements both when reading and rendering.
  Existing scenes will still use the older SDK version to ensure that
  rendering does not change [bug 39813]

* Updated to OpenJPEG SDK version 2.2. This brings a minor improvement
  in encoding and decoding speed of JPEG 2000 material without a GPU
  JPEG 2000 acceleration license [bug 38662]

Miscellaneous 기타 
-------------

* The following multi-resolution operations are now scalable:
  - Boost Range
  - Denoise
  - Deflicker
  - Streak Filter
  - Texture Blend
  - Texture Equaliser
  - Texture Highlight

  These should now look similar when rendered at different
  resolutions. The fine detail is still handled at the local pixel
  resolution, but the longer-range effects should scale with the image
  rather than being a fixed number of pixels. The original scene
  resolution render is unchanged. We do not expect an exact match when
  rendering at other resolutions, but it should be closer than before.
  This is versioned, so old strips will not change [bug 46966]

* Added "Apply Foreground Blurs To Matte" (Customise menu) option to
  composite layers. If enabled, any blurs applied to the foreground
  operators will also applied to the layer's matte input [bug 46728]

* Added two new looks to Truelight Scene Looks: 
트루라이트 씬 룩에 새로운 2개의 룩 추가 

  - C-104 Bipack is a spectral simulation of a two strip process from
    the ~ 1950. As it is a two strip process it does not render
    greens, but shifts the look to a distinct cyan/orange axis.

  - C-202 ALF-2 emulates the appearance of the ARRI ALF-2 DRT Family,
    matching viewing condition Video-100 [bug 48843]

* Added negative clamps in the "Sodium High Pressure Lamp" and "Xenon
  Arc Lamp" looks. This prevents the looks from producing NaNs in some
  cases [bug 48542]

* Added support for the NVIDIA Quadro M620 UI GPU [bug 45506]

* You can now use the Job Manager to compact jobs. This reclaims
  unused space in the PostgreSQL database for that job. Select a job,
  and from its action menu choose "Compact Job" [bug 46656]

* Baselight will now auto-compact jobs as part of the nightly backup
  task [bug 47110]

* Improved error reporting when renaming jobs [bug 47717]

* bl-export will now enforce a "bljob" or "blscene" file extension
  [bug 47501]

* bl-export has improved help text [bug 48393]

* bl-export has improved progress output [bug 38209]

* Colour spaces which are only ever suitable for use as an Input
  Colour Space (typically those specific to a particular camera) are
  no longer offered in other colour space menus [bug 43832]

* Added "Resolution" and "Quality" options to Still Export [bug 46313]

* Changed automatic Mastering Colour Space for VideoWide and 
  OfficeWide viewing conditions to DCI: 2.6 Gamma / P3 D65 [bug 48247]

* Added new "Transform Alarm Overlay" feature (available from the
  "Display" menu). Once enabled, if a transform is introduced into the
  stack (explcitly or via a format conversion) that results in pixels
  outside the original image being introduced into the result image,
  those pixels will be displayed in a custom colour (also set from the
  "Display" menu) [bug 28017]

* The Shots View now supports 2 modes of selection (from the
  "Customise" menu):

  - Select Cuts View Shots : In this mode, selecting a shot in the
    Shots View will also (red square) select the shot in the Cuts View
    (and vice-versa).
  - Select Stack Top Strips : In this mode, selecting a shot in the
    Shots View will also explicitly select the top/input strip of the
    corresponding stack in the timeline (and vice-versa) [bug 45486]

* The command line tool for KDM creation, fl-kdmtool, now provides
  improved control over forensic mark flags and the authorised devices
  list. The built in help text has been updated accordingly, see the
  output of 'fl-kdmtool -h' [bug 46023]

* Added bl-encryptshaders tool which enables Shader authors to create
  encrypted versions of their shaders for distribution [bug 36745]

* Queue Monitor now shows elapsed time and overall fps for renders,
  and overall MB/s for copy operations [bug 30623]

* 50fps frame rate is now offered on frame rate popups [bug 48350]

* Added "Clip Negative Inputs" as an option for HDR Value Handling (in
  Scene Settings). This prevents negative values in VFX images from
  entering the grading stack [bug 46796]

* When inserting from FLUX Manage View with Timecode 2 selected,
  sequences with no Timecode 2 now use the sequence Timecode for the
  Shot Timecode [bug 47880]

* A folder of sequences can now be dragged from FLUX Manage View onto
  Shots View or Cuts View [bug 49005]

* Added option to Shape strip "Customise" menu for setting the default
  keyframe bar display mode [bug 49070]

* Added help text to DCI: 2.6 Gamma / X'Y'Z' space [bug 48784]

* Added the ability to export left and right eye BLGs at the same time
  during BLG Export. Simply select the new "Both Eyes in Separate
  BLGs" option in the "Stereo" setting [bug 49110]

* A deliverable preset defined with the same Render Frame Rate as the
  scene's Working Frame Rate no longer applies this frame rate when it
  is used in a scene with a different Working Frame Rate [bug 45124]

* fl-make-secure will now stop with an error if it is not run on
  FilmLightOS 6 [bug 48962]

* Added "Constant Bitrate" option to Apple ProRes QuickTime renders,
  to produce rendered files which are compatible with third-party
  video editing tools [bug 46983]

* Client View is now available in Baselight CONFORM [bug 47391]

* Added reference sub-stacks inside copy and destination subsets while
  using Blackboard copy and paste or DBS Apply (see Smart Dissolve or
  composite layer with foreground reference) [bug 44095]

* Cmd+H now hides the application on macOS [bug 49048]

* Numeric metadata such as %{Event} can now be padded in render
  filename templates, using the same syntax as for frame numbers:
  %.8{Event} will pad Event with leading zeros up to 8 digits
  [bug 49106]

* The "Clip to Legal" and "Soft Clip to Legal" video LUT options are
  not recommended and are now hidden in the Render View and Display
  menus; they can be revealed by pressing Shift [bug 49109]

* The controls for Dual Colour Spaces Layout have been changed. Two
  Viewing Colour Spaces are now shown on Cursor View with a toggle
  button next to each to control which is used for scopes, histogram
  and overlays [bug 49254]

* The timeline "Display All Note Text" option can be toggled on to
  permanently display all of the mark note text in the timeline
  simultaneously [bug 43750]

* LUT Export: Added option to export Left and Right LUTs
  simultaneously when using the Export LUTs dialog in Shots View
  [bug 49094]

* LUT Export: Full path to expected filename is now shown [bug 49090]

* Added new "Copy Files and Trim Sections From Movies" option to
  Consolidate. This creates multiple consolidated movies when more
  than one section of a movie file was used in the original scene
  [bug 45757]

* Added Truelight to "Strip colours" preference [bug 46498]

* The Truelight 'zview' application is now included with Baselight
  [bug 48299]

* Added support for 48@24 fps and 50@25 fps timecodes when reading ALE
  and CMX EDLs [bug 46246]

* Added bl-dump-edids utility, which can be used to save the EDID for
  monitors/projectors attached to the display and rendering GPUs on
  Linux systems. EDIDs are written into /usr/fl/etc/edids [bug 46978]

* Added mechanism that allows OFX plugins to improve their colour
  space handling [bug 49695]

* Added caching and compression to the internal operation of Paint, to
  improve the drawing speed [bug 41546]

Bug Fixes Since Baselight 5.1.11140
베이스라이트 5.2.11140 이후 버그개선 
===================================

* Shadow Boost gave a small jump in the histogram when the controls
  moved off the default settings. This is fixed for new Shadow
  Boost strips, but old ones are as before [bug 46870]

* Fixed an issue in Chalk which could cause multiple buttons to turn
  blue on the desk diagram [bug 45873]

* Fixed an issue that could cause the scratchpad scene to behave
  slowly over time [bug 46228]

* Scene loading performance is improved, particularly with scenes that
  contain complex trackers [bug 46310]

* Fixed rare crash that could occur when switching in/out of
  follow-mode or when cancelling an edit [bug 49469]

* The Job Manager will now show the user and software build of when
  the scene was last saved [bug 45973]

* bl-backupdb could fail with a mkdir error when running in test mode.
  It will now report the missing directory as an error instead
  [bug 45976]

* bl-shots and bl-containers can now be used on scenes that are
  currently open for editing [bug 47775]

* Fixed bug which could cause shapes to shift slightly vertically when
  "Lock Y Positions" option enabled [bug 45933]

* Fixed rare crash when reading from job database [bug 47395]

* Fixed rare crash when performing Save-As [bug 48778]

* Fixed possible cursor jump when performing Save-As [bug 46500]

* Cursor settings are now preserved when upgrading 4.4m1 jobs
  [bug 48097]

* Fixed crash with multiple spaces in a ccc file [bug 45880]

* Fixed a potential memory leak in disparity histogram [bug 45955]

* Renamed the Actions for the "Render Line Up" and "Render Line Down"
  desk buttons to be more consistent with their equivalents in the
  Navigate menu [bug 45480]

* Fixed an issue on Slate which could cause the Slate Layout toggle
  button to display a nonexistent Slate Layout [bug 29876]

* Fixed a potential memory leak in stereo geometry fix [bug 45957]

* Fixed a potential memory leak in MatteXYZ [bug 45956]

* Fixed a perspective operator issue which occurred when tracking was
  done in the 'In' side. After a stack split or a stack copy, it was
  left in an incorrect state [bug 46032]

* Fixed a potential crash when swapping 2 layers in the timeline
  [bug 45707]

* Added all cache formats to Display And Timeline Cache entry in
  Setups editor [bug 46128]

* Fixed issue which prevented using the 375.66 NVIDIA Driver with
  GTX 980, Quadro NVS 810, Quadro K6000, M4000, M5000 and M6000 GPUs
  [bug 46135]

* Fixed bug in 'Find Stereo Correspondence' when the working and
  viewing formats differed [bug 46165]

* Fixed thumbnails for movies which have an orientation of +/- 90
  degrees [bug 46153]

* Fixed potential cause of cached playback slowdown with huge scenes
  [bug 46238]

* The Blackboard 2 jog wheel can no longer move the cursor back beyond
  the start of the timeline [bug 45593]

* Fixed paint clone bug with very small strokes disappearing under
  transforms [bug 46254]

* Fixed crash when inserting a Pan&Scan operator into a scene after
  using it in another scene that uses a format unknown to the current
  scene [bug 46301]

* Fixed picking display in semi-automatic Stereo Geometry Fix not
  taking colour space transforms into account [bug 46177]

* Fixed group grading the stereo split state of a set of strips. Now
  it will only change the state if it matches the parameter strip
  [bug 46515]

* Speed up (grouped grade) 3D stereo splitting of multiple selected 
  strips [bug 46340]

* Fixed incorrect colour space when FLUX Manage Preview is used with
  the colour space set to Unknown and a scene is open [bug 46545]

* Fixed flash of a sequence's first frame when entering FLUX Manage
  Preview [bug 46542]

* Fix potential hang and disparity histogram picking display not
  working with certain grading stacks [bug 46532]

* Fixed naming of erase operations from FLUX Manage [bug 46546]

* The "Audio Toggle" desk button now works correctly on Slate: a 
  short key press toggles Mute and a long key press pops up a
  transient volume adjustment panel [bug 34069]

* Detection of corrupt scene databases is improved [bug 46657]

* Fixed issue with Paint strokes not updating after resetting a
  transform [bug 46576]

* Improved grouped paste error handling [bug 46645]

* Image orientation is now interpreted when reading QuickTime files
  written by ARRI cameras [bug 46761]

* Select next/previous strip of the currently selected type now obeys
  (Shots View) playback/navigation filtering [bug 46891]

* Fixed potential crash when adjusting shape "Inner Scale" encoder 
  [bug 45303]

* Fixed an issue where an incorrect index for a temporally compressed
  movie could crash the movie reader. This situation will now produce
  an error message about a bad index for the affected frames instead
  [bug 46745]

* Fixed render issue where the render frame rate was different to the
  working frame rate and the stack contained temporal effects
  [bug 46782]

* Changed ganging behaviour of scale parameters in a transform strip 
  such that the aspect ratio is maintained [bug 44898]

* Fixed issue with Apply skipping strips if the mode was set to 
  "Primaries" and contained copy protected strips [bug 46972]

* Fixed crash toggling the Paint layer opacity keyframe button
  [bug 46975]

* Added colour space selection to the paint colour brush colour
  selection tool to allow picking colours in a defined colour space
  [bug 46273]

* The Colour Panel now allows a colour space to be specified when
  setting the colour of Text [bug 46134]

* The Area Tracker and Area Tracker Perspective have been reworked to 
  work better with non-planar motions, like faces [bug 44762]

* On Mac OS X, the Cmd, Alt and Ctrl buttons on Slate now show the
  correct text [bug 46312]

* Fixed issue with Paint when resetting a layer caused keyframes to 
  be added [bug 47162]

* Fixed an issue where rendering to XDCAM could fail to encode video
  when images were noisy [bug 38728]

* Fixed rare crash which could occur when loading some old 4.4m1 BLGs
  containing Shapes [bug 47043]

* Fixed crash on drag and drop in the layer view [bug 47246]

* Extended BMD cube import to cope with special case of cubes with
  range and shaper LUTs but no 3D LUT [bug 47405]

* Added limits to colourspace transforms to prevent infinite or
  illegal values, tone curves with negative slope, etc. The colour
  space transforms are the same over the useful range [bug 43827]

* Added a separate erase brush to the paint operator [bug 46372]

* Fixed issue with Try not using the correct poster frame [bug 47229]

* Fixed issue in paint when the "All Strokes" Tab was enabled but no
  strokes were present [bug 47373]

* Truelight operator parameters are now correctly disabled when in a
  locked strip or read-only scene [bug 47481]

* The "End Alpha" parameter in Dissolve now resets to 1.0, not 0.0
  [bug 46708]

* Improved the display of small numeric values on Blackboard 2 and
  Slate, such as "Amount" in the Soften operator, which now displays
  to three decimal places rather than two [bug 29317]

* Fixed an issue where Sony VENICE files with resolutions other than
  4096x2160 were incorrectly marked as trimmable [bug 47307]

* Fixed issue with the Layer View not updating if the stack changed
  during a drag action [bug 37310]

* Paint stroke should no longer cause a shift from the centre when
  scaling down/up from the working format [bug 46945]

* Avid "Color Adapter" effects are removed from AAFs when Remove Avid
  CCs is selected during AAF update [bug 47535]

* Fixed potential crash when importing a BLG containing shapes that
  have cloned curves [bug 47247]

* Fixed an issue where the ScreenAspectRatio element in Interop DCPs
  could contain values other than 1.33, 1.66, 1.77, 1.85, 2.00 and
  2.39 [bug 47612]

* Paint matte no longer will be cut off when changing viewing format
  if it is larger than working format [bug 47585]

* On Blackboard 1, Blackboard 2 and Slate, the "Return to Strip" desk
  button in the Tracker operator has been updated to work with all the
  correct strip types [bug 47332]

* Improved smoothness of scene open progress panel [bug 47404]

* Fixed an issue on Blackboard 2 and Slate where the "Inside/Outside"
  desk button would go blank if there was no matte [bug 47743]

* Fixed bug which could result in negative event numbers being written
  to a CMX3600 when exporting an EDL for selected shots in a sorted
  Shots View tab [bug 46924]

* Fixed crash when group grading a Matte Tool containing an Edge
  Filter while in a stereo scene [bug 44990]

* Fixed next/previous poster frame navigation when timeline filtering
  enabled [bug 46486]

* Fixed bug which could cause the cursor to jump when 'Try'ing a grade
  from the DBS with timeline filtering enabled [bug 46357]

* Reduce console output when opening old scenes [bug 46535]

* Fixed Scratchpad "Original Version" toggling when playback filtering
  enabled [bug 46356]

* Fixed an issue that could cause conform to fail with an error
  message when a source sequence had keycode embedded in it
  [bug 47826]

* Re-aligned the layer view matte selection highlight [bug 47525]

* Fixed issue with the layer view changing the cursors rendering mode
  and not setting it back [bug 47688]

* Fixed bug which could cause incorrect matte (or matte overlay) mode
  display for composite layers with bypassed operators [bug 47909]

* The ASSETMAP and ASSETMAP.xml files present in DCPs are no longer
  recognised as movie files. Use the corresponding CPL-file instead
  [bug 47687]

* Apply SDL Events conform option is no longer given for files that
  are not a .edl containing SDL data [bug 47998]

* Made the Tracker numbering better in the Layer View [bug 29030]

* Clone paint no longer slows down rendering when there is an extreme
  perspective transform but instead causes a render failure
  [bug 47653]

* Stopped doing any layer number or reference layer number 
  consistency checking on broken stacks [bug 48125]

* Fixed issue with the cursor position in the cutview not being 
  correct [bug 48105]

* Fixed the "Next Ungraded Shot" and "Previous Ungraded Shot" Actions
  [bug 48171]

* Layer button double-tap behaviour on Blackboard, Blackboard 2 and
  Slate has been changed. By default, a double-tap will select the
  bottom layer in the stack. Alternative behaviour of selecting a
  higher-numbered layer on double-tap can be accessed via the
  "Layer Selection Double Tap" preference, which has moved to the
  Timeline section of the application preferences dialog
  [bug 44494]

* Allow timecode and keycode columns to be resized in Shots View
  [bug 48264]

* Fixed issue with the the shots view displaying the incorrect CDL
  values [bug 48257]

* Prevented the paint parameters being changed when a stroke is being
  drawn [bug 47329]

* Fixed several issues with Prepare For Review [bug 43435]

* When copying a file sequence in FLUX Manage, the destination
  directory is refreshed to show the copied sequence [bug 47041]

* Fixed crash reading a TIFF file that is 1 pixel high [bug 47727]

* Improved Colour Space Journey View warning when there is no DRT
  selected [bug 47756]

* Fixed crash in Queue Monitor View when rapidly clicking [bug 47759]

* Fixed failure to start flux service when preferences database cannot
  be contacted [bug 47821]

* Added Colour Space Journey View warning when Input and Stack colour
  space are both DCI: 2.6 Gamma / X'Y'Z' [bug 47850]

* Fixed crash when Cuts View has a specific size [bug 47926]

* Fixed behaviour when cancelling a directory search in FLUX Manage
  [bug 47963]

* Improved reduction in scene size after using Clear Undo History on a
  scene that has been rendered many times [bug 48008]

* The Colour Space menu on FLUX Manage View now shows the colour
  spaces as the Input Colour Space menu, which can be edited from
  Manage Colour Spaces [bug 48205]

* Fixed crash in renderer [bug 32792]

* Fixed import of Circle Take metadata [bug 48039]

* Fixed crash when picking in BaseGrade with a colour space that
  couldn't be evaluated [bug 47207]

* Fixed Job Manager host list not updating after editing [bug 48210]

* Fixed tnd service not starting if its cache folder has been deleted
  [bug 48203]

* Fixed paint rendering error on MultiGPU systems when using small 
  strokes and non-working format viewing formats [bug 48246]

* Desk firmware updates now prevent the user from putting the wrong
  firmware on the version of hardware already present by making sure
  that the major version numbers of installed and proposed firmware
  match [bug 46100]

* Using Flip and/or Flop in a Sequence operator no longer softens the
  image, nor crops the edge [bug 25159]

* The "Keyframe Toggle" desk button can now control keyframes 
  in DKey [bug 48514]

* Added conform option for FrameFlex layer number [bug 48417]

* Digital Cinema Packages (DCP) and JPEG 2000 MXF files now set the
  DCI_XYZ colour space from metadata when inserted [bug 48304]

* Fixed issue with FrameFlex scale not matching Avid for some AAFs
  [bug 48416]

* Fixed issue with FrameFlex not matching Avid for some media formats
  [bug 48278]

* Ensure correct tracker strip tab selected when adding a new 
  perspective track to a primitive (eg. a shape) [bug 48726]

* Fixed issue in paint where clone and colour strokes were being
  placed into the same layer [bug 48774]

* FrameFlex strip is no longer added when no transform is necessary,
  crop operator is reset correctly [bug 48704]

* Support for keyframed FrameFlex effects has been added [bug 47509]

* Fixed an issue where fl-kdmtool incorrectly changed unrecognised key
  types in the XML metadata to 'MDIK'. This affected e.g. 'MDEK'-type
  keys for Dolby Atmos audio [bug 48827]

* Fixed failure with temporal operators (e.g. Denoise) applied at the
  start or end of a sequence, when there is was a cached operator
  above the temporal operator [bug 48867]

* Clone brush paint shifts wrongly when using a perspective transform
  and switching to a viewing format that is larger than the working
  format [bug 48771]

* Fix clone brush not working correctly with interlaced material
  [bug 48157]

* Added substitutions to LUT Export for:
  Source Frame Number - %M,
  Source Timecode as Frame Number - %H
  Event Number - %E
  [bug 47184]

* Fixed crash when drawing a paint stroke and holding the pen still at
  the end of the stroke [bug 48939]

* Fixed an issue where some 1080i DNxHD encoded MXF files would appear
  to have a height of 2160 [bug 48933]

* Added preference to select Dissolve strip added when the Smart
  Dissolve macro is executed [bug 46168]

* The Compress Gamut operator parameters are now mapped to the
  trackball rings of any control surface [bug 38304]

* Reinstated %nW substitution syntax in Shots View. When %W is used as
  a column value or expression it is substituted with the Shot
  Filename. If %5W is used for example, the first five characters of
  Shot Filename are substituted [bug 47193]

* ASC CDL data can now be read from sub-clips in .aaf files
  [bug 49054]

* Fixed crash when cancelling the progress panel when dropping a
  folder from FLUX Manage View onto Timeline View [bug 49005]

* Fixed issue with exporting a LUT in a stereo scene failing silently
  [bug 46592]

* Fixed issue with exporting a LUT in a stereo scene failing when the
  scene contains spatial operators, like Stereo Alignment, that are in
  3D mode (with separate parameters for left and right eyes)
  [bug 49071]

* Improved text rendering performance (including burnin) [bug 48341]

* Fixed issue with dragging to the end of the Cut View when a playback
  navigation filter is active [bug 48872]

* Fixed an issue on Blackboard, Blackboard 2 and Slate which caused
  inside grades to be incorrectly copied to the outside on RGBKey,
  MatteXYZ and Paint mattes. This behaviour is now fully controlled by
  "Automatically initialise outside grades" in the application
  preferences [bug 48578]

* During conform the tape name of another clip isn't applied to clips
  with a blank tape name [bug 46275]

* During conform tape names are now read from sequence metadata when
  not specified in the EDL [bug 49066]

* Fixed "Use Cursor Settings" button in Still Export View not
  correctly transferring Truelight settings [bug 48871]

* Fixed quoting of strings sourced from Media Decode Parameters
  [bug 49040]

* Fixed a crash after recalling a group with shot(s) no longer in the
  timeline and turning the grouped grading on [bug 48180]

* Fixed Smart Paste and Smart Paste Grouped when the selected strip
  was a matte [bug 48048]

* Clip wrapped AES and BWF audio in MXF can now be read, and decode
  performance of clip wrapped audio has been improved [bug 49188]

* Creative LUT files which are referenced by R3D movie files and are
  in the same folder as the R3D files are now copied when the R3D
  files are copied or consolidated [bug 49021]

* Fixed flickering status messages sometimes seen at the top of file
  browser columns [bug 45373]

* Menus with submenus are now positioned to the left of their parent
  menu if they're too close to the right edge of the screen [bug 9785]

* Grid Warp Blackboard Overlay button now disables only the Grid Warp
  Overlays [bug 48892]

* Enabled resizing of Shots View columns Tint, Length, Event, and 
  Thumbnail [bug 46322]

* Fixed poster frame positions not being copied when pasting
  [bug 49270]

* Fixed failure to load scenes after updating an OFX plugin to a
  version that no longer uses one or more parameters [bug 49305]

* Fixed crash when doing a blackboard paste or an Apply on a empty 
  location in the timeline [Bug 48756]

* Fixed appearance of open scenes in Job Manager [bug 40018]

* Fixed corruption seen when decoding 6054-pixel width Sony VENICE
  media at half-resolution [bug 48358]

* Fixed crash when setting render filename template to some unusual
  values [bug 48929]

* Fixed creating of /vol/images symlink on macOS [bug 49172]

* Fixed incorrect reading of OpenEXR files which have a Display Window
  that is the same width as the Data Window, but a shorter height,
  when using the Data Window as the Input Format [bug 49275]

* Fixed issue with paint picking selecting the wrong colour due to
  the viewing format being different [bug 49210]

* Removed non-functional preference "Swap Next/Prev Cut/Poster
  Controls." In order to do this, use the menu entry in Navigate menu
  instead [bug 49152]

* Fixed "Sequence types cached in input strips" preference for ARRIRAW
  and Sony RAW [bug 49150]

* Fixed Job Manager crash which could occur if one chose
  "Sort Jobs by Size" before any jobs had been shown [bug 49298]

* Fixed BaseGrade's Contrast having no effect below 0.5 and above
  1.5 [bug 42255]

* Removed restrictions on gallery job and scene names - Upper case
  characters and periods can now be used. This also fixes the issue
  where using %J in the Gallery Job didn't work properly if a job name
  contained upper case characters [bug 47045]

* Fixed missing "Snapshot" text on the image when a snapshot has been
  taken [bug 46149]

* Fixed potential hang when jumping to previous poster frame 
  [bug 47867]

* Fixed failures when DRT cube files are stored in subfolders in
  /vol/.support/etc/colourspaces [bug 49418]

* OFX operators and Shader operators with optional inputs can no
  longer be 3D-split in a stereo scene, to prevent crashes [bug 49429]

* Changed lower limit of UI font size preference [bug 49358]

* Scratchpad grab and recall now obey the copy and paste protect 
  categories [bug 35792]

* Fixed potential crash when deleting a mark/strip category
  [bug 40235]

* Fixed "Legal to Full Scale" option on Sequence being incorrectly
  cleared when changing the sequence [bug 49272]

* Fixed frame numbers reported in "Scene has sections that have not
  been analysed for Dolby Vision" error when exporting Dolby Vision
  XML [bug 49184]

* Fixed failures in Cuts View when using some OFX plugins on a system
  with a low-VRAM UI GPU [bug 49431]

* Increased maximum sensitivity of trackballs, trackball rings, and 
  encoders to 5 to allow for greater freedom when adding acceleration
  and normalised Tangent gearings to better match the Blackboard 1,
  Blackboard 2, and Slate [bug 48310]

* Fixed incorrect assignment of %C when a file path uses a longer
  folder name (e.g. with the container set to /vol/abc and using media
  from /vol/abc-2) [bug 49594]

* Fixed aspect ratio metadata written to Avid OP-Atom MXF files which
  are neither 4:3 nor 16:9 shaped [bug 49553]

* Fixed an issue where the interlaced XAVC frame rates available for
  rendering were doubled due to a discrepancy between Sony and
  FilmLight notation. Supported interlaced XAVC operating points are:
  1920x1080:
  - XAVC HD Intra Class100 @ 25i, 29.97i
  - XAVC HD Long422 25     @ 25i, 29.97i
  - XAVC HD Long422 35     @ 25i, 29.97i
  - XAVC HD Long422 50     @ 25i, 29.97i
  [bug 49591]

* Ensure any unused categories in a scene are deleted when clearing
  that scene's undo history [bug 48822]

* Fixed issue which caused clip lengths to be calculated incorrectly
  when updating an AAF [bug 49554]

* Fixed appearance of burnin text when the Viewing or Render Format
  has a different pixel aspect ratio from that of the Working Format
  [bug 48425]

* DCI compliant JPEG 2000 essence will now be created using the
  maximum allowed number of DWT decomposition levels. This fixes an
  issue where the GPU accelerated JPEG 2000 encoder would use fewer
  DWT decomposition levels than the non-accelerated encoder, and also
  means that 4K essence will now use 6 levels instead of 5
  [bug 49616]

* Added diagnostic support for Adaptec 315x series raid controller.
  These controllers also need Flos 6.4.11159 or later [bug 49476]

* DCI compliant JPEG 2000 essence using a bitrate too close to the
  limit of 250 Mbit/s can cause issues with some DCP players. To
  accommodate this, the default bitrate of this essence has been
  reduced by 2%. Control of the bitrate of DCI compliant J2C files has
  been improved and it can now be manually specified [bug 49433]

* Fixed crash when resetting a legacy DNG Parameters operator
  [bug 49443]

* Connecting removable media while FLUX Manage is open now opens a new
  browser tab rather than changing the current one [bug 48806]

* Improved the description of H.264- and HEVC-encoded source media in
  QuickTime containers. Bit depth and subsampling information is now
  part of the source description. AVC Profile and AVC Level metadata
  entries are now added when available [bug 49638]

* No longer crash when conforming some CMX3600 EDLs with overlapping
  strips, instead attempt to resolve the strips into multiple tracks
  [bug 49507]

* When picking from the image the colour panel and colour well will
  interactively update [48938]

* Fixed crashes in Audio Waveform View when audio media has more than
  16 channels [bug 46662]

* Added an option to Timeline Sort View to simplify a scene so that it
  is able to be opened by Daylight. This option can also check if a
  scene is able to be opened by Daylight [bug 45848]

* Fixed occasional crash when importing BLG resources [bug 47627]

* bl-shots no longer fails when used on a scene containing an unknown
  OFX operator [bug 47133]

* Fixed incorrect behaviour when double-clicking on a tile in the FLUX
  Manage tile library [bug 47136]

* Fixed tooltip on the Input Colour Space control [bug 47143]

* Fixed crash when scrubbing the timeline very quickly [bug 48303]

* Fixed potential crash after deleting a Slate layout from Chalk 
  [bug 45642]

* Fixed issue with the stereo split button still being active in a
  read-only scene [bug 46510]

* Fixed recognition of 60@30 fps drop-frame, 50@25 fps and 48@24 fps
  timecodes in MXF media [bug 49685]

* Fixed failure to correctly update a Sequence's DRT when importing a
  BLG [bug 47020]

* Fixed an issue causing thumbnails to not be displayed on the first
  run after installing a licence. Services are now restarted after
  installing a licence [bug 46668]

* Fixed mattes being too bright when set to "Use Viewing Colour Space
  White Point" and viewed in an HDR Viewing Colour Space [bug 47046]

* Fixed bug preventing some UI elements (like ganging state, 
  extended ranges etc) from being restored when a grade is stored
  as a BLG and then recalled [bug 45632]

* The handling of MXF indexes and partitions has been
  restructured. This fixes an issue where MXF-files with many
  partitions could be slow to open. It also adds decode support for
  some previously unsupported MXF flavours, e.g. AS-11 [bug 34020]

* Fixed issue with Chalk for Slate when importing from a file would
  wipe all non-Home customisation [bug 45705]

* Fixed issue with temporal operators and rendering at frame rates 
  that are different to the scene's working frame rate [bug 46781]

* Fixed issue causing variable retime option to be missing when
  conforming from FCP7 XMLs [bug 49709]

* Fixed issue affecting Blend Controls on Blackboard and Slate
  [bug 46604]

* Improved naming on some blackboard and slate buttons [bug 45840]

* Added function to rename Chalk layouts [bug 46042]

* Added Blackboard and Slate action to reset the Matte XYZ [bug 46731]

* Added Blackboard and Slate actions to reset and select the Matte 
  Sequence and Matte Reference operators [bug 47028]

* Corrected the text display when adding an "Insert Layer" button to 
  the Slate using Chalk [bug 47071]

* Support nvme-based cache on Z840 (as a replacement for SSD cache)
  [bug 49629]

* Fixed a reference issue in the context of a composite layer.
  A reference could not point at any foreground layer when the
  foreground layer 0 was a reference itself (e.g Alpha reference or
  Dkey reference) [bug 46441]

* Fixed rendering of 4:2:2 Apple ProRes movies when zooming
  [bug 49623]

* Lowered the sensitivity of encoders to make them more user
  friendly [bug 37298]

* Removed the Default Stack Colour Space option from Scene Settings
  because using it incorrectly can easily cause errors in colour
  pipelines [bug 49772]

* Improved the behaviour of some OFX plugins using dialogs (e.g.
  Sapphire Preset Browser) [bug 34954]

* Fixed failure of DRTs which use other cube formats [bug 49628]

* Fixed bug which meant that only one GPU was used on a Mac with
  multiple GPUs, if the Mac was configured as a 'ws' in its cloud.cfg
  [bug 49618]

* Fixed missing Shot Timecode metadata for Audio Renders when audio
  file is specified as Scene Audio in Scene Settings [bug 49674]

* Improved Colour Space Journey View for OFX operators [bug 49695]

* Fix crash in paint operator with non-existent matte resource 
  [bug 46095]

* Fixed occasional crash in Multi-Paste with weird stack morphologies
  [bug 48409]

* Fixed FLUX Manage failing to cache thumbnails [bug 49856]

* Fix 'Bind Failures' in Denoise using the optical flow option. It
  will only have an effect in newly created operators [bug 47091]

* Fixed performance issues when using Truelight cubes (in Cursor View
  or a Truelight operator) located in folders with very many cube
  files [bug 49909]

* Fixed an issue where the "Legal to Full Scale" option on Sequence
  could be incorrectly set when reading MXF-files with certain
  transfer functions, notably "Rec.709" [bug 49952]

--------------------------------------------------------------------------

Baselight Release 5.1.11140 (2018-11-13)

New Features Since Baselight 5.1.11047
베이스라이트 5.2.11047 이후 새로운 기능 
======================================

Miscellaneous 기타 
-------------

* New "Export SDL Data" option in EDL Export to write StereoGrade
  parameters as SDL metadata in CMX 3600 files [bug 26152]

* Added "LUTN.Filename", "LUTN.Path" and "LUTN.RelPath" variables
  to Shots view, where N is an index representing the Truelight
  operator found within the shot.

  The index N will be 0 for the Truelight operator in the Input layer.
  The index N will be 1 or above for each Truelight operator found in
  the grading stack below the Input layer.

  LUTN.Filename will give the base filename of the LUT.

  LUTN.RelPath will give the path to the LUT relative to the scene's
  current container directory.

  LUTN.Path will give the full path to the LUT [bug 49344]

* Added support for Quadro P4000, P5000 and P6000 display GPUs
  [bug 49495]

Bug Fixes Since Baselight 5.1.11047
베이스라이트 5.2.11047 이후 버그개선
===================================

* Fixed bl-config-xorg tablet mapping for Blackboard ONE [bug 48888]

* Fixed incorrect colours in Phantom Cine files which do not have a
  recorded colour temperature [bug 49236]

* Fixed an issue where the coding equations tag could be omitted from
  MXF metadata when rendering XAVC codecs. This affected renders which
  produced the warning 'Unable to move index to header' [bug 49297]

* Fixed connection failure when rendering with remote server with
  a user id that does not exist on the server [bug 49309]

* Fixed rare crash on database access [bug 49169]

* The application will now report an error rather than crash on certain
  corrupt scenes [bug 49377]

* Full-sensor resoltions are no longer offered as Input Formats for
  Sony RAW media, because the Sony RAW SDK cannot decode at these
  resolutions [bug 49241]

* Fixed issues when using a Baselight TRANSFER licence [bug 49251]

* Scenes using a cube-based DRT or Dolby Vision Software CMU no longer
  invalidate the timeline cache on every new build [bug 49187]

* Fixed memory leak when repeatedly opening/closing scenes [bug 49367]

* Fixed issue where changing the timecode setting for Audio Metadata
  in the Render panel would not change the timecode embedded in
  rendered audio files [bug 49393]

* Fixed issue where a separate audio file associated with a shot would
  repeat at the end of the shot if the audio file was shorter than the
  movie or image sequence [bug 49404]
* Fixed crash reading HDE-compressed ARRIRAW media on multi-GPU
  systems [bug 49405]

* Fixed issue conforming from R3D files that could cause the conform
  percentage to drop and alternative options to be offered for some
  events [bug 49408]

* Fixed Render View "Prefer Source Codec" button becoming disabled
  after selecting it [bug 49416]

* Fixed crash when an invalid Dolby Vision licence file is installed
  [bug 49391]

* Fixed issue with the cut view displaying the wrong thumbnails when
  a reverse sort order was selected in the shot view [bug 46383]

* Fixed file descriptor leak if a port scanner is run on a Baselight
  system [bug 49432]

* Fixed incorrect colours in some FLUX Manage thumbnails [bug 49236]

* Fixed Stereo Dual Output display option [bug 49485]

* Fixed Shader operator failing in Baselight CONFORM. Unfortunately,
  Shader operators added in Baselight 5.1.11047 will remain broken and
  will need to be re-inserted in the newer build [bug 49517]

--------------------------------------------------------------------------

Baselight Release 5.1.11047 (2018-10-05)
베이스라이트 릴리즈 5.2.11047 버전 

New Features Since Baselight 5.1.10917
베이스라이트 5.2.10917 이후 새로운 기능 
======================================

* Added new Overlay Grids for Luma Waveform and YCbCr parade to
  display the luminance in cd/m2. Five new overlays are available to
  adapt the spacing of the luminance grid for specific use cases and
  customer needs:

  - nits base2
    This mode will draw lines at every stop (twice the luminance)

  - nits base10 - 1
    This mode will draw lines for every order of magnitude (0.1, 1,
    10, 100 etc) and one divider line between these steps

  - nits base10 - 2
    Same as "nits base10 - 1" but with two divider lines

  - nits base10 - 3
    Same as "nits base10 - 1" but with three divider lines

  - nits base10 - Perceptual
    Same as "nits base10 - 1" but with approximated perceptual
    equidistant steps. That means it will draw fewer divider lines in
    the low luminance range and more in the high luminance range

  In addition lines are always drawn for the creative-, clip- and
  peak-white luminance levels of the selected viewing colour space
  [bug 46999]

* Added Balance Offset function to CDL Grade, which allows a colour
  picked from the image to be made neutral [bug 30497]

* Added "Colour Space of Rendered HDR Media" option when exporting
  Dolby Vision XML, to support workflows where the Dolby Vision
  Mastering Display is P3/D65 but the rendered HDR media is Rec.2020
  [bug 48895]

* Added "Linked Property" setting for columns in Shots view. This
  allows you to configure a bi-directional link between a column in
  Shots view and decode parameters. For example, if you set the
  "Linked Property" setting for a column to "ARRIRAW.WhiteBalance",
  the White Balance value will be available via the column, and any
  changes to the value in the column will be propagated back to the
  White Balance parameter of the ARRIRAW Params operator.

  This allows decode parameters to be transferred between scenes,
  or updated via EDL/ALE, using the Multi-Paste view [bug 49059]

* Added a Subsequence tile to FLUX Manage, which is shown when Mark
  In/Out has been used. This tile allows subsequences to be copied,
  deleted etc [bug 44863]

* It is now possible to drag from the Non-media files list in FLUX
  Manage [bug 41928]

* Baselight can now connect to PostgreSQL services using a PostgreSQL
  service name. Just use the service name instead of a host name in
  the Job Manager etc. PostgreSQL service definitions can include
  alternate ports, login credentials and so on. They are useful
  when using SSH tunnels to connect to remote database servers. An
  example minimal .pg_service.conf file could contain:

  [my_tunnel]
  host=localhost
  port=54321

  This would be useful if the local port 54321 is tunnelled to some
  remote system. With this in place, using "my_tunnel" instead of
  a regular host name would allow Baselight to connect through the
  tunnel to the remote server.

  For more details on the .pg_service.conf file format, see the
  PostgreSQL documentation, "The Connection Service File", at
  https://www.postgresql.org/docs/9.2/static/libpq-pgservice.html
  [bug 48920]

* Added the ability to export BLGs containing only the operator
  values for the current eye. In addition, added %e and %{Eye}
  substitutions to BLG Export to allow the eye name (L/R) to be
  included in the filename [bug 49087]

* Added a new operator to the Matte Tool called "Edge Filter". This
  is designed primarily for use on keyer derived mattes and can be
  used to restore low frequency detail from the keyer's source image.
  It is particularly helpful with contours and hard keys, where it
  can help bring back edge gradient levels from the original image.

   The Edge Filter has 2 controls:
    - Radius: determines how localised the treatment should be
    - Blur:   controls how much smoothing needs to be done
   [bug 49082]

Bug Fixes Since Baselight 5.1.10917
베이스라이트 5.2.10917 이후 버그개선 
===================================

* Fixed issue with incorrect Time Reference value calculation in
  Broadcast WAV metadata when writing WAV files [bug 48876]

* Fixed an issue where AAC-encoded audio in MP4-files could fail to
  decode at the end of the file [bug 48835]

* Fixed failure to apply Software CMU to Secondary Output when the
  primary output is not also using Software CMU [bug 48857]

* Fixed issue causing slow down when scrolling through shots in Cuts
  View with Try held down [bug 48854]

* Fixed incorrect timecode handling when using QuickTime movies with
  timecodes that cross midnight [bug 48647]

* Fixed DPX image corruption when writing to an SMB share from OSX
  [bug 39929]

* Fixed behaviour of multi-stage Shader operators that distort or blur
  the image, when using a viewing format whose mapping uses an area
  smaller than the entire input image [bug 48951]

* Fixed crash when displaying error message as burnin text [bug 47605]

* Fixed crash when tracking with YCrCb 420 scene format [bug 48466]

* Fixed arbitrary failures of Modify AAF render [bug 48919]

* Fixed failure when viewing a gallery grab of offline media which was
  grabbed from a Sequence whose Input Format was a crop [bug 48467]

* Fixed issue with playback due to picking being enabled in some 
  operators [bug 45876]

* Fixed failure to correctly switch versions of flux and/or render
  services when operations in the queue require a different
  application version [bug 48524]

* Fixed an issue where audio could fail to read from trimmed ALEXA
  mini MXF-files [bug 48982]

* Fixed "CL_OUT_OF_RESOURCES" errors when decoding R3D and Canon RAW
  media [bug 47669]

* Fixed Job Manager sometimes starting with blank columns [bug 45113]

* Fixed errors in FLUX Manage when attempting to copy a file with a "
  in its filename [bug 48832]

* Fixed 1 pixel jumps observed when editing blurred mattes [bug 48983]

* Fixed occasional hang when using Sony RAW media [bug 48769]

* Fixed artefacts that can appear at the edges of Shader operators,
  particularly when their output is blurred. Note that this fix only
  applies to newly-inserted Shader operators; existing scenes are
  unchanged unless you re-insert the Shader operator(s) [bug 48950]

* Fixed crash in Nuke script generation which would occur if the 
  filename of the generated BLG didn't end in ".blg.exr" [bug 48401]

* Fixed issue with fl-config-master attempting to restart disabled
  service [bug 48569]

* Fixed FLUX Manage showing out-of-date thumbnails for files which
  have been overwritten [bug 49096]

* Fixed crash when conforming from cloud media [bug 49075]

* Fixed errors in Dolby Vision display menus that could occur when
  using a Hardware CMU [bug 48855]

* Improved error reporting in "Database access" diagnostic [bug 49078]

* Improved Job Manager connection time & reliability [bug 46456]

* Fixed bug with audio channel mapping not refreshing correctly
  when creating new channel mappings or deleting existing channel
  mappings via the Edit Channel Mappings window [bug 49132]

* Increased disk cache maximum size [bug 49154]

* Fixed issue with Dual Colour Space Layout outputs becoming
  unsynchronised during playback when using the option to show
  scopes/histogram from the secondary output [bug 48850]

* Fixed the command line conform tool 'bl-conform', the diagnostic
  option '-v' could cause it to fail with an error [bug 49140]

* Fixed occasional assertion in layout by converting it to a
  diagnostic message which will hopefully help narrow down the
  cause [bug 49216]

--------------------------------------------------------------------------

Baselight Release 5.1.10917 (2018-09-03)
베이스라이트 릴리즈 5.1.10917 버전 

New Features Since Baselight 5.1.10836
베이스라이트 5.1.10836 이후 새로운 기능 
======================================
 
* Added option to Scene Settings and Setups to control the Stack
  Colour Space of newly-inserted Sequence operators [bug 48555]
 
* Added options to export and import Global Formats from the formats
  editor [bug 43895]
 
* Basic cursor synchronisation is now available to remote grading
  sessions. The cursor position and render layer are mirrored, as well
  as play state, play speed, loop mode and shot filtering settings.
  Nothing is required to enable this feature, it is automatic when a
  scene is opened in follow-mode [bug 41583]
 
* Updated to Canon RAW SDK 2.2. This adds support for Canon C700 FF
  media [bug 46472]
 
Bug Fixes Since Baselight 5.1.10836
===================================
 
* Fixed Dolby Vision Software CMU not being applied when rendering
  more than 500 frames [bug 48612]
 
* Fixed poor quality of ProRes 4:4:4 media when decoded at optimised
  half-resolution (note that existing Sequence operators in scenes
  will not change behaviour) [bug 48581]
 
* Fixed unpredictable crash in FLUX Manage [bug 48418]
 
* Fixed Shader operators losing optional inputs when split or pasted
  [bug 48407]
 
* Fixed crash when using a bad BLG that refers to an unknown colour
  space [bug 45693]
 
* Fixed crash when updating the tracker controls in shapes [bug 48043]
 
* Prevent shapes from setting up the state of the 'selected track only'
  button during navigation to the tracker strip [bug 48613]
 
* Fixed behaviour of Shader operators that distort or blur the image,
  when using a viewing format whose mapping uses an area smaller than
  the entire input image [bug 48788]
 
* Fixed an issue where some XDCAM encoded MXF files written by Avid
  software were decoded with blocky artefacts [bug 48796]
 
* Fixed crash within paint when switching to All Strokes tab after a
  reset [bug 48558]
 
* Fixed crash when conforming for Tape Ingest [bug 48594]
 
* Added a diagnostic preference to override the number of nvme cards
  expected [bug 48527]
 
* Fixed errors in dissolves in Dolby Vision XML export when using
  Record Timecode numbering [bug 48811]
 
* Fixed incorrect use of P3 D65 colour space in Dolby Vision XML when
  using a Rec.2020 Dolby Vision Mastering Display [bug 48791]
 
* Fixed issue that caused keyboard and mouse input to be ignored
  during playback in some situations [bug 48587]
 
--------------------------------------------------------------------------

Baselight Release 5.1.10836 (2018-07-31)

Bug Fixes Since Baselight 5.1.10830
===================================

* Fixed "Remote root access" diagnostic to allow hostnames containing
  hyphens [bug 48586]

* Fixed Modify AAF rendering [bug 48585]

--------------------------------------------------------------------------

Baselight Release 5.1.10830 (2018-07-27)
베이스라이트 릴리즈 5.1.10830 버전

New Features Since Baselight 5.1.10720
베이스라이트 5.1.10720 이후 새로운 기능 
======================================

Dolby Vision Software CMU 돌비비젼 소프트웨어 CMU
-------------------------

* Dolby Vision content mapping is Dolby's technology for mapping HDR
  images for SDR displays. Until now grading with Dolby Vision has
  required the use of a Dolby Vision Content Mapping Unit (CMU)
  connected to the SDI stream, and rendering SDR deliverables using
  Dolby Vision has required command-line tools.

  Now, the content mapping can be applied inside Baselight during
  grading, playback and rendering. This functionality is known as
  "Software CMU".

  An additional licence must by purchased from Dolby in order to allow
  the trim controls in the Dolby Vision Trim strip to be adjusted when
  using the Software CMU.

  Scene Settings View (on the Format & Colour tab, Dolby Vision section)
  allows a scene to be set to use the Sofware CMU. Once this is done,
  the Cursor View's Viewing Colour Space menu shows (at the top) the
  colour space of the Dolby Vision Mastering Display and of each Dolby
  Vision Target Display. Choosing a Target Display will cause the
  Software CMU to be used to convert to the SDR colour space instead
  of Baselight's normal colour pipeline. The Colour Space Journey View
  updates to show what is being done.

  The Render Colour Space menu on Render View shows the same new
  colour space options.

  If a Mask is selected on Cursor or Render View, the Software CMU is
  only applied within the masked area [bug 44614]

Other Dolby Vision Changes 기타 돌비비젼 변화 
--------------------------

* The Dolby Vision strip has been replaced by separate Dolby Vision
  Analysis and Dolby Vision Trim strips, for clarity and to prevent
  issues caused by copying and pasting strips [bug 48199]

* Dolby Vision analysis is now always automatically performed in the
  appropriate colour space; there is no longer any need to change the
  cursor's viewing colour space before analysis.

* Changing a scene's Dolby Vision Mastering Display to one with a
  different brightness invalidates all analysis data stored in its
  Dolby Vision Analysis strips, requiring them to be re-analysed.

* Analysis numbers ("L1") are now shown on the Dolby Vision Analysis
  operator UI, to assist troubleshooting.

Dual Colour Spaces Layout 듀얼 컬러스페이스 레이아웃 
-------------------------

* When using dual outputs from an AJA card or combiner, the Display
  menu now offers Dual Colour Spaces Layout. In this layout, the two
  video outputs each show the current cursor, but using two separate
  viewing colour spaces. The viewing colour space for the secondary
  output is chosen on Cursor View.

  When using this layout, Cursor View also allows you to select which
  video output is used for Histogram View, the various Scopes Views
  and Colour Space Journey View.

  This layout is particularly useful when combined with the Dolby
  Vision Software CMU, as it allows you to:

  - connect the HDR mastering display to one output and an SDR target
    display to the other output, and view both the HDR and SDR
    versions at the same time

  - connect two different target SDR displays so you can refer to one
    SDR trim while adjusting the trim for the other target display

  - connect two identical target SDR displays so you can compare
    Baselight's DRT-based SDR version of an HDR scene with the Dolby
    Vision Software CMU version

  This layout could also be used with a hardware CMU, sending the
  mastering HDR image to the CMU and showing another colour space on
  the other output.

  In this layout, the timeline is cached for both colour spaces.

Miscellaneous 기타 
-------------

* Added Audio Codec Parameters to Render view. These codec parameters
  can be modified in the same way as Codec Parameters for movie
  codecs, and are presented for any audio file types & codecs that
  support parameters [bug 46438]

* Added support for writing Broadcast WAVE header information into
  rendered WAV audio files.

  The Broadcast WAVE header is populated with:
    - origination date & time
    - origination reference containing FilmLight software version used
      to render the audio file
    - timecode that matches the record timecode of the source scene
    - description field, that can be specified via the Audio Codec
      Parameters in the Render View. The "BWAV Description" codec
      parameter is a string that can include standard variable names
      like %{Scene} or %{Job}.

  Any variables in the BWAV Description parameter will be substituted
  when the audio file is rendered [bug 46438]

* Added support for selecting which timecode to embed when rendering
  audio files. This option is available when rendering "Audio Only" or
  "Sequence + Audio".

  You can select from the following options for the timecode embedded
  in the audio file:
    - Record Timecode : Timeline timecode
    - Shot Timecode : Source Timecode of the shot
    - Audio Timecode : Audio Tiemcode of the shot
    - File Timecode : Audio Timecode from source audio file

  The audio timecode can be specified via the bl-render command line
  using -atc option [bug 46438]

* Added %{Host} and %{Zone} as variables which can be used in Text
  operators, burnins, render filenames and audio metadata.

  %{Host} : the database server that contains the scene being rendered
  %{Zone} : the machine that is performing the rendering  of the scene

  NOTE: If you submit a render to a remote render queue, the remote
  system's zone name will be used for the Zone variable [bug 46438]

* Updated the Sony RAW SDK to version 3.1.0, which adds support for
  reading X-OCN 4K 6:5, 6K 17:9 and 6K 1.85:1 bitstreams [bug 47819]

* Added option to apply stereo grade data to both eyes simultaneously
  during conform [bug 47694]

* Added support for reading HDE-compressed ARRIRAW files (.arx)
  [bug 47699]

* Updated to RED SDK 7.0.7. This contains some bug fixes and improves
  load times for R3D clips recorded on newer sensors and camera
  firmware [bug 47797]

* Reduced snap size of ARRIRAW Params White Balance parameter from 100
  to 25 to allow more precise White Balance adjustments [bug 48287]

* Added support for reading Input Format from ALE during EDL Import.
  If an "Input Format" column is present in the ALE, the option to
  "Use Input Format from EDL" will be shown in the EDL Import window.

  When this option is set to "Yes", EDL Import will attempt to use the
  named format as the Input Format when conforming the event against
  source media. If the named format is not one of the possible formats
  that can be used for the matching source material, a warning will be
  added to the EDL Import window for the event [bug 48241]

* Added ability to import keycode from an ALE [bug 48141]

* Changed the EDL Import view's container handling to match FLUX
  Manage. Now, if the search directory for a conform lies outside the
  current container, a dialog will pop up offering a range of possible
  containers based on the search directory. This will occur even if
  the search directory isn't on a filesystem mounted under /vol
  [bug 46364]

* Files rendered by Baselight or copied by FLUX Manage now respect the
  umask of the user who submitted the render/copy [bug 44569]

* Added "Apply Exposure Index" option to Sony RAW Params, to allow the
  exposure to match files rendered from Sony's RAW Viewer application
  which doesn't apply the Exposure Index [bug 48383]

* Added "Has Speed Change" column in Shots view. This will show any
  shots that have an Increment value other 1.0, where the frame rate
  of the shot does not match the scene, or any shot that has a Retime
  operator. It can be used as a filter in Shots view to identify shots
  which do or do not have any speed change [bug 48420]

Bug Fixes Since Baselight 5.1.10720
===================================

* Fixed image corruption with OFX plugins, especially when using a
  transform after the OFX operator [bug 46111]

* Fixed image corruption with Shader operators, especially when using
  a transform after the Shader operator [bug 41601]

* Fixed an issue where AVC-Intra MXF files using the Panasonic V-Log
  colour space incorrectly set the 'Legal to Full Scale' option by
  default [bug 48177]

* Added View, Try and Apply hotkeys to the keyboard. View is ';' Try
  is '/' and Apply is '@'. Note that Align Timeline has been moved to
  'ctrl + ;' now [bug 31910]

* Fixed issue with pasting layer 0 not taking all the correct colour
  space parameters [bug 35459]

* Fix a "Object Id 0 is out of range" error when upgrading 4.4m1
  scenes [bug 48197]

* Fixed a rare crash that could occur when recovering a scene that
  was upgraded from 4.4m1 [bug 48428]

* Enabled drag and drop from the gallery layer view [bug 46315]

* Added option in copy and paste menu to turn off pasting of colour
  space information in the layer 0 paste [bug 47129]

* Fixed an issue with sudoers configuration [bug 48201]

* Fixed crash exporting a LUT from a stack containing spatial
  operators [bug 48095]

* Fixed render service on a FLUX Store not using all available GPUs
  [bug 48121]

* Prepare For Review now correctly uses the colour space and proxy
  resolution settings of the currently-open cursors [bug 43435]

* Fixed crash writing stereo ALE with no clip name metadata
  [bug 48111]

* Greater accuracy in variable retimes from Premiere XMLs, particularly
  when velocity ramps are used [bug 47962]

* Fixed crash when clips that are ignored during EDL import have
  effects applied to them [bug 44350]

* Fixed keyframing issues when applying SDL events from .edl files
  during conform [bug 47697]

* SDL data in .edl files with no valid events no longer causes a crash
  [bug 48217]

* Increased the responsiveness of the Tangent Element MF trackball
  ring [bug 48280]

* Improved reporting of errors in fl-service [bug 44643]

* Fixed flux and render service processes continuing to run after
  installing a new Baselight/Daylight build or using fl-vers to switch
  the current build [bug 48155]

* Fixed bug in BLG export/Update Avid AAF with Baselight Grades which
  caused the behaviour of a ColourSpace operator to change if it was
  set to convert to the scene's Working Colour Space [bug 47919]

* Fixed issue on multi-GPU systems with JPEG 2000 where too much GPU
  memory was set aside for rendering [bug 48050]

* Fix bug parsing frame offset in keycode from ALE [bug 48297]

* The tracker strip will display and track all trackers by default.
  This behaviour can be changed to track and display only the selected
  tracker using the (persistent) "Selected Tracker Only"
  button/setting [bug 48114]

* Fixed appearance of the Frame Rate menu in Sequence [bug 48356]

* Fixed an issue that could cause decode failure of Sony RAW MXF files
  on upgraded scenes [bug 48369]

* Sony RAW media now shows ISO metadata [bug 48383]

* Fixed issue that prevented USB audio devices from being used at
  44.1kHz sample rate [bug 47663]

* Fixed reading RGB and greyscale Phantom cine files [bug 48390]

* Fixed failures when copying MXF movies with linked audio and video
  files [bug 48406]

* Fixed filtering based on floating-point value columns in Shots view
  [bug 48429]

* Fixed failure in "bl-render -set" [bug 48450]

* Errors in /vol automounting are now logged [bug 48459]

* The first diagnostic run after installing a new build will now run
  the "daily" diagnostic tests, and will not ignore any warnings that
  were previously ignored [bug 48476]

* Fixed bug to pass through audio track names when track number is 
  larger than number of channels in audio file [bug 48489]

* Fixed timecode metadata read from OpenEXR files having an incorrect
  "Timecode" metadata string [bug 48501]

* Diag "GPU texture test" is now multi-gpu aware [bug 47235]

* Fixed failure to decode ARRIRAW media between 4321 and 5120 pixels
  wide on a Linux system with a 3GB GPU (e.g. GTX 780). This media is
  now decoded on the CPU [bug 48462]

* fl-make-secure script creates ssh configuration files if necessary
  [bug 48530]

* Fixed ssh connection diagnostic [bug 48198]

* Fixed fl-make-secure syntax error expanding hosts/* directory names
  [bug 48529]

* Fixed pre-render hanging in some queued renders [bug 48460]

* Fixed crash when the user's group list has many group IDs longer
  than 7 digits [bug 48541]

* Updated flos-tools package to add support for 6.4TB nvme. Also
  includes minor fixes to fl-config master and fl-setup-raid to
  require a reboot if nvme sector size is changed, and to connect to
  other hosts in the local zone using ssh instead of rsh [bug 48411]

* Added nvme support to dpm command [bug 47142]

--------------------------------------------------------------------------

Baselight Release 5.1.10720 (2018-06-19)

New Features Since Baselight 5.1.10637
======================================

* Added a "Pick" button to Blackboard, Blackboard 2 and Slate desks.
  This mirrors the "Pick" toggle in the BaseGrade user interface. It
  will appear next to 'Ext Rng' in the operator-specific area of the
  desk when the BaseGrade operator is selected [bug 45489]

* In Chalk for Blackboard 2 and Chalk for Slate, import/export of desk
  layouts to USB is now handled via the "Load..." and "Save As..."
  dialogs. To import a desk layout from USB, click "Load...", select
  the drive from the volumes drop-down, then locate and open the
  layout file. To export, click "Save...", select the drive as before,
  choose a save location and click OK [bug 46405]

* MXF files containing audio tracks which are linked to an MXF video
  file are now added to an Audio operator when the video is inserted
  into a scene from FLUX Manage. This also applies to audio files with
  the same name as the first frame of an image sequence, e.g. an audio
  file 000100.wav will be added when it is found alongside an image
  sequence starting 000100.dpx [bug 47800]

* Added an IPP2 tab to R3D Params, which contains controls for these
  recently-added settings:
  - Exposure Adjust
  - Tone Map
  - Highlight Roll Off
  - HDR Peak Nits
  - CDL [bug 46379]

* bl-render -set can now be used without -queue to perform a
  multiple-deliverable render on the command-line [bug 47896]

* In the "Update Avid AAF with Baselight Grades" EDL Export panel,
  the "Input Video LUT" option has been renamed "Input Legal to
  Full Scale" to match what the setting is called in full Baselight.
  The options have also been changed:
    "No": No legal to full scale will be applied.
    "Leave Unchanged": The state of the "Legal to Full Scale" toggle
      in the Sequence operator will be left unchanged (the default).
    "Yes": A legal to full scale will applied.
  [bug 47766]

* Added new "Quick Guide" documentation to the Help menu [bug 47990]

* Added ability to read input "Legal to Full Scale" values from BLG
  payloads when applying Baselight Grades from AAF files [bug 47807]

Bug Fixes Since Baselight 5.1.10637
===================================

* Fixed copy operations hanging in the Operations Queue when the
  application build used to submit the operation is not installed on
  the system hosting the queue [bug 47770]

* Add support for upgrading Adaptec firmware on Gen VII deskside
  [bug 47726]

* Adaptec raid diagnostic now warns instead of failing if an array is
  degraded [bug 45932]

* Fixed Params operators not working if used in a layer containing no
  other active operators [bug 47803]

* Fixed an issue where 3X10 DPX files written by Scanity would
  incorrectly identify as being 1X10 DPX-Y after being copied by fl-cp
  [bug 47809]

* Fixed burnin text opacity [bug 47404]

* Fixed an issue where some XDCAM MXF files were not properly
  recognised, resulting in the error message 'Unindexed movie'
  [bug 47732]

* Creating a new cursor now correctly copies the quality (max quality,
  optimised, draft) of the previous cursor [bug 46334]

* The overlay colour set on Cursor View is now saved and restored with
  the scene/job cursor settings [bug 46146]

* Added logic to detect and improve performance of incorrectly indexed
  XDCAM MXF-files created by Avid software [bug 47000]

* Fixed an issue where a crashing movie reader could sometimes cause
  the application to hang [bug 46916]

* Fixed multipasting of Circle Take Metadata [bug 45868]

* Fixed Scratchpad "Original Version" toggling when playback filtering
  enabled [bug 46356]

* Fixed issue causing some sequences not to be recognised during AAF
  import [bug 47748]

* Fixed a crash during EDL import when "Add extra metadata" is enabled
  [bug 45666]

* Fixed renderer crash when updating xml files with an empty <pathurl>
  element [bug 45285]

* Allowed the user to enable the Layer Matte rendering mode (in the
  cursor view) in a read only scene [bug 38443]

* Fixed sudo diagnostic failure when custom rules are added to
  /etc/sudoers [bug 47836]

* Fixed occasional crash in BaseGrade "Match" picks [bug 47841]

* Improved scene database compaction [bug 47708]

* Improved smoothness of scene open progress panel [bug 47704]

* Fixed occasional delays in screen updates on Linux, for example
  after scrolling thumbnails in FLUX Manage [bug 47757]

* Fixed rendering masks whose sizes are not defined in whole pixels
  (e.g. 2.39:1 mask in HD format) [bug 47871]

* Fixed masks and guides shown in Display View so they accurately
  represent the pixels that will be masked in a (high-resolution)
  render [bug 47871]

* Fixed crash when trying to link a One Point Track or Two Point 
  Track, when an underlying tracker is missing [bug 47564]

* Shot timecode/keycode no longer changes after a Consolidate
  [bug 47886]

* Fixed crash if FLUX Manage View is closed (using a keyboard
  shortcut) during a drag [bug 47903]

* Fixed crash when playing a scene containing an unknown OFX operator
  [bug 47906]

* Fixed exporting of A/B dissolves in CMX3600 EDLs [bug 44631]

* Fixed crash reading a truncated ARRIRAW MXF file [bug 47921]

* Dolby CM Metadata can no longer be exported from a scene whose Dolby
  Vision strips have not been analysed [bug 47874]

* Fixed incorrect behaviour of "REDgamma 2" and "Hybrid Log Gamma"
  colour space options in R3D Decode Params [bug 47771]

* Fixed incorrect Mastering White Point sometimes shown on Colour
  Space Journey View [bug 47944]

* Fixed bug in conform when using '%W' when conforming against
  similarly named movies [bug 47946]

* Fixed crash when using GPU OFX plugins on a multi-GPU Baselight
  system [bug 47934]

* Fixed hang when dragging scenes/jobs from Job Manager into FLUX
  Manage [bug 47893]

* Fixed behaviour of directory browsing on Render View when choosing
  an output path that starts with the scene's container (e.g. choosing
  /vol/a_b when container is /vol/a) [bug 47601]

* Fixed file permission issues in FLUX Manage, notably when accessing
  a remote NFS volume that uses root_squash [bug 47720]

* Fixed file mode and timestamp preservation when copying sequences to
  a remote NFS volume that uses root_squash [bug 48015]

* Corrected behaviour of 'preserve' mode when copying media; it
  preserves timestamps and permissions but now can only preserve
  user/group ownership if running as root (matching the behaviour of
  cp -p) [bug 48015]

* Fixed incorrect treatment of Legal to Full Scale when (a) grabbing
  to gallery, resulting in incorrect images when a gallery shot is
  viewed with the source media offline, and (b) when exporting BLGs,
  resulting in incorrect images if the BLG file itself is inserted
  into a timeline [bug 46654]

* Fixed default size of disk cache to make better use of the full
  capacity of an SSD cache drive on a Baselight ONE [bug 47510]

* Fixed perfomance regression reading Sony RAW media on Generation VII
  Baselight ONE systems [bug 47961]

* Controls on Look operators are now correctly disabled in read-only
  scenes and locked strips [bug 45750]

* Changed Gen VII BL1 current_clocksource to tsc to reduce read_hpet
  overhead on large system with many CPUs [bug 46792]

* Improved performance of Scopes, and of image display on multi-GPU
  systems [bug 47804]

* Change sudo diagnostic to 'warn' instead of 'fail' if custom sudoers
  rules conflict with Baselight rules [bug 47836]

* Fixed application startup slowdown due to ssh handshake overhead
  [bug 47790]

* Fixed crash when using temporal clone in paint [bug 47993]

* Fixed bug where input colour space values were not being read in EDL
  Import when applying Baselight grades.

* Fixed a crash in Shots View when entering an invalid time code
  [bug 48064]

* Fixed issues when many FLUX Manage browser tabs and/or file browsers
  are opened [bug 48096]

* Reduced fl-diag NVNe SSD write / overwrite performance warning
  thresholds to reflect performance after extended use [bug 46973]

--------------------------------------------------------------------------

Baselight Release 5.1.10637 (2018-06-04)
 
Bug Fixes Since Baselight 5.1.10534
===================================
 
* Fixed an issue that could cause movie reading to be slow,
  particularly on Generation VII hardware [bug 47957]
 
* Fixed regression in speed of reading Apple ProRes 4444 camera media
  at optimised/draft quality [bug 47870]

--------------------------------------------------------------------------

Baselight Release 5.1.10534 (2018-05-02)

New Features Since Baselight 5.1.10418
======================================

* Added "Show All Hosts" option to Job Manager which causes every
  Baselight system on your local network to be shown as a database
  host [bug 47258]

* Generation VII Baselight ONE/ASSIST systems are now supported.

* Due to Baselight for Avid now supporting the rendering of temporal
  operators in the Avid timeline, checking for temporal operators has
  been removed from the "Update Avid AAF with Baselight Grades" EDL
  Export option for progressive scenes. So, it's now possible to
  export AAFs containing Denoise, Deflicker and other temporal
  operators.

  Because Baselight for Avid doesn't support temporal operators in
  interlaced projects, the check has been retained for interlaced
  scenes. [bug 47362]

* Added "Full Area" Guide option to Cursor View [bug 46071]

* Time vs Time variable retimes in AAF files are now supported
  [bug 39721]

* Added option to the "Marks" menu to delete all marks in the scene
  of a specific category [bug 46667]

* Added Tangent Setup view that allows control over
    - Trackball Sensitivity & Acceleration
    - Trackball Ring Sensitivity & Acceleration
    - Encoder Sensitivity & Acceleration

  The Tangent Setup view is accessible via the Baselight or Daylight
  menu when Tangent control surfaces are enabled in Preferences
  [bug 37429]

Bug Fixes Since Baselight 5.1.10418
===================================

* Improved temporal degrain performance on Gen VII machines
  [bug 47301]

* Updated the format of the 'ACLR' atom written when rendering DNx
  codecs into QuickTime. This fixes an issue where Avid Media Composer
  version 8.6.5 and later would decode the resulting files very
  slowly. The legal field in the atom is now set correctly instead of
  always being set to full range. This fix also ensures that the
  'ADHR' atom correctly indicates bit depth and RGB/YCC [bug 45092]

* Fixed crash in bl-mkscene [bug 47413]

* Fixed crash when adjusting Truelight parameters in cursor 
  [bug 44775]

* Fixed incorrect frame time/offset calculation of strips above layers
  containing only unmodified grading operators in misaligned stacks
  [bug 47340]

* Fixed crash selecting OFX operator from the right-click menu on a
  layer [bug 47437]

* Fixed crash from using Boost Shadows with DRT with no inverse.
  [bug 47406]

* Fixed precision loss when generating Autodesk CTF from cube with
  a very non-linear input gamut LUT. [bug 46363]

* Fixed an issue where some AVC-LongGOP encoded MXF files would be
  very slow to decode [bug 47425]

* Fixed an issue that caused rendering to DNxHR HQ, LD & SQ codecs to
  fail with a message about precision of input component being too low
  [bug 47372]

* Fixed an issue that caused some MXF-files to be unsupported
  [bug 46658]

* Fixed inaccuracies in constant retimes in AAF files [bug 41072]

* Fixed crash when importing FCP7 XMLs with variable retimes
  [bug 46464]

* Fixed issue whereby the keyframes of variable retimes in AAFs were 
  placed incorrectly if the frame rate of the clip with the retime
  differed from the primary frame rate of the AAF. [bug 46186]

* Fixed crash when importing FCP7 XMLs with retimes of speed 0.0
  [bug 45884]

* Fixed issue with Wacom not being configured correctly [bug 40613]

* Fixed issue that prevented Baselight or Daylight from playing back
  on macOS when the system hostname is set to something that cannot
  be resolved to an IP address [bug 47441]

* Fixed DVI/HDMI/DisplayPort output from processing gpus [bug 40543]

* Fixed clipping issue when playing or rendering from movies or 
  audio files containing normalised audio data [bug 28217]

* Changed the default Image Transform Colour Treatment to Native,
  because this gives better results on modern wide-gamut camera media
  than the Linearised setting. You can revert to Linearised in Setups
  or by editing your Scene Templates [bug 32821]

* Fixed crash on Consolidate [bug 47273]

* Fixed repeated import of the same DRT every time a BLG is inserted
  [bug 47311]

* Fixed a bug in bl-conform's handling of the --template option 
  [bug 47422]

* Fixed issue with invalid/missing audio output on AJA SDI hardware on 
  macOS [bug 47480]

* Updated keyboard shortcut documentation [bug 47482]

* Fixed changes to Ref TC column or Circle Take column in Shots view 
  not taking effect [bug 47385]

* Fixed AAF import issue whereby multiple 3D Warp effects caused
  unintended warnings and could not be applied in some cases
  [bug 47471]

* Fixed failure when using Dolby Vision analyse on a shot with missing
  media [bug 47502]

* Fixed Dolby Vision strips incorrectly showing "Found analysis data
  in another Dolby Vision strip" [bug 47504]

* Fixed Dolby Vision analysis of a black frame reporting "This shot
  has not been analysed" [bug 47505]

* Fixed slow Dolby Vision analysis [bug 47503]

* Fixed crash when trying to link an existing one point track 
  [bug 47439]

* Fixed performance reduction in stacks containing a mixture of
  ColourSpace operators and References to upstream grading layers
  [bug 47479]

* Fixed thumbnails of ProRes 444 media [bug 47237]

* Fixed an issue that prevented the render panel from working with
  DCPs using multiple reels [bug 47515]

* Fixed an issue where some DCP parameters were not cleared properly
  when unset [bug 47517]

* Fixed bug in "Update Avid AAF with Baselight Grades" when checking
  for stacks containing multiple Sequence strips [bug 47362]

* Fixed bug which prevented the output image from updating when 
  changing a layer's "Inside Source" mode (if none of the layer's
  operators had been modified) [bug 47513]

* Fixed ARRIRAW chromaticities being written into rendered OpenEXR
  files [bug 46107]

* Fixed crash when applying an operator preset [bug 47477]

* Fixed issue where some operations (e.g. Dolby Vision analysis, Cache
  All Cursors) would occasionally pause unless the mouse was moved
  [bug 47545]

* Fixed bug which could result in incorrect frame ranges being
  calculated when rendering based on shot category [bug 47590]

* Fixed crash when using Prepare For Review on a scene with a basic
  working format [bug 47642]

* Fixed the operations queue sometimes failing to progress, due to a
  pre-render task not correctly completing [bug 47638]

* Fixed hang when rendering with RAW input media and burnins
  [bug 47631]

* Fixed incorrect errors when exporing Dolby Vision XML from scenes
  with Dissolve strips [bug 47664]

* Fixed issue when after linking an area tracker to a shape, and 
  modifying its position or size, the shape would jump [bug 47078]

--------------------------------------------------------------------------

Baselight Release 5.1.10418 (2018-04-04)
 
Bug Fixes Since Baselight 5.1.10395
===================================
 
* Fixed bug where the area track would not work when the cursor's
  viewing format is too different from the working format [bug 47213]
 
* Fixed crash when using a pre-5.1 scene with no mastering colour
  space [bug 47272]

--------------------------------------------------------------------------

Baselight Release 5.1.10395 (2018-03-28)

New Features Since Baselight 5.0.10254
======================================

* Baselight 5.1 builds will remain compatible with each other, and
  ensure a grade that can be reliably reproduced using BLG data in all
  other FilmLight 5.1 products such as Prelight, Daylight and
  Editions. This grade exchange compatibility will be retained across
  all 5.1 builds. When a new feature is added that could break this
  compatibility, a 5.2 release will be made available across all
  FilmLight products.

  Scenes created or modified in a Baselight 5.1 build will not open in
  Baselight 5.0 or earlier.

  In order to make use of files and resources on other FilmLight
  systems in your local cloud, all systems will need to have a
  Daylight or Baselight 5.1 build installed [bug 45713]

File Trimming
파일 트리밍
-------------

* Some camera movie files can now be trimmed during Consolidate and
  FLUX Manage copy. Currently the supported file types are:
일부 카메라 파일들은 콘솔리데이트작업이나 플럭스에서 복사중에 트림작업이 가능합니다. 현재 지원되는 파일 타입은 아래와 같습니다. 
  - RED R3D files (except some very old RED ONE files)
  - Vision Research Phantom Cine files
  - Sony XAVC MXF files
  - Sony RAW MXF files (F65, F55, F5 etc) [bug 20962]

Boost Range
부스트 레인지
-----------

* Added new Boost Range operator. This boosts the dynamic range of an
  SDR image to HDR.

  Example usage:
  - Create a scene using the FilmLight Scene Template
  - Set cursor Colour Space to match the display (ideally HDR)
  - Insert SDR video footage, with its Input Colour Space correctly
    set to Rec.1886, and Input DRT set to None
  - Insert a Boost Range operator, set Boost to 1.0 [bug 43192]

Look
----

* The updated Look operator offers a selection of colour-space-aware
  creative looks. Many of the supplied Looks are optimised to work
  with the Truelight CAM DRT, in both SDR and HDR grades. Please see
  the tooltips in the Look operator for information on each Look. If
  you wish to explore creating your own Looks please contact FilmLight
  Support [bug 44050]

DKey
----

* DKey has been reworked to perform better with modern wide gamut
  colour spaces:
  - The picking precision has been improved, particularly for small
    volumes
  - The radius and softness sliders are now logarithmic based, with a
    finer granularity. Their maximum value can be altered using an
    extended range button [bug 46380]

Client View
-----------

* Added Client View, which is a web-based presentation of the current
  shot accessible to clients using their phone/tablet/laptop. Use the
  phone icon in the menu bar to enable this functionality and to set a
  passcode for security [bug 45052]

Shots Layout
------------

* Added Shots Layout options, which display a shots grid on the main
  image display, either 1x1 using the whole display or 1x2 showing the
  current cursor's image above. The metadata and categories shown can
  be set using the Customise menu in Shots View. If "Fit Information
  Text To Home Area" is enabled then the 1x1 Shots Layout will scale
  to fit the shape of the current cursor's format. Note this feature
  is only available when using an external display, and is not
  available on Baselight FOUR/EIGHT systems [bug 45119]

Strip Selection
---------------

* Added ability to select all strips of a specific type (or the type
  of the current operator strip) and navigate forwards & backwards
  through them.

  To select strips of a specific type, use the Select menu's new
  submenu: "Select Strips Of Specific Type". This submenu is
  automatically populated with the types of all the strips in the
  scene.

  The Select menu also contains another new option: "Select All XXX
  Strips". This will select all strips that are the same type as the
  current parameter strip (XXX in this example).

  To navigate through the selections, use the Navigate menu's "Next
  Selected Strip" and "Prev Selected Strip" options.

  There are also Blackboard 2 and Slate actions for these operations.
  These can be found in the "Transport" action category [bug 46148]

* Added ability to navigate to the previous/next strip with the same
  type as the current strip. This is available from the Navigate
  menu's "Next XXX Strip" and "Prev XXX Strip" options. These can
  also be accessed using the Ctrl+DownArrow and Ctrl+UpArrow
  keyboard shortcuts.

  There are also Blackboard 2 and Slate actions for these operations.
  These can be found in the "Transport" action category [bug 46387]

Strip Locking
-------------

* Added ability to lock strip operator parameters based on the
  categories associated with that strip. The categories which
  determine the strips that are locked can be set from the Scene
  Settings View (on the "Category Groups" tab). Strips with locked
  parameters are drawn with a lock icon on the timeline [bug 12949]

Categories
----------

* A new Bypass Categories option is available on Cursor View and
  Render View; this allows strips to be bypassed based upon their
  categories [bug 46299]

* Added the option to show categories on Cuts View, Gallery View,
  Burnins and Counters [bug 43910, bug 45259]

File Formats
------------

* Improved speed and image quality of Apple ProRes 422 media read from
  QuickTime and MXF. Note that Sequence operators added in older
  Baselight builds will continue to perform and render as they did;
  this improvement only affects newly-added media [bug 46567]

* Improved colour of Phantom Cine files [bug 35214]

* Added support for crop areas in Phantom Cine files [bug 45652]

Security
--------

* 'sudo' permissions have been tightened. Baselight on FilmLightOS is
  configured by default to allow users to run commands as root using
  'sudo'. Although convenient for many installations there are sites
  where this may not be desirable.

  To optionally tighten security at sites that do not wish their
  users to run general commands as root, Baselight now includes a
  pro-forma 'sudoers' configuration file listing the command lines
  it (and its diagnostics) need to run as root in normal operation
  (without the need for a password). This is copied by the installer
  into /etc/sudoers.d/sudo_baselight-<version>.

  When this file is active, all other 'sudo' commands require the root
  password. (They are not blocked completely because using 'sudo
  <command>' is a useful, documented approach to system maintenance.)

  The Baselight diagnostics verify the 'sudo' rules in action allow
  at least the commands required by the Baselight version being run.

  In addition rsh, rexec and rlogin have been disabled and replaced
  with similar ssh functionality and ssh has been configured to use
  host-based authentication: a user logged into any machine in the
  local zone can ssh to this machine (as the same user) without a
  password, but everything else needs a password.

  A new script - share/fl-make-secure - is provided to apply the
  configuration changes described above. Use

    # /usr/fl/baselight/share/fl-make-secure -secure

  to enable sudo command checking; and

    # /usr/fl/baselight/share/fl-make-secure -insecure

  to return to the original configuration [bug 6138]

Multi-Paste
-----------

* Added "EDL/ALE files" source option to Multi-paste. It is now
  possible to use .edl, .ale, .aaf or .xml EDL files as a source of
  data for Multi-paste. This is primarily for use with the new "Paste
  Metadata" option, which allows you to merge metadata from these
  sources with shots in the current scene.

  If the EDL or ALE contains ASC CDL SOP and SAT values, these can be
  pasted as grades into the scene using the "Load CDL from EDL"
  option, and setting "Paste Grades" to "Yes" [bug 44034]

* Added "Paste Metadata" option to Multi-paste. It is now possible to
  paste metadata from any supported data source (Scenes, Copy buffer,
  BLGs, EDLs) into the current scene.

  You can specify which columns in the destination scene you wish to
  update with metadata using the "Metadata Columns" setting.

  You can control whether columns containing existing data are
  preserved or overwritten using the "Overwrite Existing Metadata"
  setting.

  You can merge new columns of metadata into the scene using the "Add
  Extra Metadata" setting. This allows you to merge new columns of
  data into the scene from sources such as ALEs, or other scenes
  [bug 32449]

* Added ability to detect grade changes to multi-paste. This can be
  enabled using the "Detect Grade Changes" option on the Multi-Paste
  View. Once enabled, if the stack being pasted has a different grade
  to the existing grade stack, the stack's shot strip will be tagged
  with the category specified.

  Additionally, the "Remove If Unchanged" option can be used to remove
  the category from the shot strip if the grade being pasted matches
  the existing one [bug 45160]

Colour Spaces
-------------

* Added "DJI: D-Log / D-Gamut" Colour Space to Baselight. This colour
  space is used by DJI X5s and DJI X7 in ProRes recording
  [bug 44885]

* Added P3 D65 colour space to Baselight [bug 40214]

Miscellaneous
-------------

* Added ability to install and run on macOS 10.13 High Sierra. See
  Known Issues for support on older hardware [bug 44949]

* Added the ability to control the type of KDMs issued with a DCP,
  making it possible to issue SMPTE KDMs with Interop DCPs, and
  Interop KDMs with SMPTE DCPs. The default type of KDM issued with
  Interop DCPs has changed from Interop to SMPTE. When issuing a SMPTE
  KDM for an Interop DCP, a so called MT1 (Modified Transitional 1)
  KDM is written. It is not possible to use the Content Authenticator
  field when issuing SMPTE KDMs for Interop DCPs, nor Interop KDMs
  for SMPTE DCPs [bug 39580]

* Enable daily backups of Database on Mac. Backups are stored on local
  disk in /Library/PostgreSQL/9.3.4/backup [bug 45110]

* On Blackboard 2 and Slate, added the ability to cycle backwards
  through available display layouts by holding Shift as well as
  Control [bug 44729]

* Added option to show shot-relative frame number on the cursor bar on
  Timeline View [bug 45183]

* Added shot-relative frame number as a Counter [bug 45183]

* Added optional table outline to PDF reports [bug 45580]

* AAC audio encoding is now enabled (without the need for an
  additional licence) when writing to QuickTime/MP4 files [bug 45561]

* Added search option in preferences. Clicking on the magnifying glass
  in the preference window will open a search dialog. Once a
  preference is selected the preference window will switch to that
  tab, scroll to the preference section and highlight the label
  [bug 45322]

* In Chalk for Blackboard 2 and Slate, added new Actions allowing the
  creation of desk buttons for Base Grade, Denoise, Paint, and over 30
  other new operators. Note that Chalk layouts containing these new
  Actions will not be recognised in Baselight 4.4m1, and may not be
  recognised in earlier Baselight 5.0 builds [bug 45600]

* The Job Manager now shows the user, time and software version of
  when the scene was last opened [bug 46137]

* Added new "Left Eye", "Right Eye", and "Stereo Split/Join" desk
  buttons for Blackboard 2 and Slate. These can be found in the new
  "Stereo" Button Category in Chalk [bug 45971] [bug 45972]

* Colour Space Journey View now shows layer numbers, Truelight
  operator information and the colour space where grading operations
  occur [bug 46015]

* Added low-level logging of AJA audio playback pci register (Linux)
  to help to diagnose occasional glitches when playing from external
  storage [bug 46057]

* Added a new mode to Auto strip selection called "Deselect on Stack
  Change". This acts similar to Strip Auto Select On except when the
  stack is changed the selected strip is changed to the bottom of the
  new stack. The Auto selection has also been moved to a new section
  in the cursor controls. The default preference has also been updated
  [bug 46219]

* Added additional options to each keypad key in the "Mark/Shot Keypad
  Setup" dialog. Now individual keypad keys can be configured to:
  - Add/Remove categories to/from a shot
  - Add/Remove categories to/from the currently selected strip
  - Add/Remove a mark to/from a shot
  - Add/Remove a mark to/from the currently selected strip
  - Add/Remove a mark to/from the timeline [bug 46147]

* Added keyboard shortcut to edit strip name [bug 46255]

* Added ability to easily create composite layers which use a
  reference to an existing layer in the stack as a foreground image
  (rather than a new sequence). To enable this, select the
  "Foreground/Background From Reference" toggle in the "Layer Mode"
  menu before selecting the the type of composite (from the same menu)
  [bug 46430]

* It is now possible to perform searches of the 'Buttons' and
  'Actions' lists in Chalk. To do this, click the small filter icon at
  the top-right of the respective list. A new Action Category ('All'),
  which shows the full list of all Actions available for use on desk
  buttons, has been added to facilitate searching for available
  Actions [bug 46525]

* When "Auto Update When Job/Global Formats Change" is changed to be
  active (on Scene Settings View), you are now given the option to
  update any scene formats that differ from the corresponding
  job/global/factory format [bug 46673]

* You can now use the Job Manager to compact jobs. This reclaims
  unused space in the PostgreSQL database for that job. Select a job,
  and from its action menu choose "Compact Job" [bug 46656]

* The database backup script, bl-backupdb has gained new
  functionality. You can now use a config file to specify multiple
  hosts to back-up. This is useful for including a central backup
  server in the nightly scheduled backups. The command can also be run
  from the shell to perform manual backups. Run 'bl-backupdb -i' for
  detailed usage information [bug 46281]

* Compaction of jobs is now more robust and usually faster [bug 46409]

* Job Manager now shows the version of scenes that were last saved in
  a version (ignoring build number) different from the current
  version. Scenes saved from newer versions (e.g. 5.2 when running
  5.1) are indicated in orange [bug 47108]

Bug Fixes Since Baselight 5.0.10254
===================================

* Changed default BaseGrade Contrast Pivot to 0.0 [bug 45251]

* Fixed an issue where DCP options set in the render panel could
  persist when switching scenes [bug 45116]

* Fixed issue with stacks with dissolves not combining correctly in
  stereo scenes [bug 45108]

* Added support for Avid 3D Warp and FrameFlex effects in AAF files.
  Many 3D Warp parameters are read, and implemented as either a
  transform or perspective strip in Baselight. Non-keyframed FrameFlex
  is replicated using a set of transformations, taking into account
  the Baselight format selected for the clip [bug 24187]

* Fixed ordering of Baselight grade and FrameFlex when exporting AAF
  files [bug 33787]

* Fixed crash when creating a new folder in FLUX Manage if the folder
  name ends in / [bug 45197]

* The bl-delete help text is updated to reflect the fact that the
  command can delete jobs as well as scenes [bug 46408]

* The Job Manager will now show the user and software build of when the
  scene was last saved [bug 45973]

* Fix potential crash when upgrading 4.4m1 jobs [bug 46883]

* Fixed rendering issue with a paint operator using an invalid
  perspective transform [bug 45162]

* Fixed (blank) Blackboard 1 displays when using the Grid Warp
  operator [bug 45123]

* Fixed single frame offset when conforming CMX EDLs containing 
  keyframed SDL events [bug 36141]

* Updated the audio reading library to include the latest
  bugfixes. This fixes an issue that prevented some wav-files from
  being read [bug 44300]

* Fixed crash adding custom columns to Shots View [bug 44266]

* Fixed font size of burnins and Text operators to match previous
  Baselight versions [bug 45215]

* Fixed crash doing audio sync [bug 43537]

* Add limited diagnostics to Mac build [bug 33703]

* Speed up reading of diagnostic results [bug 45239]

* Clearing undo history will also remove undo history from tagged
  renders in the scene, which can potentially reclaim a significant
  amount of database storage space [bug 45241]

* Fixed an issue in stereo scenes which could cause the 1x1 display 
  button on Blackboard 2 and Slate to toggle incorrectly
  [bug 44729]

* Fixed undo/redo of toggling stereo grade's "Automatically Adjust 
  Windows". Separated out setting of the default value (via the
  "Customise" menu) from the setting of the currently selected op's
  value (via a toggle button below the sliders) [bug 45187]

* Restored the <Browse> option in the Text operator to allow selection
  of fonts that are not in the default font folders [bug 45133]

* Fixed the gestural editing of ganged controls. Editing more than one
  of the controls in the group using gestures no longer leads to
  incorrect values for those previously edited [bug 39068]

* Fixed issue with group grading not changing the other eye when 
  editing the input colour space of a sequence [bug 45145]

* Moved the CDL grade power value to be between 0-10 [bug 45173]

* Fixed coloured lines appearing in over-exposed Phantom Cine footage
  [bug 45147]

* Fixed out-of-range values in Dolby Vision analysis and XML export
  [bug 45144]

* Fixed bug which would cause strips not contributing to the image
  to not be greyed out in the timeline when in stereo viewing modes
  (in single stack stereo scenes) [bug 45192]

* To make the paint cursor more visible, it has been made thicker and
  the soft brush has been made less transparent [bug 45326]

* Fixed matte paint strokes causing square artifacts [bug 45035]

* Fixed issue that created duplicate .fltransform files [bug 44740]

* Fixed behaviour of rescan DRT button [bug 44740]

* Fixed bl-codecs so it correctly saves settings [bug 45049]

* Fixed error rendering from some scenes to 12-bit or 16-bit DPX files
  [bug 45357]

* When selecting a stereo OpenEXR file in FLUX Manage, the View now
  defaults to "Automatic left/right" [bug 45354]

* Fixed timeline alignment issues in single stack stereo scenes when
  removing unreferenced strips [bug 45192]

* Fixed crash when shots had a negative frame increment and no source
  timecode [bug 44671]

* Fixed missing colour space mapping when "Show Source Input Image" 
  enabled in Grid Warp's "Source" tab [bug 44512]

* Enabled overlays in both eyes when in a stereo viewing mode and
  fixed cursor only appearing in the left eye [bug 40313]

* Fixed crash when previewing audio file [bug 45413]

* Fixed layer config not applied when inserting a layer from the 
  keyboard, the insert layer blackboard key and the insert menu
  [bug 45220]

* The NCLC primaries tag and Dolby Vision XML metadata has been
  corrected for the colour space "Dolby: ST 2084 PQ / XYZ / 108 nits"
  [bug 45404]

* Fixed issue when multi-pasting metadata only [bug 45435]

* Improved text / burnin rendering speed [bug 45046]

* Fixed issue where selected metadata columns in Multi-Paste view were
  not being restored correctly after restarting the software
  [bug 45539]

* Fixed crash when multipasting from an EDL with overlapping events
  [bug 45547]

* Fixed issue with adding strokes to a keyframed layer after it had
  been reset [bug 45500]

* Enhanced Filename matching in conform operations to allow filenames
  to match if only the extension is different [bug i45307]

* Fixed operator names shown on Blackboard 2 and Slate, e.g. for Boost
  Contrast operator [bug 45499]

* Fixed handling of matte merge with values outside 0 to 1
  [bug 45333]

* Added %0S to Render View help [bug 45548]

* When inserting a mark in follow-mode, Baselight now returns the lock
  back to the master [bug 46045]

* Render View help text now uses a clearer font for the "%"
  substitutions, to make %I clearer [bug 45384]

* Fixed bug which could cause "Join Adjacent Strips" to fail when
  joining (input) strips containing audio operators set to "No Audio"
  [bug 45567]

* Fixed crash which could occur when doing a "Pick" drag in Base Grade
  with a corrupted colour space [bug 44813]

* OpenEXR tracks containing X, Y and Z channels are now read as RGB
  rather than just the Y channel as luma [bug 45451]

* Fixed crash in Multi-Paste which could occur if a strip overlapped
  multiple shots [bug 36924]

* Fixed appearance of old ARRI camera media (e.g. from D21 camera)
  [bug 45619]

* Fixed an issue identifying and reading certain Scanity DPX-Y 10-bit
  single channel DPX files, that previously incorrectly identified as
  containing 3x10 bit image data [bug 45650]

* Fixed crash in Multi-Paste which could occur if the source shot
  lay above a destination shot but contained a bottom-most strip
  which didn't overlap the destination shot [bug 45573]

* Fixed Source In timecode of certain clips with retimes in FCP7 XMLs
  [bug 45263]

* Moved crash report flushing from system bootup script to a background
  task. This improves boot time on Linux-based systems [bug 44986]

* Fixed failure to export scenes and jobs where the job name contains
  unusual characters [bug 36293]

* Fixed an Area Tracker issue, where the tracking box corners could 
  not be moved around using the overlay [bug 45690]

* Fixed cached strips being needlessly re-cached when the cursor
  viewing colour space changes [bug 45679]

* Fixed an issue where the shape keyframe mode changed after inserting
  a tracker [bug 45452]

* Added standard masks to UltraHD 3840x2160 format [bug 45671]

* Fixed failure of temporal effects (e.g. Denoise) when applied to the
  last frame of a movie file [bug 45597]

* In Paint, added a cross to small brushes cursors to help identify 
  the cursor at large resolutions [bug 45156]

* When an RGBA Sequence is marked as Premultiplied, the RGB values are
  no longer clipped to [0,1] when unpremultiplying, to fix issues when
  compositing HDR images. To update the behaviour in existing Sequence
  operators turn Premultipled off then on again [bug 45691]

* Fixed Mastering Colour Space menu not showing some colour spaces in
  older scenes [bug 45617]

* Fixed Mastering Colour Space menu not updating correctly after
  opening an older scene [bug 45011]

* Fixed failure to delete Chalk layout files whose names contain
  spaces [bug 45704]

* Fixed failure to copy sidecar files when using fl-cp to copy from a
  non-/vol path [bug 45697]

* Fixed unexpected layer renumbering in an overlap edit when changing
  the start for an entire stack. Also preserved the layer number of
  strips moving in a different context (a different sub branch or
  stack) [bug 45590]

* Fixed green drag-and-drop highlighting being left on-screen after
  dropping onto Timeline View or Cuts View [bug 45415]

* Added reset buttons to the Paint layer exposure and opacity controls
  [bug 45712]

* New gallery folders are now browsable by FLUX Manage [bug 44038]

* Per-scene galleries no longer report an error when the scene is within
  a folder [bug 46431]

* Fixed failure when loading a P3-space QuickTime movie [bug 45720]

* Improved behaviour when Blackboard is disconnected while application
  is running [bug 43022]

* Fixed potential file permissions problem reading multi-part OpenEXR
  files [bug 45117]

* Added Colour Space Journey View warning if using DCI: 2.6 Gamma /
  X'Y'Z' as a Mastering Colour Space [bug 45205]

* Cuts View and Shots View no longer show burnins when they are
  enabled in Cursor View [bug 45348, bug 45349]

* Fixed omission of some OpenEXR metadata [bug 45379]

* Fixed the pane description shown on Display View when scrubbing a
  thumbnail in Shots View [bug 45381]

* Fixed crash on macOS when switching away from the application and
  back again [bug 45385]

* Fixed some buttons not responding correctly to repeated mouse clicks
  [bug 45437]

* Fixed "temporary failure in name resolution" errors caused by DNS
  server configuration issues [bug 45476]

* Fixed crash pasting sequence template paths with stereo colour
  matching [bug 45543]

* Fixed missing CPU diagnostic on Baselight TWO and Baselight X
  systems [bug 45588]

* Made baselight more robust against machines disappearing from the
  network [bug 43434]

* Consolidate View now explains the reasons why it cannot show an
  example path [bug 45735]

* Fixed diag test for Blackboard 2 [bug 45709]

* Fixed crash opening read-only a scene using OFX [bug 45751]

* Fixed Read only and locked strip issues in Paint [bug 45753]

* Fixed layer 0s toggling broken when a tracker is in the stack
  [bug 45766]

* Correct SMPTE MXF tags and embedded colour tags in the XAVC essence
  are now used when writing XAVC encoded Sony MXF files. The legal
  range flag embedded in XAVC essence is now interpreted when reading
  XAVC encoded MXF files, and the default value of the 'Legal to Full
  Scale' option on the input strip set accordingly [bug 45109]

* Fixed wrong Layer 0 insertion at the bottom current cursor's stack
  after pressing the Layer 0 key when there is no strip selection on
  it [bug 45591]

* Added Find Stereo Correspondence to the Paint operator [bug 45765]

* Fixed incorrect Text scale and position when viewing format is
  changed [bug 45746]

* Added Blackboard 2 firmware 1.1.48.76 (original LCD screens) and
  2.0.2.76 (new LCD screens) which handles broken DVI modes better.
  Displays a message on the back LCD screens if the DVI mode is
  invalid [bug 41719]

* The image dimensions of Sony ILCS-7SM2 ARW files are interpreted as
  slightly larger than some other applications, e.g. Flame and
  Photoshop. These files are now read with an additional crop that
  matches the image interpretation of Flame and Photoshop [bug 45273]

* Fixed bug in giving random noise on right hand and bottom edge for
  integer 3 frames Denoise. Versioned so old scenes do not change
  [bug 45572]

* Fixed bug which could cause potential crash on exit depending on the
  strip selected at the time [bug 45776]

* Fixed error when using Texture Equaliser with matte [bug 45332]

* Fixed inconsistent Merge/Replace pasting to multiple strip
  selections [bug 45818]

* The thumbnail size of Shots View grid and Shots Layout can now be
  adjusted using ctrl-middle button drag [bug 45649]

* Fixed bug which could cause shapes to shift slightly vertically when
  "Lock Y Positions" option enabled [bug 45933]

* Fix perspective crash when toggling between tabs [bug 45816]

* Fixed crash related to duplicated colour spaces imported onto a
  system under more than one name [bug 42971]

* Fixed playback glitch when adding marks to the timeline [bug 46033]

* Fixed crash when a custom fltransform file refers to an unknown
  colour space [bug 46005]

* Fix crash when inserting a new tracker after copying a strip
  [bug 46049]

* Fixed ordering of five-digit build numbers in 'fl-vers' tool
  [bug 46012]

* Fixed locked status not being transfered when doing a multi-paste
  [bug 46151]

* Changed behaviour when linking / unlinking a tracker. The keyframes
  and their animations will be kept [bug 46236]

* Prevented a crash during a paste operation (from the cut view or the
  paste key) when no destination stack is selected [bug 46173]

* Fixed multi-paste of LUTs (also Apply LUTs in EDL Import) when the
  same LUT was used on multiple shots [bug 45778]

* Fixed use of up/down arrow keys to adjust Offset in frames in
  Sequence parameters [bug 46307]

* Changes to the strip name now only apply to the current strip,
  unless Grouped Grading is enabled [bug 46341]

* Fixed crash when stereo splitting an edge shape, which is linked to
  a two point tracker [bug 46389]

* Fixed incorrect positioning of some Gallery shots, when the grabbed
  stack contains cached strips [bug 46390]

* Fixed bug when viewing Stereo Grade strips in the gallery
  [bug 46390]

* Fixed bug which prevented 'Home' & 'End' shortcuts from working with
  multiple selected strips [bug 46455]

* Fixed issue where stereo split was not obeying group grading
  [bug 46391]

* Fixed bug in Shapes where using the middle trackball to translate a
  perspective shape with "Lock Y Positions" enabled would sometimes
  cause the shape to move vertically [bug 46452]

* Enabled 3D toggle button on the UI and panel when the strip was
  locked [bug 46445]

* Desk buttons formed from the "Toggle Overlay" Action in Chalk now
  work as expected in stereo [bug 46457]

* When navigating from a tracker section inside an operator (for
  example shapes) to the tracker strip, only the current tracker
  overlay will be displayed when appropriate [bug 46386]

* Fixed tracker issue when linking a one point or two point track
  the shape would move [bug 46292]

* Fixed crash exporting an EDL to a read only file system [bug 45886]

* Fixed crash when having the paint transform overlay on and 
  deselecting the paint strip [bug 46103]

* Fixed crash when dragging a layer to a layer view [bug 46008]

* Disabled the Paint layer opacity button when the strip is locked
  [bug 45872]

* Disabled the menu in Matte tool when the strip is locked [bug 45749]

* Fixed issue with the preference search highlight moving the text
  [bug 45732]

* Fixed outdated DRT assigned when using a Scene Template [bug 46200]

* Fixed MXF timecodes for 60@30 drop-frame, 50@25 and 48@24 timecode
  frame rates [bug 46602]

* Fixed permissions of cache directory created from Preferences
  browser [bug 46003]

* Improved performance when multiple Sequence or Reference operators
  in the same stack each read different channels from the same OpenEXR
  file [bug 46109]

* Fixed the loading of AAF files in which the timeline resolution
  is not specified [bug 46099]

* Fixed issue with bl-config-xorg selecting the appropriate tablet
  mappings for Blackboard 2 control surfaces without keyboards.
  bl-config-xorg will now ask if your BB2 has an integrated keyboard.
  and apply the appropriate tablet mapping [bug 30516]

* Improved playback reliability when using DVI or Display Port outputs
  [bug 46819]

* Fixed slowdown caused by Truelight operators with long lists of
  cubes [bug 46726]

* Improved playback reliability when using DVI or Display Port outputs
  [bug 46819]

* Fixed diag test for ssh volumes [bug 46825]

* Fixed issue with dragging from FLUX Manage View to an empty Shots
  View [bug 45791]

* Improved playback from disk cache. This fix has caused the format of
  the disk cache files to change. Cache files from previous versions
  are no longer valid and are deleted by this version. All scenes will
  need to be recached [bug 46872]

* Fixed loading of cursor settings from job [bug 45811]

* Added Shutter Angle metadata from R3D files [bug 46321]

* Fixed crash renaming custom columns [bug 46596]

* Fixed paint clone bug with very small strokes disappearing under
  transforms [bug 46254]

* Fixed unresponsive mouse and keyboard when playing at 60+ fps with
  Scene Settings View visible [bug 46093]

* bl-import can now import legacy scenes to databases using a FQDN
  hostname [bug 45804]

* Fixed FLUX Manage incorrectly making resolution directories when
  copying movie files [bug 46869]

* Updated xfs driver to fix fl-fsr failure to defragment image
  sequences [bug 46890]

* Fixed crash when dragging from the layer view into a popup layer
  view [bug 45988]

* Fixed mastering colour space application to input media when
  mastering white space is set to "(from Mastering Colour Space)".
  Note this fix does not change existing scenes, it only applies to
  Sequence operators added in version 5.1 or later [bug 47003]

* Fixed use of ":" in volume.cfg to allow mounting a volume with a
  space in its name [bug 41219]

* Fixed tabbing between fields in the Shots View causing unintended
  edits [bug 45029]

* Fixed crash which could occur when exporting BLG of stereo
  scenes with an empty row in the input layer [bug 46361]

* Improved error message when a scene cannot be loaded due to an
  unknown operator [bug 47120]

* Fixed "This render will not proceed" warnings when submitting a
  render, notably to a FLUX Store [bug 45786]

* Fixed failures when a user is a member of a very large number of
  supplementary groups [bug 46826]

* Fixed incorrect transforms if resolutions didn't match when
  conforming from FCP7 XML files [bug 46552]

* Fix corrupted audio output when using Stems for audio and
  audio channel mappings [bug 46962]

--------------------------------------------------------------------------

Baselight Release 5.0.10254 (2018-02-22)

New Features Since Baselight 5.0.10184
======================================

* Updated to ARRIRAW SDK v5.4. This adds support for the ALEXA LF
  camera [bug 46621]

* Dolby Vision EDR export now has the option to use frame numbers
  derived from the Record (Timeline) Timecode [bug 45916]

* Added support for NVIDIA Quadro P1000 UI GPU [bug 46664]

* Added keyboard shortcut for "Combine/Separate Stereo Stacks" command
   - Ctrl-Shift-` on Linux
   - Cmd-Shift-PlusMinus on macOS [bug 24869]

* Added support for conforming audio from ALE during EDL Import. 

  Currently only full, container-relative paths to audio files are
  supported.

  The ALE must contain the following columns to conform the audio
  file:
    - "Audio Path" : a container-relative path to the audio file
    - "Audio Offset" : an offset in seconds within the audio file

  Audio metadata will also be carried over if the ALE contains the
  following columns:
    - "Audio TC" : audio timecode at the start of the shot
    - "Audio Fps" : audio timecode framerate
    - "Audio Roll" or "Soundroll"
    - "Audio Channels" : number of audio channels in audio file
    - "Audio Track Names" : a comma-separated list of audio track
      names [bug 46691]

Bug Fixes Since Baselight 5.0.10184
===================================

* Dolby Vision EDR export now fails if there is not a Dolby Vision
  strip at every frame of the scene [bug 46613]

* Dolby Vision EDR export now includes valid UniqueID data [bug 46311]

* Fixed Shots View tab configuration not saving properly on scenes
  created from template [bug 46587]

* Fixed crash when trying to paste a stack that had been deleted after
  it had been copied [bug 44161]

* Fixed crash renaming custom columns [bug 46596]

* Increased resolutions of R3D and ARRI media that can be decoded on
  macOS with a 3GB GPU [bug 45226]

* Enabled left/right eye source timecode columns when exporting a
  stereo ALE with "Use Shot (Src) Timecode" option enabled [bug 46665]

* Fixed incorrect negative Sequence frame numbers, notably at the
  first frame of the shot when the Offset is -1 [bug 43357]

* Fixed bug which could result in the metadata for the wrong eye
  being written to stereo ALE columns [bug 46689]

* Fixed missing Audio Timecode for Right eye in Single Stack Stereo
  scenes after using Audio Sync operation [bug 46686]

* Fix floating-point number precision in Shots View (read-only
  columns), EDL export and Report export [bug 46690]

* Fixed locking issues when clearing undo/redo history [bug 46207]

* Fixed ambiguity in volume lists, for example when there are several
  systems each mounting the same SAN [bug 46669]

* Fixed reading 60fps and 120fps ALEs [bug 56770]

* Added 120p to the list of default frame rates in the New Scene
  dialog [bug 46771]

* Fixed issue where applying a BLG to a sequence from FLUX Manage
  would reset the flip/flop parameter of the Sequence operator when
  the "Include Layer 0 Operations" copy/paste option was disabled
  [bug 46809]

* Fixed the right eye filename sometimes being incorrectly used for
  the rendered filename (e.g. with %W) when rendering a stereo scene
  as anaglyphic or muxed [bug 46810]

* Changed Gen VII BL2 current_clocksource to tsc to reduce read_hpet
  overhead on large system with many CPUs [bug 46792]

* Fixed filename issue in adaptec_fwflash script [bug 46818]

* Fixed temperature / hours not appearing in 8TB drive dpm statistics
  [bug 46814]

* Changed fl-setupssh to generate rsa keys (instead of dsa) to allow
  connection to MacOS 10.12 [bug 40385]

* Stop prompting to save if you try and close a scene immediately
  after opening it [bug 46838]

--------------------------------------------------------------------------

Baselight Release 5.0.10184 (2018-02-02)

New Features Since Baselight 5.0.10074
======================================

* Added support for HP Z2 UI Host [bug 45230]

* The conversion of 4.4m1 jobs into 5.0 jobs requires the installation
  of Baselight 4.4m1.10068, available from the FilmLight website.

  This is a 'conversion' release, and should not be used for 4.4m1
  jobs, it only needs to be installed for this and later 5.0 releases
  to convert 4.4m1 jobs fully.

* Added support for 8TB drives [bug 46274]

* Added support for the Sony VENICE camera [bug 43258]

* Updated to RED SDK v7.0.6. This includes a fix for failures on AMD
  GPUs on macOS 10.13.2 and up [bug 46469]

* Generation VII Baselight TWO/X systems are now supported.

Bug Fixes Since Baselight 5.0.10074
===================================

* Fixed an issue which could cause crashes when working with custom
  Blackboard 2 desk layouts [bug 46239]

* Fixed port number on Quadro M620 GPU [bug 46243]

* The Job Manager now shows the correct scene last modified date/time
  [bug 46248]

* Fixed an issue that could cause the scratchpad scene to behave
  slowly over time [bug 46228]

* Fixed Sequence "Legal to Full Scale" not being applied for "Input
  Only" renders [bug 46258]

* Improved support for reading JPEG 2000 encoded MXF-files. Additional
  tags are now recognized, and files with 4 channels as well as files
  with subsampled YCC data can now be read [bug 46263]

* NVIDIA driver version 367.44 is known to cause rendering artefacts
  and should be replaced by the 375.66 driver available from the
  FilmLight support website [bug 45659]

* Fixed crash when using 8-bit Phantom Cine file [bug 46288]

* Fixed Audio Sync crash when syncing with single-channel audio files
  [bug 46300]

* Fixed incorrect file paths exported to DLEDL from sequences on cloud
  media [bug 45950]

* Fixed an issue which caused the installation script to incorrectly 
  identify old builds on machines low in disk space [bug 46350]

* Fixed additional tabs remaining in FLUX Manage View, and eventual
  application crash, after using it for many sequence replacements
  [bug 44381]

* Added pre-compiled aja driver for 2.6.32-696.6.3.el6.x86_64 kernel
  [bug 44623]

* Fixed "Copy Grades" option in EDL Import not working [bug 45217]

* Fixed "Apply LUT", "Apply LUT2" and "Apply CCC/CDL XMLs" options
  in EDL Import not working [bug 46406]

* Fixed an issue where AVC LongGOP essence stored in QuickTime movie
  files could occasionally be decoded with frames in the wrong order
  [bug 46423]

* Fixed an issue where Y'CbCr formatted DPX files would turn green
  when copied with FLUX Manage or fl-cp [bug 45995]

* Fixed support for reading Scanity DPX-Y 10-bit single channel DPX
  files [bug 46475]

* Fixed rendering from flycc files with non-identity transforms
  [bug 36926]

* To prevent decode failures, when IPP2 colour science is selected for
  R3D files, decoding is not attempted on RED Rocket cards [bug 46497]

* Fixed drawing of RGB parade in overlay mode [bug 45974]

* Fixed "On-disk image cache size" preference being incorrectly reset
  to its lowest possible value after being increased beyond its
  highest possible value [bug 46516]

* Fixed bl-install not correctly offering the latest installed builds
  from other machines [bug 46518]

* Fixed occasional application startup failures on macOS [bug 46520]

* Fixed ALE export for stereo scenes [bug 46528]

--------------------------------------------------------------------------

Baselight Release 5.0.10074 (2018-01-04)

New Features Since Baselight 5.0.10007
======================================

* Added support for NVIDIA Quadro M620 UI GPU [bug 45506]

* Updated to RED SDK v7.0.5. This includes:
  - Option to use new IPP2 colour science
  - New tone curves (Hybrid Log Gamma, Gamma 2.2 & 2.6, REDlog Film)
  - New primaries (DCI P3, DCI P3 D64, ProPhoto RGB)
  - Support for Helium 8K S35 Monochrome sensor
  - Support for Weapon Monstro 8K VV sensor [bug 45542]

* Files can now be renamed in FLUX Manage [bug 46214]

Bug Fixes Since Baselight 5.0.10007
===================================

* Fixed bug with Audio Sync when syncing by Timecode [bug 44937]

* Fixed crash in format auto-update when job/global format has been
  deleted [bug 45881]

* Fixed an issue preventing PhotoRAW from working on multi-GPU systems
  [bug 45401]

* Fixed issues when dragging a scene from Job Manager to a Copy
  Destination on FLUX Manage View [bug 44992]

* Muxed stereo renders (anaglyphic, interlaced, side by side and
  over/under) now render burnins into each eye separately [bug 18446]

* Audio files can now be inserted onto the timeline from FLUX Manage
  [bug 45834]

* Fixed licence issue with Baselight TRANSFER [bug 46097]

* Fixed issue which prevented using NVIDIA Driver 375.66 with
  GTX 980, Quadro NVS 810, Quadro K6000, M4000, M5000 and M6000 GPUs
  [bug 46135]

* Fixed range and default value of Dolby Vision Tone Detail Weight
  control [bug 46204]

* Fixed bug with Audio Sync settings not being saved when the scene
  is closed [bug 46178]

* Fixed bug with Audio Sync failing to correctly sync audio
  when the Audio TC frame rate does not match the scene's working frame
  rate [bug 46208]

* Fixed handling of media with 48 and 48@24 fps timecodes [bug 46231]

* Fixed incorrect Shot Timecode for media whose timecode has a doubled
  frame rate (60@30, 48@24 etc) and its first frame is the second of a
  timecode pair [bug 46231]

* Fixed Log section of Queue Monitor not updating correctly when
  selecting a new operation [bug 45188]

--------------------------------------------------------------------------

Baselight Release 5.0.10007 (2017-12-04)

New Features Since Baselight 5.0.9964
=====================================

* Added second vectorscope to allow viewing at multiple scales
  simultaneously [bug 45831]

* Added ability to recover an older version of a scene that cannot be
  opened because it has been saved from a future Baselight release
  (e.g. 5.1) [bug 45583]

Bug Fixes Since Baselight 5.0.9964
==================================

* Fixed an issue that prevented creation of non-encrypted DCPs due to
  invalid errors about certificates [bug 45768]

* Improved display of vectorscope graticule [bug 45831]

* Addressed corruption of font textures on the blackboard [bug 44755]

* Fixed issues on Render View when cloud media volumes have names
  containing special characters such as parentheses [bug 45793]

* Fixed hang in OFX, for example when using a custom preset dialog
  [bug 45952]

* Fixed out of memory condition when using scopes and a blackboard
  [bug 45717]

* Fixed crash when multi-pasting BLGs [bug 45163]

--------------------------------------------------------------------------

Baselight Release 5.0.9964 (2017-11-16)

Bug Fixes Since Baselight 5.0.9940
==================================

* Fixed crash loading some OpenEXR files [bug 45525]

* Improved interactivity of certain grading operations [bug 45683]

* Fixed incorrect drive performance diagnostic 'no target disk rates'
  warning when no errors are found [bug 45715]

* Fixed smart dissolve shot not adding the grade strips on both 
  dissolve's inputs [bug 45730]

* Fixed bug that prevented audio output on systems with RME Hammerfall
  sound cards [bug 45733]

--------------------------------------------------------------------------

Baselight Release 5.0.9940 (2017-11-08)

New Features Since Baselight 5.0.9853
=====================================

Formats
-------

* A new Scene Setting (initialised from Setup and Scene Templates)
  controls the auto-update behaviour of Scene formats when opening a
  scene. You can choose to automatically update a Scene format
  whenever the corresponding Job or Global formats that was previously
  the same as that Scene format has been edited since the scene was
  last saved [bug 44817]

* When saving changes made to a Job or Global format that is the same
  as a corresponding Scene format, the Scene format is automatically
  updated if auto-updating is enabled, otherwise you are given the
  option to update the Scene format with the same changes [bug 44816]

* When creating a new format from the New Scene dialog, you can now
  choose to create a Job or Global format instead of a Scene format
  [bug 44818]

* When creating a new format from the New Scene dialog, you can now
  set the format resolution from the format selected in FLUX Manage
  View [bug 44819]

* The Input Format menu on Sequence parameters now shows all formats
  that match the resolution of the input media at the top of the list
  [bug 44824]

* WARNING: The above changes have necessitated a modification to how
  formats are stored - therefore scenes created or saved in this build
  will *not* be able to be loaded into older versions of the software.

Miscellaneous
-------------

* Added options to the preferences to change cursor colours
  [bug 43419]

* Added an option to blend highlights in Photo RAW files, which avoids
  the loss of highlight details that can occur by clipping. The new
  option is available in the Photo RAW Parameters operator, and is set
  to blend by default for new operators [bug 43600]

* Added support for reading P2 XML metadata from Panasonic QuickTime
  movies. This enables colour space detection from metadata for some
  colour spaces, e.g. V-Log [bug 44721]

* Increased the amount of metadata that is shown from OpenEXR files
  [bug 40100]

* Added support for nvme-based RAID-0 cache [bug 43802]

* The command line utility for issuing KDMs, fl-kdmtool, now has
  parameters to set the valid time interval and type of the new KDM.
  It also attempts to use the default generated certificates for
  decrypting the input KDM and issuing the new KDM, reducing the
  amount of information that needs to be specified in many use
  cases. Run 'fl-kdmtool' with no options to get a summary of the
  available parameters, or run 'fl-kdmtool -h' for more information
  [bug 42879]

* Added diagnostic that warns if share volumes are defined without a
  fully-qualified hostname, since this can cause access via /vol to
  fail [bug 40476]

* The way in which legal-range images (notably ProRes movie files) are
  treated has changed. There is now a "Legal to Full Scale" toggle
  button on the Sequence parameters which allows you to specify
  whether the data stored in the file is squashed into legal range.
  This allows ProRes files containing full-range data (e.g. Panasonic
  V-Log) to be correctly used. This option can be used for any input
  file except those for which an Automatic Input Colour Space is
  offered. Legal-range colour spaces are no longer recommended for any
  purpose in the application [bug 44539]

* Added tooltips to the Copy Destinations section of FLUX Manage View,
  so long paths can be distinguished [bug 44979]

* The Canon RAW SDK is now used to decode Canon RAW media (RMF and CRM
  files). This adds support for C200, C700 etc. Existing scenes using
  RMF media are unaffected [bug 41280]

* Added support for drag and drop to the Shots View. Sequences can now
  be inserted into the scene by dragging from FLUX Manage View to the
  Shots View [bug 44651]

* Audio Channel Mixing

  You can now mix multiple audio channels into a single audio channel
  when rendering to a movie or audio file.

  In the Edit Layout dialog, accessed via the Audio Channels settings
  in the Render View, you can specify one or more source audio
  channels to route into an output audio channel.

  If multiple audio channels are assigned to one output channel, those
  audio channels will be summed together [bug 38888]

* Added support for controlling which local volumes and local media
  are advertised to other Baselight systems.

  By default on a system in a zone, all local volumes and media are
  advertised; on a system not in a zone no local volumes and media are
  advertised. To change this behaviour, create the file
  /vol/.support/etc/advertise.conf containing either

  volumes_public = [set ...];
  -or-
  volumes_private = [set ...];

  where each entry in the set is either the name of a local volume
  (e.g. "bl999-images") or a regular expression that's used to match
  against the volume names.

  For example

  volumes_public = [set "bl999-images"];
  advertises only /vol/bl999-images and nothing else.

  volumes_public = [set #SAN#];
  advertises all local volumes which contain "SAN" in their name, and
  nothing else.

  volumes_private = [set "bl999-secret"];
  advertises all local volumes except /vol/bl999-secret.

  Similarly, use media_public or media_private to control advertising
  of local media volumes.

  media_public = [set "My Data"];
  advertises a local media volume called "My Data" (if it is
  connected) but no other local media.

  media_private = [set #^Backup#];
  advertises all local media except any media volume whose name starts
  with "Backup".

  Note that you must restart the advertise service on the zone master
  after making any changes to advertise.conf [bug 29426]

* In previous versions, strip caching would cache the output of a
  strip at the working format resolution. If the image and the working
  format were different sizes the cached image would be padded with
  black. The black padding changed the behaviour of certain
  operations, in particular boost contrast. An option has been added
  to cache just the active image area. This is the default for all new
  scenes. Older scenes retain the original behaviour and this can be
  changed in Scene Settings. [bug 42092]

* Added option to set grid space on scopes [bug 45265]

Bug Fixes Since Baselight 5.0.9853
==================================

* Fixed behaviour of scene referred renderings from scenes using
  DRTs with BlackOffset. This bug caused a mismatch of scene
  referred renders compared to the actual grading stack when
  viewed through the same DRT [bug 45344]

* Fixed Boost Shadows bug that gave different results with large
  viewing formats [bug 44597]

* Fix for Denoise with negative XYZ values.

  The original Tone setting put the XYZ values through a gamma curve.
  The XYZ values clipped at zero. There is no meaning to negative XYZ,
  and some colour spaces may also clip at zero. Nevertheless, on some
  unusual scenes, the tone clip at zero has been seen to raise the
  dark tones, giving milky shadows.

  The new Denoise tone curve is an offset gamma curve with a linear
  region below zero. This does not clip, so should it should preserve
  negative values. The offset is a fixed value set from the Denoise
  version number. Old strips have a zero offset and a clip, so they
  will render as before [bug 44467]

* Fix for Boost Shadows with matte. This was giving a cross and an
  error message when the controls were set to the defaults [bug 44558]

* Improved performance of undo/redo in scenes with many changes
  [bug 43872]

* Improved performance of editing in very large scenes [bug 44478]

* Invalid SMPTE timecode values (with hours or frames > 39) are no
  longer written to DPX files [bug 44484]

* Fixed Matte reference to upstream layer mattes [bug 44700]

* Fixed browsing for a burnin image in Formats editor [bug 44735]

* Fixed error when saving a global format in Formats editor after
  adjusting an opacity slider [bug 44639]

* Fixed crash when recalling groups in an empty scene [bug 44731]

* Fixed incorrect application of Mastering Colour Space to exported
  BLG source images [bug 44746]

* Fixed failures when a Shader's definition specifies an invalid
  colour space [bug 42995]

* Fixed bug in BLG export which could cause keyframes to slip
  incorrect in Baselight for Nuke when exporting multi-input BLGs
  [bug 44805]

* Fixed an issue that prevented thumbnails for encrypted DCPs from
  being shown in the Sequence Browser, even when a valid self-KDM was
  present [bug 44814]

* Fixed Replace Grades With LUTs which was failing when including the
  Grade but not the Input Colour Space [bug 44807]

* Fixed a DCP render issue where invalid KDM parameters or
  certificates would not trigger errors until the end of the render.
  All KDM parameters and certificates are now checked at the beginning
  of the render to fail early. This fix also improve the error
  messages to include the name of the problematic certificate where
  possible [bug 42780]

* Fixed issue with AJA HDMI output not generating a valid signal
  [bug 44834]

* Fixed failure of fl-cp to copy secondary files for some sequences,
  notably run-on R3D files [bug 44617]

* Fixed Wipe Layout display on SDI output on macOS [bug 44841]

* Fixed format mapping inside/outside setting not being preserved
  correctly [bug 44854]

* Fixed the keyframing of transform effects in FCP7 xmls when constant
  retimes are applied [bug 44428]

* Fixed intermittent Cubix Xpander diagnostic failure [bug 44241]

* Fixed an issue that could flag KDM validity dates in the render
  panel as incorrect when they were not. The check has also been
  improved to better detect invalid dates and times [bug 44832]

* Added support for reading Avid 1:1x encoded QuickTimes [bug 33505]

* A KDM for the issuing certificate (self-KDM) is now always created
  when rendering encrypted DCPs. The self-KDM is no longer listed in
  the render panel. To create an encrypted package without the
  self-KDM, the file named kdm_fl_self.xml must be manually removed
  from the rendered DCP. A warning will be presented in the render
  panel if any specified filename collides with that of the hidden
  self-KDM. This warning may occur for existing scenes where the
  self-KDM is not hidden, but can in that case be safely ignored
  [bug 44752]

* Fixed display of shots with missing source timecode in Shots View
  [bug 44647]

* Fixed crash resizing some windows (e.g. fl-queue) [bug 44983]

* Fixed a problem where online licencing would fail if you clicked
  the 'activate' button too quickly [bug 44966]

* Fixed incorrect colour space for thumbnails in FLUX Manage when
  colour space is set to "From Metadata" [bug 44540]

* Fixed crash if the filename template in a sequence is edited to
  "/vol" [bug 44568]

* Increased speed of reading uncompressed half-float RGB/RGBA OpenEXR
  files [bug 44604]

* Renamed "Rec.2100: HLG 1.2 Gamma / Rec.2020 / Preview SDR Conversion
  200 nits (on 1000 nits)" colour space to have a name with a more
  sensible length [bug 44739]

* Fixed behaviour of "Fix DRT Behaviour" button when opening a scene
  with a custom/legacy DRT [bug 44720]

* Fixed issue with mouse click not working when in dual stereo display 
  mode in stereo scenes [bug 35347]

* Fixed the "Stereo Corr" button on Blackboard 2 [bug 44852]

* Fixed issue in Paint crashing when switching between operators 
  [bug 44351]

* Fixed issue in Paint where the last stroke colour was still 
  editable in read-only scenes [bug 44634]

* Fixed crash in Mattetool with non default configuration [bug 44633]

* Fixed crash in CDL grade when using group grade reset [bug 44989]

* Fixed Paint layer opacity and exposure slider not interactively
  updating [bug 44803]

* Fixed an issue that prevented some QuickTime files from being
  opened, e.g. screenrecordings made on iOS 11 [bug 45008]

* Blackboard devices can now be selected in bl-prefs [bug 44972]

* Fixed rare crash when gallery scene could not be opened [bug 44580]

* Fixed issue with Matte tool crashing when new stages are added and
  removed [bug 44990]

* Fixed Group Grade Reset behaviour for CDL Grade [bug 44638]

* Fixed bug where changing the burnin font setting would have no
  effect [bug 44080]

* Changed Text operator to show increased list of font options in Font
  menu [bug 44081]

* Fixed crash when joining shots [bug 44676]

* Fixed 48fps timeline timecodes becoming 30fps after re-opening the
  scene [bug 45099]

* Fixed incorrect naming of "mount" volumes in a zone when they are
  advertised to other systems.

  PLEASE NOTE: this fix may break existing scenes that use an
  unqualified volume path to access "mount" volumes remotely. This can
  be fixed by editing your volume.cfg file; please contact
  baselight-support@filmlight.ltd.uk for more information [bug 45065]

* Fixed the network interface which is used to access an advertised
  volume not listed in the local volume.cfg file [bug 45065]

* Fixed crash when cancelling a drag from a layer view with escape
  [bug 45042]

* Fixed incorrect creation of /images1 directory when installing
  Baselight before running fl-setup-pfs on a Baselight ONE with no SSD
  storage [bug 41207]

* Fixed crash in stereo scenes when clicking on the tracker list 
  dropdown [bug 44778]

* Fixed default burnin font [bug 45118]

* Fixed issue with Apply from a Blackboard or Slate not taking the 
  correct poster frame time [bug 44860]

* Improved the Colour Space Journey View message when converting from
  display-referred colour scene to a scene-referred viewing colour
  space [bug 39726]

* Fixed crash in FLUX Manage View if the Setup uses a saturated Error
  Cross Colour [bug 45201]

* Fixed artefacts in thumbnails sometimes seen when using Linearised
  image transform settings [bug 43951]

* Fixed incorrect timecode adjustment when splitting Bars and similar
  strips in a single-stack stereo scene [bug 44787]

* Fixed issue with paint strokes in scenes with formats that have 
  non square pixels [bug 44719]

* Fixed memory leak when rendering paint or grid warp [bug 45248]

* Fixed an issue where scenes created using templates were not picking
  up Shots View tab and filter settings from template [bug 45178]

* Fixed bug in VTRE where the "VTRE Deck Control" tab no longer
  appeared [bug 45313]

* Fixed bug in Denoise which could sometimes raise the black
  level of images, especially when colour spaces were incorrectly
  tagged [bug 44467]

* Fixed usage of ARRI Look files on multi-gpu systems [bug 43912]

* Improved speed of diagnostic tests [bug 45078]

* Variable retimes from FCP7 xmls now placed after transforms, meaning
  that transform keyframing is correctly reproduced [bug 44871]

--------------------------------------------------------------------------

Baselight Release 5.0.9853 (2017-10-03)

New Features Since Baselight 5.0.9842
=====================================

* The conversion of 4.4m1 jobs into 5.0 jobs requires the installation
  of Baselight 4.4m1.9850, available from the FilmLight website.

  This is a 'conversion' release, and should not be used for 4.4m1
  jobs, it only needs to be installed for this and later 5.0 releases
  to convert 4.4m1 jobs fully.

Bug Fixes Since Baselight 5.0.9842
==================================

* Fixed crash using "Set Timecode From Frame Number" in Shots View
  [bug 45074]

* Fixed a UTF-8 encoding issue in the conversion process of 4.4m1 jobs
  into 5.0 jobs [bug 45067]

--------------------------------------------------------------------------

Baselight Release 5.0.9842 (2017-09-28)

Bug Fixes Since Baselight 5.0.9754
==================================

* Fixed an issue that could cause FLUX Manage to fail to show all the 
  available sequences and movies in a directory [bug 44789]

* Fixed an issue that could cause FLUX Manage to report the file size
  of some movies to be zero [bug 44795]

* Fixed crash when attempting to track missing media [bug 44767]

* Fixed crash in FLUX Manage after using a USB device in Chalk for
  Slate [bug 44839]

* Fixed pattern matching in conform for subdirectories and file names
  that could cause some files to be ignored incorrectly [bug 44625]

* Changed event track in exported CMX EDLs from "V1" to "V" 
  [bug 44804]

* Fixed metadata loss through Shader operator [bug 44945]

* Fixed colour spaces not being correctly embedded in scenes when they
  are saved, which can cause failures to load when loaded on other
  systems without the necessary spaces installed [bug 45010]

* Fixed bug which made it difficult to select text to edit in the LUT
  export panel's 'Name' control [bug 44806]

* Fixed memory leak in burnin [bug 44988]

* Fixed playback issues when Paint Colour brush was selected 
  [bug 45007]

--------------------------------------------------------------------------

Baselight Release 5.0.9754 (2017-09-07)

New Features Since Baselight 4.4m1.9553
=======================================

PLEASE NOTE: Upgrading Scenes 주의사항 : 업그레이드 씬 안내

-----------------------------

* Baselight 5.0 currently cannot open scenes from earlier releases of
  the software. Instead, existing jobs need to be upgraded to the new
  database storage back-end (see "Scene Storage" below).

  To do this upgrading, Baselight 5.0 uses Baselight 4.4m1.9747 as a
  helper application. You must have this 4.4m1 build installed on your
  system if you wish to upgrade or import pre-v5.0 scenes & jobs.

  This requirement will be removed in a later Baselight 5.0 release.

Base Grade 베이스 그레이드

----------

* Base Grade is a new grading operator which works in a linear colour
  space modeled on human perception, thus ensuring that changes to
  tint and saturation have the same apparent effect regardless of the
  colour they are applied to. 
  베이스그레이드는 인간의 지각체계를 모델로 한 선형 색공간(linear colorspace)에서 작동하는 새로운 색보정 오퍼레이터(operator)이므로 색조(tint)와 채도(saturation)의 변경사항이 적용된 색상과 관계없이 동일한 이미지 결과를 보장합니다. 


* Base Grade is colour-space aware, converting appropriately to its
  internal space, so it retains the same feel regardless of the
  working colour space. However, this makes it extremely important
  that the user is accurate when tagging input material with a colour
  space - if input material is incorrectly tagged, then Base Grade
  will use an incorrect conversion to/from its internal grading space
  and will therefore feel odd.  
  베이스그레이드에서는 색공간을 인식하여 내부 색공간에서 적절하게 변환하므로, 작업 색공간들(Working colour spaces)과 관계없이 동일한 느낌을 유지할 수 있습니다. 그러나 이는 입력소스의 색공간을 정보를 업데이트(tagging)할 때 컬러리스트는 정확하게 해야하는 것이 매우 중요하게 되었습니다. - 만일 입력소스의 잘못된 정보가 업데이트되면 베이스그레이드는 내부 색공간의 잘못된 변환을 사용하여 이상하게 느껴질 수 있습니다. 


  For this reason, Base Grade is often used first in a stack, when the
  input to the Base Grade operator accurately reflects the working
  space of the scene. If you wish to use Base Grade lower down the
  stack, after something which makes a large contrast change, it will
  likely be necessary to insert a ColourSpace operator in "Identify"
  mode before the Base Grade to ensure that the Base Grade performs
  the correct conversions. So, for example, if the stack contains a
  Truelight operator which converts from ARRI LogC Wide Gamut to P3,
  then a Colour Space operator in "Identify" mode with "Convert To"
  set to "DCI: 2.6 Gamma / P3 DCI" should be inserted after the
  Truelight operator and before the Base Grade. 
이러한 이유로 베이스그레이드는 입력에서 베이스그레이드 오퍼레이터 순으로 씬의 작업색공간(워킹 컬러스페이스)으로 정확히 반영할때 종종 첫번째 사용됩니다. 만일 베이스그레이드를 스택 아래에 사용한다면 콘트라스트(명암비)를 크게 변경한후 베이스그레이드가 올바른 변환을 수행할 수 있도록 베이스그레이드보다 “Identify”모드에 Colour Space(색공간) 오퍼레이터를 삽입해야 할 수 있습니다. 예를 들면 스택에 ARRI LogC Wide Gamut에서 P3 로 변환하는 Truelight 오퍼레이터가  포함된 경우, “Convert To”가 “DCI : 2.6 Gamma / P3 DCI” 로 설정된 “Identify”모드의 컬러스페이스 오퍼레이터가 Truelight 오퍼레이터 후와 베이스그레이드 전에 삽입되어야 합니다. 


* Base Grade has four settings which affect the entire image: 
  베이스그레이드는 전체 이미지에 영향을 주는 4가지 설정이 있습니다. 


    - Flare: Sets the zero level by modifying the lower part of the
             tone curve. Everything lying at the zero level will be
             unaffected by exposure changes.
    - Balance: Overall exposure and two tint axes.
    - Contrast: The overall contrast of the image, around the
             Control Pivot setting.
    - Saturation: The overall colourfulness of the image. 
    - 플레어 : 톤커브의 하단부분을 수정하여 제로 레벨을 설정합니다. 제로 레벨에 놓여진 모든 데이터는 노출의 변화에 영향을 받지 않습니다.
   - 발란스 : 전체적인 노출과 두개의 틴트(색조)축
   - 콘트라스트 : 이미지의 전체적인 명암비, 컨트롤 피벗 설정 주위
   - 새츄레이션 : 이미지의 모든 컬러 영역 


* In addition, there are 4 additional "zones", each representing a
  part of the tone curve - Dark, Dim, Light and Bright. Each zone has
  the following settings: 
추가적으로, 다크(Dark), 딤(Dim), 라이트(Light), 브라이트(Bright) 톤커브의 부분을 나타내는 4가지 추가적인 “Zone”이 있습니다. 각 영역(zone)은 설정은 다음과 같습니다. 


    - Exposure + Tint: Localised exposure and tint change applied
             to the zone. The full effect is only realised once past
             the falloff area.
    - Pivot: Point in the tone curve where the localised changes
             begin to take effect.
    - Falloff: How quickly the full localised effect of the zone
             correction is reached.
    - Saturation: The colourfulness of the zone.
 - 노출+색조 : 적용된 영역에만 국한된 노출과 색조 변화, 전체 효과는 최근에 감소된 영역을 지나 한번만 구현됩니다.  
   - 피벗 : 지역적인 변화되기 시작하는 톤커브의 포인트
   - 감소(폴오프) : 얼마나 빨리 영역 수정의 전체 지역화된 효과가 빨리 도달하는지
   - 채도 : 색의 영역 


* All Exposure and Pivot values are expressed in stops relative to the
  18% grey card. This scale was chosen because it is familiar to both
  cinematographers and colourists. 
  모든 노출과 피벗값은 18% 그레이 카드의 기준으로 노출값으로 표시합니다. 이 스케일(비율)은 촬영감독과 컬러리스트 모두에게 익숙하기 때문에 선택하게 되었습니다. 


* The axes of the graph representing the effect of the Base Grade are
  also expressed in stops relative to 18% grey. 
  베이스그레이드의 효과를 나타내는 그래프의 축은 18% 그레이 기준으로 노출값으로 표현됩니다.


* A luma waveform, again expressed in stops relative to 18% grey, is
  drawn behind the graph and pivot lines. This makes it very easy to
  position pivot points in areas of the tone curve which have very few
  pixels, allowing large changes in a zone's exposure to be made
  without introducing artefacts. 
  루마(밝기) 웨이브폼, 그래프와 피벗라인뒤에  18% 그레이를 기준으로 노출값으로 다시 표현됩니다. 이렇게 하면 매우 적은 픽셀를 가지고 톤커브의 영역에 피벗포인트를 위치하는게 시워지므로 인위적인 표현없이 영역의 노출에서 큰 변경을 할 수 있습니다. 


* When in trackball mode, all of the parameters relevant for a given
  zone can be manipulated directly from a single trackball. By
  default, the trackball ring controls the Exposure. However the
  Pivot, Falloff and Saturation can be temporarily manipulated by
  holding down the modifier buttons lying directly above the
  trackball. 
  트랙볼모드일때, 특정영역과 관련된 모든 파라미터를 단일 트랙볼에서 직접 조작할 수 있습니다.
 기본적으로 트랙볼의 링은 노출을 제어합니다. 그러나 피벗, 폴오프(감소), 채도는 트랙볼 바로 위의 수정버튼이 눌러진 상태에서만 일시적으로 조작할 수 있습니다. 


* Base Grade introduces a new on-screen colour wheel control, with the
  following advantages:
    - Dragging in the colour wheel area now applies a smaller relative
      change, rather than exactly following the mouse cursor. This
      makes making subtle corrections using only the mouse much more
      convenient.
    - There is now a virtual trackball ring around the colour wheel,
      any part of which can be dragging in a clockwise/ anti-clockwise
      fashion to raise/lower the exposure in a zone.
    - The size of the master correction is now shown as a blue arc
      drawn superimposed over the left hand side of the virtual
      trackball ring. This is much more visible than the old standard
      slider and also saves space.
    - Secondary parameters for a zone like Pivot, Falloff and
      Saturation are represented by text boxes to the bottom-right of
      the virtual trackball. They can be directly manipulated by using
      the new gestural grading functionality.
베이스그레이드는 다음과 같은 장점을 가진 새로운 온 스크린 컬러휠 컨트롤을 도입했습니다.
   - 컬러휠의 영역에서 그래그(볼을 돌리면)하면 마우스커서 따라가는게 아니라 보다 작은 변화가 적용됩니다. 이렇게 하면 훨씬 편리하게 마우스를 사용하여 미묘한 수정을 할 수 있습니다.
   - 컬러휠주위에 가상의 트랙볼링이 감싸고 있으며 여기를 잡고 시계방향/ 반시계방향을 드래그하면 영역의 노출을 높이거나 낮출수 있습니다. 
   - 마스터 보정의 크기가 가상의 트랙볼의 원쪽에 겹쳐져서 그려진 파란색 호(아크) 형태로 표시됩니다. 이것은 기본의 표준 슬라이더보다 가시적이며 GUI의 공간을 절약합니다. 
  - 피벗, 폴오프, 채도와 같은 영역의 보조 파라미터는 GUI의 가상트랙볼의 오른쪽 하단의 텍스트상자로 표시됩니다. 새로운 제스쳐 그레이딩 기능을 사용하여 직접 조작할 수 있습니다. 



* Base Grade supports colour matching, making match-grading of similar
  shots much more convenient. Below the graph, there is a colour well
  representing the colour to match against - by default it is 18%
  grey. To change the match colour, simply enable the "Pick" toggle
  and drag in the image viewer - it will sample pixels from the
  *output* of the Base Grade and store the average of the drag in the
  colour well. If you want to edit this colour, or match a specific
  sRGB colour, simply click the colour well to launch Baselight's
  standard view. 
  베이스그레이드는 컬러매칭을 지원하므로 비슷한 샷의 매칭그레이딩을 할때 훨씬 편리합니다. 그래프 아래 일치시킬 색상을 나타내는 색상 표시가 있으며 기본적으로 18% 그레이 입니다.
 일치될 생각을 변경하려면, “Pick”(선택) 토글(동그란) 버튼을 활성화하고 이미지 뷰어에서 그래그만 하면 베이스그레이드의 *출력*에서 픽셀을 샘플링 추출하고 드래그한 색의 평균값을 픽옆의 박스에 저장합니다. 이 색상을 편집하거나 특정 sRGB 색상과 일치시키려면 색상박스를 클릭하면 베이스라이트의 표준뷰어가 실행됩니다. 


  To match this colour, enable the "Match" toggle (it will switch on
  automatically after a successful "Pick" drag) and in the same or
  another Base Grade instance, simply drag in the image viewer - the
  Base Grade settings will be updated to make the average colour of
  the dragged area match the previously picked colour.  
색을 매칭시키기 위해서, “매치(일치)” 토글 버튼을 활성화시키고(성공적으로 ‘픽’이 드래그된후 자동으로 활성화됩니다.) 동일한 또는 다른 베이스그레이드 인스턴스에서 단순히 이미지 뷰어에서 드래그하면 베이스그레이드설정이 드래그된 영역의 평균 색상으로 업데이트되어 이전에 선택한 색상과 일치하게 됩니다.  


FLUX Manage 플럭스 매니지(관리)

-----------

* A new graphical file manager replaces the Sequence Browser and the
  flux application. 
새로운 그래픽 파일 관리자가 시퀀스 브라우저와 플럭스 프로그램을 대체 합니다. 

  The main FLUX Manage view shows tabs on one or both sides of an
  information area. 
플럭스 매니지의 메인뷰는 정보 영역을 한면 또는 양쪽명으로 보여줄 수 있습니다. 


  The tabbed views are where the file system searching, filtering and
  management is controlled. 
탭뷰영역은 파일시스템의 검색, 필터링과 관리가 제어되는 영역입니다.

  Browser Tab 브라우저탭

  -----------

  The initial Browser Tab shows a standard volume and file browser at
  the top with a view below showing the sequences found in the
  selected directory. 초기 부라우저 탭은 상단에 스토리지(볼륨)과 파일 브라우저를 보여주며, 아래의 보기에서는 선택한 디렉토리내의 시퀀스파일을 보여줍니다.  


  The file browser allows multiple selection using ctrl-click
  (command-click on Mac).
파일 브라우저는 컨트롤+클릭(Ctrl+Click)사용하면 다중 선택할 수 있습니다. (맥OSX의 경우 CMD+Click)


  The controls at the top of the sequence view are: 
시퀀스보기의 위쪽에는 설정이 있습니다. 


  - view buttons which change the display between a grid of sequence
    thumbnails, a list of sequences showing additional metadata and a
    list of non-sequence files. 
보기 버튼은 시퀀스 썸네일(작은미리보기) 격자표시와 추가적인 메타데이터를 볼수 있는 시퀀스 리스트와 시퀀스파일이 아닌 리스트 사이에서 변경하여 볼 수 있습니다. 


  - a Pivot button which shows the breakdown of all the metadata in
    the displayed sequences, and allows selection based on metadata.
    Double-clicking opens a new filter tab using the selected
    sequences.
표시된 시퀀스파일의 모든 메타데이터로 분류되어 보여주는 피벗 버튼이 있으며, 메타데이터기반으로 선택을 허용합니다. 선택된 시퀀스를 사용하여 새로운 필터탭을 열 수 있습니다.


  - a filter button which creates a filter tab using all the sequences
    and adds a filename filter to allow selection by filename.
필터버튼은 모든 시퀀스 파일을 사용하여 필터탭을 만들고 파일이름을 선택하여 파일이름 필터를 추가할 수 있습니다.


  - a draggable tile representing all the sequences. On the left side
    of this tile is a pin which allows these sequences to be retained
    and added to another search from another browser directory. 드래그가능한 타일로 모든 시퀀스를 나타낼 수 있습니다. 이 타일의 왼쪽에는 이러한 시퀀스를 유지하고 다른 브라우저 디렉토리로부터 다른 검색을 추가할 수 있게 해주는 핀이 있습니다.


  - a Descend button which causes all subdirectories of the selected
    directory to be searched. This can be slow on an unindexed
    filesystem.선택한 디렉토리의 모든 하위 디렉토리를 검색하게 하는 Descend(내림) 버튼이 있으며, 인덱싱이 되지 않은 파일시스템의 경우 느릴 수 있습니다. 


  - a refresh button to re-scan the directory. 디렉토리를 재스캔하는 Refresh(리프레쉬) 버튼


  Under this are the sequences, with a control at the top right to
  select which metadata is displayed. 그 아래에는 시퀀스 파일들이 있으며, 오른쪽 상단 제어부분에서 메타데이터가 표시된 부분을 선택할 수 있습니다. 


  Managing Sequences 시퀀스 관리

  ------------------

  Anything which represents one or more sequences (including a
  thumbnail, multiple selected thumbnails, any sequence tile, a scene
  or a job from the Job Manager, a directory from the file browser)
  can be right-clicked or dragged in order to filter the selection or
  to perform an action on the sequences, such as copying them to
  another location or erasing them. 
썸네일, 다중선택한 썸네일, 시퀀스 타일, 씬, 또는 잡매니저로 부터의 잡 파일브라우저로부터의 디렉토리 포함한 하나 또는 그이상의 시퀀스를 표시하여 마우스 오른쪽 버튼을 클릭하거나 그래그하여 선택된 파일을 필터링하거나 다른 곳으로 복사하거나 삭제할 수 있습니다.


  - drop onto a directory in the file browser at the top to copy to
    that directory.
파일 브라우저의 맨위에 있는 디렉토리로 넣어서 해당 디렉토리를 복사할 수 있습니다. 


  - drop onto a directory in the Copy Destinations area to copy to
    that directory.
Copy Destination(복사 목적지) 디렉토리 영역에 디렉토리를 넣어서 복사를 합니다.


  - drop onto the Action Bar which appears at the bottom of the window
    to filter, convert, copy or erase.
플럭스 창아래로 파일/디렉토리를 드래그하면 액션바가 나오며 필터, 변환, 복사, 삭제등이 가능합니다.


  Filter Tab 필터탭

  ----------

  FLUX Manage introduces a powerful filtering mechanism to allow you
  to locate precisely the sequences you wish to find, with an
  intuitive graphical filter editor. 
플럭스 매니지에서는 강력한 필터링 매커니즘을 도입하여 직관적인 그래픽기반의 필터에디터를 가지고 찾고자 하는 시퀀스를 정확하게 찾을 수 있습니다. 


  A Filter Tab is started with a collection of sequences you wish to
  filter. This can be done in several ways:
Filter Tab(필터탭)은 필터링을 원하는 시퀀스를 모은 것으로 부터 시박됩니다. 이것은 여러가지 방법을 할 수 있습니다. 


  - right-click on a sequence thumbnail, or any tile representing a
    set of sequences and choose "View or Filter".
시퀀스 썸네일을 마우스 오른쪽 클릭하거나 시퀀스 형태로 된 타일들을 선택한 후 ‘뷰 또는 필터’(View or Filter)를 선택합니다.


  - drag sequences to the Action Bar and drop on "View or Filter".
시퀀스를 하단의 액션바로 드래그하여 “뷰 또는 필터”에 내려놓습니다.

  - drag a filter tile from the Tile Library over the sequence view.
타일 라이브러리로 부터 필터 타일을 시퀀스 뷰 위에 드래그합니다. 

  - drag a metadata name over the sequence view.
시퀀스뷰위의 메터데이터 이름을 드래그 합니다.

  - double-click a value in the Pivot view.
피봇뷰의 값을 더블 클릭합니다.

  - press the F key to start creating a filter from the keyboard.
키보드에서 F키를 눌러서 필터를 생성합니다.

  - press the S key to start creating a sort filter from the keyboard.
키보드에서 S키를 눌러서 정렬 필터를 생성합니다.

  A Filter Tab shows, from top to bottom: 
 필터탭은 위에서 아래로 봅니다.

  - a draggable tile representing the result of the filter. This tile
    contains the specific sequences which are the result of the
    filter; this collection of sequences will not change if the
    filesystem changes.

  - a Recalculate button which clears the calculated filter results
    and regenerates them. This may be a slow operation if it requires
    scanning the file system, or scenes.

  - Undo and Redo buttons which step through your changes in the
    filter editor.

  - the Filter Editor.

  - a sequence view which is very similar to the sequence view on a
    Browser Tab, but without some of the additional controls on the
    top bar.

  Double-click on the tab itself to rename it.

  Filter Editor 필터 에디터
  -------------

  The Filter Editor is where FLUX Manage filters are constructed.

  Drag a tile over an existing tile in the Filter Editor to add it to
  the filter.

  Often a tile can be applied in more than one way (e.g. the Tape
  filter can either filter the sequences by Tape, or sort the
  sequences by Tape) - if so the tile is split into drop zones which
  are described above the tile.

  Right-click on a tile to edit or remove it. Many tiles also allow
  double-click to edit.

  Many filters can be applied using a variety of tests. Numeric
  filters such as Width can use less-than, greater-than, equal-to etc.
  Textual filters such as Tape can use equal-to, not-equal-to and
  regular expression comparison to look for parts of words (e.g.
  matching Tape against A will show all sequences whose Tape contains
  the letter A). Regular expression syntax such as ^A\d may be used.

  Filters may be dropped to expand ("or") or restrict ("and") the
  selection, or to refine the sort order ("then").

  Sequence tiles may be dropped to add ("plus") or subtract ("except")
  the sequences. This allows filters like "all sequences in these
  three directories except the ones used by these scenes".

  Dropping a single sequence offers the "Match Metadata" drop zone to
  quickly filter to match by one or more metadata value.

  The Information Area 정보영역
  --------------------

  The information area contains, from top to bottom:

  - a button to open the Tile Library, a text field for searching the
    Tile Library, and view buttons to control whether a tabbed view is
    shown to the left, right or on both sides. Having two views can be
    useful when copying media from one volume to another.

  - the Tile Library (initially hidden) containing draggable filter
    tiles which can be used to construct filtering operations.

  - a draggable tile representing the currently selected sequence(s).

  - metadata for the currently-selected sequence. If more than one
    sequence is selected, metadata is shown for the last-clicked
    sequence, indicated by a dashed selection box.

    Most metadata names (e.g. Encoding, Tape etc) can be dragged to
    create a filter matching the value of that metadata for the
    selected sequence.

  - a list of keyboard shortcuts that are currently available.

  - Copy Destinations, where directories can be dropped for ease of
    access.

  - Operation History, where queued operations submitted from FLUX
    Manage are shown, and from which the Queue Monitor View can be
    opened.

  - Preview and Play buttons which present the currently-selected
    sequence(s) on the main Baselight display.

  File Operations 파일 오퍼레이션 
  ---------------

  Operations to copy, convert and erase sequences are submitted to the
  Operations Queue and performed by the flux service (just as
  Consolidate copies were in Baselight 4.4m1). There is no need to
  leave FLUX Manage or Baselight running while these operations are in
  progress.

  Using FLUX Manage to insert Sequences in Baselight 플럭스 매니지를 사용하여 시퀀스 파일을 베이스라이트에 삽입하기
  --------------------------------------------------

  - double-clicking on a sequence thumbnail inserts it into the scene.

  - double-clicking on an all-sequence tile inserts all the sequences
    into the scene.

  - sequences can be dragged and dropped onto the Timeline View or
    Cuts View to insert into the scene.

  - scrubbing a thumbnail displays the sequence on the main Baselight
    display, in the same way as scrubbing in the Gallery View or Cuts
    View.

  A row of controls at the bottom of FLUX Manage View allows:

  - Channel/Track and View options which show the OpenEXR
    channels/layers and views for the selected sequences and which
    both change all thumbnails to use these settings and control the
    behaviour of the sequences when inserted into a scene

  - Colour Space, Format and Frame Rate options to control the
    behaviour of the sequences when inserted into a scene.

  - Insert button to insert the selected sequence(s) into the scene.

Compress Gamut 색공간 압축(컴프레스 개멋)
--------------

* The new Compress Gamut operator fixes strange colour effects in
  saturated colours from very small or negative RGB values. Turn up
  the threshold to see the effect. 0.1 is a typical threshold setting.
새로운 컴프레스 개멋(색공간 압축) 오퍼레이터는 채도가 너무 많은 색상영역에서의 낯선 색효과를 매우 작거나 또는 마이너스된 RGB 수치값을 수정합니다. 효과를 보기위해서 한계점(threshold)를 조정해야 하며, 일반적인 한계점 설정은 0.1 입니다. 




  Suppose you point a camera at a scene with a bright yellow light.
  The camera records sensible raw red and green signals from the
  yellow light, but the raw blue may be little more than noise. When
  the raw signals are converted to image RGB, the blue channel may be
  very noisy, clipped, or negative. Subsequent grades may make this
  worse.
밝은 옐로우 광원이 있는 씬에 카메라 있다고 가정해 봅니다. 카메라는 옐로우 광원으로 부터 감지할 수 있는 raw 레드와 그린 신호를 기록하지만, raw 블루의 경우 노이즈가 약간 있을 수 있습니다. raw 신호가 이미지의 RGB로 변환될때, 블루 채널은 매우 노이즈가 있는 상태 있거나, 클립되어 있거나 또는 네거티브(음수)상태입니다. 후속적인 보정작업은 이를 악화시킬수 있습니다. 


  In this yellow light case, Compress Gamut picks up when the B value
  is much less than max(R,G), and applies a smooth function to map all
  small and negative values onto small positive values. 
이런 옐로우 광원경우는, 컴프레스 개멋(색공간 압축)는 최대 레드, 그린값보다 블루 값을 적게하고, 모든  작은 수치값을 조절하여 부드럽게 매핑하고, 네거티브 값을 작은 포지티브(양수)값으로 변환하는 것입니다. 


Texture Equaliser 텍스쳐(질감 또는 표면) 이퀄라이져
-----------------

* The new Texture Equaliser operator divides the image into a set of
  spatial frequency bands. 
새로운 텍스쳐 이퀄라이져 오퍼레이터는 이미지를 공간 주파수 대역의 집합으로 나눕니다.


  Each frequency band has a separate Gain control. Each Gain control
  scales the signal in its frequency band. This can be used to
  smooth or enhance textures such as flesh tones in each band. The
  default 1.0 setting gives no scaling. 각각의 주파수 대역은 별도의 게인 컨트롤을 가집니다. 각 게인 컨트롤은 해당 주파수 대역의 신호의 크기를 조절합니다. 이 기능을 사용하여 각각의 대역에서 피부톤과 같은 질감을 부드럽게 하거나 강하게 표현할 수 있습니다. 기본 설정인 1.0에선 크기조절이 되어 있지 않습니다.


  The Threshold setting puts a soft limit on the gain. Sharp features
  such as edges have a large component in each band. We do not usually
  want to change the gain on these features. The default setting lets
  us change our textures, without changing the sharp features too
  much.임계값 설정의 경우 게인에서 부드러운 제한이 적용되어 있습니다. 엣지와 같이 샤픈 기능은 각각의 대역에서 큰 값을 설정하면 됩니다. 


  Example: If we reduce the Gain on the 2:1, 4:1 and 8:1 bands, this
  will smooth skin tones, but preserve the texture of the pores and
  other fine detail. Increasing the Gain on the 16:1 band may restore
  some of the shadow modelling. Use a mask to restrict the filter to
  the face we wish to smooth.

Texture Blend 텍스쳐 블랜드
-------------

* The new Texture Blend operator divides each image into a set of
  spatial frequency bands. Each frequency band has a separate Blend
  control. This allows you to get a smooth join between two images
  with a sharp-edged matte.

Denoise 디노이즈
-------

* A new, third-generation Denoise operator replaces the earlier
  Denoise function seen in Baselight 4.4m1. The controls have been
  re-arranged to give a better separation between the spatial and the
  temporal passes. The controls are disabled until you pick your
  sample region. The pick should give better performance with the
  default settings. There are options to track moving detail using
  optical flow; this can give better results, but is slower.

  The denoiser tries to remove noise while preserving features like
  edges that extend over many pixels, and/or several frames. The first
  and last frames may not have the full set of neighbours, so start on
  a frame in the middle of a sequence before setting the controls.

  Denoise can be used anywhere in the stack, but is best used on raw
  image data, before any colour or spatial operations. If your image
  has a fixed pattern, a filter tuned to remove this pattern will do a
  better job than this general purpose filter, and this will give the
  denoiser a better chance. You might usefully put something like the
  Nyquist filter before Denoise. If your sequence has filter options,
  you may want to try those too: a filter for a specific camera may be
  more effective than a general tool.

  The Denoise tool starts off disabled, with Pick set to 'None'. You
  need to drag a rectangle over a featureless region on the image to
  sample the noise. This rectangle must be bigger than 16x16 pixels,
  but does not have to be huge. A second drag will overwrite the
  previous one. If you are happy with you pick, set Pick to 'Locked'.
  This will protect it against accidental overwrites if you click on
  the image.

  You may get a warning about detail within the pick. There may be
  some texture or fine detail that you could not see until the noise
  was removed. Or you may deliberately pick some subtle features that
  are on the limits of the ones you want to keep. If you are happy
  with what the filter is doing, you can ignore this warning. If there
  are problems, click on the Pick '?' help button for more details.

  Next, set the Denoise Level control. A larger value takes out more
  noise, but may remove image detail too.

  Removing noise from an image can make it look softer, even if no
  real detail has gone. Resharpen may restore some of the look of the
  original image.

  The Temporal filter has several modes. The 3-frame integer fit is
  the fastest option that gives good results. The flow options are
  slower, but can give better results with steadily moving features.
  The 1-frame setting turns off all temporal processing. This is
  faster, but not as good at removing noise. It is mainly used as a
  diagnostic to distinguish the Spatial filtering from the Temporal
  filtering.

  The Temporal filter uses the Frame Threshold. Increasing this
  removes more noise, but you may lose sharpness, or introduce 'ghost'
  edges from other frames. The default value is good for the 3-frame
  modes, but this setting becomes more critical when you use more
  frames.

  For most material, that should be all you need to do.

  There are three sections of Advanced settings. These parameters were
  used for development, and have been retained as they may help with
  exceptional images.

  Advanced Colour sets the luma-chroma colour space the Denoiser works
  in. Quiet scales all the internal colour space values. Tone Bias
  changes the power law, favouring the highlights or the shadows.
  Chroma bias scales the chroma values, so you can denoise the chroma
  channels more than the luma. There are also three sliders for
  blending a fraction of the original image in this luma-chroma colour
  space.

  Advanced Spatial sets up the Denoise first pass that works on a
  single frame. Advanced Temporal sets the Denoise second pass that
  can use several frames.

Boost Contrast 부스트 콘트라스트
--------------

* The new Boost Contrast operator boosts the contrast in the midtones.
  The effect is similar to a Sharpen with a very large radius, but it
  is rolled off for the highlight and shadow tones to keep the fringe
  values in gamut.

  The Gain control varies the amount of sharpening. A zero value gives
  no effect. A negative value makes the image softer.

  The blur radius is set to a useful default value for the gain. You
  can scale the blur radius using the Scale control in the Advanced
  settings. A Scale of zero gives no effect. This filter uses very
  large blurs: if you are not hitting rate, try a smaller Scale
  setting.

  The anamorphic control can be used to correct for non-square pixels.
  This may not be necessary: even if you are working with 2:1
  anamorphic material the elliptical correction can look good.

Boost Colour 부스트 컬러
------------

* The new Boost Colour operator boosts the saturation for the
  mid-gamut colours in the usual way, but this boost is rolled off
  toward the gamut limits, so we do not get unrealistic saturation in
  highlights, bright colours, and flesh tones.

Boost Shadows 부스트 쉐도우 
-------------

* The new Boost Shadows operator scales the dark values in extended
  shadows. This is to simulate our eyes' adaption as they scan from
  highlights to shadows in the original scene with the original
  extended contrast radius.

Shader 쉐이더
------

* The new Shader operator allows Autodesk Matchbox shaders to be used
  in Baselight. This provides a powerful way to extend Baselight's
  functionality using a simple established cross-platform mechanism.

  A set of "crok" shaders from logik-matchbook.org are installed with
  Baselight. Please note that these shaders are not supported by
  FilmLight, and that bugs or incompatibilities may prevent them from
  working in Baselight.

  Additional shaders may be downloaded from logik-matchbook.org, but
  note in particular that many of these shaders are not licensed for
  commercial use [bug 32178]

Grid Warp 그리도 워프 
---------

* The Grid Warp operator can be used to warp/distort areas of a
  sequence by modifying 2 grids of control points (CPs): the "Source"
  grid & "Destination" grid. These 2 grids are accessed separately
  from the 2 tabs in operator's parameter controls.

  Image pixels under the CPs of the source grid will be warped to the
  position of the matching CP of the destination grid.

  Both the source & destination grids share a transform (which can be
  tracked). You can toggle between editing the grid CPs & the
  transform by clicking in the space between the CPs.

  You can also explicitly drag out a rectangle for the grid's transform
  on the image using the "Set New Transform Rectangle" button.

  Adding/Removing Control Points & Grid Lines 제어점과 그리드 라인을 추가/삭제
  -------------------------------------------

  Both grids always have the same number of CPs. You can add a new CP
  by holding the Windows keyboard modifier (Ctrl on a Mac) & clicking
  where you want to add a CP. A complementary CP will be automatically
  added to the other grid.

  You can remove a CP (or grid line) by holding down the Windows+Shift
  modifiers and clicking on the CP (or grid line).

  Editing Control Points & Handles 제어점과 핸들 편집
  --------------------------------

  By default, CP handles are hidden and automatically calculated based
  on the position of the CP itself. Handles can be manually edited by
  switching off the "Auto Handles" option. Once disabled, handles
  become visible & draggable. Handles can be individually adjusted by
  holding down the Ctrl modifier (Cmd on a Mac) whilst dragging a
  handle endpoint.

  Multiple CPs can be selected for movement by dragging out a
  selection rectangle. Additional CPs can be added to the selection by
  holding down the Ctrl modifier & dragging out another rectangle. CPs
  can be removed from the selection by holding down Shift & dragging
  out a rectangle over the CPs to be excluded.

  To reset the selection, drag out a small rectangle between the CPs.

  Blackboard/Slate Support 블랙보드/슬레이트 지원 
  ------------------------

  These desks have additional controls for streamlining common grid
  editing operations. For example:

  Left Trackball        Modify the position of the currently selected
                        control point (or control points).
  Middle Trackball      Modify the translation/rotation of the grid's
                        transform.
  Right Trackball       Modify the scale of the grid's transform.

  There are also explicit buttons/encoders for selecting/modifying
  rows and columns of control points, hiding overlays etc.

  Example Workflows
  -----------------

  1. Modify the destination grid/transform only - For basic warps, the
     source grid/tab can be ignored completely. Simply position the
     (destination) transform to cover the image area to warp and
     add/modify CPs on the grid to achieve the desired result.

  2. Setup source/destination CPs *before* warping the image - To do
     this, first go to the "Source" page. You will see an additional
     toggle button - "Sync Destination Grid To Source" When enabled,
     any modifications you make to the source grid will be
     automatically copied to the destination grid. When the 2 grids
     are the same, the warp has no effect on the image. So, with this
     option enabled you can use the source grid to initially
     position/add/remove CPs in & around areas you wish to affect
     without modifying the image.

     To then warp the image, return the the destination grid & adjust
     the CPs from there.

Paint 페인트
-----

* A new Paint operator has been added. It has two distinct modes,
  Matte and Composite. 
새로운 페인트 오퍼레이터가 추가되었습니다. 이는 매트와 합성(컴포지트) 2가지 구별되는 모드가 있습니다. 

  Matte Mode 매트모드
  ----------

  Much like the Shape operator it can be used to add or remove areas
  from the matte using paint strokes.

  Each stroke is defined by a brush, where the width, hardness, and
  opacity can be set.

  The Paint operator can be added with the 'e' shortcut, selecting it
  from the Matte Operators grid or from the Blackboard/Slate. This
  means that the Dilate and Soften hotkey has been moved to shift-m
  from shift-e.

  Once the operator is added, strokes can be drawn directly onto the
  monitor (make sure the render mode is displaying matte channels).
  Layers can be managed by right clicking on the layer control. Brush
  size and softness can be adjusted via the brush controls but will
  only affect the next newly created stroke. The existing stroke's
  brush can be edited in the 'Existing Stroke' tab. This will change
  all the values in the current layer by a relative amount. The
  'Previous Stroke' tab will just change the previous strokes brush
  values.

  Strokes creation can be animated in the layer controls, so motion
  can be created with the addition and removal of areas. To turn the
  brush into an eraser click on the button next to the style drop down
  or press q.

  When drawing a stroke you can force the current line to be a
  straight line by holding down the shift key.

  Each layer also has a separate opacity control which can be
  keyframed.

  Each layer can be transformed and the transformation can be animated
  independently of each other. Each layer transform can also be
  attached to trackers allowing each layer to follow a different
  feature on the original image. This also allows the use of
  perspective planes. A perspective plane can be drawn and the 'area
  perspective' tracker used to define a 3d plane throughout the
  duration of the strip. Once a perspective plane has been defined
  then the cursor will follow the perspective plane and all stroke
  will be drawn in perspective. You can define a different perspective
  plane per layer. When creating a new layer the currently selected
  layer's perspective plane will be copied onto the new layer. This
  can be removed or adjusted with the perspective controls.

  Composite Mode 컴포지트 모드 
  --------------

  Paint can also be used in composite mode with the clone or colour
  brush. You can add a paint strip as a layer, click on the comp
  button, and start painting on the image. In Colour mode the colour
  can be selected by holding down the meta key and moving the mouse.
  The colour selected will match your mouse location. When in Clone
  mode the offset can be set by holding meta key and click and
  dragging out from the clone source to the desired painting location.
  You can add to your current offset by holding Meta + shift. If you
  have set a time offset then holding meta will show your source
  frame.

  Composite brush modes also have an additional parameter called
  exposure. This allows adjustment of the exposure values of the clone
  and colour strokes, so they can be match graded into place. This can
  be done either by setting an initial value or by switching to the
  'Previous Stroke' or 'Existing Strokes' Tab and editing the exposure
  values of the existing strokes. This is the same for other values of
  the brush as explained above in the Matte section. This allows to
  match grade the stroke in place on the image.

  The layer also has a separate keyframable exposure setting.

  The time offset can be set as an absolute value from the start of
  the strip, or as a relative offset from the current frame. To set
  the value either enter it in frames, move the mouse to the correct
  frame and click set, or hold down ctrl and windows key and drag the
  mouse left and right

Perspective 퍼스펙티브 (원근법)
-----------

* The Perspective operator allows an image to be transformed in
  perspective by specifying four points (In Corners) and their
  corresponding Out Corners.

  This operator is available through the 'Layer Mode' Menu in the
  Inside/Outside operator, by choosing 'Matte From Shape', 'Matte From
  Foreground Shape', or 'Matte From Foreground Alpha'. It can also be
  inserted as the last foreground operator or as a standalone strip,
  via the 'Insert' menu.

  The Perspective operator has 3 tabs:

  - 'In Corners', used to defined four independent screen corners
    representing a plane. They can be edited interactively, or via
    sliders. The 'New Quad' option can be used to define an axis
    aligned rectangle on the screen using dragging. The corners can be
    animated.
  - 'Transform' tab, a standard Transform used to reposition, scale,
    or rotate the image without affecting the In or Out planes.
  - 'Out Corners', used to defined the four independent screen
    corners, representing a plane. They can be edited the same way
    as the 'In Corners' tab.

  The 'Crop to Out Rectangle' option will turn on cropping to the Out
  Corners.

  The 'Show Grid' option displays an overlay which helps to position
  the quad according to the scene's natural geometry.

  The 'New Seq. Pick' option allows us to define a quadrilateral using
  four sequential picks (left click) on the image. The current picks
  can be discarded using right click if the quadrilateral is not
  complete.

  The Motion Blur option is designed to reintroduce blur due to motion.

  Tracking 트래킹
  --------

  The 'In Corners' and 'Out Corners' can be tracked independently
  using Perspective Trackers.

  A new 'Perspective Tracks' tab has been added to the tracker
  operator, which encapsulates either four Point Trackers on a
  perspective plane or a Perspective area tracker.

  Blackboard/Slate Support 블랙보드/슬레이트 지원
  ------------------------

  These desks have additional controls to edit the quadrilateral in the
  In / Out tabs or the standard transform in the Transform tab:

  Left Trackball        Modify the selected corner position
                        (In / Out tabs), of the currently selected
                        control point (or control points).

  Middle Trackball      Modify the translation (All tabs)
                        / rotate (Transform tab)

  Right Trackball       Modify the scale in X and Y / the scale in
                        X (All tabs).

  There are also explicit buttons for selecting the desired corner
  to modify using the left Trackball.

Perspective Plane 퍼스펙티브 플레인
-----------------

* Shapes, Grid Warp and Paint now have the ability to define a plane
  to work in perspective.

  The 'New Seq. Pick' option is used to define the plane using four
  sequential picks (left click) on the image. The current picks can be
  discarded using right click if the quadrilateral is not complete.

  The 'Show Grid' option displays an overlay to help positioning the
  quadrilateral according to the scene's natural geometry.

  The 'Plane' option will display/hide the plane overlay.

Tracker 트래커 
-------

* The Tracker strip now supports Perspective Trackers to track / lock
  controls to planes in 3D. This information is available in the
  'Perspective' tab.

  The Perspective information of the scene is extracted using one
  of two types of tracker: the '4 Point Persp.' or the
  'Area Persp.'. Both work with reference to one plane, albeit
  in a different manner:
  - The four Point Trackers can be positioned anywhere in that plane,
    as long as the tracked area stays still relative to that plane.
  - The Area Tracker created from a 'Area Tracker Persp.' will
    compute the motion using a perspective model in the selected
    area, the same way the Area Tracker extracts a 2D motion.

  The Perspective Track can be created only from within strips that
  support it, e.g., Shape, Perspective, Paint and Grid Warp. When the
  Perspective Track is linked to the current frame, the latter will
  not move and it will be used as a reference to obtain the relative
  position of the previous and next frames respectively.

  The Perspective Track can be converted from a Perspective Area
  Tracker to a four Point Tracker and vice versa.

  The Tracking widget (available in Shape, Transform, Paint and Grid
  Warp) has a new dropdown list indicating the trackers available to
  the tracker strips above the selected strip. Hovering the mouse over
  an entry will display the corresponding tracker overlay.

Mastering Colour Space 마스터링 컬러 스페이스 
----------------------

* Baselight is a floating-point colour corrector, and in the near
  future most DRTs will be formula-based. This means that the user can
  (and will) generate values outside of the display colour space used
  while grading. This happens when contrast and saturation are added to
  an image: strong saturated colours will be pushed far outside of the
  display colour space. While grading the signal is clipped on the SDI
  output signal. As this is an integer device, 'Out Of Gamut' colours
  will be clipped. But if the image gets rendered to a bigger colour
  space after grading (for example generating 'DCI XYZ' after grading
  in 'DCI P3') colours may be encoded in the deliverable which
  were not seen while grading. This is especially crucial in
  Telecine- or Video-Style Grading. 
 베이스라이트는 플로팅 포인트 기반의 색보정 소프트웨어이며, 대부분의 DRT는 가까운 미래에는 수식기반으로 변경될 것입니다. 이는 사용자가 색보정할때 보고 있는 디스플레이 컬러스페이스밖의 영역으로 값을 만들 수 있음을 의미합니다. 이미지를 명암이나 채도를 더하면 발생할 수 있습니다 : 강한 채도의 색상은 보여지는 디스플레이 컬러스페이스의 영역밖으로 멀리 밀려나며 색보정시 SDI 출력신호에서 클리핑(clipping)됩니다. SDI 출력장치는 정수형 장치이기 때문에 색영역밖의 색상은 잘리는 것입니다. 그러나 만일 색보정후 이미지를 더 큰 컬러스페이스로 랜더링함나면 색보정시 보지 못한 색상이 딜리버리를 위한 렌더링시 나올수 있습니다. (‘DCI P3’ 상태에서 색보정후 ‘DCI XYZ’으로 랜더링시) 이것은 텔레시네나 비디오스타일의 색보정시 특히 중요합니다. 


  In Baselight 5.0, a Mastering Colour Space can be specified which
  acts as the maximum allowed gamut. After the DRT or after the "Grade
  Result Colour Space", Baselight now clips to the gamut of the
  Mastering Colour Space. Its behaviour can be thought of as a 3D
  Colour Limiter. This clipping only applies in the display pipeline
  if the cursor or render colour space is a display-referred colour
  space.
 베이스라이트 5.0 버전 이후에는 마스터링 컬러스페이스는 최대한 허용 색영역으로 지정할 수 있습니다. DRT 또는 ‘색보정이후의 색영역’후, 베이스라이트는 마스터링 컬러스페이스 색영역으로 (클리핑되어) 넣어집니다. 이러한 과정은 3D 컬러 리미터처럼 생각될 수 있는데, 만일 커서 또는 랜더러 컬러스페이스가 디스플레이 연관 컬러스페이스라면 이러한 클리핑과정은 단지 보여지는 디스플레이 파이프라인에서만 적용됩니다. 


  The Mastering Colour Space is set in the Scene Setting for the whole
  scene. However when changing the display viewing condition, the user
  may also wish to change the Mastering Colour Space (e.g. because
  there is a different gamut for 48 nits vs 1000 nits). To simplify
  this, a specific Mastering Colour Space (and Mastering White Point)
  can be defined per in a DRT Family. Baselight then automatically
  chooses the Mastering Colour Space and Mastering White Point based
  on the Cursor or Deliverable colour space.
마스터링 색공간은 전체 씬을 위해서 씬설정(Scene Setting)메뉴에서 설정합니다. 그러나 디스플레이의 시청환경이 변화한다면, 사용자는 (예를 들면,영화의 48nit vs  HDR 1000nit 다른 색영역이 있기 때문에) 마스터링 색공간을 변경할 수 있습니다. 이를 단순히 하기 위해서, 특정 마스터링 색공간(과 마스터링 화이트 포인트)를 DRT 패밀리별로 정의내려 사용할 수 있습니다. 그러면 베이스라이트에서는 커서나 딜리버리 색공간을 기반으로 마스터링 컬러스페이스와 마스터링 화이트 포인트가 자동으로 선택됩니다. 


  The Mastering Colour Space setting can be found in the 'Advanced'
  Section of 'Scene Settings' -> 'Formats and Colour' [bug 35216]
마스터링 색공간 설정은 씬설정(Scene Setting) > 포맷과 컬러(Formats and Colour)의 하단 고급(Advanced)에서 찾을 수 있습니다. 


* In Baselight 4.4 the handling of the neutral axis was neglected. In
  the most cases, Baselight performed an implicit white-point remapping,
  but in some cases Baselight performed a white-point shift at the end
  of the chain (for display-referred colour spaces with a creative
  white-point). This meant that it was impossible for the colour grading
  operations to know what the white point in a given step was and that
  what R=G=B actually meant was not defined.
베이스라이트 4.4에서는 뉴트럴축(블랙부터 화이트까지 동일한 RGB값의 축)의 처리를 방치되어져 왔습니다. 대부분의 경우 베이스라이트는 절대적인 화이트포인트 리매핑을 수행했지만, 일부의 경우 베이스라이트는 (생성된(;따로 정의된) 화이트 포인트를 가진 디스플레이 참조 색공간을 위한) 작업과정 끝에 화이트포인트가 이동될 수 있었습니다. 이는 화이트 포인트를 주는 단계에서 R=G=B가 실제로 의미하는 바가 무엇인지 색보정과정에서 알 수 없다는 것을 의미했습니다. 


  This changes in Baselight 5.0. In the 'Mastering Colour Space'
  section the user specifies a 'Mastering White Point' for the scene.
  This tells the system what R=G=B in the stack should actually mean.베이스라이트 5.0에서 이부분이 변경됩니다. 마스터링 색공간 색션에서 사용자가 씬의 마스터링 화이트 포인트를 지정할 수 있습니다. 이것은 스택(Stack)에서 R=G=B(정의된 화이트포인트)가 실제로 어떠한지를 시스템에게 알려줍니다.


  This introduces several advantages:
이는 여러가지 장점이 있습니다. 

  - White-Point Handling on the Output 
출력에서 화이트 포인트 처리

    By knowing what R=G=B should mean from a creative standpoint,
    Baselight can displays the neutral axis consistently over a
    variety of actual display-referred colour spaces and automatically
    perform a correct white-point shift for displays which have a
    different white-point from the Mastering White Point. 
크리에이티브 관점에서 R=G=B가 어떻게 의미되는지 알면, 베이스라이트는 다양한 실제 디스플레이 참조 색공간에서 뉴트럴축을 일관되게 표시할 수 있으며, 마스터링 화이트 포인트에서 다른 화이트 포인트로 되어 있으며 디스플레이에서 자동으로 올바른 화이트포인트로 이동하여 표시합니다. 


    That also means Baselight no longer needs display-referred colour
    spaces with "creative white points", so they are removed
    in Baselight 5.0. 
베이스라이트에선 더이상 디스플레이 참조 색공간에서 크리에이티브 화이트 포인트(creative white point)가 필요하지 않으므로 베이스라이트 5.0버전 이후에는 제거되었습니다. 


  - White-Point Handling on the Input 입력에서 화이트 포인트 처리


    If scene-referred data is imported, it is rational to assume that
    R=G=B in the data should be mapped to R=G=B in the stack colour
    space. Thus it follows that scene-referred to scene-referred
    colour space conversions do not alter the neutral axis.씬 참조 데이터를 불러올때, 데이터의 R=G=B축이 스택 색공간의 R=G=B축으로 매핑되는게 합리적입니다. 따라서 씬참조(데이터) 에서 씬참조 색공간(스택) 변환과정에서 뉴트럴축의 변경을 일어나지 않습니다. 


    If display-referred data is imported into a scene-referred stack,
    Baselight assumes that the source will be graded. Thus it follows
    that display-referred to scene-referred colour space conversions
    do not alter the neutral axis. 디스플레이참조 데이터를 씬참조 스택(Stack)에 가져올 경우, 베이스라이트에서는 소스가 색보정 될 것이라고 추측합니다. 그러므로 디스플레이참조 에서 씬참조 색공 변환에도 뉴트럴축의 변경을 하지 않습니다.


    If display-referred data is imported into a display-referred
    stack, Baselight assumes that the user wants to see the image as
    it was authored. Thus it follows that display-referred to
    display-referred colour space conversion take the white-point of
    the input data and the white-point of the scene into account. 디스플레이참조 데이터가 디스플레이참조 스택으로 가져오면 베이스라이트에서는 사용자가 작업이 된  이미지를 보고 싶어한다고 추측합니다. 따라서 디스플레이참조 에서 디스플레이참조 색공간 변환과정에서 입력데이터의 화이트 포인트와 씬의 화이트 포인트를 고려합니다.


    The Colour Space Journey View shows the Mastering Colour Space and
    Mastering White Point in use [bug 35922]
색공간 프로세싱 뷰(컬러스페이스 져니 뷰) 에서 사용되는 마스터링 컬러스페이스와 마스터링 화이트 포인트를 보여줍니다. 


DRT Families DFT 패밀리
------------

* With the development of wide-gamut and High Dynamic Range displays,
  the visual difference between displays is getting larger and a
  single Display Rendering Transform (DRT) is no longer sufficient to
  ensure a similar viewing experience across displays.

  A DRT Family is a collection of DRTs that will elicit a similar
  visual result on different displays. Baselight automatically uses
  the appropriate DRT based on the ViewingCondition tag in
  display-referred colour spaces.

  DRT Families are identified with a 'multiple-curve' icon in DRT
  menus. Normal DRTs have a 'single-curve' icon. If a DRT Family is
  selected another menu appears, where an individual DRT from the
  Family can be selected. However an 'Automatic' mode can be used, so
  that the correct DRT is chosen based on the colour space used by the
  Cursor or Deliverable.

  The Colour Space Journey View shows the selected DRT.

  This release includes two DRT Families:

  - Truelight CAM (Colour Appearance Model)

    This is a newly-developed parametrised DRT. Its aim is to achieve
    a robust colour reproduction based on human perception of colour.
    It does not include any pleasing or preferred colour reproduction
    like a 'Film Look'. But it models the apparent colours on a given
    display.

  - ACES RRT 1.0.1

    This reflects the RRT 1.0.1 and the tone-mapping parts of the
    different ODTs to elicit the same result as a given RRT + ODT
    combination [bug 35538]

Matte XYZ 매트 XYZ
---------

* Matte XYZ is a new matte operator that works with additional
  compositing channel information to extract a matte using world
  position information. This allows matting a specific volume in 3D
  space, using image data often generated in 3D CG pipelines and
  rendered into floating point image formats.

  To set up the stack correctly, a sequence that contains world
  position information should be inserted. Ensure that there are
  no colour space conversions affecting the sequence and no
  non-floating point caching on the input sequence strip, as that will
  clip and alter the pure floating point data, leading to potentially
  skewed results.

  The position of the matte volume can be manipulated using the four
  central 3D viewports displayed in the main UI. These have following
  controls:

  - Clicking on the little arrow buttons will expand/collapse the
    current viewport to a single viewport or back to the four
    viewports.

  - The home button will reset the viewport camera back to its initial
    position.

  - Holding the middle mouse button and dragging will pan the camera
    left/right/up/down.

  - Holding the middle mouse button and control-dragging left/right
    will zoom in/out.

  - Holding the middle mouse button and shift-dragging in free camera
    view will rotate the camera around a specific point in space.

  - Right-clicking will bring up a context menu for changing some
    operator and viewport parameters.

  - Left-clicking will put the gizmo location to the nearest position
    to that point.

  - In all views except the free camera, dragging allows selection of
    an volume around the displayed gizmo location.

  - Dragging on any of the gizmo arrows will move the gizmo in the
    direction pointed by the arrow.

  Alternatively it is possible to select the volume in the main output
  display area, by simply left clicking on the centre of the area you
  want the volume to be initially positioned. Selecting the volume in
  the main output works in the same fashion as in any of the other
  matte key operators.

  Currently MatteXYZ has the option of two different matte volumes: a
  sphere with arbitrary radius, and a 3D box.

New Shots View 새로운 샷 뷰 
--------------

* Baselight's Shots View has now been replaced with the one from
  Daylight. The new Shots view includes improvements such as:

  - The ability to set up multiple tabs, each with a different
    list of shots from the scene based on custom filter criteria
    (e.g. "all graded shots from camera A").
  - Improved shot metadata handling, including the ability to add
    new custom metadata columns, column metadata expressions etc.
  - Much improved performance/interactivity in scenes with large
    numbers of shots.

  By default, the Shots view has 3 shot tabs: "All Shots", "Graded"
  and "Current Tape". At the bottom of the view there's a "Filtering"
  section which determines the shots that are visible in the current
  tab. As "All Shots" is selected by default, there are no filter
  options set. However, if you select "Graded" or "Current Tape" you
  will see these options change to ensure the appropriate shots are
  listed in that tab.

  The current tab's shot list can be locked using the lock icon button
  at the top of the view. This ensures shots are not added to/removed
  from the shot list - even if they're altered to no longer match the
  filter criteria (e.g. a shot transitioning from ungraded to graded).

  A tab's shot list can also be sorted based on columns other than
  event number by clicking on the header/title of the column you wish
  to sort by. Clicking a second time on the column header will reverse
  the sorted order.

  The current tab's filtered shots (and ordering) can also be applied
  to the timeline for playback and navigation. This can be enabled by
  either:

  - Enabling the "Playback/Navigation" toggle at the bottom of the
    Shots View.
  - Selecting a tab page from the "Playback Filtering" section of
    the play controls.
  - Holding down the Windows key (Ctrl on the Mac) and pressing the
    Tab key to cycle through the tab pages.

  Once enabled, the timeline will grey out/darken areas containing
  shots not in the current tab's filtered shot list. Also, during
  playback those areas will be skipped. Jumping between shots (and
  stepping frames) will also ignore filtered out areas of the
  timeline.

  Which columns are visible can also be customised per-tab (using the
  dropdown to the right of the column headers) as well as their
  display order (by dragging and dropping the column header text). All
  of these tab customisations are saved along with the scene.

  Timeline strip selections can be synced to the selected shots using
  the "Sync Strip Selections To Shots" option (available from the
  "Customise" and right-click menus). Once enabled, the Shots View
  will attempt to automatically select all strips in the timeline that
  constitute the red square selected shots in the Shots View.

  If (while this mode is enabled) a new, explicit strip selection is
  made in the timeline that doesn't match the current shot selection,
  a message will be displayed at the bottom of the Shots View,
  together with a 'Resync' button. Pressing this will synchronise the
  timeline strip selection to the shot selection again.

  The timeline's selected strips can also be synchronised with the
  selected shots without enabling this mode from the "Select" menu's
  "Select Strips For Selected Shots" option (or the Ctrl+R shortcut)
  [bug 40156]

Formats 포맷 
-------

* Edits to formats can be undone and redone along with all other scene
  edits. If a remote session is following, it will also see changes to
  formats as they are made.

  The Formats editor window left pane lists all formats and shows the
  levels at which they are defined. Icons to the right of the format
  name represent factory, global, job and scene formats. The icon is
  white if the format definition is different from the higher-level
  definition, or dimmed if it is the same. It is absent if the format
  is not defined at that level. There are buttons to hide a format
  from the format list, create a new format, and to reload the
  global/job format sets to pick up changes made elsewhere.

  The right side of the Formats window shows the details of the
  selected format. Use the bottoms at the top to see the format's
  definition at each level at which it is defined. At the bottom
  right, the Format Actions pop-up menu is used to perform various
  actions on the selected format.

  To edit a factory, global or job format, it must first be copied
  into the scene. If the "Scene Format" button is disabled, select a
  definition that is enabled, and choose Edit Format from the actions
  menu. The fields in the editor will become active and you can make
  changes. The changes occur live, and you can undo or redo as
  required.

  When the format is defined and working correctly in a scene, it
  might be desired to share it with other scenes in the job, or even
  other jobs. To do this, copy the format from the scene-level up to
  the job or global level using the Format Actions menu. Once copied to
  the higher level, it is then available for use by other scenes. It
  can be copied into other scenes via the Format Actions menu, or by
  simply using the format for the first time at which point it is
  automatically copied into the scene.

  A format may be deleted from a scene, but only if it is not
  currently being used in the scene.

Deflicker 디플리커 
---------

* The Deflicker operator removes inter-frame flicker from an image
  sequence.

  When you insert a Deflicker operator, it will deflicker the sequence
  using the default settings. Most other Baselight operators have no
  effect when they are first inserted.

  The 'Scale' parameter scales the flicker correction. There should be
  a setting that gives minimum flicker. If you have a simple flicker
  with a period between 2 and 4 frames, 'Scale' should be between 1.0
  and 2.0, and 'Frame Step' should be left at 1. If your flicker has a
  period longer than 4 frames, you should increase the 'Frame Step'
  parameter. If you have a complex or irregular flicker, add a second
  or third filter with different 'Frame Step' settings.

  Most ordinary images will not need the 'Advanced' settings.

  The 'Show' mode, under the 'Advanced' settings, shows the flicker
  signal to be subtracted. You should see a smooth flicker signal. If
  you see a lot of image features in this mode, you may need to
  increase the 'Blur' or the 'Pyramid depth' setting, under 'Advanced'
  controls. Use the 'Scale' control to increase the contrast if the
  flicker is hard to see.

  The deflicker tool can be used anywhere in the stack, but it is best
  used on the raw image data, before any colour or spatial operations.
  The only operations you might put above it are filters that remove
  noise or other details that may make the flicker easier to
  recognise.

Text 텍스트 
----

* The Text operator has been updated and now uses the high quality
  rendering used in the Subtitle operator. Fonts can be selected from
  files in a variety of standard formats. Outline and shadow options
  have been added to the existing lozenge and rectangle border
  options, and the blend level can now be adjusted. Burnins have also
  been updated to use the high quality text rendering.

Colour Matrix 컬러 매트릭스 
-------------

* The Colour Matrix operator transforms the current image using a
  matrix and an offset. When transforming from rgb to RGB...

  R = Rr*r + Rg*g + Rb*b + Roffset
  G = Gr*r + Gg*g + Gb*b + Goffset
  B = Br*r + Bg*g + Bb*b + Boffset

  The user interface has three groups of four sliders to control the
  four parameters for each of the three outputs. The desk controls
  come in groups of three, so to make things neat, the offsets have
  all been moved to their own group.

  There is a scale slider at the bottom. This will scale all these
  parameters, and so scale all the output image values.

  There is an Invert button. When Invert is Enabled, the plug-in will
  do the inverse transform. If the transform cannot be inverted (set
  scale to zero for example), you will get an error message.

  You can use this plug-in to perform grades in a crude
  luminance-chrominance space as follows...

  L:  Rr=+0.6   Rg=+0.3   Rb=+0.1   Roffset=0.0
  a:  Gr=+0.5   Gg=-0.5   Gb=+0.0   Goffset=0.5
  b:  Br=+0.0   Bg=+0.5   Bb=-0.5   Boffset=0.5

  Copy and paste the ColourMatrix strip. On the second copy, select
  Invert Enable. This should restore you to the original image
  coordinates.

  If you do a grade between these two strips, the grade will be
  working in a luminance-chrominance space.

Streak Filter 
-------------

* The Streak Filter operator is designed to remove the low-amplitude
  horizontal and vertical streak noise that you can get in
  underexposed digital camera images. The filter can be used anywhere
  in the stack, but is probably best used close to the top of the
  stack, before any colour or spatial operations.

  You will need to increase Threshold from the default zero setting to
  see any filter effect. The other settings can be left at their
  default values. These parameters were used in development, and have
  been retained in case they have some application for new images.

  The filter may make the image look softer, even if no useful image
  detail has gone. You may want to add a Sharpen strip after the
  denoiser to restore the appearance.

Scene Storage 씬 스토리지 
-------------

* Baselight's scene storage back-end has been improved to offer much
  improved performance, especially when loading and saving large
  scenes. This new back-end is incompatible with existing Baselight
  4.4m1 (and earlier) jobs, so all 5.0 scenes need to created inside
  new jobs. Baselight 5.0 jobs will *not* be visible inside Baselight
  4.4m1 and earlier.

* It is now possible to open a scene which is already open on another
  Baselight system. If the other system has a write lock, then the
  local user will be asked if they wish to open in "follow mode" - if
  they agree, any changes made by the remote user will be instantly
  reflected in the local timeline. When in follow mode, the local user
  only has a read lock on the scene - they will be unable to modify
  the scene in any way. If the media is available on both Baselights,
  this allows remote grading, where a remote read-only viewer can
  follow the grading changes made by a colourist on another system.

* When a scene is opened and a format which it used has been edited or
  deleted, a Scene Format is created to maintain the previous
  behaviour of the scene. A dialog box is now presented when a scene
  is opened to explain this [bug 34467]

* A new backup script, bl-backupdb, can be used to manually backup
  all jobs on a host. Linux-based Baselight systems will automatically
  backup the local database. The script can be run from cron to backup
  other systems if required. Run "bl-backupdb -i" for usage info.

Reports View 리포트 뷰 
------------

* Baselight now includes Daylight's report editor & generator. 

  The report editor can be accessed from the "Reports" view under the
  Views menu.

  It currently supports PDF & CSV report generation.

  Multiple report templates can be defined for a scene. The report
  templates are copied into new scenes when you create a new scene
  based on a Template Scene. Therefore we advise that you create your
  report templates inside a Template Scene, so that they are
  automatically propagated to new scenes.

  Each report template can source its data from one of the tabs
  defined in the Shots View. Using a tab from Shots View allows you to
  specify which columns of data you wish to be included in the report,
  and how the events should be filtered and sorted.

  For example, you can define a tab which filters only shots that are
  marked as "Circle Takes", and sorts them by tape name and timecode.
  If you select this tab as the basis for the report, only the events
  that match the filter will be included in the report, and they will
  be sorted in the order specified by the tab.

  A PDF report currently consists of the following elements:

  - Cover page 커버 페이지 

    This can include a cover image, and multiple "Fields" with
    associated labels & values.

    The labels & values are arranged into columns. You can split a
    column to start a new column by putting the value '\n' as the
    Label for a Field.

    The value for a field can include variables which are substituted
    to include information from the current scene. See the section
    below on Variables.

  - Summary page 요약 페이지

    The summary page can collate various values based on the media in
    your scene.

    The shots in the scene are grouped based on specific criteria,
    such as "Tape", "Mag ID", etc. Baselight can then calculate the
    count, total size, total duration, etc of all the shots in the
    same group.

    For example, if you choose to group based on Tape, you will get
    summary groups as follows:

      Tape        Shots   Duration        Size
      A100RX23    10      01:02:03:04     132.25 GB
      A101RX23    12      00:59:58:02     125.04 GB

  - Event pages 이벤트 페이지 

    The event pages contain columns of data for the shots to be
    included in the report. The list of events to include in the
    report, and their sort order, are determined by the Shots View tab
    that the report is based on.

    You can include thumbnails with each event, and specify the size
    of the thumbnails.

  - Headers/footers 헤더/ 끝맺음 

    You can specify an image & label to use for the header/footer, and
    how the header/footer should be aligned. The labels for the header
    & footer can also include variable expressions.

  A CSV report will use the columns for the Shots view tab specified
  by the "Based On" parameter. You can specify the value delimiter to
  use, and what unit to use for formatting file sizes (using one unit
  allows file sizes to be summed easily in external tools/scripts).
  Columns that use two timecodes (like Source TC) will be split into
  two values i.e. "Source TC Start" and "Source TC End".

  Variables 변수 
  ---------

  The report system supports the following variables:

    Token               Description
    -----               -----------
    %J                  Baselight job name for the current scene
    %S                  Baselight scene name for the current scene
    %{Page}             Current page number (only in header/footer)
    %{Pages}            Total number of pages (only in header/footer)
    %{Date}             Current date, the format of which is
                        controlled by the "Date Presentation Format"
                        in the Scene Settings.
    %{IsoDate}          Current date in ISO format: YYYY-MM-DD
    %{Time}             Current time when report is exported.
    %{SummaryShots}     Number of shots in the report
    %{SummarySize}      Total size of shots, formatted as MB/GB/TB
    %{SummaryFrames}    Total number of frames of all shots
    %{SummaryFeet}      Equivalent to SummaryFrames formatted as feet
                        of 35mm/4perf film
    %{SummaryDuration}  Length of all shots, formatted as hh:mm:ss
    %{SummaryTapes}     List of tape names referenced in the scene
    %{SummaryTapeCount} Number of tapes referenced in the scene
    %{SummaryMags}      List of camera magazines referenced in the
                        scene
    %{SummaryMagCount}  Number of camera magazines referenced in the
                        scene

  Also included are any variables defined in the Scene Settings
  "Metadata" tab, such as "Project", "Director", "DoP", "DIT", etc
  [bug 40156]

Still Export View 스틸 추출 뷰 
-----------------

* Added "Still Export" view and "Export Still" shortcut (Cmd-Shift-E).

  The Still Export view allows you to specify settings for exporting
  still frames from your current scene.

  You can specify:
  - Which frames to export, options:
        - Current Frame Only
        - Poster Frames
            - All Shots
            - Selected Shots
        - Marked Frames
            - All Shots
            - Selected Shots
        - Marked Frames of Category
            - All Shots
            - Selected Shots
  - Output directory
  - Filename, which can include variable name expressions. See the
    Help text for the list of supported variable names.
  - File Type (JPEG, TIFF, DPX, OpenEXR, etc)
  - Colour Space
  - Resolution

  The Still Export settings are saved in the scene. You can save the
  settings in a template scene, and any new scenes created from the
  template scene will inherit the Still Export settings. The "Export
  Still" shortcut uses the current settings from the Still [bug 40156]

Layer View 레이어뷰 
----------

* The Layer View is now a dockable view and will update dynamically to
  represent the stack at the current cursor position. It can be used
  to select layers and mattes.

  As well as displaying layers in a stack, the Layer View can be used
  to re-order the current stack or copy layers from one stack to
  another. This can be done by dragging and dropping layer thumbnails.

  A dragged layer thumbnail can be dropped onto the same stack
  (between thumbnails) to reorder layers.

  Additionally, hovering over a Cuts view thumbnail with a dragged
  layer thumbnail will pop-up the destination stack's Layer view. The
  dragged layer can then be dropped on the destination Layer view to
  insert between or replace existing layers [bug 40156]

Truelight Colour Spaces 트루라이트 컬러 스페이스 
-----------------------

* Modified Layout in 'Scene Settings' -> 'Format and Colour' to
  simplify the overall operation of Truelight Colour Spaces. In the
  standard section there are only the three most common Settings
  (Working Colour Space, Grade Result Colour Space and Display
  Rendering Transform). All other settings have been moved to an
  'Advanced' Section below the main settings [bug 36008]

* Added a new Colour Space 'Filmlight: T-Log / E-Gamut' (Truelight
  Log, Enhanced Gamut). This colour space is specifically designed to
  be used as a Working Colour Space (for camera-agnostic colour
  workflows).

  In addition 'Filmlight: Linear / E-Gamut' was added to provide a
  colour space for linear light VFX Renderings, using the same
  primaries as the working colour space. EXRs rendered to this colour
  space are automatically detected correctly on input [bug 38165]

* Added new HDR colour spaces for different max brightness levels.
  Mathematically each set of spaces are the same, but have different
  clip levels and belong to different display viewing conditions

  - Dolby: ST 2084 PQ / P3 D65 / 108 nits
  - Dolby: ST 2084 PQ / P3 D65 / 1000 nits
  - Dolby: ST 2084 PQ / P3 D65 / 2000 nits
  - Dolby: ST 2084 PQ / P3 D65 / 4000 nits
  - Rec.2020: ST 2084 PQ / Rec.2020 / 108 nits
  - Rec.2020: ST 2084 PQ / Rec.2020 / 1000 nits
  - Rec.2020: ST 2084 PQ / Rec.2020 / 2000 nits
  - Rec.2020: ST 2084 PQ / Rec.2020 / 4000 nits [bug 35538]

* With the development of wide-gamut and High Dynamic Range displays,
  the visual difference between displays is getting larger. In order
  to adapt to those differences, all display-referred colour spaces in
  Baselight 5.0 store more colourimetric information about the given
  display. This then allows for a more advanced display colour
  pipeline, notably by other functions in Baselight like 'DRT
  Families' and 'Mastering Colour Space'.

  The following information has been added to display-referred colour
  spaces:

  - 'RGB_XYZ' is a matrix which specifies X'Y'Z' values, which should
    be used instead of the 'mat' Matrix for display-referred colour
    spaces.

  - 'White_XYZ' describes the maximum X'Y'Z' Tristimulus a
    display-referred colour space can represent. It describes what
    R=G=B=1.0 means in a given colour space.

  - 'Creative_XYZ' (optional) describes the desired value the display
    should elicit for R=G=B=1.0 in linear light.

  - 'Clip_XYZ' (optional) describes the maximum allowed code value the
    colour space should receive. This value is incorporated when the
    colour space is used as a Mastering Colour Space.

  A new command-line tool 'tl-utils TcsMatrix' can be used to generate
  all the needed colourimetric information.

  - ViewingCondition' (optional) is a tag to group certain colour
    spaces together. The ViewingCondition tag is used to select the
    correct DRT from a DRT Family (see below). Currently Baselight
    understands these viewing conditions:

    "Cinema-48"
    "Cinema-108"
    "Video-100"
    "VideoWide-100"
    "Office-100"
    "OfficeWide-100"
    "VideoWide-600"
    "VideoWide-1000"
    "VideoWide-2000"
    "VideoWide-4000"

    Additional Viewing Condition tags can be specified in a text file
    located at /usr/fl/etc/colourspaces/extraviewingconditions.txt,
    with one tag per line [bug 31392]

Mark/Shot Categories keypad mode 마크/샷 카테고리 키패드 모드  
--------------------------------

* Added new numeric keypad mode: "Mark/Shot Categories". Once selected
  (from the 'Edit -> Numeric Keypad Mode' menu) the numeric keypad can
  be used to add/remove marks as well as set/unset shot categories.

  By default, the '1' key adds a mark to the current shot (of category
  'Generic Mark') and the '2' key sets the current shot category to
  'Default Strip Category' ('Shift'+'1' and 'Shift'+'2' remove the
  mark and shot category respectively). However, the 9 keypad keys can
  be customised to add marks/set shot categories as required using the
  setup panel accessed via the menu option 'Edit -> Numeric Keypad
  Mode -> Configure Mark/Shot Keypad Keys'.

  The new mode also supports the following keypad keys:

  '-'           : Remove all marks at current position.
  'Shift' + '-' : Remove all categories associated with current shot
                  [bug 40156]

Layer Numbering 레이어 넘버링 
---------------

* The way layer numbers in dissolve/composite stacks are assigned has
  been improved. Previously, layer numbers within a stack were
  assigned sequentially from the top down. This meant, for example, if
  a stack consisted of a single dissolve of two primary graded shots,
  the top shot's grade would be assigned layer 1 and the bottom shot's
  grade would be layer 2.

  Now, each of the 2 shots' grading layers ('sub-stacks') that feed
  into the dissolve are numbered separately, so both of these shots'
  grade layers will be assigned layer 1. This allows you to easily
  identify & navigate sub-stacks within a single stack comprising
  multiple elements.

  Similarly, in a composite stack the foreground shot sub-stack will
  be numbered separately from the background.

  When operations act on layers in other stacks (e.g. grouped grading)
  and there are multiple uses of the same layer number within a stack,
  Baselight will try to match the current selection with an equivalent
  selection in other stacks.

  Repeatedly selecting the same layer number from the desk will cycle
  through all layers with the same number in the current stack.

  Copy and Paste 복사와 붙여넣기 
  --------------

  The "Copy - Paste/Apply Options" (on the "Edit" menu) have been
  simplified. There are now only 3 paste/apply options:

  "Replace" - Layers in the destination stack will be completely
              replaced by the layers in the copy buffer.
  "Below"   - All layers in the copy buffer will be pasted below the
              bottom-most layer of the destination stack.
  "Merge"   - Merges the copy buffer and destination stacks, according
              to the layer numbers of the layers.

              Layers present only in the copy buffer stack will be
              copied into the destination stack.

              Layers present only in the destination stack will be
              left unchanged.

              Layers which exist in both copy buffer and destination
              stacks are resolved according to the "Protect Existing
              Layers" option. If set, then layers which exist in both
              stacks will be left alone. If not set, these layers will
              be overwritten with their equivalent layer from the copy
              buffer stack.

  When copying, only the sub-stack containing the currently selected
  strip in the timeline is copied to the copy buffer.

  Similarly, when pasting in "Replace" and "Merge" modes, the timeline
  strips affected will be those in the sub-stack containing the
  currently selected strip [bug 43047]

BLG Improvements BLG 개선사항
----------------

* Improvements have been made to the BLG file format to allow additional
  functionality:
    - Input, Working and Viewing formats used by the Baselight stack
      are now stored inside the BLG. This means that in plugins like
      Baselight for Nuke, the complete image transform applied to an
      image in full Baselight can now be replicated.
    - The Sequence operator's "Orientation" option is now supported
      within BLG files, including the additional "Centered on Mask"
      option.
    - EXR Channel/Track references in full Baselight stacks are now
      stored inside BLGs. This means that plugins where the host
      supports EXR image channels (like Baselight for Nuke) can now
      load BLGs referencing matte channels or non-default image
      tracks.
    - Stacks containing multiple input Sequences can now be represented
      within a BLG. This means the stacks containing composites
      (e.g. sky replacements etc) can now be represented within
      compliant plugins (e.g. Baselight for Nuke), simply by linking
      in additional inputs to the node.
    - The "Stack Colour Space" and "Input Display Rendering Transform"
      options are now included in BLG files.
    - Locked BLG files are now encrypted. In addition, it is now
      no longer possible to load locked BLGs into full Baselight or
      Daylight, thus preventing the internal structure of a locked
      BLG from being examined. Locked BLGs are intended to be
      distributed to VFX/Editorial partners for use in Baselight for
      Nuke and/or Baselight for Avid.

* When inserting BLGs in the timeline, Baselight is now more clever
  about when it inserts additional ColourSpace operators. It now
  only adds them when:
   - There are existing grades in the stack. If there aren't, it
     directly modifies the Sequence operator's Stack Colour Space
     and Input Display Rendering Transform settings instead
     [bug 43801]
   - When the BLG were exported from a scene whose Grade Result
     Colour Space differed from that of the scene being inserted
     into [bug 34932]

* Operator versioning in Baselight has changed to become per-operator
  in v5.0. By this we mean that older builds of v5.0 will still be
  able to load scenes/BLGs produced by later builds, as long as the
  operators used in the BLG/scene have not had their individual
  version numbers incremented. This makes it much more likely that a
  given BLG will be able to be loaded by older software. For this
  reason, the "Version Compatibility" option has been removed from the
  "BLG Export" and "EDL Export" settings [bug 42401]

* Changed the "Quick Grab BLG" keyboard accelerator to be Ctrl+Alt+e
  (or Cmd+Alt+e on the Mac) to avoid clashing with the Alt+e (Insert
  Paint on second matte column) accelerator [bug 44210]

LUT Export LUT 추출 
----------

* Updated LUT export with Extended Ranges support for HDR input.
  Truelight cubes and the newly added Autodesk CTF format support an
  extra input LUT for mapping high dynamic range inputs. There is now
  an option to include this in the LUT export dialog [bug 33499]

* LUT export also now includes an option to override the input colour
  space, replacing the one used for a sequence with one specified for
  the LUT export. This allows LUTs to be generated for use in other
  applications using images that have been converted to a different
  colour space [bug 33157]

* LUT export has been extended to include options for the Input
  Display Rendering Transform when the Input Colour Space is set to
  anything other than the Sequence Input Colour Space. Previously the
  Input DRT was not handled in the LUT export [bug 35118]

Miscellaneous 기타 
-------------

* OFX plugins using OpenGL rendering are now supported [bug 25574]

* The layout of the Insert menu can now be changed between the new
  structured version and the legacy unstructured version [bug 42207]

* Added a new "FilmLight" Scene Template. This sets up a scene in a
  scene-referred recommended fashion. The following Scene Settings are
  defined:

  - Timeline Caching: Full
  - Display And Timeline Cache: 10-bit Integer RGB
  - Working Colour Space: FilmLight: T-Log / E-Gamut
  - Grade Result Colour Space: From Stack
  - Display Rendering Transform: Truelight CAM
  - Colour Treatment: Native (as we have a HDR Working Format)

  You should set your Image Container to the Project/Job level in the
  file structure in order to get the deliverables to work properly.
  Render Deliverables are included that should cover most of the
  deliverables needed in a production:

  - Dailies Avid graded
  - VFX Plates ungraded
  - VFX Plates graded
  - QT for Approval
  - P3 Deliveries
  - DCI XYZ Deliverable
  - DSM Archive
  - Rec709 Deliverable [bug 39561]

* Added new colour spaces:

  - Dolby: ST 2084 PQ / X'Y'Z' / 108 nits

    This space is needed to export a Dolby Vision Cinema DCDM

  - Rec.2100: HLG 1.2 Gamma Legal Range/ Rec.2020 / 1000 nits

    This space is needed to import legal range HLG content. It is not
    intended to be used as Cursor or Render Colour Space.

  - Red: Log3G10 / REDWideGamut and RED: Linear / REDWideGamut

    These colour spaces are RED's new default wide gamut colour
    spaces. They build the foundation of the upcoming RED IPP2 DRTs.

  - Rec.2100: HLG 1.2 Gamma / Rec.2020 / 1000 nits and Rec.2100: HLG
    1.2 Gamma / Rec.2020 / Preview SDR Conversion (on 1000nits)

    Technically they are identical to the ad hoc colour spaces
    published on FilmLight's webpage 'Rec.2390 Hybrid Log-Gamma
    package'. Just the naming was changed to reflect the recent ITU
    Specification ITU.BT.2100 [bug 38751]

* Added tl-utils LcmsList function. This converts ICC profiles to
  Truelight list transforms using the Little CMS library. This library
  supports the full ICC v4.3 standard, so it should be able to convert
  profiles that use the new v4.3 features. LcmsList complements but
  does not replace the existing ICCtransform or TcsDisplay: these will
  probably make a better conversion on a display profile, and display
  profiles rarely use the new ICC v4 features [43671]

* Added new fltransform constant "BlackOffset". This value is useful
  to specify which linear light (LMS) scene referred value is mapped
  onto 0.0 on the display signal. Some DRTs map negative values onto
  0.0. That results in linear light scene referred 0.0 to be mapped
  into a positive value greater than 0.0. Modern grading tools like
  Base Grade operate in the linear domain and linear light scene
  referred 0.0 is the anchor point of those tools. Base Grade in
  combination with a DRT that maps linear light scene referred 0.0
  onto a positive value on display would cause a strange behaviour
  using Base Grade, as a user could not reach true 0.0 on the display
  signal. The "BlackOffset" value in the DRT is used to offset Base
  Grade's working point. Base Grade does this dynamically based on the
  DRT in use in the stack [bug 40650]

* Renamed "ACES: 2.6 Gamma / P3 D60" colour space to "DCI: 2.6 Gamma
  / P3 D60", to reduce confusion in Non-ACES Workflows [bug 41192]

* Added option to sort jobs by size (note that this feature is not
  available when browsing jobs on FLOS 2.1 systems) [bug 5208]

* Added support for 12-bit encoding in the DNxHR HQX codec [bug 34868]

* Added support for reading multi-part OpenEXR files (except where the
  display window is not the same for all parts) [bug 34972]

* Added support for reading multi-view OpenEXR files. This includes
  automatically selecting left/right views in stereo scenes for both
  the image and any referenced matte channels [bug 35059]

* Updated to RED SDK v6.1.0. This includes three new HDR Output Tone
  Curve options: HDR-2084, Rec.1886 and Log 3G12 [bug 35054]

* The Manage Colour Spaces dialog now allows more fine-grained choices
  of which colour spaces to hide in which menus - e.g. a colour space
  may be hidden from the Working Colour Space menu but still visible
  in the Render Colour Space menu [bug 35147]

* Added support for NVIDIA driver 352.63 on systems with GTX 580, GTX
  680, GTX 780, GTX 980 and GTX TITAN X GPUs. This driver is compatible
  with systems using an AJA Kona 4 or direct GPU display. This driver
  is NOT compatible with systems using FilmLight DVI2SDI or Framestore
  SDI display hardware [bug 33008]

* Added support for NVIDIA driver 340.96 on systems with GTX 680 and
  GTX 780 GPUs and DVI2SDI or Framestore SDI display hardware
  [bug 35367]

* Added ability to specify how shapes are combined within a single
  shape strip.

  Each shape in a shape strip is drawn in order based on its position
  within a 'draw list'. The currently selected shape's position in
  that list is indicated in the 'Shape Management' section (e.g. 'Shape
  3 Of 5 Selected'). The shape's position in the list can be adjusted
  by the up/down arrow buttons next to the position indicator.

  How the shape is combined with any shapes already drawn is controlled
  from the 'Operation' dropdown. 3 different operations are available:

  Union         The shape is unioned/merged with any shapes already
                drawn.
  Subtract      The shape cuts a hole in any shapes already drawn.
                This is useful, for example, when a graded object
                passes behind another ungraded object.
  Stamp         The shape is stamped on top of any shapes already
                drawn. In this mode the 'Opacity' (slider) value is
                replaced by 'Intensity'. This mode is useful, for
                example, when you have foreground objects (partially)
                obscuring background objects and you want a grade to
                affect the foreground less then the background.

  Additionally, when soft edge shapes overlap in 'Union' mode (the
  equivalent of the old shape rendering behaviour), where the shapes
  intersect there will be a less visible band [bug 32582]

* All the default setups have been updated to reflect modern grading
  workflows:
  - Default Working Colour Space is changed to "FilmLight: T-Log /
    E-Gamut"
  - Default Display Rendering Transform is changed to "Truelight CAM"
  - SDI Output "Clip to Legal" is changed to "Full to Legal"
  - Default HD Viewing Colour Space is changed to "Rec.1886: 2.4 Gamma
    / Rec.709"
  - Default UHD Viewing Colour Space is changed to "Rec.2020: 2.4
    Gamma / Rec.2020"
  - Default DCI Viewing Colour Space is changed to "DCI: 2.6 Gamma /
    P3 DCI" [bug 34406]

* Added the concept of a "cursor group" to the cursor drop-down in
  the Cursor View. Each cursor can now be a member of one of three
  groups: Cyan (the default), Yellow or Magenta.
  This is helpful because:
    - When using the Wipe, 2x1, 1x3 etc display modes, only cursors
      from the current cursor's group are displayed. Thus, for
      example, if you have cursors 1, 2 & 3, it is possible to
      display 1 & 3 side-by-side simply by using a 2x1 display
      mode and having cursors 1 & 2 being in a different group to
      cursor 2.
    - Each cursor group has a separate gang state, so you can have
      some cursors ganged together whilst leaving others alone
  [bug 27050]

* Added ability to cycle through different numeric keypad modes by
  holding down the Windows key (Ctrl on the Mac) and pressing 0 on
  the numeric keypad [bug 40156]

* Added recall stack -2 to +2 actions to Chalk [bug 33306]

* fl-diag zones test no longer warns about volumes which are not
  defined on all systems [bug 39273]

* fl-diag zones test no longer warns about minor internal differences
  in other systems [bug 39272]

* On Flos 6.4 systems, the PostgreSQL work_mem setting will be changed
  from the default (1MB) to 32MB [bug 43135]

* All numeric edit control controls now support gestural grading.
  To use it, simply click in the edit control and drag clockwise
  or anti-clockwise in a circular manner. This change means that
  to sweep-select text in an numeric control, you'll need to first
  click in the edit control to  obtain the input focus, after which
  you can sweep select [bug 38973]

* Updated to ARRIRAW SDK v4.5. This adds additional colour space
  options including Rec.2100, for compatibility with ARRI's camera
  Software Update Package 5.0 [bug 43457]

* Added support for Retina displays on Mac OS X.

* Added "SDI Full Range Levels" option to SDI setups editor. This
  option specifies how full range data is mapped to the SDI outputs
  of the AJA Kona 4.

  It has two options:

  - "0-1023 (Full)" : Full range data is passed unmodified to the
    SDI output. Code values below 4 and above 1019 in a 10-bit range
    (below 16 and above 4076 in a 12-bit range) are clipped. This is
    the default behaviour and corresponds to the existing behaviour
    in Baselight.

  - "4-1019 (SMPTE Full)" : Full range data is scaled to the range
    4-1019 for 10-bit signals, or 16-4076 for 12-bit signals. No data
    is clipped, but display devices must be configured to handle full
    range data to be mapped to SDI SMPTE Full Range [bug 44060]

* Added support for reading stereoscopic DCPs and stereoscopic JPEG
  2000 encoded MXF-files [bug 30322]

* When pasting shots between scenes that use different containers,
  there is now the option to keep the original container paths when
  pasting into the destination scene.

  If you choose to preserve the paths within the original container,
  the pasted shots will use absolute paths to the original
  image/movie/audio files so that the media is still accessible in the
  destination scene. This is useful if you then wish to Consolidate
  material using the destination scene container.

  You can set the default behaviour for remapping containers when you
  paste shots using the "When Pasting Between Scenes" setting in the
  Image Container section of Scene Settings.

  This setting has three options:

  - "Ask Before Updating File Paths": A dialog will be shown after
    pasting shots between scenes if the source scene and destination
    scene use different containers, asking whether you wish to keep
    the paths within the original scene's container, or use paths
    relative to the destination scene's container. This is the default
    behaviour.

  - "Keep Source Container Paths": Always keep the original paths
    within the source container. The sequences pasted into the
    destination scene will use absolute paths so that the original
    material can be found.

  - "Use Destination Container Paths": Use paths relative to the
    destination scene's container [bug 20250]

* Since Baselight for FCP7 is no longer supported, the "Update FCP XML
  with Baselight Grades" option has now been removed from the EDL
  Export panel [bug 43787]

* Added Border Colour option for burnins, which allows you to change
  the colour of the border behind text elements in a burnin
  [bug 44618]

Bug Fixes Since Baselight 4.4m1.9553
====================================

* Denoise cannot work if you pick a completely flat region. The error
  message has been changed to something more helpful if this happens
  [bug 43883]

* Fix for problem with blur + grain + flip transform. This was a 
  very strange special case where the flip disappeared when the blur
  went above a certain threshold, but only when the grain was applied
  [bug 43449]

* New softer pyramid option used in Texture Blend, Texture Equaliser,
  and Streak Filter, with versioning so old scenes are unchanged.
  This gives a smoother result if you have large filter changes between
  one level and the next [bug 41584]

* Changed HLG black point to 0.0. This prevents crushed blacks.
  Changed the clipping within the from_lin function. This fixes some
  artefacts with strong saturated blues. Changed the to_lin function
  of the HLG Preview space. This fixes a bug with this space in
  combination with an active Mastering Colour Space [bug 41781]

* Colour Temperature now bypasses all processing when there is no
  temperature shift and all other controls are at the default settings.
  Prior to this we got some small colour shifts due to precision errors
  in the colour space transforms [bug 41943]

* Fixed incorrect colour space conversions which were applied when two
  inputs to a Matte Merge operator had different colour spaces. Please
  note this may change the appearance of Baselight 4.4m1 scenes using
  Matte Merge operators when upgraded to Baselight 5.0 [bug 38916]

* Fixed black point and white point setting in ACEScct.flspace. This
  does not change the transformation itself, but only where lines are
  displayed in the histogram [bug 41494]

* Fixed flickering at right and bottom edges occasionally seen when
  blurring with large radii [bug 2359]

* Increased the amount of memory dedicated to thumbnails on Baselight
  systems with a UI host to 25% of available RAM. This allows more
  thumbnails to be kept in memory, reducing thumbnail re-rendering
  when scrolling [bug 34183]

* Fixed LUT export which was failing for Shots with Hue Angle and
  Matte Tool Blur [bug 34225]

* Fix new files being reported as zero size over /pfs (flood)
  interface when they were written using flux [bug 28121]

* Improved accuracy of warning counter on EDL Import View [bug 34284]

* Sequences on cloud media are no longer reported as missing when
  using Verify on a render [bug 32311]

* Fixed crash starting image output on FLOS 2.1 Baselight ONE systems
  [bug 34168]

* Fixed bug where the "sRGB Display (Ignore Truelight & Viewing Colour
  Space)" (now renamed to "Use sRGB for Thumbnails") would have no
  effect in some galleries [bug 33145]

* Fixed bug where normal scenes loaded into galleries sometimes
  wouldn't scrub using the current viewing colour space [bug 29231]

* Fixed bug where the current cursor's mask and guide mask settings
  sometimes weren't being applied when scrubbing in a gallery. Now, as
  long as the user elects to turn on the "Viewing Format and Masks"
  options in the Gallery's right-click context menu, any current mask
  or guide mask should always be applied when scrubbing [bug 34117]

* Fixed bug which could occur when a mask, burnin and a Truelight
  profile were switched on in the current cursor and the user scrubbed
  in a gallery thumbnail which was grabbed with a different viewing
  format which didn't contain a mask of the same name [bug 23458]

* Fixed crash when grabbing a movie to the gallery if the user the
  Baselight UI was running as didn't have permission to read the movie
  [bug 26004]

* Fixed alpha channels in thumbnails of ProRes 4444 media [bug 34334]

* Fixed keyboard accelerator for changing Edit Type on Mac [bug 34336]

* Fixed error with zero handling in "Dolby: ST 2084 PQ / P3 D65"
  colour space [bug 34382]

* Fixed bug which cause shape overlays to not match the rendered shape
  image when adding/modifying keyframes [bug 34376]

* Fixed intermittent crash related to periodic events in the user
  interface [bug 34305]

* You can now use the same expressions available in the Shots view
  in burn-ins and the render panel. For example, you can now use
  %[FileMetadata.ISO} in a burn-in, or %{MyCustomColumn} in a path
  in the render panel [bug 36888]

* Added option to specify the font to use for burn-ins. The software
  can use any Truetype font (extension .ttf) [bug 41562]

* Improved font search paths. The software will search a set for
  Truetype fonts in a set of per-user and system directories.

  On macOS the font search directories are:
  - /Library/Application Support/FilmLight/fonts
  - $HOME/Library/Fonts
  - /Library/Fonts

  On Linux the font search directories are:
  - /usr/fl/fonts
  - $HOME/.fonts
  - /usr/share/fonts/truetype [bug 41562]

* To reduce confusion which was caused by the introduction of correct
  QuickTime colour space tagging in Baselight 4.4m1.9029, the Render
  View now offers the choice to use "Legacy" tagging. This tags output
  QuickTime movies as Rec.709, PAL or NTSC based purely on the
  resolution of the image. The new behaviour which tags the movie
  using information from the render colour space is available by
  selecting "Automatic" tagging [bug 31853]

* Fixed remote rendering on a multi-GPU FLUX Store [bug 40086]

* Added mechanism for white-listing non-standard GPUs [bug 42852]

* Fixed cp_sync slowdown accessing NFS volume on OSX [bug 41248]

* MJPEG encoded material in MXF files is no longer stretched from
  legal to full on read [bug 34402]

* Fixed screen switching by double tapping the UI/Image button on
  systems with both multiple monitors and a Blackboard 1 [bug 32511]

* Updated the ACES Scene Template to use ACES Cineon Log / AP0 as a
  working colour space, due to issues with ACEScc [bug 34051]

* Fixed bug setting up floating-point cubes that take negative values.
  This gave visible pixels in regions that should be fully dark. Such
  cubes are not used outside development work, so we do not expect
  current Baselight jobs to be affected [bug 34465]

* Fixed Group Grading of several operator parameters [bug 34407]

* Fixed issues with Cloud Media connected to the node of a Baselight
  TWO system [bug 34297]

* A missing source file will no longer cause a Consolidate operation
  to abort [bug 34240]

* Adaptec web interface no longer requires an SSL connection because
  many browsers refuse its self-signed certificate [bug 31422]

* BLG export using unavailable filename templates (e.g. %P when the
  shot has no clip name) now correctly report the error [bug 30551]

* Fixed an issue that prevented interop DCPs being rendered via
  command line [bug 31693]

* Rendering a DCP now finishes with 'Wrote DCP package', to better
  indicate the completed status of the render job [bug 31967]

* Fixed an issue that could cause frames to be repeated in MP4 movies
  with frame rates of 100 fps or higher [bug 34594]

* Fixed occasional out-of-memory errors when rendering [bug 34226]

* Fixed excessive file searching when opening some R3D movie files
  [bug 34690]

* Adjusted calculation of max frame size in JPEG 2000 compressed MXF
  files to avoid introducing minor bitrate overshoots when creating
  DCPs in e.g. Clipster [bug 31622]

* Fixed LUT export for a LUT transforming from a Log Colour Space to a
  Linear Colour Space, which previously clamped output values to 1.0
  [bug 34423]

* Fixed LUT export for shots with pixel aspect ratio other than 1.0
  [bug 34611]

* Fixed broken handling of some parameters when rendering H264 to MP4
  or Quicktime containers. These parameters would previously generate
  warnings about undefined parameters on the console, and their
  settings would be ignored if set to something other than the default
  value. The affected settings are "Weighted prediction for P-frames",
  "early SKIP detection on P-frames" and "Transform coefficient
  thresholding on P-frames" [bug 34825]

* Added aspect ratio information to Dolby EDR Metadata [bug 32794]

* Deleting a format which overrides another format no longer removes
  some mappings to the remaining format [bug 34920]

* Fixed crash when activating a licence from a downloaded file
  [bug 33708]

* Improve licensing dialog and activation process [bug 33418]

* Improvements to Licence window layout [bug 34464]

* Updated to latest version of fl-setup-vol, which removes support for
  Avid Unity filesystems (superseded by Avid ISIS) [bug 34599]

* Fixed an issue that could cause decode failures, frame offsets and
  incorrect frame ordering in MXF files with start-position offsets.
  This particularly affected XDCAM encoded files [bug 33591]

* Improved error message when trying to open an encrypted DCP or MXF
  [bug 34979]

* Fixed reading audio from split-file MXF media [bug 34903]

* Improved cursor lag on image display when using AJA SDI output
  hardware [bug 34357]

* Fixed reading audio from some MXF files [bug 30294]

* Fixed 100% quality JPEG output [bug 35034]

* Fixed deselect on paste still clearing the selection when it was 
  turned off [bug 25917]

* Improved Baselight decode of ARRIRAW media so the levels more
  closely match the ARRI decode. Note that this only affects
  newly-added Sequences to prevent changes to existing scenes; to
  update existing scenes use the Update button on the Sequence
  parameters [bug 35043]

* Fixed crash when pasting a tracker strip having a two point track 
  with no tracker linked to it [bug 35046]

* Updated the default Setup behaviour so that new scenes are created
  using the ARRI Photometric v2 DRT. This replaces the legacy ACES RRT
  0.7 which was previously used [bug 35086]

* Avoid running overnight disk defragmentation process twice on 
  Baselight TWO systems [bug 34925]

* Errors are no longer generated if there are AppleDouble files in the
  colourspace directories (e.g. ._foo.flspace) [bug 35053]

* Reduced risk of GPU memory errors when working with large RED media
  (e.g. 8K WEAPON) [bug 35041]

* Fixed bug which caused incorrect cache size warnings on multi node
  systems [bug 23199]

* Updated preview features licence support [bug 34539]

* Diagnostics no longer reject hostnames that are the same as the
  system zone name. This helps integration with certain 3rd-party SANs
  [bug 31174]

* Diagnostics now report detection of Intel EIST technology
  [bug 25667]

* Fixed problem with copy protect categories on the input strip
  preventing the strip directly underneath from being pasted to the
  destination [bug 35174]

* Fixed CDL grades not appearing in the bl-shots -ascsop and -ascsat 
  options [bug 35204]

* Colour Space Journey View no longer displays entries for bypassed
  strips [bug 34977]

* Fixed a memory allocation issue which could cause subtitles not to
  appear in DCP output [bug 35012]

* Fixed temperature query tool 'sdi-info -temp' bug [34978]

* Fixed Input Colour Space shown on Sequence Parameters when a BLG is
  inserted onto the timeline [bug 35220]

* The Reference strip no longer converts its input to the Working
  Colour Space and Working Format. Note that since this can affect
  grading behaviour, this change only applies to newly-added Reference
  strips; old scenes retain their old behaviour [bug 35206]

* Truelight resources used by operators inside layers with mattes are
  now correctly included in exported BLG files [bug 35240]

* Fixed an issue where the Blackboard 'Undo' functionality was no
  longer available after a Tracker modification using any blackboard
  trackball or ring [bug 35192]

* Fixed a problem with retime node in Optical Flow mode, where cluster
  machines would render differently than single node machines
  [bug 35091]

* The Job Manager "Move Scene Into Folder" command now prevents moving
  a scene into a folder which already has a scene of the same name
  [bug 35278]

* Fixed issues with Dolby Vision Mastering Display [bug 35268]

* Fixed a problem with Optical Flow retime, where Baselight FOUR and
  EIGHT systems would render incorrectly [bug 35091]

* Fixed decode of ARRIRAW Open Gate (3414x2198 or 3424x2202) media
  using ARRI decode mode [bug 34605]

* Fixed a crash that could occur while setting the time on KDMs in the
  render panel [bug 43034]

* Internal /media/_mnt_slot* volumes are now hidden from cloud media
  [bug 35300]

* Fixed crashes reading some 16-bit RGBA TIFF files [bug 35357]

* Bypassed Dolby Vision strips are no longer exported with EDR XML
  [bug 35356]

* Fixed order of gestural grading gang controls [bug 35352]

* Fixed export format of .cc files [bug 34345]

* Prevented Consolidate overlapping-sequences warning dialog from
  getting too large [bug 35227]

* Fix playback and render errors when Audio Sequence operator has a
  negative offset [bug 35375]

* Fixed bug with fl-service xorg service running on IO node of cluster
  systems [bug 35409]

* Don't attempt to stop Adaptec raid verification at Baselight startup
  because it may cause a kernel panic [bug 35345]

* Fixed an issue with the bitrate selection dialog when rendering DCI
  compliant JPEG 2000 files, where the dialog did not update to
  reflect the selected bitrate [bug 34844]

* The sequence operator now correctly displays a selection dialog for
  handling frame duration when reading a movie file with uneven frame
  duration [bug 32262]

* Bundle a newer version of xfs_repair (4.3.0) [bug 35186]

* Fixed render hang on BL4/BL8 [bug 35453]

* Fixed bug in the Gallery which could occur when grabbing RAW media
  (e.g. R3D, ARRIRAW etc) when multiple debayer parameter operators were
  in the stack. When the original media disappeared, the grabbed frame
  could have been generated using the incorrect debayer parameters
  [bug 35511]

* Updated pivot point in CDL grade to match FG. Also fixed the maximum
  slope value [bug 35464]

* Improved serial number and licence file validation support
  [bug 35363]

* Fix application hang caused by Audio Waveform view [bug 35512]

* Fix behaviour of "Reset All To Camera Metadata" on R3D Params
  operator [bug 35516]

* Select Missing Material now reports that it cannot check material
  which is on remote cloud media [bug 35523]

* Fixed decode of ARRIRAW Alexa Plus anamorphic (2578x2160 or
  2592x2160) media using ARRI decode mode [bug 33915]

* Negative button in Video Grade now works as expected [bug 17462]

* A failover routine has been added when encountering missing
  reference frames in XDCAM MXF-files. This will allow reading valid
  XDCAM essence from MXF-files with invalid indexes [bug 35633]

* Added support for a number of QuickTime codec tags, including 'aivx'
  for XAVC [bug 35615]

* Fixed failure to read some QuickTime files with badly-formatted
  metadata [bug 35761]

* Update licensing to allow appropriate licenses to be installed
  [bug 35896]

* Fixed an issue that caused blocky artefacts and green frames when
  decoding XDCAM [bug 36016]

* Fixed conform / re-conform issue that caused failure with overlapping
  sequence strips [bug 36344]

* The 'Tracker Zoom' functionality now correctly takes into account
  the viewing format, when it differs from the working format
  [bug 33995]

* Fixed stereo geometry fix not working on scenes that contain a 
  DRT in their colour space scene settings [bug 40870]

* Fixed possible crash in Multi-Paste View when doing "Restore Config
  to Defaults" [bug 41316]

* MPEG-4/SStP codecs are not currently available for rendering on Mac,
  pending a library update from Sony [bug 36974]

* Stopped spurious "Multi-Paste Settings have changed" warning when
  closing Baselight [bug 27308]

* Fixed crash which could occur after a Timeline Sort was done when
  Cuts View selections were removed by the sort [bug 41482]

* Updated ACEScg tooltip text [bug 41047]

* Fixed bug which would prevent shape control points from animating
  correctly when manually keyframed [bug 41760]

* Fixed bug which prevented keyframes from automatically being added 
  to a shape's feathering & opacity when dragging control points
  [bug 41778]

* Fixed an issue causing the tracker strip 'show input' button to 
  be modified when coming from a shape or transform strip
  [bug 41919]

* Fixed crash in layer view drag and drop on replace [bug 42082]

* Stop burnin opacity from being reset on scene open [bug 42682]

* Fixed a memory leak in the QuickTime and MXF movie reading proxies
  [bug 42683]

* Ensured that movie, image and header counts are shown on conform
  results [bug 40110]

* Fix an issue that prevented conforming with TapeName or ClipName in
  Path or Filename from working [bug 41206]

* Fixed display of media counts when doing a conform [bug 41203]

* Fixed floating layer views initially appearing empty [bug 41442]

* Fixed flicking green line when inserting layer in the layer view
  drag and drop [bug 42693]

* JPEG 2000 Params strips are now automatically inserted for JPEG 2000
  encoded files and MXFs [bug 42829]

* Fixed spurious changing of ganged cursor positions if "Always
  Restore Cursor Position on Undo/Redo" was switched on [bug 41938]

* Fixed an issue where DCPs with missing entries in the ASSETMAP could
  cause dcpproxy to crash [bug 42998]

* Fixed bl-conform which was failing to detect existing jobs and 
  to create new jobs [bug 43055]

* Added support for reading audio from Op1B MXF-files. Previously,
  these files tended to cause movie reader crashes when attempting to
  read audio [bug 43113]

* Fixed an issue with missing metadata that prevented the consolidate
  function from working correctly with DCP packages [bug 39846]

* The "Grouped Grade Stacks Above/Below" (edit) menu option has now
  been replaced with "Grouped Grade Both Eyes". This option is only
  available in stereo scenes [bug 42917]

* Updated the QuickTime library to prevent crashes produced by
  malformed files [bug 43585]

* Fixed copying of compressed TIFF files resulting in much larger
  uncompressed files in the destination [bug 43305]

* Linking a tracker to a transform strip for a stabilisation no longer
  resets the transform parameters [bug 43638]

* Fixed an issue that could prevent some Op1A MXF files with CBE
  essence from being decoded correctly. This affected at least one
  type of AVC-Intra MXF [bug 43440]

* Fixed keyframing errors which could occur when BLGs were exported
  from stacks with misaligned start frames [bug 44104]

* Fixed Gamma and Gain being swapped in dissolve shots in Dolby EDR
  export [bug 42200]

* Fixed Mac numeric keypad behaviour [bug 43808]

* Fixed a problem where rendering XAVC or XDCAM to Sony MXF did not
  set the duration correctly in the file header [bug 43464]

* Updated the QuickTime library to prevent crashes produced by
  malformed files [bug 43585]

* Improved the handling of XAVC LongGOP, making random access much
  more efficient. This type of media can now be used for grading
  [bug 32458]

* Fixed Mac installer to ensure Truelight displays and profiles
  folders are writable by all users [bug 44163]

* Fixed bug with burnin rendering that would cause incorrect black
  levels in borders outside the image area when images are rendered
  with a Video LUT applied [bug 43855]

* Fixed a crash that could occur when reading QuickTime files with
  invalid comment atoms [bug 43905]

* bl-reset-cache no longer resets the thumbnail cache by default
  [bug 43753]

* Fixed an issue where the frame count of some QuickTime movies could
  become very high [bug 44200]

* Premiere XMLs with reversed clips, and old XMLs, now start on the
  correct frame [bug 32377]

* Unreadable effects in XMLs are now simply ignored, rather than
  giving the warning "Speed change ignored" [bug 40945]

* XMLs with unknown effects now give a warning that the effects are
  not supported in Baselight [bug 34891]

* Fixed crash when unlinking trackers [bug 44142]

* Linking a tracker to an already keyframed control no longer deletes
  any existing motion keyframes [bug 43221]

* Changed pop up window when unlinking a tracker, which now has
  simplified options and text message [bug 43458]

* Fixed bug where it became impossible to close a scene after hitting
  "Cancel" in the discard confirmation dialog [bug 44375]

* Improved error message when verifying a render that includes a gap
  in the timeline [bug 44258]

* Fixed possible increased sluggishness when using keyboard bumps with
  "Maintain Density" being off [bug 43632]

* The Subtitles operator is now detected and rejected during BLG
  Export [bug 44195]

* In FCP XMLs sources with empty reel names no longer generate a
  warning [bug 44475]

* Fixed tracker issue, where the point tracker preview box was showing
  an incorrect image when the "show input" button was on [bug 43734]

* Fixed corrupted warning message on SDI output when GPU is in use by
  another application [bug 43351]

* Added support for variable retimes from FCP7 XML files [bug 44427]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9553 (2017-07-13)

New Features Since Baselight 4.4m1.9480
=======================================

* Added support for nvme-based storage [bug 42991]

Bug Fixes Since Baselight 4.4m1.9480
====================================

* Added support for reading audio from Op1B MXF-files. Previously,
  these files tended to cause movie reader crashes when attempting to
  read audio [bug 43113]

* Fixed a problem where rendering XAVC or XDCAM to Sony MXF did not
  set the duration correctly in the file header [bug 43464]

* Linking a tracker to a transform strip for a stabilization no longer
  resets the transform parameters [bug 43663]

* Fixed a memory leak that could cause mxfproxy processes to consume a
  lot of memory over time [bug 43726]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9480 (2017-06-15)

Bug Fixes Since Baselight 4.4m1.9418
====================================

* Fixed failure to render image sequences to paths which are not
  within /vol [bug 43256]

* The Avid DNxHD/DNxHR SDK crashes when used on older CPUs which lack
  SSSE 3 and/or SSE 4.1, including some Generation III and older
  Baselight systems. To prevent this, the SDK is no longer available
  on these systems, which means DNx media can no longer be read or
  written using these systems.

  We apologise for this loss of functionality, which is due to the
  behaviour of a 3rd-party SDK [bug 43240]

* Turned off CRC generation in DNx encoding, and CRC checking in DNx
  reading, due to ambiguities between the VC3 specification and Avid's
  SDK leading to false reporting of CRC errors in both Baselight and
  other software [bug 43236]

* Fixed decoding using RED Rocket on Baselight FOUR/EIGHT systems, and
  when using a RED Rocket installed in a remote system [bug 43369]

* Added support for NVIDIA 375.66 driver for Titan Xp GPUs

* Allow baselight systems running 367.44 driver to use 375.66 driver to
  fix incorrect RED GPU decoding [bug 42821]

* Fix problem pasting existing formats [bug 42975]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9418 (2017-05-30)

New Features Since Baselight 4.4m1.9286
=======================================

* Updated to ARRI Metadata Bridge 1.1.0.1. This SDK manages the
  transfer of metadata from ARRIRAW input media to OpenEXR output
  media [bug 41456]

* Updated to DNxHD/DNxHR SDK version 2.3.3. This includes bug fixes
  and adds CRC integrity checking of DNx data [bug 41552]

* Added additional movie frame rate options to Render View [bug 41699]

* Added "Show SDK Versions" button to About dialog to display version
  numbers of 3rd-party SDKs [bug 41740]

* The Sony XAVC Encoder SDK has been updated to version 1.1.6, and the
  Sony SMDK Toolkit has been updated to version 4.12. This adds
  support for the following new 10-bit XAVC operating points:
  
  - XAVC QFHD Long422 100           @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long422 140           @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Long422 200           @ 23.98p, 25p, 29.97p, 50p, 59.94p

  The XAVC-encoder update also brings a picture quality improvement
  for HDR content, and updated AVC-essence colour space tags for SLog3
  and PQ / Rec.2020 [bug 41772]

Bug Fixes Since Baselight 4.4m1.9286
====================================

* Fixed black point and white point setting in ACEScct.flspace.
  This does not change the transformation itself, but only where 
  lines are displayed in the histogram [bug 41494]

* Prevented the mona lisa symbol from disappering when the previous
  selected strip has the same matte configuration than the new one
  [bug 40108]

* Fixed crash when an audio filename entered on Scene Settings View
  does not contain a / [bug 41144]

* Improved text shown when dragging buttons in Chalk [bug 41170]

* Fixed swapped colour channels in rotated Canon RMF media [bug 41168]

* Fixed a crash on shutdown that could occur after reading JPEG 2000
  material without a GPU JPEG 2000 acceleration licence [bug 41194]
  
* Fixed hang when selecting stack bottoms left and having the timeline
  cursor off the end in filler [bug 41215]

* Fixed issue creating a zero-area area tracker from a zero-area 
  shape [bug 39048]

* Fixed crash when tracking some very large material [bug 39209]

* Relaxed the per colour component bitrate restriction when rendering
  DCI compliant JPEG 2000 material at 4K using GPU acceleration. This
  can improve image quality somewhat in a few cases. A progression
  order change (POC) has also been added to the codestream for this
  essence type to improve compliance with the 4K digital cinema
  profile [bug 41292]

* Fix crash importing CDL [bug 41365]

* Fixed reading of subsampled JPEG 2000 files using GPU JPEG 2000
  acceleration, and added support for bitdepths other than 8 or 16
  [bug 41420]

* Fixed possible crash in Multi-Paste View when doing "Restore Config
  to Defaults" [bug 41316]

* Fixed hang reading damaged JPEG2000 files [bug 41178]

* Fixed issue where OFX plugins could become unavailable [bug 41554]

* Fixed an issue where the GPU JPEG 2000 decoder could grab GPU memory
  when it shouldn't, e.g. when using the sequence browser, generating
  thumbnails or when the acceleration parameter was set to CPU only
  [bug 41681]

* Fixed incorrect colour space warnings on Render View when using "Use
  Input Format" [bug 41697]

* GPU JPEG 2000 acceleration is no longer done on the GPU in image
  server processes. CPU acceleration will still be used if a licence
  is available [bug 41700]

* The GPU JPEG 2000 licence dialog no longer appears in Baselight
  CONFORM [bug 41345]

* Fixed dpm (disk performance monitoring in fl-diag) enumerating the
  incorrect devices on Gen VI systems due to a change in the way
  Adaptec formats device data on later RAID controllers [bug 41753]

* The XAVC Encoder SDK has been updated to version 1.1.6, which fixes
  an issue where the encoder was prone to hang at the end of the
  render. Rendering to XAVC LongGOP codecs is now enabled again. The
  supported XAVC LongGOP operating points are:
  
  1280x720:
  - XAVC HD Long422 50     @ 50p, 59.94p

  1920x1080:
  - XAVC HD Long422 25     @ 50i, 59.94i, 23.98p, 25p, 29.97p
  - XAVC HD Long422 35     @ 50i, 59.94i, 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC HD Long422 50     @ 50i, 59.94i, 23.98p, 25p, 29.97p, 50p, 59.94p

  3840x2160:
  - XAVC QFHD Long 60     @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long 100    @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long 150    @ 50p, 59.94p
  - XAVC QFHD Long422 100 @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long422 140 @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Long422 200 @ 23.98p, 25p, 29.97p, 50p, 59.94p

  [bug 39814]

* Improved error messages shown when the advertise service is not
  running [bug 41812]

* Fixed appearance of tooltip glow when the control being highlighted
  is scaled down [bug 41903]

* Fixed an issue where the QuickTime 'glbl'-atom was not handled
  correctly when encoding and decoding the FFV1 codec, resulting in
  invalid files being rendered and decode failures on read [bug 31971]

* The identification of XDCAM essence in MXF-files has been
  improved. Some files that previously identified the source simply as
  "MPEG" now identifies it as "XDCAM HD/EX". Files with a
  picture essence coding label matching XDCAM HD 422 specifically will
  now present the source as "XDCAM HD 422" [bug 42043]

* Files with the source codec "XDCAM HD 422" now correctly identifies
  the writer codec as XD42, allowing use of the "Prefer Source Codec"
  option when rendering [bug 42045]

* Fixed an issue where bl-reset-cache refused to reset the cache if
  it contained Apple '._' resource files [bug 41281]

* Fixed a bug which prevented bl-reset-cache from hard-resetting an
  SSD array on a cache-only BL1 [bug 41106]

* Fixed display of 8 bit 420 YCrCb disk cache files on OSX [bug 39375]

* Fixed errors using ARRIRAW media with a 2868x2152 resolution in a
  2880x2160 sensor [bug 40649]

* Fixed errors decoding ARRIRAW media at proxy resolutions using CPU
  rendering [bug 42541]

* Fixed incorrect use of %R resolution directory when conforming media
  with mulitple resolutions, e.g. ARRIRAW files [bug 42642]

* The libraw library, used to decode camera RAW files, has been
  updated to version 0.18.2. This adds support for a number of new
  cameras, and also improves decode of some existing formats, e.g.
  reading of correct black levels from Sony SR2-files. NB: This can
  alter the look of RAW-files in existing scenes [bug 42628]
  
* Fixed issue with 5.0 operators stored in the matte tool
  configuration crashing when adding a matte tool in 4.4m1 [bug 42116]

* Fixed corruption at node boundaries on BL4/BL8 when viewing in
  floating point format [bug 42696]

* Fixed errors setting filmlight user's home directory in macOS
  installer [bug 42543]

* Allow an empty hostname to be used in the preference database dialog
  box [bug 42701]

* Fixed an issue where ProRes rendered to QuickTime could be missing
  up to a seconds worth of audio at the end of the file [bug 35642]

* Fixed incorrect interactive render of very small blurs [bug 41662]

* Fixed errors decoding RED media on a system with a RED Rocket or RED
  Rocket X card, when the media is unsupported by the card, notably
  from 8K Helium sensors [bug 41201]

* Fixed failures when rendering on a multi-GPU FLUX Store [bug 42871]

* Fixed an issue where DCPs with missing entries in the ASSETMAP could
  cause dcpproxy to crash [bug 42998]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9286 (2017-04-20)

Bug Fixes Since Baselight 4.4m1.9274
====================================

* Fixed crash accessing audio files/movies on external media or
  remote Baselight systems [bug 41679]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9274 (2017-04-06)

New Features Since Baselight 4.4m1.9217
=======================================

* Sony RAW media (from F5, F55, F65, FS700 cameras) is now decoded
  using the Sony SDK. This makes the image quality match the decode
  from other applications using the same SDK. In addition, supersize
  decodes of F65 media are now supported (to 8192x4320, 7680x4320,
  8192x2160 and 6144x3240). Note that existing Sony RAW media in
  existing scenes will continue to decode as they did before; this
  change only applies to newly-added media [bug 41256]

Bug Fixes Since Baselight 4.4m1.9217
====================================

* Fixed application lock-up issues when using a Dolby Vision CMU on a
  network where DNS lookups produce a very long delay [bug 36823]

* Fixed an issue in 'Import EDL' that can occur when filenames in an
  AAF contain special characters [bug 38820]

* Fixed crash when conforming using Keycode [bug 41267]

* Fixed a bug in conform that affected some EDLs with zero length
  events, when conforming with relative frame offsets [bug 30483]

* Fixed occasional "Discontinuous timecode" errors when rendering to
  ProRes or DNxHD QuickTime [bug 41518]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9217 (2017-03-27)

Bug Fixes Since Baselight 4.4m1.9174
====================================

* Fixed resolutions read on Mac OS X from some QuickTime movies with
  non-square pixels and clean-aperture metadata [bug 41164]

* Fix crash importing CDL [bug 41365]

* Fixed freezing of image on node 0 of a BL4/8 during playback
  [bug 41746]
재생시 베이스라이트 4/8시스템의 노드0(node0)에서 이미지가 멈추는 현상 개선
--------------------------------------------------------------------------

Baselight Release 4.4m1.9174 (2017-03-14)

New Features Since Baselight 4.4m1.9153
=======================================

* To reduce confusion which was caused by the introduction of correct
  QuickTime colour space tagging in Baselight 4.4m1.9029, the Render
  View now offers the choice to use "Legacy" tagging. This tags output
  QuickTime movies as Rec.709, PAL or NTSC based purely on the
  resolution of the image. The new behaviour which tags the movie
  using information from the render colour space is available by
  selecting "Automatic" tagging [bug 31853]

Bug Fixes Since Baselight 4.4m1.9153
====================================

* Fixed failure to copy some file types in flux/fl-cp [bug 41500]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9153 (2017-03-07)

New Features Since Baselight 4.4m1.9103
=======================================

* Updated Linear Colour Space Package on Support Website, to reflect
  latest MetaData updates [bug 39435]

* Added "ACEScct: ACEScct / AP1" colour space. This is a improved
  working colour space for grading in an ACES Workflow. It is similar
  to ACEScc in the midtones and highlights, but has a "toe" in the
  shadow region of the curve [bug 38783]

* The command line utility for creating KDMs, formerly called
  'dcptool', has been renamed to 'fl-kdmtool' [bug 38946]

* Added Photo RAW Params dialog for handling control of exposure,
  camera white balance and colour space of camera RAW files. Automatic
  colour space selection now works for camera RAW files as well.
  PLEASE NOTE: Scenes using this new operator cannot be opened in
  previous versions of the software [bug 32363]

* fl-imageinfo -v now reports pixel aspect ratio when it is not 1:1
  [bug 39324]

* Added support for writing little endian PCM audio to QuickTime files
  on Linux [bug 26720]

* Added diagnostic for Cubix Xpander chassis [bug 36457]

* The New Workspace command now requests a workspace name [bug 40258]

* Added support for additional codec identifiers in QuickTime, MP4 and
  AVI containers. 'h264', 'H264', 'x264', 'X264', 'h265', 'H265',
  'x265', 'X265' fourCC codes are now recognised [bug 40377]

* Baselight 4.4m1 will no longer allow a job to be created if a 5.0-
  format job of the same name exists [bug 36816]

* The lists of reels and KDMs in the DCP render tab are no longer
  displayed in a small scrollable window, instead expanding to always
  show the full list of entries. A number of additional columns that
  can be optionally displayed have been added as well [bug 40715]

* The GPU JPEG 2000 acceleration can now be controlled via the DCP
  Params strip when reading DCPs. Options to control its usage have
  also been added when rendering supported J2C-files, DCI compliant
  MXFs and DCPs. The different settings only have an effect on
  machines with a GPU JPEG 2000 license [bug 40581]

* Updated ACES and Telecine Scene Templates. The templates now use %w
  for filename and folder name in shot-based deliveries. The ACES
  template now uses ACEScct as its Working Colour Space [bug 39079]

* Updated Apple ProRes library. It now encodes additional internal
  metadata, but has no visual or performance changes [bug 39611]

* The colour space of some QuickTime files with known 'nclc' and
  'gama' tags is now assigned appropriately [bug 39480]

* This release adds the ability to respond to a version 5.0 or later
  application running on another system [bug 39384]

Bug Fixes Since Baselight 4.4m1.9103
====================================

* Fixed crash exporting a LUT including the Input transform for a
  stereo input sequence [bug 38918]

* Fixed issues with gallery grabs from cloud media [bug 39114]

* Fixed comments read from ARRIRAW files, particularly ALEXA Mini MXF
  files [bug 39148]

* fl-imageinfo now shows "full sensor" resolution of files, to match
  Sequence Browser [bug 39168]

* Updated MPEG-4/SStP libraries, making rendering of these codecs
  available on Mac again [bug 37707]

* Fixed crash verifying some scenes [bug 39454]

* Fixed warning message when quitting bl-render while a movie render
  is in progress [bug 39810]

* Fixed bug stopping .LUT-CLUT files being included in cube file lists
  [bug 39825]

* Fixed an issue with the bitrate selection dialog when rendering DCI
  compliant JPEG 2000 files, where the dialog did not update to
  reflect the selected bitrate [bug 39851]

* Timecode 2 is now displayed from OpenEXR sequences written by
  FilmLight tools [bug 39927]

* Fixed failure to write OpenEXR files from some ARRIRAW source files
  that had bad timecode metadata [bug 39038]

* Fixed an issue that could cause a crash when annotations to a DCP
  could not be parsed for display in the render panel [bug 40201]

* When editing the size of burnin text by dragging on the image, the
  text height is now constrained to the same limits as on the Formats
  editor [bug 40349]

* DCP related movie writing parameters no longer clutter the render
  command after visiting the DCP render tab. This also fixes an issue
  where an error dialog would appear when setting movie writing
  parameters for a codec other than DCP after visiting the DCP tab.
  The 'dcp_bitrate' movie writing parameter has been deprecated in
  favor of using 'dci_bitrate' for DCI MXF and 'dcp_video_bitrate' for
  DCP to achieve the same effect [bug 38859]

* Disabled the Discrete / Interleaved audio setting in the DCP render
  tab as it is determined by the format and thus has no effect
  [bug 39844]

* Fixed use of the keyboard Escape key to trigger the Cancel button on
  modal dialogs [bug 40546]

* Sliders for R3D Parameters controls that have no effect in Automatic
  decode mode are now disabled [bug 40628]

* Fixed crash with dragging and dropping a cut view thumbnail when the
  mouse cursor was in filler and there was no strip selected
  [bug 36988]

* Fixed an issue where the default number of threads displayed in the
  QuickTime H264 codec parameters dialog did not match the number of
  threads actually used. The default number of threads displayed is
  now 0 to signify that the value will be determined automatically
  [bug 40702]

* Fixed potentially incorrect colour space conversions between strips
  in misaligned stacks [bug 40729]

* Added support for reading timecode from Sony XAVC MP4-files with
  realtime metadata tracks [bug 40706]

* Improved the wording of a warning on the Colour Space Journey View
  [bug 39725]

* Fixed excessive CPU usage by cleaner service [bug 40066]

* Improved help text for fl-setupssh [bug 40196]

* Prevented illegal hostnames for preference database [bug 40541]

* Fixed hang/crash changing "Display and Timeline Cache" format
  [bug 40975]

* Fixed crash in MXF reader when audio read fails, e.g. from Panasonic
  Varicam files [bug 40968]

* Fixed bug where saved cursor settings for a Truelight profile or
  cube were not correctly reloaded on reopening the scene
  [bug 40880]

* Fix a problem that prevented a job being exported on OS X and 
  then re-imported [bug 40935]

* Improved performance when reading large multi-part OpenEXR files.
  Note that this improvement only affects newly-inserted OpenEXR
  sequences; to apply to existing sequences use the Update sequence
  button on the Sequence operator [bug 41123]

* Fixed an issue where KDMs created using fl-kdmtool could contain
  empty ContentAuthenticator and DeviceListDescription tags
  [bug 41156]

* Fixed resolutions offered when conforming media with crop
  resolutions [bug 40370]

* Fixed resolutions read from some QuickTime movies with badly-formed
  clean-aperture metadata [bug 41164]

* Improved Chalk for Slate button lists [bug 37281]

* Fixed incorrect warnings about linear colour spaces in the Colour
  Space Journey View [bug 39434]

* Fixed a crash on shutdown that could occur after reading JPEG 2000
  material [bug 41194]

* Added Chalk for Slate save-to and load-from file [bug 37394]

* Updated parts of RED SDK to version 6.2.2 [bug 41209]

* Fixed failure to decode some ARRIRAW media at half-resolution when
  using CPU rendering [bug 40368]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9103 (2017-02-20)

New Features Since Baselight 4.4m1.9029
=======================================

* Added new NCLC Tagging for Quicktime Exports. Quicktime NCLC Tags 
  can now but specified in the .flspace file. This should fix
  current Gamma Shifts when Quicktime Movie Files are viewed in a
  ColorSync managed Application like Quicktime X and Safari.
  [bug 31853]

Bug Fixes Since Baselight 4.4m1.9029
====================================

* Fixed an issue that caused the GPU accelerated JPEG 2000 decoder to
  attempt decoding other codec types as well, resulting in error
  messages printed to the console [bug 40857]

* Fixed crash in bl-applyblg [bug 40881]

* Fixed a decoder failure that could occur when attempting to read
  XDCAM encoded MXF files with missing reference frames in the stream
  [bug 40851]

* Fixed reading QuickTime clean aperture (crop rectangle) metadata on
  Mac OS X [bug 36665]

* Fixed hang/crash changing "Display and Timeline Cache" format
  [bug 40975]

* The GPU accelerated JPEG 2000 encoder now sets the correct value of
  the rsiz capabilities parameter in the codestream [bug 41087]

* Fixed dragging and dropping between galleries [bug 39529]

--------------------------------------------------------------------------

Baselight Release 4.4m1.9029 (2017-02-02)
 
New Features Since Baselight 4.4m1.8951
=======================================
 
EDL Import
----------
 
* We are now able to read the following additional metadata columns
  from CMX3600, AAF and ALE files:
     ASC_CC_XML     Filename of a CDL/CCC colour correction XML file,
                    or the name of a correction within a CCC XML file.
     LUT            Filename of a 3D LUT file.
     LUT2           Filename of an additional 3D LUT file.
 
  When in CMX3600 EDLs, they are represented as comments. For example:
   002 Day04A021L3CG V    C        09:24:53:07 09:24:54:17 10:00:04:21 10:00:06:06
   * LUT: input_A021C006_121018_L3CG.new.01_4.cub
   * LUT2: output_A021C006_121018_L3CG.new.01_4.cub
   * ASC_CC_XML: shot1.cdl
 
* The ASC_SOP, ASC_SAT, ASC_CC_XML, LUT and LUT2 columns are now shown
  in the EDL Import's scrolling metadata, when present.
 
* The ASC_CC_XML, LUT and LUT2 columns can now be selected for display
  in the Shots View.
 
* When LUT metadata is present in an EDL, the "Apply LUTs" option
  become available. If "Yes" is selected, then EDL Import will search
  a specified directory looking for LUT files whose filename matches
  the contents of the LUT column. If found, a layer containing a
  Truelight operator referencing the LUT will be inserted. Additional
  controls allow the user to specify the layer number, colour and
  categories of the inserted layer.
 
* Similarly, when LUT2 metadata is present, the "Apply LUT2s"
  option appears - it's behaviour is identical to "Apply LUT".
 
* When ASC_CC_XML metadata is present in an EDL, the
  "Apply CCC/CDL XMLs" option become available. If "Yes" is selected,
  then EDL Import will search a specified directory looking for CCC/CDL
  XMLs files whose filename matches the contents of the LUT column. If
  a matching file isn't found, it will look for a match in the
  description field of corrections within the CCC XML files. If found,
  a layer containing a CDL operator representing the correction will be
  inserted. Again, controls allow the user to specify the
  layer number, colour and categories of the inserted layer.
 
* It is now possible to specify the layer number, strip colour and
  categories of strips inserted by the "Apply ASC CDL Grades" option.
 
Multi-Paste
-----------
 
* Added the following additional "Match By" filters:
    Source LUT
    Source LUT2
    Source Scene
    Source Scene & Take
    Source Camera Roll
    Source Lab Roll
    Source Camera
    Source ASC_CC_XML
 
* Added the ability to multi-paste 3D LUT files and CDL/CCC XML files,
  in a similar way to how BLGs are pasted now. When either of these
  options is selected, options appear to allow the user to select the
  directory to search for the files, as well as the layer number,
  colour and categories of any inserted strips.
 
  The functionality is that same as that offered during EDL Import,
  but more flexible because multi-paste can paste LUTs/XML files
  by matching against any column.
 
Miscellaneous
-------------
 
* Added Big Metadata View which provides an easily-visible display of
  metadata on the UI monitor [Bug 19640]
 
* Updated to RED SDK v6.2.2. This includes bug fixes and the following
  changes:
  - 8K sensor support.
  - New colour primaries option "RED Wide Gamut RGB".
  - New tone curve option "Log 3G10".
  - Minimum Rocket-X driver version is now 2.1.34.0
  - Minimum Rocket-X firmware version is now 1.4.22.18 [bug 38924]
 
* In HD/2K video modes, the image output is now cloned across all
  outputs on AJA Kona 4 and Io4K devices. This is particularly useful
  on Mac OS X where some applications will use SDI 3/4 for HD video
  output whereas FilmLight applications use SDI 1/2 [bug 33661]
 
* "fl-queuetool log" now shows the operation's progress and last
  action [bug 37924]
 
* Added "%w" substitution for render filenames. This expands to the
  filename prefix, defined as the filename up to the last set of
  digits, if present, omitting a '.', '-' or '_' character before the
  digits. If the digits are at the start of the filename they are
  removed, along with a following '.', '-' or '_' character and the
  filename extension [bug 38369]
 
* Added additional metadata to OpenEXR output files identifying the
  scene DRT and the Input, Working, Grade Result and Viewing (Render)
  Colour Spaces [bug 38493]
 
* Added Draft quality option in Cursor View and Render View. This
  option selects a faster lower-quality decode for large ARRIRAW media
  [bug 37062]
 
* Black or chequer frames produced during renders as replacements for
  error frames now use the black and white levels of the render colour
  space [bug 37925]
 
* Added "ACEScct: ACEScct / AP1" colour space. This is a improved
  working colour space for grading in an ACES Workflow. It is similar
  to ACEScc in the midtones and highlights, but has a "toe" in the
  shadow region of the curve [bug 38783]
 
* Added Colour Space Journey View info for OFX plugins [bug 38752]
 
* Added new sequence output type "FLYCC". This writes files which are
  optimised for efficient playback when the file variant matches the
  scene's Display And Timeline Cache setting [bug 36543]
 
* Render which are in progress in the Operations Queue when an
  application crash occurs are no longer automatically resumed when
  the application is next launched, to reduce the likelihood of a
  repeated application crash [bug 33472]
 
* Added 'Tetrahedral' option to Truelight settings in Render panel to
  specify high-quality Tetrahedral interpolation for profiles/cubes
  applied via the Render panel [bug 29283]
 
* Improved workflow for rendering on FLUX Store systems. It is no
  longer necessary to run bl-render on another system; a worker
  service runs on the FLUX Store to process operations submitted to
  its queue [bug 33791]
 
* Updated to ARRIRAW SDK 5.3.0.12. This includes performance and image
  quality improvements [bug 38923]
 
* Updated to Sony RAW SDK v2.4.0. This improves image quality and
  addresses some minor bugs, notably with X-OCN decoding [bug 38910]
 
* Added support for writing little endian PCM audio to QuickTime files
  on Linux [bug 26720]
 
* Added diagnostic for Cubix Xpander chassis [bug 36457]
 
* Dolby Vision functionality is now included in Baselight without a
  licence since Dolby now handle licensing in their CMU [bug 40334]
 
* Baselight 4.4m1 will no longer allow a job to be created if a 5.0-
  format job of the same name exists [bug 36816]
 
* Added support for reading of an additional variant of AVC-Intra MXF
  files as created by e.g. Airspeed/Nexis [bug 40556]
 
* AJA SDI monitoring is now enabled for Baselight CONFORM on macOS
 [bug 39146]
 
* GPU accelerated JPEG 2000 encoding and decoding is now available
  with an additional license on systems equipped with at least one
  Titan X GPU. Resolutions up to full frame 4k (4096x2160) will be
  handled on the GPU. Formats larger than 4k may fall back to a CPU
  implementation which is significantly faster than what is available
  without the additional license. Acceleration is supported for DCP,
  JPEG 2000 codestream files (J2C) and JPEG 2000 encoded MXF movie
  files at this time [bug 32939]
 
Bug Fixes Since Baselight 4.4m1.8951
====================================
 
* Reverted Disk Performance Monitoring (dpm) to test with small files
  on 3ware equipped systems so that latency figures and their
  thresholds are consistent with previous versions [bug 37490]
 
* Fixed pixel aspect ratio of QuickTime movies on Mac OS X [bug 37551]
 
* Fixed error when verifying a both-eyes render [bug 37629]
 
* Fix support for AJA Kona 4 and Io4K devices when using UFC
  firmware [bug 37770]
 
* Improved Truelight file list generation to prevent delays when first
  opening a scene which uses a Truelight directory with a large number
  of LUT files [bug 36826]
 
* Fixed incorrect deliverable duration when rendering using "All
  Frames" and with a Render Frame Rate different from the scene's
  Working Frame Rate [bug 37861]
 
* Fixed LUT export problem when exporting more than one LUT per shot,
  when the input colour space conversion could be included in all
  LUTs when only selected for the first [bug 37881]
 
* MXF files with ARRI LogC tone curve are now assumed to be in Wide
  Gamut and are assigned an appropriate colour space [bug 36916]
 
* Fix to Compress Gamut for all negative values [bug 37826]
 
* Fixed crash on exit related to changes in formats [bug 37996]
 
* Fixed labels on pivots in FilmGrade's graph not appearing
  when hovering over the pivot lines [bug 38164]
 
* Fixed incorrect animation when splitting some strips, including Edge
  Crop strip [bug 38284]
 
* Fix copying and pasting parameters in Colour Space, Look, Image
  Transform Settings and Dolby Vision strips [bug 38283]
 
* Fixed an issue that prevented reading of MXF files with CBR indexed
  material spread across multiple file partitions, e.g. some MXF files
  with DNxHD essence [bug 37808]
 
* Fixed crash reading a specific badly-formed AAF file [bug 38441]
 
* Fixed incorrect errors reported when reading some TIFF files
  (e.g. from DVS Clipster) [bug 38514]
 
* Fixed channel and track handling from multi-part OpenEXR files
  written by Nuke [bug 38431]
 
* The "Maximum number of entries in on-disk image cache" preference
  can now be increased to 4 million [bug 36553]
 
* Fixed crash viewing single eye in a stereo scene (while scrubbing)
  [bug 36012]
 
* Fixed errors rendering both-eye stereo when there is an error on the
  right eye [bug 37860]
 
* Fixed flioinfo read failure: no such file or directory [bug 38537]
 
* Fixed incorrect frames being rendered at shot boundaries when
  rendering at a much slower frame rate than the working frame rate
  [bug 38601]
 
* Fixed "Waiting for in-use movie to be closed" error when two
  deliverables write to the same output movie filename [bug 33767]
 
* Fixed "Movie is not open" error during rendering on some system
  configurations [bug 39231]
 
* Fixed failures when using OpenEXR files with very large numbers of
  channels [bug 38716]
 
* Fixed decode of QuickTime movies with rotated video, as created by
  for example iPhones [bug 38249]
 
* Limited warnings about screen layout changes on OS X to only report
  when screen resolutions or layouts have actually changed
  [bug 36194]
 
* Fixed an issue that prevented some MXFs with broken footer
  partitions from being read, e.g. some files containing ARRIRAW
  [bug 38842]
 
* Fixed an issue where renders of XAVC to Sony MXF could sometimes
  leave a 'Processing index' progress message less than 100% after
  completion [bug 38844]
 
* Fixed crash due to invalid mask settings being retained from one
  scene to another [bug 35026]
 
* Fixed issue which could cause movie renders not to restart after
  being suspended (e.g. during playback) [bug 35514]
 
* Reduced sequence fragmentation when rendering files, which can
  significantly improve playback speed [bug 37892]
 
* Fixed reading of MXF files without given duration but with
  CBE-index, making it possible to determine duration from essence
  size [bug 38866]
 
* Fixed an issue where KDMs created by the command line utility
  dcptool did not correctly transfer forensic mark flags and
  authenticated devices from the DKDM [bug 39173]
 
* The fix to bug 36285, full range 4:2:0 data in MP4 and QuickTime
  containers was squashed to legal range on read, did not preserve the
  behaviour of existing scenes. Behaviour preservation is now
  restored. This in turn may change the behavior of some existing
  scenes created in release 4.4m1.8720 or later. Behaviour in those
  scenes can be restored by updating sequences to match media
  [bug 39176]
 
* Fixed failures copying using fl-cp to a non-volume directory local
  to the current machine [bug 38180]
 
* Fixed various issues preventing EDL conform and subsequent Modify
  AAF/Modify XML rendering when the EDL and/or the source or rendered
  movies are on cloud media [bug 31869]
 
* Reduced video memory usage to fix playback slowdowns
 
* Fixed issue which could cause scenes to be marked as needing saving
  immediately after opening [bug 37260]
 
* Fixed reading of 10-bit RGB from AVC-encoded MXF files [bug 39359]
 
* Fixed progress updates when consolidating large files [bug 32517]
 
* Fixed bug which could cause the UI to become sluggish when temporal
  effects were placed at the bottom of very complex stacks [bug 39390]
 
* Fixed freetype error message on application startup [bug 39493]
 
* Fixed mask drawing so the top line of the image is no longer visible
  outside the mask at 4K [bug 34378]
 
* Encrypted Interop DCPs were previously created using the wrong
  signing algorithm; SHA256 instead of SHA1. This affected Interop
  DCPs, corresponding KDMs and the certificates used to create and
  sign these packages. Two separate certificates are now created on
  install, one for SMPTE and one for Interop. The SMPTE one is named
  fl-certificate-chain as before, and the interop one is named
  fl-interop-certificate-chain. Both are stored in /usr/fl/etc/cert on
  Linux or /Library/Application Support/FilmLight/etc/cert/ on Mac. A
  new preference for specifying default Interop certificate has been
  added. Preferences have also been simplified to remove the need to
  specify the public certificate separate from the chain of trust, as
  the chain of trust is commonly appended to the public certificate
  [bug 39035]
 
* Fixed a bug where Interop KDMs were written with SMPTE formatted
  cipherdata payloads. The cipherdata payload in all KDMs also
  referenced an incorrect certificate reference [bug 39665]
 
* Fixed reading of MXF OpAtom files where the index is split over
  multiple segments [bug 39700]
 
* Fixed a broken path to the openssl command in fl-certgen on Mac
  [bug 39775]
 
* Fixed crash when using some OFX plugins [bug 39590]
 
* Fixed "Internal error - bad movie type" error when rendering on
  commandline [bug 39566]
 
* Fixed fl-diag error in X11 configuration test on FLUX Store systems
  [bug 39818]
 
* Fixed crash editing burnin in a newly-created format [bug 39830]
 
* Fixed crash Analysing Dolby Vision sequences [bug 39667]
 
* Improved LUT file reading to minimise delays [bug 39692]
 
* Fixed an issue that could cause the sequence browser to fail to
  find the default self-KDM on encrypted DCPs [bug 39881]
 
* Fixed failures with some OpenEXR files with non-standard channel
  naming schemes [bug 39544]
 
* Fixed an issue where the PackingList (PKL) file in DCP packages had
  mismatched values for the asset Type-tags. Interop values were used
  for SMPTE DCPs, and SMPTE values were used for Interop DCPs
  [bug 40263]
 
* Ensure that the tnd service is started after the vol service
  [bug 39897]
 
* Ensure that the render service is started after the xorg service
  [bug 40115]
 
* Fixed bug where rendering to Movie+Audio with channels set to Auto
  would not create any audio channels in the rendered movie in the
  following situations:
 
    - a movie with audio was inserted into the timeline
    - audio was set in the Scene Settings using an audio/movie file
    - audio was set in the Scene Settings using stem files
 
  Baselight will now correctly determine the source audio channel
  count in these situations [bug 39836]
 
* Fixed bug where rendering to Audio file with channels set to Auto
  would fail with poor error message [bug 39887]
 
* Fixed interpretation of Circle Take values when importing a scene
  from Daylight. Circle Take flags from Daylight are converted into
  "Y" or "N" in Baselight Shots View and in Burnins [bug 37324]
 
* Fixed incorrect colour space assignment to some varieties of ARRIRAW
  media [bug 40489]
 
* The Subtitle reader will additionally look for its fonts in the
  directory containing the subtitle xml file [bug 38899]
 
* The default number of threads used to encode ProRes and H264 written
  to QuickTime movies now has an upper limit of 16. This fixes an
  intermittent issue with slow encoding speeds of H264 on newer Linux
  systems [bug 40641]
 
* A dissolve that used a colour space name longer than 22 characters
  could cause a fatal error, usually during the conform process
  [bug 40725]
 
* Fixed render corruption on systems running 304/319 nvidia drivers
  [bug 38365] [bug 38459] [bug 39902]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8951 (2017-01-05)

Bug Fixes Since Baselight 4.4m1.8932
====================================

* Fixed "excessive recursive invocations" error seen with some scenes
  when opening Shots View [bug 34400]

* Fixed an issue in conform with saved EDL search directories that 
  would cause conform to fail with a 'canonical path' error
  [bug 34987]

* Fixed failures on "Not connected to Audio System" errors [bug 20213]

* Fixed bright pixels caused by bad sensor data in non-packed Phantom
  Cine RAW files [bug 40187]

* Fixed an issue that could cause 4:2:0 material in QuickTime and MP4
  containers to be stretched from legal to full on read. Notably
  affected AVC/H264 [bug 39525]

* Fixed remote rendering on a multi-GPU FLUX Store [bug 40086]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8932 (2016-12-13)

Bug Fixes Since Baselight 4.4m1.8800
====================================

* Updated Dolby Vision analysis algorithm to match latest Dolby
  specification [bug 39428]

* Updated Slate firmware to 1.0.21.25.  This new firmware resolves
  some USB connection issues experienced at a few customer sites.
  Please contact FilmLight support before updating your Slate.
  [bug 39614]

* Fixed startup crash on BLX systems during "Starting Renderer"
  [bug 38505]

* Fixed a bug that could cause fl-diag to fail on the Adaptec Remote
  Access check [bug 33146]

* The Adaptec StorMan services can affect disk performance; run only
  when required (via the raidadaptec diagnostic's 'launch web interface'
  button) [bug 39944]

* Fixed bug that caused the Blackboard output on a Quadro K1200 GPU
  to be mapped to the wrong connector [bug 39689]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8800 (2016-11-08)

Bug Fixes Since Baselight 4.4m1.8766
====================================

* Fixed OpenEXR writing on FilmLightOS 2.1 systems [bug 38977]

* Fixed ARRIRAW Params "Colour Primaries" setting in legacy scenes
  using Baselight decode [bug 39154]

* Fixed access to 2560x2145 decode of ALEXA Mini MXF files captured at
  this resolution [bug 39104]

* Fixed a misnamed XML tag in KDMs generated for encrypted DCPs. KDMs
  created prior to this fix will no longer be usable, but can be
  recovered by manually editing the KDM XML file to rename
  DCinemaSecturityMessage to DCinemaSecurityMessage [bug 39158]

* Fixed crash reading latest 8K R3D media [bug 39156]

* Fixed video memory over allocation [bug 39152]

* Fixed Dolby Vision operation in stereo modes with AJA Kona4 hardware
  [bug 38187]

* Fixed crash when reading audio from some cloud-media movie files
  [bug 38494]

* Reduced video memory usage to fix playback slowdowns [bug 39168]

* New Blackboard2 firmware is available for customers having specific
  DVI issues. Contact FilmLight support for important instructions
  on how to apply this. Do not attempt this update without FilmLight
  involvement, as you risk damage to the Blackboard2 [bug 39058]

* Reliability fixes to slate-update-firmware [bug 39105]

* New Slate firmware (1.0.16.16). Please contact FilmLight support
  before updating to prevent damage to the Slate. New Slate firmware
  displays logo on back screens when baselight is not running, and
  improves reliability of Slate. [bug 27724] [bug 38997] [bug 39108]

* Fixed "Error processing RED data" errors when rendering some R3D
  media [bug 37705]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8766 (2016-10-26)

Bug Fixes Since Baselight 4.4m1.8720
====================================

* Fixed lists of Dolby Vision mastering and target displays not being
  updated when a CMU is detected [bug 38909]

* Fixed incorrect Dolby Vision XML export with dissolves [bug 38930]

* Fixed rendering of Northlight mattes on OSX [bug 39000]

* Fixed long delays after stopping cached playback of ARRIRAW media
  [bug 39090]

* Fixed failure to start remote rendering on a FLUX Store when there
  are vncserver processes running [bug 39070]

* Fixed loading of ASC_SOP values from CMX3600 EDLs [bug 39005]

* Fixed crash rendering long scenes with subtitles [bug 39007]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8720 (2016-10-06)

New Features Since Baselight 4.4m1.8607
=======================================

File Formats
------------

* Added support for reading HEVC (h.265) encoded QuickTime and MP4
  files [bug 36531]

* Added support for reading Sony X-OCN format from MXF files
  [bug 37061]

* Added V-RAW Params for controlling the exposure and colour
  temperature of Panasonic Varicam RAW files [bug 36975]

* Added support for reading the "clean aperture" rectangle stored in
  QuickTime files. This is used, for example, in ProRes files written
  by ARRI cameras [bug 36665]

* Support for reading and writing encrypted DCPs has been added, as
  well as a new dedicated DCP render tab allowing improved control
  over DCP structure and metadata.

  Certificates and self-encrypted DCPs
  When the software is installed, it will create a self-signed root
  certificate, an intermediate certificate and a leaf certificate. The
  default certificate preference point to this generated leaf
  certificate.

  To select a different certificate, open the Preferences dialog, go
  to the 'System' tab and scroll down to the 'DCP' section. There you
  need to select three files:
  1. A file containing the private key, stored in PEM format. The
     contents of the file should start with =-----BEGIN RSA PRIVATE
     KEY-----=. The private key must be usable without a password.
  2. A file containing the public certificate, also in PEM format. The
     contents of the file should start with =-----BEGIN
     CERTIFICATE-----=.
  3. A certificate trust chain for the certificate. Instructions for
     creating such a file can be found e.g. here:
     https://www.digicert.com/ssl-support/pem-ssl-creation.htm

  A DCP is considered self-encrypted when the default certificate, as
  specified in the preferences, can be used to read an encrypted DCP,
  using a KeyDeliveryMessage (KDM) stored in a file named
  kdm_fl_self.xml located in the root of the DCP. The default
  configuration of the render dialog is to create such a KDM when
  creating an encrypted DCP.

  Self-signed certificates for the purposes of DCP creation can be
  created with the command-line tool fl-certgen. It takes a
  destination directory as an argument. A self-signed root
  certificate, an intermediate certificate, a leaf certificate and a
  certificate trust chain will be created in the destination
  directory. This tool is included for testing and support
  purposes. It is not expected to be necessary for normal operation.

  Decoding / Playing a DCP
  To read a DCP, open the Sequence Browser and select the desired
  CompositionPlayList (CPL) from the DCP. Due to legacy reasons, it is
  also possible to select the ASSETMAP file, which will have the same
  effect as selecting the CPL listed first in the PackingList (PKL). A
  DCP Params strip will be available, where you can specify the
  correct private key and KDM if required.

  Creating DCPs
  To create a DCP, open the Render dialog and click the DCP output
  button. The first step is then to select the DCP type. The choices
  are SMPTE + Audio (the default), SMPTE (no audio), Interop + Audio
  and Interop. Both video and audio contents will be encrypted by
  default. Which components to encrypt, and what certificate to use
  can be selected in the 'Encryption' section. The subsequent controls
  provide control over the file names and different metadata fields of
  all XML and MXF files created as part of the rendered DCP. It is
  currently only possible to create packages with a single CPL.

  It is possible to create a DCP consisting of multiple reels by
  clicking the 'Add Reel' button. When creating a DCP consisting of a
  single reel, the number of frames in the reel is determined by the
  number of frames to render. To be able to alter the number of frames
  in the first reel, you must first add a second reel. You can then
  select any reel in the list, including the first one, and change the
  number of frames it contains.

  By default, a single KDM will be created for the default
  certificate. KDMs for additional certificates can be created by
  clicking on the 'Add KDM' button. NB: If no KDM is created for any
  certificate for which you have the private key, you will not be able
  to view the result of the render!

  To create additional KDMs for an existing DCP there is a command
  line tool called dcptool. It takes as arguments a current KDM, the
  private key, a certificate chain for that private key, a recipient
  certificate and the file name of the new KDM. The plan is to provide
  an interface for additional KDM generation in a future release
  [bug 36976]

Dolby Vision
------------

* Updated Dolby Vision XML output to include details of the render
  colour space. This is selected on the file browser when using
  "Export Dolby EDR Metadata" [bug 36702]

* Added additional controls to Dolby Vision View to allow the CMU
  state to be seen and changed, and to launch the web control
  interface [bug 36718]

* Analysing a Dolby Vision strip under a Dissolve now sets the Trim
  and Advanced parameters so they animate between the values in the
  two Dolby Vision strips either side of the dissolve [bug 36698]

Miscellaneous
-------------

* The flos-tools package has been updated to version 6.4.8119. This
  includes the following fixes & enhancements:
  - netboot-chkconfig: Improve parsing of service script levels
  - fl-create-network-template: Avoid spurious error disabling
    firstboot.
  - mknetbootrd: Make image world-readable after running dracut.
  - fl-config-master: Avoid crash when no avahi-daemon.conf
  - fl-setup-database: Add support for PostgreSQL 9.5

* Updated the H.264 encoder. Rendering speed when creating H.264
  QuickTime files on Linux has improved significantly [bug 33923]

* The formats editor now allows the opacity of burnin text and borders
  to be set [bug 17432]

* Histogram View may now be floated in a window [bug 36616]

* When viewing in Stereo Anaglyph Layout, you can choose between five
  anaglyph modes using a submenu on the Display menu [bug 34383]

* When rendering in Muxed Anaglyphic, you can choose between five
  anaglyph modes [bug 34383]

* Added in Play Controls View a new speed : 1.25x [bug 28710]

* In Preferences/Display, the pencil screen switching can be turned 
  off now [bug 28830]

* Added a new kind of view, BigMetadata (available of course in the
  view menu), which allows to display metadatas in a large scale about
  the current cursor output image as timecode or keycode [Bug 19640]

* Added "Force Expand By" option to Timeline Sort View's "Handles"
  parameter. When used, this option will ensure that shots are *always*
  expanded by the amount specified, regardless of whether or not there
  is sufficient image data for those handles. This can be useful in
  pipelines where the user wishes the Baselight timeline to refer
  to image data which has yet to be generated [bug 37211]

* EDL Import is now able to load and apply CDL values from
  AAF files [bug 27763]

* Updated to RED SDK v6.2.1. This includes bug fixes and the following
  changes:
  - 8K sensor support.
  - New colour primaries option "RED Wide Gamut RGB".
  - New tone curve option "Log 3G10".
  - Minimum Rocket-X driver version is now 2.1.34.0
  - Minimum Rocket-X firmware version is now 1.4.22.18 [bug 37708]

* "Full Sensor" resolutions are now available for several ARRIRAW
  resolutions, including for ALEXA Mini. PLEASE NOTE: using the
  3424x2202 full sensor area from a 3414x2198 image may reveal
  artefacts at the sensor edges [bug 38714]

* Added support for NVIDIA Quadro K1200 UI GPU [bug 38815]

Bug Fixes Since Baselight 4.4m1.8607
====================================

* Fixed an issue reading QuickTime and MP4 movies where subsampling is
  less than 4:2:2 and bitdepth larger than 8 [bug 36531]

* When changing the Frame Rate of a Sequence, you are now offered the
  choice to maintain the Offset in seconds or in frames, as was the
  case in Baselight 4.4 [bug 36557]

* Fixed reading ActionCam files with certain colour temperature
  settings [bug 36549]

* Fixed crash when adding an image to a Burnin using the right-click
  menu [bug 36600]

* Fixed bl-reset-cache -hardssd error 'umount2: No such file or
  directory' [bug 35318]

* Fixed failures making chequer/black frames on errors, when rendering
  scenes using cached strips to some image/movie formats [bug 35306]

* Addressed a number of issues with dpm which is used in fl-diag to
  test disk performance:
  - Fixed directory generation error when run on Gen VI machines
    outside of fl-diag [bug 36128]
  - Hardened the application against scrambled output from command
    line RAID management utilities [bug 35847]
  - Provide a fail indicator ‘!’ for diagnostics with clear limits
    that can in the future be incorporated into fl-diag [bug 18448]

* Fixed scenes incorrectly remaining locked after using "bl-render
  -queue" [bug 36666]

* Stereo Colour Match is now automatically excluded from LUT export as
  its operations cannot be matched by a LUT [bug 35916]

* Fixed bug in switch diagnostic for non-contiguously numbered
  interfaces that could cause divide by zero error [bug 35534]

* Fixed error in PQ colour spaces (Dolby: ST 2084 PQ / P3 D65 and
  Rec.2084: ST 2084 PQ / Rec.2020) which could cause errors when
  resizing [bug 36773]

* Fixed crash reading some corrupt OpenEXR files [bug 36806]

* Reduced time taken to open the first scene using a Truelight
  directory with a large number of cube files [bug 36555]

* bl-render commandline now reports when it is waiting for the GPU to
  become available [bug 31808]

* Fixed crash using edit mode on single strips [bug 35581]

* Fixed performance degradation which could occur for some minutes
  after launch when connected to a Dolby Vision CM Box [bug 36823]

* Anamorphic R3D media now selects an anamorphic format where possible
  [bug 36862]

* Fixed an issue where reading ProRes media in QuickTime files with
  varying frame durations could produce incorrect results on Linux
  [bug 36851]

* Fixed bug in Timeline Sort which, when used in a single stack
  stereo scene with different frame offsets for each eye, would
  result in the non-current eye's frame offsets to be incorrectly
  overwritten [bug 36914]

* Fixed an issue that prevented certain types of RAW images from
  decoding correctly [bug 36921]

* Fixed zones diagnostic which would fail on systems with OS X 
  CONFORM nodes that are version 10.11.1 (El Capitan) [bug 36880]

* Fixed reset operator not working on the Slate [bug 36978]

* Fixed unwanted switching of a colour space to a different space with
  the same tone curve, when opening a scene which uses a colour space
  different from any already known on your system [bug 37020]

* Changed the behaviour when navigating up/down through the layers of
  a (complex) stack (using 'Page Up' & 'Page Down'). Previously, if a
  layer had more than one input (a composite layer, for example),
  navigating to the layer above would select the first layer of the
  first (foreground) input. Now the first input is ignored and the
  first layer of the last (background) input will be selected.
  Similarly, navigating down though a stack will skip foreground (and
  matte) strip inputs to a layer [bug 24500]

* Fixed failures and crashes when using OpenEXR files with a very
  large number of channels [bug 36999]

* Audio is now correctly written to QuickTime movies when using Modify
  XML workflow [bug 37139]

* Generate a warning when attempting to render a Sony MXF with an
  invalid timecode, and prevent render failure due to the drop-frame
  flag being incorrectly set [bug 37091]

* Fixed issue where the CDL grade always took control of the numeric 
  keygrade [bug 37168]

* Fixed problem with zone discovery when cloud.cfg contains a null
  mac address [bug 37165]

* Improved keyframing behaviour in OFX plugins to behave more like
  other keyframes [bug 37210]

* Fixed incorrect Canon MXF metadata when there are multiple clips in
  one directory sharing the same INDEX.MIF file [bug 37170]

* Added a diagnostic to check that SMART functionality is disabled on
  drives behind Adaptec RAID controllers because when it's enabled we
  see regular transfer latency spikes which can affect playback. Added
  a utility to disable SMART on drives behind Adaptec RAID controllers
  [bug 37254]
아답텍 레이드 컨트롤러 사용시 SMART 기능이 비활성화 되었는지 fl-diag에서 확인. 

* Errors which occur while making movies fast-start no longer cause
  renders to fail [bug 37245]

* Fix crash when exporting a BLG containing several large Truelight
  cubes [bug 36622]

* Fixed list scrolling behaviour in the application on macOS when using 
  mouse scroll-wheel or trackpad [bug 37301]

* Fixed an issue where rendering to RLE or v408 codecs in QuickTime
  containers would incorrectly stretch colours [bug 36984]

* Fixed failures with Truelight operators when submitting a render
  from Baselight CONFORM to the operations queue on a Linux system
  [bug 37330]

* Fixed bug in Despot on first/last frames when 'Use Source Handles' 
  mode set to 'None' [bug 29222]

* Added option to display Scene & Take metadata in Gallery and Cut 
  views [bug 37331]

* Fixed hangs when reading some badly-formed QuickTime files on macOS
  [bug 37366]

* Fixed errors when using R3D movies comprised of very many separate
  files [bug 35330]

* Fixed crash in CDL grade when switching between to 2 scenes and 
  editing values [bug 37053]

* Fixed render out issue with mismatched sizes [bug 37663]

* Fixed "Source data did not contain required samples" error when
  rendering or playing back audio that requires resampling
  [bug 36407]

* Fixed failure to decode 2560x2145 ARRIRAW MXF media [bug 37660]

* Fixed render operation hang when grading while rendering to ProRes
  [bug 37831]

* Fixed crash using Truelight with 1x1 interleaved stereo layout
  [bug 37531]

* Fixed bug with audio output stopping intermittently during 
  playback [bug 37105]

* Fixed incorrect pixel aspect ratio read from some QuickTime movies
  [bug 38501]

* Fixed issues with "Sony: Linear / S-Gamut3" colour space when
  installed using the Linear Colour Spaces pack from
  www.filmlight.ltd.uk [bug 37706]

* Fixed ordering on the Manage Colour Spaces panel [bug 37706]

* Fixed issues where rendering XAVC to MXF did not close partitions,
  and 1280x720 XAVC Intra and interlaced XAVC Intra formats did not
  properly write CBE indexes [bug 38174]

* Changed the location of the VBE index in XAVC LongGOP and XAVC Intra
  VBR encoded MXF files. It is now in the header instead of the footer
  of the file [bug 38524]

* Fixed crash when area tracker is applied to a zero-area shape
  [bug 38508] [bug 37495]

* Fixed bl-render on multi-GPU systems [bug 38604]

* Fixed bug which could slow performance when working with very 
  complex stacks [bug 38340]

* Fixed playback stall when using multiple cursors on multi-gpu machines
  [bug 38658]

* Fixed bug with AJA Kona 4 SDI output when switching between RGB 1.5G
  dual-link and 3G-A output configurations [bug 38519]

* Fixed crash when sorting by 'Circle Take' column in Shots view with
  a scene imported from Daylight [bug 37574]

* Fixed failure to read some malformed ARRIRAW files which presented
  as 2578x2160 resolution instead of 2880x2160 [bug 38128]

* Fixed incorrect decode of RED and ARRIRAW media on Baselight
  FOUR/EIGHT when rendering from queue [bug 38792]

* Reduced delays when playing scenes containing mixed formats of
  ARRIRAW media [bug 38797]

* Fixed "LUT data" errors reading ALEXA Mini MXF files [bug 36987]

* Fixed video memory overallocation when rendering, this could cause slow
  rendering or replay [bug 38834]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8607 (2016-09-05)

New Features Since Baselight 4.4m1.8489
=======================================

* Added support for NVIDIA 304.131 driver to fix image corruption
  on legacy systems (GTX 8800 to GTX 580) [bug 37134]

* Added support for NVIDIA 367.44 driver for GTX 1080 and Titan X
  Pascal GPUs [bug 37267]

* Added support for NVIDIA Titan X (Pascal) GPU [bug 37992]

Bug Fixes Since Baselight 4.4m1.8489
====================================

* Fixed bug which could cause FilmGrade bump buttons to stop
  responding after using bump buttons with Ctrl (half bump)
  modifier [bug 37253]

* Fixed memory handling to avoid Baselight crashing with message
  "Warning: System has run too low on memory resources and must exit"
  [bug 23036]

* Fixed crash using Switch Dust on a BLX [bug 37686]

* Fixed over-allocation of GPU memory, causing playback slow downs
  after extended use of the Baselight application [bug 37255]

* Fixed crash when rendering to audio-only on a Baselight FOUR/EIGHT
  [bug 37926]

* Fixed problem with tearing on AJA SDI output when using 4K display
  resolution [bug 37915]

* Fixed bug which could cause FilmGrade bump buttons to stop
  responding after using bump buttons with Ctrl (half bump)
  modifier [bug 37253]

* Fixed black render from R3D media on Mac using non-linear decode
  options [bug 38157]

* Fixed playback when using dual combiner display modes [bug 37567]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8489 (2016-07-22)

New Features Since Baselight 4.4m1.8289
=======================================

File Formats
------------

* Added support for reading ARRIRAW MXF files as written by the Alexa
  Mini camera [bug 34960]

* Added support for writing XAVC Intra and LongGOP to MXF. The
  following operating points are supported:

  1280x720:
  - XAVC HD Intra Class100 @ 50p, 59.94p
  - XAVC HD Long422 50     @ 50p, 59.94p

  1920x1080:
  - XAVC HD Intra Class100 @ 50i, 59.94i, 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC HD Long422 25     @ 50i, 59.94i, 23.98p, 25p, 29.97p
  - XAVC HD Long422 35     @ 50i, 59.94i, 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC HD Long422 50     @ 50i, 59.94i, 23.98p, 25p, 29.97p, 50p, 59.94p

  2048x1080:
  - XAVC 2K Intra Class100 CBG @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p
  - XAVC 2K Intra Class100 VBR @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p

  3840x2160:
  - XAVC QFHD Intra Class300 CBG @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Intra Class300 VBR @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Intra Class480 CBG @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Intra Class480 VBR @ 23.98p, 25p, 29.97p, 50p, 59.94p
  - XAVC QFHD Long 60            @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long 100           @ 23.98p, 25p, 29.97p
  - XAVC QFHD Long 150           @ 50p, 59.94p

  4096x2160:
  - XAVC 4K Intra Class300 CBG @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p
  - XAVC 4K Intra Class300 VBR @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p
  - XAVC 4K Intra Class480 CBG @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p
  - XAVC 4K Intra Class480 VBR @ 23.98p, 24p, 25p, 29.97p, 50p, 59.94p

  Rec.709, Rec.2020 and S-Log colour spaces are tagged in the file
  metadata [bug 28628]

Miscellaneous
-------------

* ARRIRAW files are now decoded using the ARRI SDK, to maximise
  compatibility with other software tools including Daylight. (This
  only applies to newly-added Sequences; existing scenes continue to
  behave as they did before.)

  On a system using GPUs with 3GB or more VRAM, ARRIRAW media up to 5K
  in width is decoded using the GPU. On a system using GPUs with 4GB
  or more VRAM, ARRIRAW media 5K or wider (e.g. ALEXA 65) is decoded
  using the GPU.

  On Linux, the GPU cannot be used for ARRIRAW decoding if the NVIDIA
  driver is older than version 340. See the About Baselight dialog for
  information [bug 33118]

* Updated to RED SDK v6.1.0. This includes three new HDR Output Tone
  Curve options: HDR-2084, Rec.1886 and Log 3G12 [bug 35054]

* R3D media can be decoded using the GPU only if the GPU has 3GB or
  more VRAM. See the About Baselight dialog [bug 37071]

* When reading XAVC Intra tagged with Rec.709 or Rec.2020, the colour
  space is assumed to be full range rather than video legal, as
  recommended by Sony [bug 28628]

* The Manage Colour Spaces dialog now allows more fine-grained choices
  of which colour spaces to hide in which menus - e.g. a colour space
  may be hidden from the Working Colour Space menu but still visible
  in the Render Colour Space menu [bug 35147]

* fl-config-master has error message improvements for Baselight
  CONFORM [bug 19086]

* fl-config-master has been updated to deprecate network-layout 1 
  [bug 34452]

* Updated fl-setup-raid / fl-setup-pfs for BLX, they both now support
  '-force' when checking tgtd [bug 35162]

* fl-setup-database has been updated to increase the database server
  memory setting, for improved performance [bug 12676]

* fl-host produces an appropriate error when there is no cloud.cfg
  file [bug 35039]

* fl-setup-adaptec no longer hangs on some systems at script end 
  [bug 34301]

* Added support for sending crash logs to baselight when unexpected
  failures occur, and for trimming log directories to size [bug 36517]

* Improved EDL Import and Export of AAF EDLs to support Baselight for
  Avid effect payloads larger than 64kb (the limit is now 1.2MB) when
  working with 4.4m1 Version Compatability. This means that the "The
  grade data was too large to fit inside an AAF event" error produced
  by "Update Avid AAF with Baselight Grades" is now much, much less
  likely to occur [bug 35138]

* Updated to AJA SDK 12.3 and updated AJA Kona 4 firmware [bug 35288]

* Added support for 3G-SDI Level A RGB output via AJA Kona 4 [bug 31835]

* Added support for independent 4K to HD downscaling on SDI and HDMI
  outputs of AJA Kona 4. There are now separate HDMI and SDI
  Downscaling options that are available in the Setups editor when the
  master resolution is 3840x2160 or 4096x2160 [bug 35289]

Bug Fixes Since Baselight 4.4m1.8289
====================================

* Addressed R3D GPU decoding errors, including errors at application
  startup and CL_OUT_OF_HOST_MEMORY failures [bug 35489]

* Fixed reading audio from split-file MXF media [bug 34903]

* Fixed reading audio from some MXF files [bug 30294]

* Improved Baselight decode of ARRIRAW media so the levels more
  closely match the ARRI decode. Note that this only affects
  newly-added Sequences to prevent changes to existing scenes; to
  update existing scenes use the Update button on the Sequence
  parameters [bug 35043]

* Fixed crash when pasting a tracker strip having a two point tracks
  with no tracker linked to it [bug 35046]

* Updated the default Setup behaviour so that new scenes are created
  using the ARRI Photometric v2 DRT. This replaces the legacy ACES RRT
  0.7 which was previously used [bug 35086]

* Errors are no longer generated if there are AppleDouble files in the
  colourspace directories (e.g. ._foo.flspace) [bug 35053]

* Diagnostics no longer reject hostnames that are the same as the
  system zone name. This helps integration with certain 3rd-party
  SANs [bug 31174]

* Fixed problem with copy protect categories on the input strip
  preventing the strip directly underneath from being pasted to the
  destination [bug 35174]

* Fixed CDL grades not appearing in the bl-shots -ascsop and -ascsat
  options [bug 35204]

* Colour Space Journey View no longer displays entries for bypassed
  strips [bug 34977]

* Fixed temperature query tool 'sdi-info -temp' bug [34978]

* Fixed Input Colour Space shown on Sequence Parameters when a BLG is
  inserted onto the timeline [bug 35220]

* The Reference strip no longer converts its input to the Working
  Colour Space and Working Format. Note that since this can affect
  grading behaviour, this change only applies to newly-added Reference
  strips; old scenes retain their old behaviour [bug 35206]

* Truelight resources used by operators inside layers with mattes are
  now correctly included in exported BLG files [bug 35240]

* The Job Manager "Move Scene Into Folder" command now prevents moving
  a scene into a folder which already has a scene of the same name
  [bug 35278]

* Internal /media/_mnt_slot* volumes are now hidden from cloud media
  [bug 35300]

* Fixed crashes reading some 16-bit RGBA TIFF files [bug 35357]

* Bypassed Dolby Vision strips are no longer exported with EDR XML
  [bug 35356]

* Fixed order of gestural grading gang controls [bug 35352]

* Fixed export format of .cc files [bug 34345]

* Prevented Consolidate overlapping-sequences warning dialog from
  getting too large [bug 35227]

* Fix playback and render errors when Audio Sequence operator
  has a negative offset [bug 35375]

* Fixed an issue with the bitrate selection dialog when rendering DCI
  compliant JPEG 2000 files, where the dialog did not update to
  reflect the selected bitrate [bug 34844]

* The sequence operator now correctly displays a selection dialog for
  handling frame duration when reading a movie file with uneven frame
  duration [bug 32262]

* Bundle a newer version of xfs_repair (4.3.0) [bug 35186]

* Fixed bug in the Gallery which could occur when grabbing RAW media
  (eg R3D, ARRIRAW etc) when multiple debayer parameter operators were
  in the stack. When the original media disappeared, the grabbed frame
  could have been generated using the incorrect debayer parameters
  [bug 35511]

* Updated pivot point in CDL grade to match FG. Also fixed the maximum
  slope value [bug 35464]

* Select Missing Material now reports that it cannot check material
  which is on remote cloud media [bug 35523]

* Fixed decode of ARRIRAW Alexa Plus anamorphic (2578x2160 or
  2592x2160) media using ARRI decode mode [bug 33915]

* Negative button in Video Grade now works as expected [bug 17462]

* A failover routine has been added when encountering missing
  reference frames in XDCAM MXF-files. This will allow reading valid
  XDCAM essence from MXF-files with invalid indexes [bug 35633]

* Added support for a number of QuickTime codec tags, including 'aivx'
  for XAVC [bug 35615]

* Fixed failure to read some QuickTime files with badly-formatted
  metadata [bug 35761]

* Fixed a possible issue reading frame metadata from CFHD encoded
  QuickTime files with frame rates of 100 fps or higher [bug 35934]

* Fixed an issue where incorrect frames could be returned from
  temporally compressed QuickTime and MP4 files [bug 35933]

* Fixed a flfsd (pfs2 daemon) assertion error caused by a udp mount
  affecting the maximum tcp transfer size [bug 35902]

* Fixed issue where some changes made in Manage Colour Spaces would
  not be remembered [bug 35987]

* Certain preference files on Mac no longer include the hostname in
  the filename, to prevent these files changing when the hostname
  changes (i.e. when changing between networks) [bug 36023]

* Fixed hang when a scaled shape has fewer than three distinct points
  [bug 35135]

* Fixed Transform operator's "Show Grid" option [bug 36159]

* Fixed bug that prevented Scene and Take metadata being read from
  audio files when they are synced with an image sequence (via Audio
  Sync, or manually via the Sequence Browser) [bug 35689]

* Fixed an issue that prevented 60 fps timecode to be written to files
  of type Sony MXF [bug 36092]

* Fixed handling of negative audio offsets in QuickTime movies. Audio
  tracks that start after the video will now synchronise correctly.
  This fix includes a change to fix how negative integer values are
  handled in QuickTime headers [bug 36205]

* Added support for DNxHD essence stored in Op1A and Op1B MXF
  containers written by Resolve [bug 36184]

* Fix detected size and bit depth of MXF files encoded with AVC-Intra
  4:4:4 containing RGB data [bug 36260]

* Rearranged the CDL bumps and added Exposure and Constant overall
  bumps [bug 32239]

* Fixed Slate key pressing not registering long holds, especially
  "View" and "Try" [bug 28094]

* Fixed an issue where full range 4:2:0 data in MP4 and QuickTime
  containers was squashed to legal range on read [bug 36285]

* Fixed reading of open-GOP material in QuickTime and MP4 containers.
  The problem could prevent e.g. XDCAM in MP4 containers from being
  decoded [bug 34258]

* Fixed reading compressed multi-view OpenEXR files [bug 36480]

* Fixed missing metadata from movies when accessed from Text operator
  or Burnin [bug 36486]

* Fixed selection being cleared after apply [bug 25917]

* Fixed reading of some MXF files with CBR indexes split over multiple
  partition indexes [bug 36452]

* Fixed a data race which could cause renders to fail with an 'unknown
  movie' error [bug 36426]

* Fixed a problem seen when copying a section from a long play strip
  and pasting into the timeline [bug 26573]

* Changed USB handling that caused the Slate to use a lot of CPU
  [bug 35563]

* Fixed crash on Multi-GPU machines when quickly stepping between cuts
  [bug 36590]

* The "Channel" selector on the Sequence Browser no longer offers
  Alpha for some images where there is no accessible alpha channel
  [bug 36645]

* Updated Adaptec controller firmware installer to version 7-9.0. This
  firmware fixes a machine crash seen occasionally when running the
  arcconf utility [bug 35244]

* Fixed problem where multiple pivot point edit lines got added to the
  Film grade page of the CDL grade operator [bug 33400]

* Fixed crash when there was no selection and the blackboard paste key
  was pressed [bug 33947]

* Fixed interlaced image display via Kona 4 when viewing still frame
  [bug 34929]

* Fixed playback of audio via Kona 4 when scrubbing [bug 32983]

* Fixed incorrect image on Kona 4 HDMI output when using 4K to HD
  downscaling [bug 31351]

* Fixed crash using 1D LUTs [bug 36608]

* Fixed crash at startup when using DVI/HDMI/DP output on systems
  without an AJA Kona SDI card, caused by attempts to route audio
  playback via the AJA SDI card [bug 35958]

* Fixed a problem that could cause a vertical line to appear on 
  images at different resolutions [bug 36598]

* Resolution directories are no longer considered when choosing
  possible formats for ARRIRAW sequences [bug 37200]

* Fixed a pfs2 assertion error during stale handle recovery [bug 37242]

* Baselight will no longer attempt to use DVS Atomix cards for display
  output [bug 37262]

* Fixed quality issues with scopes [bug 36694]

* Updated ARRIRAW metadata "Clip" and "Camera" to match Daylight.
  Added ShutterAngle and Recorder metadata [bug 37467]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8289 (2016-05-17)

Bug Fixes Since Baselight 4.4m1.8209
====================================

* Fixed reading compressed multi-view OpenEXR files [bug 36480]

* Improved crash reporting on Multi-GPU machines [bug 36589]

* Fixed crash on Multi-GPU machines when quickly stepping between cuts
  [bug 36590]

* Fixed memory leak on Kona based systems [bug 36664]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8209 (2016-04-14)

Bug Fixes Since Baselight 4.4m1.8174
====================================

* Fix a bug in matte display and picking [bug 36359]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8174 (2016-04-07)

New Features Since Baselight 4.4m1.8085
=======================================

Baselight CONFORM
-----------------

* Added the new Baselight CONFORM product on Mac OS X. This runs on
  any Mac system with OS X 10.9 or later.

  It supports all Baselight functionality except
  - Rendering (though it can submit renders to the Operations Queue on
    a full Baselight system)
  - SDI output via an AJA device
  - Control surfaces (Slate, Tangent, etc)

  The Baselight PORTABLE product is no longer available.
베이스라이트 포터블 제품은 더 이상 가능하지 않습니다.

GPU Acceleration
----------------

* Improved utilisation of multiple render GPUs in Generation VI
  Baselight TWO and Baselight X systems, which can significantly
  accelerate caching, playback and rendering operations [bug 35237]

File Formats 파일 포맷 
------------

* DNG files with post-demosaic operations (e.g. warp corrections) are
  now read, but the corrections are not rendered [bug 34369]

* Added new cube formats for Amira and BMD with extended range.
  The IRIDAS cube worked for Amira, once they fixed their reader
  but this makes the Amira user's choice easier [bug 31767]

* Added support for reading split-file Canon EOS C300 media, and
  improved metadata reading from these files [bug 34933]

* Added support for 12-bit encoding in the DNxHR HQX codec [bug 34868]

* Added support for reading multi-part OpenEXR files (except where the
  display window is not the same for all parts) [bug 34972]

* Added support for reading multi-view OpenEXR files. This includes
  automatically selecting left/right views in stereo scenes for both
  the image and any referenced matte channels [bug 35059]

Miscellaneous
-------------

* The Rotation parameter of Transform operators is now adjustable in
  hundredths of a degree [bug 34384]

* When a scene is opened and a format which it used has been edited or
  deleted, a Scene Format is created to maintain the previous
  behaviour of the scene. A dialog box is now presented when a scene
  is opened to explain this [bug 34467]

* Updated LUT export with Extended Ranges support for HDR input.
  Truelight cubes and the newly added Autodesk CTF format support an
  extra input LUT for mapping high dynamic range inputs. There is now
  an option to include this in the LUT export dialog [bug 33499]

* LUT export also now includes an option to override the input colour
  space, replacing the one used for a sequence with one specified for
  the LUT export. This allows LUTs to be generated for use in other
  applications using images that have been converted to a different
  colour space [bug 33157]

* Added option to sort jobs by size (note that this feature is not
  available when browsing jobs on FLOS 2.1 systems) [bug 5208]

* LUT export has been extended to include options for the Input
  Display Rendering Transform when the Input Colour Space is set to
  anything other than the Sequence Input Colour Space. Previously the
  Input DRT was not handled in the LUT export [bug 35118]

Bug Fixes Since Baselight 4.4m1.8085
====================================

* Fixed LUT export which was failing for Shots with Hue Angle and
  Matte Tool Blur [bug 34225]

* Improved accuracy of warning counter on EDL Import View [bug 34284]

* Sequences on cloud media are no longer reported as missing when
  using Verify on a render [bug 32311]

* Fixed alpha channels in thumbnails of ProRes 4444 media [bug 34334]

* Fixed keyboard accelerator for changing Edit Type on Mac [bug 34336]

* Fixed error with zero handling in "Dolby: ST 2084 PQ / P3 D65"
  colour space [bug 34382]

* Fixed intermittent crash related to periodic events in the user
  interface [bug 34305]

* MJPEG encoded material in MXF files is no longer stretched from
  legal to full on read [bug 34402]

* Fixed screen switching by double tapping the UI/Image button on
  systems with both multiple monitors and a Blackboard 1 [bug 32511]

* Updated the ACES Scene Template to use ACES Cineon Log / AP0 as a
  working colour space, due to issues with ACEScc [bug 34051]

* Fixed bug setting up floating-point cubes that take negative values.
  This gave visible pixels in regions that should be fully dark. Such
  cubes are not used outside development work, so we do not expect
  current Baselight jobs to be affected [bug 34465]

* Fixed Group Grading of several operator parameters [bug 34407]

* Fixed issues with Cloud Media connected to the node of a Baselight
  TWO system [bug 34297]

* A missing source file will no longer case a Consolidate operation to
  abort [bug 34240]

* Adaptec web interface no longer requires an SSL connection because
  many browsers refuse its self-signed certificate [bug 31422]

* BLG export using unavailable filename templates (e.g. %P when the
  shot has no clip name) now correctly report the error [bug 30551]

* Fixed an issue that prevented interop DCPs being rendered via
  command line [bug 31693]

* Rendering a DCP now finishes with 'Wrote DCP package', to better
  indicate the completed status of the render job [bug 31967]

* Fixed an issue that could cause frames to be repeated in MP4 movies
  with frame rates of 100 fps or higher [bug 34594]

* Fixed excessive file searching when opening some R3D movie files
  [bug 34690]

* Adjusted calculation of max frame size in JPEG 2000 compressed MXF
  files to avoid introducing minor bitrate overshoots when creating
  DCPs in e.g. Clipster [bug 31622]

* Fixed LUT export for a LUT transforming from a Log Colour Space to a
  Linear Colour Space, which previously clamped output values to 1.0
  [bug 34423]

* Fixed LUT export for shots with pixel aspect ratio other than 1.0
  [bug 34611]

* Fixed some console warnings about undefined parameters when
  rendering H264 to MP4 or Quicktime containers [bug 34825]

* Deleting a format which overrides another format no longer removes
  some mappings to the remaining format [bug 34920]

* Fixed crash when activating a licence from a downloaded file
  [bug 33708]

* Improve licensing dialog and activation process [bug 33418]

* Improvements to Licence window layout [bug 34464]

* Updated to latest version of fl-setup-vol, which removes support for
  Avid Unity filesystems (superceded by Avid ISIS) [bug 34599]

* Improved error message when trying to open an encrypted DCP or MXF
  [bug 34979]

* Fixed 100% quality JPEG output [bug 35034]

* Fixed deselect on paste still clearing the selection when it was 
  turned off [bug 25917]

* Reduced risk of GPU memory errors when working with large RED media
  (e.g. 8K WEAPON) [bug 35041]

* Updated preview features licence support [bug 34539]

* Fixed a memory allocation issue which could cause subtitles not to
  appear in DCP output [bug 35012]

* Avoid running overnight disk defragmentation process twice on 
  Baselight TWO systems [bug 34925]

* Fixed temperature query tool 'sdi-info -temp' bug [34978]

* Fixed an issue where the Blackboard 'Undo' functionality was no
  longer available after a Tracker modification using any Blackboard
  trackball or ring [bug 35192]

* Fixed a problem with Optical Flow retime, where Baselight FOUR and
  EIGHT systems would render incorrectly [bug 35091]

* Fix application hang caused by Audio Waveform view [bug 35512]

* Improved serial number and licence file validation support
  [bug 35363]

* Fix behaviour of "Reset All To Camera Metadata" on R3D Params
  operator [bug 35516]

* Update licensing to allow appropriate licenses to be installed
  [bug 35896]

* Fixed an issue that caused blocky artefacts and green frames when
  decoding XDCAM [bug 36016]

--------------------------------------------------------------------------

Baselight Release 4.4m1.8085 (2016-02-26)

New Features Since Baselight 4.4m1.7936
=======================================

* Added support for NVIDIA driver 352.63 on systems with GTX 580,
  GTX 680, GTX 780 and GTX 980.

  This driver is compatible with systems systems AJA Kona 4 or direct
  GPU display.

  This driver is NOT compatible with systems using FilmLight DVI2SDI
  or Framestore SDI display hardware [bug 33008]

* Added support for NVIDIA driver 340.96 on systems with GTX 680 and
  GTX 780 GPUs and DVI2SDI or Framestore SDI display hardware
  [bug 35367]

  Note:
    When you install and run this version of Baselight, fl-diag may
    prompt you to upgrade your Nvidia driver. If this is the case, you
    must update your driver as the latest Baselight release contains
    software that has specific driver dependancies.

  Important:
    If you decide to roll back to a previous version of Baselight
    after you have upgraded your Nvidia driver, you will need to roll
    back the Nvidia driver as well. Contact Baselight Support to
    provide you with a custom driver installer for this purpose.

    To upgrade, see the support section of our website for the correct
    installer. This contains multiple versions of the driver that
    cover all supported Baselight hardware configurations, and will
    detect and install the correct version for your system.

Bug Fixes Since Baselight 4.4m1.7936
====================================

* Improved cursor lag on image display when using AJA SDI output
  hardware [bug 34357]

* In BLG Export and when updating AAFs for Avid, Sharpen operators
  created in 4.4m1 can now be converted into a form which can be read
  by Baselight 4.4 (plugins and full Baselight). The only caveat is
  that the "Anamorphic" setting is not supported in 4.4 and so if it
  is used in a 4.4m1 stack, that stack will not be exported
  [bug 35203]

* Fixed issues with Dolby Vision Mastering Display [bug 35268]

* Added aspect ratio information to Dolby EDR Metadata [bug 32794]

* Fixed an issue that could cause decode failures, frame offsets and
  incorrect frame ordering in MXF files with start-position offsets.
  This issue affected XDCAM encoded MXF-files in particular
  [bug 33591]

* Fixed a problem with Optical Flow retime, where Baselight FOUR and
  EIGHT systems would render incorrectly [bug 35324]

* Fixed decode of ARRIRAW Open Gate (3414x2198 or 3424x2202) media
  using ARRI decode mode [bug 34605]

* Fix new files being reported as zero size over /pfs (flood)
  interface when they were written using flux [bug 28121]

* Don't attempt to stop Adaptec raid verification at Baselight startup
  because it may cause a kernel panic [bug 35345]

* Fixed bug with fl-service xorg service running on IO node of cluster
  systems [bug 35409]

* Fixed hang rendering R3D material [bug 35426]

* Fixed render hang on BL4/BL8 [bug 35453]

* Fixed playback errors at startup on clusters [bug 35480]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7936 (2015-12-22)

New Features Since Baselight 4.4m1.7767
=======================================

* Added support for Display Rendering Transforms which use
  tetrahedrally-interpolated cubes [bug 34042]

* Added "Next/Previous Ungraded Shot" actions to Navigate menu and
  Chalk for Blackboard 2/Slate [bug 34083]

* Enabled RGBCMY encoder mode in the Curve Grade operator on a Slate
  (from the RGBY controls page). This maps the right 6 encoders and
  their buttons to red, green, blue, cyan, magenta & yellow
  respectively [bug 34078]

* Added JPEG render quality option [bug 34086]

* Added option to set the Display Window in OpenEXR files using the
  Mask specified in the Render View [bug 34122]

* The entire image contained in the Data Window of OpenEXR files can
  now be accessed by choosing an Input Format which is the same
  resolution as the data window. Note that this functionality is only
  available when the data window is larger than the display window,
  and entirely contains the display window [bug 29766]

* The Timeline View can now be panned and zoomed without using the
  middle mouse button in the same way as the Display View, using
  Alt+Click or Ctrl+Alt+Click (Option+Click or Command+Option+Click on
  Mac) [bug 24511]

* Dissolve now clamps its input images to [0,1] by default, to prevent
  negative or >1 pixel values entering the dissolve [bug 34116]

* Audio can now be read from cloud media [bug 32259]

* Added performance logging to disk i/o subsystem and GPU renderer
  [bug 34405] [bug 34526]

* Added support for BLX 4 x Adaptec RAID configuration [bug 34154]

Gallery
-------

* The Gallery View's right-click context menu now includes options
  to use the viewing format (and masks), viewing colour space or
  Truelight settings of the current cursor when rendering thumbnails
  or when scrubbing. This makes comparison of shots authored with
  different formats or viewing colour spaces much more convenient
  [bug 21955]

* If a normal scene is explicitly loaded into a gallery, then any
  default cursor settings stored via the cog menu of the Cursor
  View are respected. For example if you set a viewing colour space
  different to the working colour space and save that as the default
  for the scene, it will look the same when loaded into a gallery
  [bug 34291]

Miscellaneous
-------------

* Added a preference for the default behaviour of Matte Merge strips
  [bug 29568]

Bug Fixes Since Baselight 4.4m1.7767
====================================

* Cubes for DRTs which are shipped with 4.4m1 are no longer included in
  BLG files exported with "Version Compatibility: v4.4m1" [bug 34024]

* Fixed encoding of keycode when rendering to Avid MXF Op-Atom to
  allow 35mm 3perf keycode to be interpreted correctly in Avid
  MediaComposer [bug 34031]

* Fixed problem with Apply and paste protection causing overlapping
  strips. this occured when the source stack was part of the
  destination selection [bug 34047]

* Added checks to ensure disk cache size is not automatically 
  increased beyond the free space available on the disk [bug 23199]

* Fixed an issue that caused the image to freeze when working with
  XDCAM [bug 33529]

* Improved Fast-Start QuickTime compatibility with PIX [bug 33639]

* When formats are chosen in the Sequence Browser, scene formats and
  job formats are now chosen ahead of global formats [bug 32529]

* Fixed crash pressing UI3 button on a 2-UI-monitor system [bug 34057]

* Fixed bug which prevented image to UI monitor switching from working
  at 4K resolution when screen switching pref set to "Image Left"
  [bug 34062]

* Cursor settings saved into a scene from Cursor View are now retained
  when that scene is used as a Scene Template [bug 32222]

* bl-mkscene now retains all scene settings when using a Scene
  Template [bug 32222]

* Fixed select/delete of Layers 21-24 added using Chalk [bug 34068]

* Fixed keycode metadata from movie files shown in Sequence Browser
  [bug 34081]

* Replaced use of the term "Inside/Outside" with "Layer" when
  referring to Layer strips [bug 34096]

* Fixed orientation of flipped/flopped ARRIRAW sequences [bug 33960]

* Fixed numeric precision issues in some automatic mappings which
  could lead to unnecessary image resampling [bug 34124]

* Fixed Prepare For Review when preparing more than one scene at once
  [bug 27510]

* Fixed failures in bl-proxygen [bug 34150]

* Fixed bug which could cause a crash when picking in the Hue Angle
  keyer with "Display And Timeline Cache" scene setting set to
  floating-point [bug 34101]

* Fixed crash with DisplayPort/DVI/HDMI output on Baselight TWO
  systems with multiple GPUs [bug 34168]

* Fixed crash when configuration the resolution of an external monitor
  when using DisplayPort/DVI/HDMI output [bug 34167]

* Fixed ordering of GPUs in multi-GPU Baselight systems [bug 34166]

* Fixed inability to Multi-Paste from Daylight scenes [bug 34151]

* Fixed bug that required the application to be restarted before newly
  saved layer configs were applied [bug 34161]

* Fixed bl-applyblg tool [bug 34177]

* Fixed problem with Replace with Protect Mattes removing the
  destination stacks' mattes [bug 29039]

* Improved fl-diag DPM (Disk Performance Monitoring) latency and
  throughput reporting for Adaptec RAID controllers [bug 33641]

* Fixed duplicated entries in Colour Space Journey View when Sequence
  Resampling is Optical Flow or Mix Nearest Frames [bug 34201]

* Fixed issue using DisplayPort/DVI/HDMI output on Baselight ONE
  systems [bug 34168]

* Fixed audio glitch when adding marks during playback [bug 34195]

* Resources for overridden DRTs used by Sequence operators are now
  stored in exported BLG files [bug 31881]

* Fixed failure to import some FCP XML EDLs [bug 33730]

* Increased the amount of memory dedicated to thumbnails on Baselight
  systems with a UI host to 20% of available RAM. This allows more
  thumbnails to be kept in memory, reducing thumbnail re-rendering
  when scrolling [bug 34183]

* Fixed crash starting image output on FLOS 2.1 Baselight ONE 
  systems [bug 34168]

* Fixed bug where the "sRGB Display (Ignore Truelight & Viewing
  Colour Space)" (now renamed to ""Use sRGB for Thumbnails") would
  have no effect in some galleries [bug 33145]

* Fixed bug where normal scenes loaded into galleries wouldn't
  sometimes wouldn't scrub using the current viewing colour
  space [bug 29231]

* Fixed bug where the current cursor's mask and guide mask settings
  sometimes weren't being applied when scrubbing in a gallery.
  Now, as long as the user elects to turn on the "Viewing Format
  and Masks" options in the Gallery's right-click context menu,
  any current mask or guide mask should always be applied when
  scrubbing. [bug 34117]

* Fixed bug which could occur when a mask, burnin and a Truelight
  profile were switched on in the current cursor and the user
  scrubbed in a gallery thumbnail which was grabbed with a
  different viewing format which didn't contain a mask of the
  same name [bug 23458]

* Fixed crash when grabbing a movie to the gallery if the user the
  Baselight UI was running as didn't have permission to read the
  movie [bug 26004]

* Fixed bug which cause shape overlays to not match the rendered shape
  image when adding/modifying keyframes [bug 34376]

* Fixed crash when tracking with timeline cache set to 16-bit
  Floating-Point RGB [bug 31320]

* Fixed a crash in Cuts View drag and drop, when attempting to drag
  an incomplete stack [bug 34480]

* Improved playback performance on systems displaying via a Kona card
  [bug 34489]

* Fixed bug where gallery grabs from scenes with non-default
  containers would sometimes be "offline" after Baselight was
  restarted [bug 21976]

* Fixed issue where gallery thumbnails would change slightly when
  switching between cursors of different frame rates [bug 34553]

* Fixed occasional out-of-memory errors when rendering [bug 34226]

* Improved 'disk read limited' playback on Generation V hardware
  caused by i/o buffer contention [bug 34629]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7767 (2015-11-02)

New Features Since Baselight 4.4m1.7687
=======================================

* Added support for reading CinemaDNG files with lossy compression
  (e.g. from Blackmagic URSA) [bug 33130]

* Added support for reading and writing 4:2:2 and 4:4:4 Y'CbCr DPX
  files, at 8-, 10- and 16-bit depths [bug 33775]

* It is now possible to render to QuickTime movies using Apple ProRes
  codecs of any width [bug 30699]

* Added a View Luma option to the Cursors menu and the Cursor View
  "View Channel" control [bug 33815]

* Added filename templates to CDL ccc file export [bug 33841]

* Added "Expo Demo" for Blackboard 2 and Slate desks. Activate with
  "-deskdemo" command line parameter, or adding "Expo Demo" Action in
  Chalk. Note: Cannot be exited when launched from command line,
  otherwise press & hold any desk button to exit

* The Gallery View now stores an EXR still frame when a movie file 
  is grabbed to the gallery. This means that if the original media
  is no longer available, the gallery will continue to show a
  thumbnail, which can be scrubbed to show a full-resolution image.
  [bug 26004]

* Added new "Rec.2084: ST 2084 PQ / Rec.2020" colour space. This
  colour space can be used for grading on HDR monitors. Please be
  aware that all standard DRTs will compress the image so they cannot
  be used with this colour space. Please contact Baselight Support if
  you want to do film-style grading for HDR displays [bug 33925]

* Updated to RED SDK v6.0.4. This includes bug fixes and: 
  - Weapon 8K and Raven 4K support
  - Support for Mysterium-X Monochrome decoding on RED Rocket
  - Rec.2020 colourspace support
  - Minimum required Rocket-X driver is 2.1.24.0 with firmware
    1.3.19.40
  - Minimum required Rocket driver is 2.1.23.0 with firmware 1.1.18.0
  [bug 33479]

  PLEASE NOTE: the RED SDK does not support GPU decoding on
  FilmLightOS 2.1. If your system is running FilmLightOS 2.1 you will
  need to upgrade it to FilmLightOS 6.4 to be able to read R3D media
  using GPU acceleration.

* Added Inside/Outside button to Chalk for Blackboard 2 (in Button
  Categories: Stack Manager) [bug 34095]

Bug Fixes Since Baselight 4.4m1.7687
====================================

* New splinePoints{5} default for Looks [bug 33111]. This can be
  overridden by adding a splinePoints{..} argument in the Look profile.
  The Look was used well beyond the range of the data points so there
  is no complete fix, but this helps

* Fixed bug where bypassing a layer would give an incorrect result
  when 'Inside Source' dropdown was set to anything other than
  'Layer Input' [bug 33783]

* Improved the error message shown when QuickTime write fails e.g. due
  to no space left on device [bug 33761]

* Versioned Denoise to allow old scenes to be openened [bug 33521]

* Fixed reading of some badly-formatted QuickTime movies written by
  ARRI cameras [bug 33818]

* Fixed incorrect display of Matte Merge strip icons on Blackboard
  and Slate desks [Bug 33826]

* Fixed an issue where QuickTime files with broken edit lists were
  handled differently on Linux and Mac [bug 33821]

* Fixed bug where having a viewing format different from the working 
  format would cause trackers and keyers to fail [bug 33820]

* Rendering to Apple ProRes using Video LUT: Clip to Legal or Video
  LUT: Soft Clip to Legal now infers that the images are legal-range
  and scales them correctly [bug 33842]

* Fix bl-config-video on systems with NVIDIA GTX 285 GPU [bug 33877]

* Reverted changes to audio TC tracks for MXFs, as this broke Relink &
  ALE merge in Avid Media Composer. Audio tracks in MXFs rendered from
  Baselight & Daylight will now have the same timecode as the video
  track. Sound TC must be merged into the bin using ALE [bug 33319]

* Fixed bug that prevented rendering to MXF when the source material
  included keycode [bug 34028]

* Fast Start QuickTime movies are no longer written with compressed
  header atoms, since this can cause issues in other software packages
  [bug 33639]

* Fixed incorrect subtitle font kerning [bug 33888]

* Fixed bug where grabbing to the gallery via drag-and-drop from the
  Cut View in "Display sRGB" mode would produce thumbails which would
  use an sRGB colour space when scrubbing. [bug 33903]

* Fixed an issue where the timecode atom in some QuickTime files could
  cause the file to take a long time to open on Linux [bug 33909]

* Fixed minor issues in the "Dolby: ST 2084 PQ / P3 D65" colour space
  [bug 33925]

* Fixed problem with keyer picking when a viewing colourspace 
  conversion was applied [bug 33931]

* Selected strips with differing names can now be renamed together
  from the "Name" field at the top of Parameters View if Grouped
  Grading is enabled [bug 22863]

* Fixed crash where trackers would crash on clusters [bug 33932]

* Reduced benign error message output with hotfix script on netbooted
  hosts [bug 33936]

* Fixed copy failues in Flux to and from Kompressor volumes 
  [bug 33819]

* Fixed decode of DVCPROHD in QuickTime files on Linux [bug 31596]

* Fixed an issue that caused frames to repeat in some long QuickTime
  and AVI files on Linux [bug 33990]

* Fixed consolidate errors with Canon MXF files [bug 34029]

* Fixed issues with 3.4k ARRIRAW files using ARRI Decode [bug 34016]

* Fixed failure in AAF export that produced 'Could not lookup component' 
  error message [bug 30825]

* Fixed an issue that caused the image to freeze when working with
  XDCAM [bug 33529]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7687 (2015-09-23)

New Features Since Baselight 4.4m1.7567
=======================================

* Sharpen plug-in has new added Anamorphic control. This goes from 0.0
  (vertical sharpening) to 2.0 (horizontal sharpening). The default
  1.0 setting is the same as before [bug 32229]

* Added support for reading newer Avid MXF files using ProRes codecs
  [bug 32333]

* A new "Manage Colour Spaces" dialog can be opened from the Baselight
  menu or from the Formats editor (in Baselight or in bl-formats).
  This allows colour spaces to be set as hidden, which will hide them
  from all colour space menus unless Shift is pressed. The list of
  hidden colour spaces is stored in the global preference database
  [bug 32641]

* Added Slate support to Retimer [bug 31921]

Bug Fixes Since Baselight 4.4m1.7567
====================================

* Fixed OFX plugin overlay drawing [bug 32713]

* Verify cache path before deleting contents [bug 28619]

* Fixed crash starting applications on a Mac without a suitable GPU
  [bug 33295]

* Moved the Matte and Clip buttons in CDL grade to match the video
  and film grade, Changed clip default to off, removed the pivot
  slider from the graph when not in Film grade tab [bug 33400]

* Removed the bump buttons when CDL grade is no longer active 
  [bug 33381]

* Added mode switching buttons to the blackboard for the CDL bumps
  [bug 32239]

* Fixed several issues with bl-scenedetect [bug 33413]

* Fixed copying of 12-bit VRW files using fl-cp/flux or Consolidate
  [bug 33424]

* Opening legacy format files now supports host and site format files
  [bug 31899]

* Improved VTRE reliability on Baselight FOUR and EIGHT systems
  [bug 33620]

* Formats with explicit mappings to/from the Working Format are now
  indicated with a mapping icon in the Viewing Format menu [bug 33431]

* Fixed issue with Arrilook not rendering when placed inside an 
  inside/outside layer [bug 33404]

* Changed the CDL grade to import and export .cc file extensions. 
  Changed the export format to match that of a CCC file if the
  extension is .cc or .ccc. Added displaying the id if mulitple color
  corrections found and a description is missing. [bug 20496]

* Fixed an issue causing MXF files with partial indexes to not be
  readable at all. The fix allows reading of the indexed frames,
  ignoring any trailing unindexed frames [bug 33485]

* Fixed problem with grabbing outgoing dissolves to the gallery 
  [bug 32296]

* Optimised the index processing when opening temporally compressed
  MXF files. Scanning directories with large MXF files is now up to 45
  times faster [bug 33359]

* Fixed an issue where audio could not be read from Quicktime movies
  with empty audio channel label (chan) atoms on Linux [bug 33565]

* Fix crash rendering audio only files [bug 33562]

* Fix crash when rendering movies or audio files with audio channel
  remapping [bug 32604]

* Fix subtitle ruby text position and size [bug 33588]

* When rendering audio MXFs fall back to video timecode if there is
  no shot audio timecode [bug 33319]

* Fixed a bug when remapping encoders in FilmGrade on Blackboard and
  Slate desks [bug 32374]

* Fix for Chalk for Slate where newly added buttons could disappear
  after closing the Chalk window [bug 32745]

* Fixed issues reading and writing DNxHR QuickTime movies [bug 33486]

* Fixed crash when subtitle PNG file can't be found [bug 33598]

* Fixed slow behaviour in operations queue monitoring when there are
  many operations in the queue [bug 33571]

* Fixed error crosses shown in in Cuts View in Start & End mode, when
  only one of the Start or End thumbnails is unavailable [bug 33488]

* Fixed failure to browse Kompressor volumes in flux [bug 33471]

* Fixed an issue where the index in some AVC-LongGOP MXF files was not
  correctly parsed, causing the decode of the affected files to be
  extremely slow [bug 33629]

* Fixed an automounter race which sometimes caused the first access to
  the /pfs/images filesystem to fail [bug 33609]

* When rendering OpenEXR output files from ARRIRAW input material, the
  ARRIRAW metadata is stored as OpenEXR metadata using the same keys
  as in ARRI's tools [bug 32893]

* Fixed a "Variable Timing" option in EDL Import View to now behave
  properly when the "No" option is selected - it now falls back to the
  pre-4.4m1 behaviour of constructing a linear speed change to arrive
  at the same end-frame [bug 33603]

* Fixed problem applying or pasting to a stack which contains a
  dissolve [bug 29204]

* Fixed bug in EDL Import where events with variable retimes on them
  would sometimes have an incorrect length, when compared to the same
  event in Avid [bug 33559]

* Fixed opening old scenes with sharpen in [bug 33643]

* Fixed opening of media that relies on group access permissions
  within Baselight [bug 33647]

* Fixed issue with correct viewing colour space not being applied when
  in stereo geometry fix [bug 33583]

* Fixed eight-channel audio output via HDMI on AJA Kona 4 and Io4K
  [bug 32867]

* Added Adaptec firmware update script 'adaptec_fwflash' [bug 31249]

* Added support for Adaptec 81605Z RAID controller [bug 33660]

* Fixed failures when decoding certain ARRIRAW files using the ARRI
  SDK [bug 33676]

* Fixed failure to decode some JPEG 2000 frames [bug 33689]

* nVidia GPU temperature diagnostics checks all cards [bug 33638]

* Don't process audio-only files during conform [bug 33686]

* Improve the speed of XML parsing during conform for XML with 
  CDATA blocks  [bug 33686]

* Fixed tracking when using a 10 bit 4:2:2 Display format [bug 33144]

* Fixed bl-reset-cache failure when cache directory doesn't exist
  [bug 33728]

* Fixed overallocation of video memory in GPU renderer [bug 33695]

* Fixed memory leak reading images from GPU -> CPU [bug 33778]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7567 (2015-07-29)

New Features Since Baselight 4.4m1.7448
=======================================

* A new "Manage Colour Spaces" dialog can be opened from the Baselight
  menu or from the Formats editor (in Baselight or in bl-formats).
  This allows colour spaces to be set as hidden, which will hide them
  from all colour space menus unless Shift is pressed. The list of
  hidden colour spaces is stored in the global preference database
  [bug 32641]

* Pixel aspect ratio values are now written into DPX files correctly
  [bug 32841]

* Pixel aspect ratio values stored in many media types now shown in
  the Sequence Browser and are used to help select formats [bug 32841]

* Added support for multiple monitors on Baselight ONE systems [bug 32185]

* bl-config-xorg has been changed to support systems without Blackboard
  control surfaces. bl-config-xorg will now ask whether you have a
  Blackbaord ONE or TWO attached to your system.

  This frees the second DVI/DisplayPort connector on Baselight ONE
  systems for use with UI monitors.

  On Gen 5 and Gen 6 Baselight ONE systems, bl-config-xorg will also
  ask which connector on the UI GPU that the Blackboard is attached to,
  allowing you to attach UI monitor(s) via the DisplayPort connector rather
  than the DVI connector [bug 30627]

* Increased maximum zoom range of retime operator's time vs time graph
  [bug 32815]

* Added Export ccc file option to the CDL operator [bug 29757]

* Improvements to BLG Export of BLGs compatible with v4.4:
    - In the BLG Export panel, changed "Version Compatibility Warning"
      to "Version Compatibility" with explicit choices of "v4.4" and
      "v4.4m1"
    - Exporting a BLG with "Version Compatibility" set to "v4.4" will
      replace all the CDL grade operators with VideoGrade operators
      with the same CDL compatible values set [bug 31861]
    - ColourSpace operators can now be included in BLGs exported with
      a "Version Compatibility" setting of "v4.4" [bug 33014]

* In preparation for the upcoming beta tests of Baselight for Avid
  v4.4m1 and Baselight for Nuke v4.4m1, added a "Version Compatibility"
  option to the "Update Avid AAF with Baselight Grades" EDL Export
  panel. By default, this is set to "v4.4", to produce AAF files
  compatibile with the released versions of the plugins. When beta-
  testing v4.4m1 versions of the plugins, use the "v4.4m1" option.
  [bug 33014]

* Added new preference "Prevent Transitions from being grabbed to
  gallery". This will prevent any incoming or outgoing transition from
  being picked up when shots are batch copied to a gallery. The
  default is set to off [bug 32296]

* Added option to create hard links to unchanged input files when
  rendering [bug 32947]

* Added support for extended sensitivity (ISOBase) metadata in
  Panasonic VRAW files [bug 33163]

Bug Fixes Since Baselight 4.4m1.7448
====================================

* Fixed potential dropped frames if a mark was added during playback
  [bug 32586]

* Fixed order of Gain and Gamma in Dolby Vision XML export [bug 32793]

* Fixed problems with using bl-conform and and --ApplyASCCDL option
  [bug 32446]

* Fixed recognition of XDCAM HD MXF files written by MOG [bug 32757]

* CDL grade now adds Metadata values to the shot [bug 32795]

* Sony XDCAM HD MXF output now permits 24p output [bug 32798]

* Fixed timecode read from R3D media when the first frame is the
  second frame of a doubled timecode pair [bug 32806]

* Fixed Replace with protect mattes paste mode moving paste protected
  layers [bug 32615]

* Denoise gives message when pick sets values and error messages when
  pick cannot set values [bug 32750]

* Fixed delta being left open when cutting up a strip [bug 32834]

* The Sequence Browser no longer offers formats for movies where a
  proxy resolution of the format matches the movie's dimensions (e.g.
  a 4K format will not be offered for a 2K movie) [bug 32836]

* Fixed crash pasting non-ASCII characters into a text field on Mac
  [bug 32889]

* Added diagnostic preference to disable Adaptec RAID configuration
  check [bug 32860]

* The nightly crash report flushing process no longer generates mail
  to root each night when there is no error [bug 29501]

* Handle degraded-rbld status in 3ware raid diagnostic [bug 32931]

* Fix 'Source Relative' conform issues for sequences with timecode
  [bug 32631]

* Fixed failed to multipaste BLGs exported from FLIP [bug 32951]

* fl-cp no longer copies movies into resolution directories; its
  behaviour now matches flux [bug 32985]

* bl-power will now accept short-form node names when performing
  actions on the nodes of a Baselight FOUR/EIGHT [bug 31358]

* "Update Avid AAF with Baselight Grades" now warns if one of the
  grades generated will not load into a v4.4 version of Baselight for
  Avid.

* Multi-paste no longer offers to change the container of every scene
  it opens [bug 32817]

* Fixed crash caused by a Truelight strip with an incomplete Truelight
  command [bug 32903]

* Fixed LUT export to match grades when the scene's Grade Result
  Colour Space is not set to 'From Stack' [bug 32999]

* Added an option to LUT export to allow the Input Colour Space
  conversion for a sequence to be replaced with the LUT [bug 33149]

* Fixed LUT export failure caused by the input strip having
  Orientation set to Flip or Flop [bug 33277]

* Allow 1.5G SDI to be selected for SDI output at UltraHD and 4K
  resolutions [bug 30200]

* Fixed behaviour of Colour Space operator when it is used in a layer
  [bug 33067]

* Fixed initialisation of Sequence Interlacing Treatment when
  inserting interlaced media [bug 33071]

* Fixed incorrect brightness of UI elements when using an HDR display
  device [bug 33105]

* Fixed Sequence Browser colour management when selected colour space
  is "Default" [bug 32902]

* Fixed problem with fl-cp caused by using the wrong effective
  identity which could cause failures on NFS drives [bug 33131]

* Fixed "View" appling the sRGB option to the main display if it was
  turned on in the cut view. Removed sRGB being disabled when the
  viewing and working colour space matched. Fixed gallery notes not
  being added correctly [bug 25416, 33073, 26786]

* Fixed Conforming a CDL not naming CDL layer correctly [bug 33126]

* EDL conform now warning if a film grade can't be created when 
  conforming a EDL with CDL values [bug 32455]

* Fixed bug which prevented 12 bit DPX files produced by the Codex
  Vault from being recognised [bug 33186]

* Fixed playback of UHD material on Gen VI machines. Playback could
  enter a slow state caused by the Nvidia driver incorrectly deciding
  that buffers used to transfer from CPU -> GPU were used for GPU ->
  CPU transfers. This issue affected cached and non-cached playback
  [bug 33257]

* Fixed a decode failure affecting the last frames of MXF files with
  start offsets [bug 32863]

* Improved accuracy of fl-diag disk controller performance
  test for faster RAID HBAs [bug 18612]

* Fixed an issue which prevented some OpAtom MXF files from being
  read, giving an 'Unsupported MXF' message [bug 33289]

* Fixed command line conform with a CDL grade [bug 32446]

* Audio Timecode written to Avid OP-Atom MXF movies now correctly uses
  the Audio TC from Shots View [bug 33319]

* Fixed tl-utils TcsToCtf to handle gammas beneath 1.0 correctly for
  Autodesk .ctf files [bug 33297]

* Fixed failure to conform material whose resolution matches the proxy
  resolution of a known format, but not the high resolution of any
  known format [bug 33301]

* Improved error handling when rendering SStP codec to a Sony MXF
  container fails with an exception [bug 33326]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7448 (2015-06-11)

New Features Since Baselight 4.4m1.7383
=======================================
 
* Added support for reading newer Avid MXF files using ProRes codecs
  [bug 32333]
 
* Added Blackboard and Slate support for bumping values in the CDL
  grade [bug 32239]
 
* Added a "Fuzzy" option to the "Match By" section of the Multi-Paste
  View. When used instead of "Exact" for Tape Name, Clip Name or BLG
  Name options, the matching process changes:
     - The match is case insensitive (this replaces the former "ignore
       case" variations in the drop-down.
     - If it can't find an exact match, it will try to find a common
       prefix and match using that instead. For example, with "Fuzzy"
       selected, "shot_abcd_v1" would match against "shot_abcd",
       "shot_abcd_v2" etc. The common prefix must comprise at least
       half of the original tape name, clip name or BLG name to
       prevent too many false matches [bug 20760]
 
* The number of audio channels in the Render view can be set to "Auto
  (from source)". This makes the output movie have the same number of
  audio channels as the source audio file. This is useful for
  rendering dailies, where each shot may have a differing number of
  source audio channels and the output movie or audio file should have
  the matching number of audio channels [bug 32190]
 
* When rendering with Audio Channels set to "Auto (from source)",
  clips with no audio will result in movie files with no audio track
  [bug 32525]
 
* You can now remap the audio channels in Render view, on a
  per-deliverable basis. This allows you to generate, for example,
  stereo h.264 movies for dailies where the left and right channels in
  the h.264 movie are mapped to the mono mix channel from the source
  audio files [bug 4508]
 
* Added option on Colour Space operator to convert to the Input Colour
  Space of the Sequence operator at the top of the stack [bug 31795]
 
* CDL Grade can now be added as an Input Layer operator [bug 32448]
 
* Several changes relating to merging events around dissolves when
  loading CMX EDLs:
 
   - Due to feedback from customers that Baselight was too aggressive
     in merging events at the out-point of dissolves, the "Merge
     events around CMX3600 dissolves" preferences has now become a
     drop-down with three options:
       "Don't Merge" - Don't merge any events.
       "Merge only zero-length incoming clips" - Baselight only merges
        events at the in-point of dissolves and only if the incoming
        event of the dissolve is zero length. This is the new default.
       "Merge incoming and outgoing clips" - Baselight will attempt to
        merge clips on both in the input and output of dissolves. This
        is the old default [bug 30088]
   - Baselight is now able to merge events where there was a speed
     change applied to both events.
   - Baselight is now able to merge if the first mergeable event's
     tape name differs from the following event's tape name only by
     having the letter B on the end (eg "100B") [bug 29070]
 
* Updated to ARRIRAW SDK v5.1. This improves colour reproduction for
  ALEXA 65 material. The Baselight ARRIRAW decoder has been updated to
  use the same colour science. Note that this only affects ALEXA 65
  material added to a scene; older scenes are unaffected.
 
* Added choice of full-resolution decode method for Sony F65 material
  in Sony RAW Params operator [bug 32664]
 
* Added preference for background caching shots before the current
  cursor position first [bug 32594]
 
* Added an extra decimal place of precision to film grade exposure
  value & bump [bug 32592]
 
* Added a new trackball mode to curve grade operator: "Control Point
  Per Trackball" (available from the 'Customise' menu). Once enabled
  the 3 trackballs map to control points at the bottom, middle and
  top end of the currently selected curve [bug 32584]
 
Bug Fixes Since Baselight 4.4m1.7383
====================================
 
* Added DPM (Disk Performance Monitoring) support for Adaptec RAID
  controllers as used on Gen VI hardware. Including adding a 3ware style
  presentation of drive latency figures.  Also amended the DPM tool so
  that Hitachi Deskstar P7K500 drives which don't always return a SMART
  value for rotational speed aren't flagged as SSDs [bug 31638, 32616,
  32684]
 
* Fixed DPX and OpenEXR being copied in the wrong format (e.g. copying
  16-bit DPX resulted in a 10-bit output sequence) [bug 32326]
 
* Badly-formatted timecodes no longer cause an EDL crash [bug 32357]
 
* Fixed crash importing a EDL with "Generate Film and Video Grades"
  selected when one of the events has no CDL values [bug 32283]
 
* Fixed bl-conform --template not applying values from the Scene
  Template [bug 32323]
 
* Fixed gallery grab failure when the grabbed stack uses a Job Format
  [bug 32277]
 
* Fixed the launching of Baselight on a display that is not ":0.0"
  [bug 27501]
 
* Fixed the stopping of an in-progress conform reporting incorrect
  results when re-started [bug 25814]
 
* Fixed the netperf diagnostic for single 10Gb link kompressors in
  environments that have a wildcard dns [bug 30563]
 
* Added default values to ALE CDL exports [bug 32398]
 
* The default Truelight profiles directory in the preferences is now
  used as the default location for the Truelight strip as well as for
  the cursor. If a profile or cube is selected from another directory,
  the list for that strip will now be populated from the same
  directory [bug 26688]
 
* The reload button on the Truelight strip now also reloads the
  contents of the list of profiles and cubes [bug 31612]
 
* Changed the ordering of cube format options in the Export LUTs
  dialog, to show Truelight formats then others in alphabetical order
  [bug 31923]
 
* Added scroll bar to OFX plugins that only have one tab of controls
  [bug 32432]
 
* Fixed display of mattes while interactively grading with interlaced
  scene [bug 32293]
 
* Fixed missing Sony: S-Log2 / S-Gamut colour space [bug 32407]
 
* Fixed crash when unable to load formats during application startup
  [bug 31582]
 
* Fixed render failure using "Prefer Source Codec" when first input
  shot is not a movie [bug 32500]
 
* Fixed rendering with pulldown [bug 32496]
 
* Fixed pulldown removal in Sequence operator [bug 32459]
 
* Fixed field order options in rendering (-interlace/-progressive in
  bl-render) [bug 32503]
 
* Fixed bl-conform to create a crash report if it fails [bug 32502]
 
* Fixed failure to read RAW image sequences (ARRIRAW, RMF etc) stored
  in resolution directories when the Input Format is set to a
  crop/full-gate resolution [bug 32507]
 
* Format editor Copy button no longer retains previously copied
  formats [bug 32508]
 
* Improved scope performance during playback on some nvidia video
  cards [bug 32501]
 
* Fixed bug where dragging a gallery thumbnail which had fallen back
  to using its grabbed still (rather than the original media) into
  another gallery would show an "X" rather than the image [bug 32504]
 
* Fixed clipping to 1.0 when rendering OpenEXR from a scene set to
  32-bit floating-point cache [bug 32247]
 
* Fixed an issue which caused very many index table segments to be
  created when rendering XDCAM MXF. This in turn caused these files to
  be slow to open [bug 32527]
 
* Fixed crash changing the Audio Codec setting in the Render view when
  Audio Channels was set to "Auto (from source)" [bug 32533]
 
* When formats are chosen during conform, scene formats and job
  formats are now chosen ahead of global formats [bug 32529]
 
* Fixed failure in Verify render [bug 32620]
 
* Added workaround for incorrect firmware in some ARRI B+W cameras
  [bug 32622]
 
* Fixed occasional issues with loss of metadata from BLG files,
  causing problems with multi-paste [bug 32662]
 
* Fixed potential "too many open files" and "bad file descriptor"
  error messages [bug 32636]
 
* Fixed slow write speeds for some image formats e.g. DPX [bug 32567]
 
* For compatibility with other software, DPX files are now written
  with both frame rate metadata fields set to the frame rate of the
  render; the timecode frame rate is no longer stored [bug 32251]
 
* Improved speed of fl-cp copies [bug 32666]
 
* Fixed renders failing when a disabled deliverable has an error in
  its configuration [bug 32235]
 
* Fixed crash when changing the displayed columns in a table (e.g. on
  the Queue Monitor View) [bug 32732]
 
* On completion, LUT generation now removes the temporary test chart
  files it has created [bug 32530]
 
* Crash when saving Denoise preferences fixed [bug 32749]
 
* Fixed issues with image corruption which could occur while or after
  working with RED material decoded using the GPU, and related "Unable
  to obtain GPU memory for RED decode" failures. Both of these issues
  were caused by a bug in the Nvidia graphics driver [bug 32729]
 
  PLEASE NOTE: since corrupted images may have been stored in the
  cache, cached images written by earlier releases are not used by
  this release; this means that scenes opened in this release will not
  retain any previously-cached frames.

* Fixed an issue which caused decode failures and hangs reading
  constant-rate MXFs with empty variable-rate indexes [bug 32388]
 
* Fixed slow replay of 3X16 files from remote machines [bug 32666]
  
--------------------------------------------------------------------------

Baselight Release 4.4m1.7383 (2015-05-12)

New Features Since Baselight 4.4m1.7340
=======================================

* fl-queuetool's "list" "log" and "tasks" commands now have a -w
  option for full-width output [bug 32114]

* fl-queuetool's "tasks" command now outputs only 150 tasks by
  default; it has new -a and -n options to change this [bug 32202]

* Added an option to the new LUT generation to replace grade
  operations in the scene with the new LUTs. This option is only
  available for LUTs that don't include Input or Output colour space
  conversions [bug 32033]

* Added "-set" option to bl-render to allow deliverable sets to be
  submitted for rendering from the command line [bug 24457]

* Added "-template" option to bl-conform to allow use of a Scene
  Template [bug 32271]

Bug Fixes Since Baselight 4.4m1.7340
====================================

* Fixed failures after resetting a Colour Space operator [bug 32113]

* On Mac, Num Lock (or Clear) no longer blocks any keypress when using
  numeric keypad grading [bug 32102]

* Fixed error handling in LUT export and improved detection of shapes
  [bug 32097]

* Fixed failure to export LUTs on multi-node systems [bug 32035]

* Fixed failure to export LUTs from ARRIRAW material [bug 32140]

* Fixed consolidate to a non-/vol location [bug 31797]

* Can no longer create a scene with a 0x0 working format when an audio
  file is selected in Sequence Browser [bug 31868]

* Fixed a bug that could cause reading of temporally compressed movies
  to hang [bug 31893]

* Fixed an issue that created broken h.264 QuickTime movies when using
  rate control with framerates of 23.976 or 29.97 [bug 32143]

* Fixed crash when group grading a CDL Grade [bug 32162]

* Improved error reporting for LUT export failures [bug 32188]

* Added warning to LUT export when overwriting cubes [bug 32179]

* Added warning for duplicate cube file names in LUT export 
  [bug 32175]

* Fixed failure to decode some AVC-Intra 4:2:2 MXF files [bug 32151]

* Replaced ACES RRT 0.1.1 inverse cube. This fix changes the render of
  old scenes that used the old cube. The old cube had incorrect values
  outside the forward RRT gamut boundary that gave banding for extreme
  colours. The new cube matches the old cube within the forward RRT
  gamut, but is continuous throughout so gives no banding. If you did
  not see banding in an old scene, the change should not be
  visible [bug 31952]

* Fixed reading cursor settings stored in jobs [bug 32001]

* Enabled Grouped Grading for Film Grade Balance Exposure [bug 32023]

* Fixed the 'zones' diagnostic which could hang on Baselight
  Kompressor [bug 32187]

* Fixed Cuts View thumbnails for 2048x1080 Sony RAW media [bug 29923]

* Fixed occasional render hang when rendering to multiple deliverables
  where the first deliverable is not a movie and another deliverable
  is a movie [bug 32200]

* Fixed failures to decode some images (e.g. F65 RAW) at a crop/marker
  resolution [bug 32220]

* Updated DNxHD SDK. This addresses failures to read some QuickTime
  DNxHD files [bug 31975]

* Fixed occasional corruption on render out [bug 32208]

* Fixed bug which could cause the timeline to crash when referencing
  mattes in one layer from another layer's matte [bug 32241]

* Fixed failure in fl-systemmonitor -live [bug 32263]

* LUT export no longer leaves open a temporary scene showing a test
  chart image [bug 32260]

* Fixed inaccuracy in audio timecode when synchronising images
  to broadcast wave files [bug 32264]

* Added support for rendering audio without resampling when source
  audio file is 48048 Hz, scene is 24 fps, and rendered movie frame
  rate is 23.976 fps [bug 32273]

* Fixed many issues in bl-conform [bug 32271]

* Fixed failure scanning a directory containing a zero-length WAV
  file, and include scanner errors in fsdb-ls output [bug 32281]

* Fixed bug where SDI scaling mode was not being correctly applied
  when the software starts [bug 32002]

* Fixed possible corruption on render of R3D files [bug 31946]

* Fixed problems with playback glitching at particular frame rates
  [bug 32216]

* Fixed display of mattes while interactively grading [bug 32293]

* Fixed crash when using the numeric keypad to enter numbers when
  group grading is active [bug 32324]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7340 (2015-04-14)

New Features Since Baselight 4.4m1.7323
=======================================

* Added min/max display range limiter for disparity histogram 
  [bug 31595]

* Added numeric keypad grading to CDL Grade Exposure [bug 29026]

Bug Fixes Since Baselight 4.4m1.7323
====================================

* Fixed warning when using old R3D colour science with GPU decoding
  [bug 31909]

* Fixed DNxHR QuickTime writing [bug 31877]

* Now defaults to lower track if content missing in AAF files. Adds a
  warning to the clip rather than an error [bug 31535]

* Fixed crash selecting reference strips if viewing and working
  formats have different widths [bug 31957]

* Fixed problem that could cause EXR files to be identfied as plain
  files rather than a sequence when copying [bug 31969]

* Fixed naming of colour spaces in Arri Look operator [bug 31968]

* Fixed corruption when rendering 6K RED movies [bug 32016]

* Fixed bad images being generated for RED movies when insufficient
  GPU memory is available [bug 32026]

* Fixed file descriptor leak importing Truelight cubes [bug 32038]

* Fixed failures when stopping and resuming multiple-deliverable
  render operations writing to more than one movie/audio deliverable
  [bug 31991]

* Fixed errors in muxed stereo renders [bug 32005]

* Fixed loss of Scanity dirt mattes when copying DPX files [bug 31941]

* Fixed deliverable formats in scene templates [bug 31987]

* Ensure dates set in Daylight display correctly in Shots View 
  [bug 32079]

--------------------------------------------------------------------------

Baselight Release 4.4m1.7323 (2015-04-01)

New Features Since Baselight 4.4.7317
=====================================

* Formats
  -------

  Formats have been significantly changed in this release.

  Formats no longer hold colour space, frame rate, field order,
  black/white points or black/white alarm points; they are purely the
  resolution of an image, with a set of masks and burnins.

  Colour space, frame rate and field order information is set
  elsewhere in the scene where it is required.

  Many formats were only necessary to bring in sequences and movies at
  a range of frame rates or colour spaces. These formats are no longer
  required since the frame rate and colour space are no longer in the
  formats.

  Basic Formats
  -------------

  There is no longer a need to create a new format for each size of
  material; conform and the Sequence Browser will automatically make a
  Basic Format (with a choice of square or 2:1 anamorphic pixels)
  which can be used as the input format for a Sequence.

  Automatic mappings
  ------------------

  Where no mapping is defined between a pair of formats, the automatic
  mapping (which used to be 1:1 at top-left) now fits the width of the
  source image to the width of the destination format. This makes
  Basic Formats suitable for most uses.

  Scene behaviour
  ---------------

  The New Scene panel allows the choice of any working frame rate and
  working field order in addition to a working format. The working
  format and working field order (but not the working frame rate) can
  be modified in Scene Settings View. The default settings come from
  the Setup.

  Old scenes require an upgrade on load, which will discard the undo
  history. Old formats in the scene are read and their colour space,
  frame rate and field order are used to update the scene (including
  working colour space, working frame rate and working field order,
  grade result space, default input colour space, render colour space,
  frame rate and field order, and all operators which use colour
  spaces, frame rates or field orders).

  Frozen Formats no longer exist. No format-related dialogs are
  presented when scenes are loaded.

  Sequence
  --------

  The Sequence operator has been reorganised to group settings
  together and move commands to an action menu. It now has separate
  frame rate and field order options, and a stack colour space option.

  The Sequence Input Colour Space can be "No Conversion",
  "Automatic/From Metadata" or a named space; the Stack Colour Space
  can be "No Conversion", "Working Colour Space" or a named space.

  When there is a conversion from the Input Colour Space to the Stack
  Colour Space, a Display Rendering Transform may be specified.

  Sequence now knows whether its images are single-channel; if they
  are then it assumes they are mattes and applies no colour space
  conversion

  When a sequence uses a Basic format as its Input Format, the actions
  menu allows a real format to be created and used; this is necessary
  if you want to define mappings, masks or custom proxy resolutions.

  Conform
  -------

  Conform no longer warns about frame rate or colour space mismatches.
  It no longer requires formats to be created for all the media
  resolutions.

  Sequence Browser
  ----------------

  Sequence Browser now has controls to specify frame rate, field order
  and colour space, including an option to use the scene's default
  colour space setting. These settings are applied to inserted
  Sequences.

  The frame rate and field order are set automatically from movies,
  but can be locked to prevent automatic changes.

  Sequence Browser assumes sRGB viewing colour space when its colour
  management option is enabled.

  Render
  ------

  Render View now shows Output Frame Rate. This is used to determine
  the pulldown options available.

  Rendering with Output Format: Use Input Format now only uses the
  Input Format geometry, not its frame rate, colour space or field
  order.

  bl-render has new options: -rate, -progressive, -interlace lower,
  -interlace upper (all of these default to the scene's working
  settings).

  Formats hierarchy and storage
  -----------------------------

  Baselight supplies a new small set of system formats, which should
  cover most requirements for scene working formats and render
  deliverables.

  Global formats are stored in a database whose location is stored in
  preferences, defaulting to the local system. This allows shared
  host/site formats to be configured far more easily.

  Formats can now be held in jobs. Job formats are accessible to all
  scenes in the job. When creating a new scene, the job's formats are
  included in the Working Format menu.

  There are no longer per-user formats.

  Formats editor
  --------------

  The formats editor now shows a tab for each format set (global,
  current scene's job and current scene). Formats on other systems and
  in other jobs can be opened. Formats can be copied and pasted
  between different hosts and jobs.

  Legacy user formats can be loaded to copy them into global or job
  formats.

  Job and global formats can be reloaded to allow format edits made by
  others (to global or job formats) to be recognised. Reloading
  formats can result in formats disappearing; if a deleted format is
  required by a scene it is automatically converted to a scene format.

  Formats can now be deleted. They can be exported to a file and
  opened from a file.

  Thumbnail resolution sizes for formats are now always automatically
  generated, and cannot be edited in the formats editor.

  Other format-related changes
  ----------------------------

  The Display tab in Setups now allows a default initial Viewing
  Colour Space to be set to match the display.

  Technical Grade no longer shows a menu for its output format; it is
  now purely a grade operator. Note that this change could affect
  scene behaviour in scenes using Technical Grade operators.

  Pan&Scan no longer converts the image to the colour space of its
  output format. Note that this change could affect scene behaviour in
  scenes using Pan&Scan operators.

* Scene Templates
  ---------------

  When creating a new scene you can now select a Scene Template which
  is used to set up the new scene's Scene Settings and Render View.

  A number of FilmLight scene templates are shown at the top of the
  menu; you can select a job containing additional scenes which are
  added to the list.

  Any existing scene can be used to set up a new scene using the
  "New Scene Using Scene Template" option on the Job Manager.

  Baselight ships with 3 Scene Templates that should give a starting
  point of how to setup a standard Baselight scene. These Templates
  should cover most of the grading workflows used in the industry
  (also explained in greater detail at:
  http://www.filmlight.ltd.uk/workflow/truelight.php)

  The three Templates are

  ACES Template
  -------------

  This should set up a scene in a ACES recommended fashion

  The following settings are set:

  Scene Settings:
  • Timeline Caching: Full
  • Display And Timeline Cache: 10-bit Integer RGB
  • Working Colour Space: ACEScc: ACEScc / AP1
  • Grade Result Colour Space: From Stack
  • Display Rendering Transform: ACES RRT 1.0
  • Colour Treatment: Native (as we have a HDR Working Format)

  You should set your Image Container to the Project/Job level in the
  file structure in order to get the deliverables to work properly.

  Render Deliverables are included that should cover most of the
  deliverables needed in a production:

  • Dailies Avid graded
  • VFX Plates ungraded
  • VFX Plates graded
  • QT for Approval
  • P3 Deliveries
  • DCI XYZ Deliverable
  • ACES Archive
  • rec709 Deliverable

  Telecine Template
  -----------------

  This should set up a scene in an "Telecine"-like setup

  Scene Settings:
  • Timeline Caching: Full
  • Display And Timeline Cache: 10-bit Integer RGB
  • Working Colour Space: ARRI: LogC / WideGamut (can be substituted
    with any log like HDR Camera Colour Space)
  • Grade Result Colour Space: Rec.709: 2.4 Gamma / Rec.709 (can be
    substituted with your primary grading display)
  • Display Rendering Transform: None
  • Colour Treatment: Native (as we have a HDR Working Format)

  You should set your Image Container to the Project/Job level in the
  file structure in order to get the deliverables to work properly.

  Render Deliverables are included that should cover most of the
  deliverables needed in a production:

  • Dailies Avid graded
  • VFX Plates ungraded
  • VFX Plates graded
  • QT for Approval
  • rec709 Deliverable
  • P3 Deliveries
  • DCI XYZ Deliverable
  • VFX Plates graded log

  Video Template
  --------------

  This should set up a scene for a Video-like grade, where most of the
  input footage is already "low dynamic range" Rec.709.

  Scene Settings:
  • Timeline Caching: Full
  • Display And Timeline Cache: 10-bit Integer RGB
  • Working Colour Space: Rec.709: 2.4 Gamma / Rec.709
  • Grade Result Colour Space: from Stack
  • Display Rendering Transform: Truelight Video 1 (this is only used
    if you bring a HDR Camera Format in the scene)
  • Default Image Transformation / Colour Treatment: Linearized (as we
    have a LDR Working Format)

  You should set your Image Container to the Project/Job level in the
  file structure in order to get the deliverables to work properly.

  Render Deliverables are included that should cover most of the
  deliverables needed in a production:

  • Dailies Avid graded
  • VFX Plates graded
  • QT for Approval
  • rec709 Deliverable
  • DCI XYZ Deliverable

* Colour Space operator
  ---------------------

  The Colour Space operator allows (a) explicit conversion of colour
  space in a grading stack, optionally with an explicit Display
  Rendering Transform, and (b) explicit assertion of an image's colour
  space (e.g. following a Truelight operator).

  Inserting a BLG adds Colour Space operator strips where required to
  match the colour spaces and DRT in use when the BLG was created.

* Retime operator
  ---------------

  Retimes can be added to a stack from the 'Insert' menu or by
  editing existing operators in a layer (typically the input
  layer/strip).

  Graph Modes:

  The Retime operator has 2 explicit graph modes: 'Velocity vs. Time'
  (the default) and 'Time vs. Time'. The graph for each mode is
  maintained separately & can be selected from the 'Graph Mode'
  dropdown. In both modes the X axis of the graph represents the output
  time (in strip start relative frames).

  In 'Velocity vs. Time' mode the Y axis represents the (percentage)
  velocity at the corresponding X axis output time. By default this
  graph has a constant value of 100%. Because the graph is constant,
  dragging the graph line up or down will set a new velocity for the
  entire shot. To vary the velocity during the shot, keyframes must
  be added at the desired times on the graph (using the toggle
  keyframe icon button, Blackboard key or keyboard shortcut).
  Additionally, a constant frame offset can be applied to adjust the
  input start time.

  In 'Time vs. Time' mode the Y axis represents the input time at the
  corresponding X axis output time. By default this graph has 2
  keyframes (at the start & end of the shot) that make a diagonal line
  mapping output time to the same input time.

  Sampling modes:

  The Retime operator has 3 sampling modes that control how the output
  image is rendered (when the input time is between 2 frames):

  Snap To Frame      - The output frame is the input frame at the
                       input time rounded down to the nearest frame.
  Mix Nearest Frames - The output frame is a mix of the 2 frames
                       on either side of the input time.
  Optical Flow       - Frames on either side of the input time are
                       processed using an optical flow based algorithm
                       to produce a single output frame. In this mode
                       additional parameters are provided to fine tune
                       the rendering:
                       Quality   - Specifies the amount of processing.
                                   Increasing the quality will increase
                                   both the precision and the rendering
                                   time.
                       Smoothing - Controls the amount of smoothing
                                   applied to compensate for incorrect
                                   motion vectors.

  A default sampling mode for any new Retimes can be set from the
  operator's "Customise" menu.

  Blackboard controls:

  The Blackboard can be used to make adjustments to the current curve
  using the following trackball mappings:

  Right Trackball  - Move the graph/current control point up or down
                     (adjusting the input time). If the graph has
                     keyframes, the trackball's buttons can be used
                     select next/previous keyframes.
  Middle Trackball - Move the current control point (if any) left or
                     right (adjusting the output time).
  Left Trackball   - Adjusts the frame offset when the graph mode is
                     "Velocity vs. Time".

  Keyboard shortcuts:

  If 'Numeric Keypad For Grading' is enabled (from the 'Edit' menu)
  the following numeric keypad shortcuts become active when a Retime
  operator is selected:

  '-'           - Toggle keyframe at the current time.
  '+'           - Move the graph/current keyframe up by either 10%
                  or 10 frames (depending on the graph mode). If the
                  'Ctrl' modifier is held down, then the change
                  applied is reduced to either 1% or 1 frame.
  'Enter'       - Move the graph/current keyframe down by either 10%
                  or 10 frames (depending on the graph mode). If the
                  'Ctrl' modifier is held down, then the change
                  applied is reduced to either 1% or 1 frame.
  'Del'         - Reset the graph/current keyframe to it's default
                  value.
  'Insert'      - Toggle the graph editor's zoom level between it's
                  default and +/- 10 output frames.

  Sequence Operator Resampling Modes:

  The input strip's Sequence operator now offers 4 resampling modes:
  'From Scene', 'Snap To Frame', 'Mix Nearest Frames' and
  'Optical Flow'.

  In 'From Scene' mode, the mode to use is derived from the scene
  settings (which is in turn initialised from the appropriate Setup
  when the scene is created).

  The 3 other modes are described in the 'Retime Operator' section
  above.

  Resampling modes come into play when a fractional 'Frame Increment'
  setting and/or input to viewing format frame rate mismatch result in
  a fractional input sequence frame number. When this occurs, the
  resampling mode is used to control how frames on either side of this
  frame number are combined to generate a single result frame.

  Note: 'Frame Repeat Count' values other than 1 are only supported in
  'Snap To Frame' mode.

* Baselight is now able to read non-linear speed changes in AAF files
  and convert them to Retime operators, if the "Variable Timing"
  option is set to "Yes" in the EDL Import panel [bug 25912]

* Colour Matrix operator
  ----------------------

  The Colour Matrix operator will transform the current image using a
  matrix and an offset. When transforming from rgb to RGB...

  R = Rr*r + Rg*g + Rb*b + Roffset
  G = Gr*r + Gg*g + Gb*b + Goffset
  B = Br*r + Bg*g + Bb*b + Boffset

  The user interface has three groups of four sliders to control the
  four parameters for each of the three outputs. The desk controls
  come in groups of three, so to make things neat, the offsets have
  all been moved to their own group.

  There is a scale slider at the bottom. This will scale all these
  parameters, and so scale all the output image values.

  There is an Invert button. When Invert is Enabled, the plug-in will
  do the inverse transform. If the transform cannot be inverted (set
  scale to zero for example), you will get an error message.

  You can use this plug-in to perform grades in a crude
  luminance-chrominance space as follows...

  L:  Rr=+0.6   Rg=+0.3   Rb=+0.1   Roffset=0.0
  a:  Gr=+0.5   Gg=-0.5   Gb=+0.0   Goffset=0.5
  b:  Br=+0.0   Bg=+0.5   Bb=-0.5   Boffset=0.5

  Copy and paste the ColourMatrix strip. On the second copy, select
  Invert Enable. This should restore you to the original image
  coordinates.

  If you do a grade between these two strips, the grade will be
  working in a luminance-chrominance space.

* CDL Grade operator
  ------------------

  CDL Grade now replaces the Video Grade operator for all CDL values
  imported into or exported from Baselight.

  The Grade operator is split up into 3 separate tabs: CDL, Film Grade
  and Video Grade. The CDL tab presents the grade using Slope Offset
  Power, the Film grade presents Exposure Power Contrast, and the
  Video Grade presents the same grade using Lift Gamma Gain. The
  saturation control remains the same between the 3 tabs.

  The text entry field below displays the current values in a CDL
  format. Values can then be copied to a file from the text, or
  entered into the text field to change the operator's values.

  In the customise menu there is an option to import a ".ccc" XML
  file, this will set the CDL operator's parameters to the values
  stored in the file.

* Feet+Frames
  -----------

  Feet+Frames can now be used as an option for timeline units. The
  timeline start footage and gearing can be set in Scene Settings.

  A new %{TimelineFootage} substitution can be used in burnins and
  Text strips to insert the timeline feet+frames.

  The "Keypad 'go to' default mode" preference can be set to default
  to navigating using Feet+frames, or to swap to Feet+frames when 0 is
  pressed [bug 18516]

* ARRI Look operator
  ------------------

  A new operator has been added to allow the import of ARRI look
  xml files. This operator will apply the ARRI look colour space
  conversion and tonemap to the image as well as any CDL, printer
  lights or saturation values present in the look file.

  The operator can also toggle each ARRI look operator or set the
  desired output colour space. Any colour space changes will be
  reflected in the colour space journey view

* Subtitling
  ----------

  Added support for Digital Cinema Interop (CineCanvas(TM)) version
  1.1 subtitling. The subtitle XML file is presented as an RGB movie
  with alpha.

  To add a subtitle overlay, create a new layer; set Layer Mode to
  "Matte From Foreground Alpha"; and select the subtitle XML file as
  the source.

* LUT export
  ----------

  LUT export has been updated to handle Colour Space conversions as
  well as grade operations. There is a separate Export LUTs option in
  the Shots View menu which gives options for up to three LUTs to be
  exported per shot.

  Each LUT can contain a combination of the Input Transform (any
  colour space conversion in the Sequence strip), Grade operations
  (from the Input strip and any grade strips) and an Output Transform,
  with a specified Output Colour Space.

  There are now also resolution options for the exported LUT: default
  settings use standard values but these can be overridden if
  required.

* Movie/RAW Decode Quality
  ------------------------

  The way by which decode resolutions are chosen for movie and/or RAW
  files has been simplified. There are now two options:

  - Optimised: this decodes at the closest resolution to the
    cursor/render resolution (e.g. half-res when decoding 4K input
    material with an HD cursor/render)

  - Max Quality: this decodes at the highest available resolution
    (which will then be scaled down as necessary by Baselight to the
    required cursor/render resolution)

  At "Medium" and "Low" resolution, Optimised decoding is used. At
  "High" resolution, the default behaviour for cursors and renders is
  that Max Quality decoding is used. This can be changed on Cursor
  View and Render View on the Resolution line.

  The behaviour can be overridden on individual Sequences by using the
  "Always Decode At Max Quality" button. For example this might be
  necessary if you use Optimised decoding but are scaling up an image
  using a Transform or mapping.

  ARRIRAW sequences decoded using ARRI Decode now always decode at Max
  Quality; this removes previous resolution-dependent switching
  between ARRI Decode and Baselight Decode methods.

  The Sequence "Medium/Low Res." option has been removed [bug 28655]

* ACES 1.0 
  --------

  Added support for the latest ACES 1.0 Specification. The Academy has
  introduced a "Target Conversion Transform" (TCT) or "Render Intent"
  (Dim Surround and Dark Surround). In order to be fully compatible
  with the Truelight Colour Space System two DRTs have been added to
  accommodate both Render Intents. Also two new working colour spaces
  have been added.

  ACES RRT 1.0 Dark Surround
  --------------------------

  ACES RRT 1.0 Dark Surround should be used in combination with
  "theatrical" Display Colour Spaces like "DCI: 2.6 Gamma / DCI P3",
  "ACES: 2.6 Gamma / DCI D60" or "DCI: 2.6 Gamma / X'Y'Z'"

  ACES RRT 1.0 Dim Surround
  ---------------------------

  ACES RRT 1.0 Dim Surround should be used in combination with "video"
  Display Colour Spaces like "Rec.709: 2.4 Gamma / Rec.709" or
  "Rec.2020: 2.4 Gamma / Rec.2020"

  ACEScc: ACEScc / AP1
  --------------------

  "ACEScc: ACEScc / AP1" is a colour space designed by the Academy for
  colour correction. It has a "pure log" tone curve and a new set of
  primaries called AP1 (ACES Primaries 1). The tone curve has no black
  compression on the bottom end and the reference black point is
  defined as CV 0.0. It is the "full range" version of "ACES Proxy"
  and should be used as a Working Colour Space within Baselight. AP1
  spans a colour gamut slightly larger then Rec.2020. It should give
  more sensible control for colour grading compared to the bigger ACES
  AP0 Primaries.

  ACEScg: ACEScg / AP1
  --------------------

  "ACEScg: ACEScg / AP1" is a colour space designed by the Academy for
  computer graphics works. It is has a linear-light transfer function
  and the same AP1 primaries. This colour space should be used in a
  compositing context but not for colour grading.

* New DRTs and Colour Spaces 새로운 DRT와 컬러스페이스
  --------------------------

  Truelight Film 1 DRT 트루라이트 필름 1 DRT
  --------------------

  Truelight Film 1 is a DRT based on the "generic film" Truelight
  profile. It is designed to introduce a filmic colour rendering, as
  produced by a typical modern print film. The inverse DRT
  Transformation is greatly improved to allow an artifact-free inverse
  transformation for Rec.709 or DCI P3 Footage.

  FilmLight: Printing Density Log / ~ADX Colour Space
  ---------------------------------------------------

  This colour space is similar to the Academy "ADX" colour space but
  with more focus on robustness and invertibility. It is designed as
  connection space for the Truelight Film 1 DRT, and should not be
  used as grading colour space for digital content. However if your
  footage is primarily camera negative log scans you can use this
  space as Input and Working Colour Space in combination with the
  Truelight Film 1 DRT.

  Truelight Video 1 DRT
  ---------------------

  This new DRT is designed to introduce a soft "video-ish" or
  "telecine-ish" colour rendering. It is designed for colourists who
  wants to grade HDR data in a display colour space. The DRT
  introduces a soft colour rendering without compressing too much
  data. But it can also be used as a Display Rendering on output.

  It does a slight highlight roll off and a gamut compression which
  starts at 90% saturation, so most colours should be unmodified. The
  inverse transform is robust. The gamut re-compression was skipped in
  the inverse function to gain robustness. So very saturated colours
  might be reproduced inaccurately. The DRT is parametrized, so it is
  possible to build custom DRTs based on Truelight Video 1 - please
  contact baselight-support@filmlight.ltd.uk if you need more
  information.

  ARRI Photometric v2 DRT
  -----------------------

  This DRT is identical to the ARRI Photometric DRT but has an
  improved inverse transform to allow artifact-free inverse conversion
  for Rec.709 or DCI P3 Footage.

* Colour Spaces - New Naming convention
  -------------------------------------

  There is a new standard naming convention for colour spaces, which
  uses {Standard or Manufacturer}: {Transfer function} / ${Primaries}
  / {Optional information like creative whitepoint etc}

  Examples are
  • ACES: Linear / AP0
  • ARRI: LogC / WideGamut
  • Sony: Slog3 / SGamut3.Cine
  • DCI: 2.6 Gamma / DCI X'Y'Z' / Creative D60
  • Rec.1886: 2.4 Gamma / Rec.709

  In order to be fully compatible with the current practice and
  correctly refer to standards, we have renamed some of the colour
  spaces. In particular Baselight 4.4 used "Rec.709" to refer to
  colour spaces actually using Rec.1886.

  Some of the important colour space name changes are:

  4.4   Rec.709 Video
  4.4m1 Rec.1886: 2.4 Gamma / Rec.709

  4.4   Rec.709 Video legal
  4.4m1 Rec.1886: 2.4 Gamma Legal/ Rec.709

  4.4   Legacy Video
  4.4m1 Rec.709 Camera: ~1.95 Gamma / Rec.709

  4.4   P3 Native White
  4.4m1 DCI: 2.6 Gamma / P3 DCI

  4.4   P3 D60 White
  4.4m1 ACES: 2.6 Gamma / P3 DCI / Creative D60

* Colour Space Hints
  ------------------

  Hints, warnings and recommendations are shown in the Colour Space
  Journey View when Baselight detects a non-optimal setup of Colour
  Space Choices, defined by a set of rules. A Truelight Colour Space
  Icon is shown in the menu bar when there is a message in the Colour
  Space Journey View, clicking on it will open the View.

Miscellaneous
-------------

* Added support for the new Generation VI Baselight hardware
  platforms.

* bl-power has been updated. There is a new -sleep option that powers
  down the nodes on a Baselight FOUR/EIGHT system. It no longer scans
  the network for available systems, but connects to the local zone
  only. This stops a lot of zeroconf-related errors [bug 20586]

* bl-power is now better able to restart the system after a startup
  failure [bug 14294]

* The Blank operator now has a colour space option. This allows
  colours to be specified in a known colour space.

* Added support for reading OP-1b MXF files with internal essence
  containers (e.g. Panasonic Varicam) [bug 26422]

* Added support for reading AVC-Intra LT MXF files from Panasonic
  Varicam [bug 31237]

* Added support for reading XAVC LongGOP MXF files [bug 27921]

* When writing QuickTime movies on Mac OS X, codecs that expect
  legal-range data will now show a warning in the render panel if a
  full-range colour space is selected [bug 25506]

* Added support for reading XAVC S MP4 files [bug 26436]

* Improved Stereo Geometry Fix two-phase transform, decreasing
  stereoscopic distortion. Added two new transform mode options:
  Translate + Scale and Translate + Scale + Perspective [bug 28893]

* Added Scratchpad preference to enable grab/recall of input layer
  operators [bug 25163]

* Added ability to change operator type across multiple strips using
  grouped grading [bug 29332]

* Added icon to strips to indicate if any of their operators have
  keyframes [bug 19774]

* Render View options for image types (e.g. the compression applied to
  an OpenEXR render) are now specified in a separate Image section
  under the File Type row [bug 30851]

* Render View "Do Not Read Cache" option has been replaced by a new
  "Disable Cache" option. This has the same effect as changing
  Timeline Caching to Disabled on Scene Settings View. This option may
  change the appearance of scenes if strips are cached. It is
  particularly useful when rendering a scene that uses strip caching
  to a format larger than the scene's Working Format [bug 28941]

* Deliverables can now be enabled and disabled from the tab titles in
  Render View [bug 30041]

* Added Pan & Scan to layer operators [bug 30021]

* Audio Encoding is now shown for QuickTime movies [bug 28489]

* Added "I/O 5" Stack Manager button to Chalk to optionally allow quick
  access to 5th Inside/Outside operator [bug 30305]

* bl-mkscene now takes options for colour space, frame rate and scene
  template [bug 30298]

* When editing directory preferences, the browser now allows new
  directories to be created [bug 30366]

* bl-shots now uses a tab character between each column of its output,
  and does not use quotation marks [bug 28759]

* The Matte Merge operator now defaults to Union rather than
  Intersection [bug 29568]

* Edit boxes are now more prominent when they have input focus
  [bug 29037]

* Added option to Consolidate View to choose whether or not to update
  the scene container [bug 30718]

* Baselight is now able to read Resize operators out of AAF files and
  convert them into Transform operators, if the "Apply Image
  Transforms" options is set to "Yes" in the EDL Import view. The
  interpolation on animated transforms can be specified in the
  "Interpolation" drop-down to the right of the "Apply Image
  Transforms" option [bug 24187]

* Vectorscope now has a new contrast control. This allows the user to
  bring out more detail in the scope [bug 28801]

* Setups have been changed to disable use of a Baselight Kompressor by
  default [bug 31010]

* Alexa 65 ARRIRAW files can now be decoded using ARRI Decode mode
  [bug 30913]

* Added "List File Size" and "Sort By Size" options to Sequence
  Browser [bug 31626]

* Colour space metadata is read from many QuickTime codecs (notably
  h.264) and is used to select a legal/full-range colour space as
  appropriate [bug 24964]

Bug Fixes Since Baselight 4.4.7317
==================================

* Fixed a bug where QuickTime movies read in Y'CbCr 4:2:0 on Linux
  were upconverted to 4:4:4 by a third-party library [bug 25972]

* Fixed a bug where QuickTime movies read on Linux in full-range
  Y'CbCr were converted to RGB by a third-party library [bug 25477]

* Fixed an issue where some QuickTime movies, particularly some XDCAM
  and Canon C300 files, would decode extremely slowly [bug 27002]

* Fixed appearance of thumbnails in Cuts View when the stack uses
  Northlight alpha channels [bug 29237]

* Fixed change in appearance of variable feather shapes when switching
  between an interlaced or anamorphic cursor/output format and a
  progressive or isomorphic one. Note that this may change the
  drop-off rate (but not the overall shape) of shapes created using an
  earlier Baselight release [bug 22561]

* Changes to Timeline Caching on Scene Settings View can now be undone.

* Sequences with % characters in their path no longer cause render
  failures [bug 27618]

* Ensure matte inputs to grades are clamped from 0 to 1 (useful if
  grading through OpenEXR matte channels with out-of-range values)
  [bug 28426]

* Fixed incorrect application of transform in pan & scan when "Output
  Format Only" mode enabled (now renamed to "When Viewing Format
  Matches Output Format") [bug 29959]

* Fixed incorrect thumbnail image in Cuts View when transforming an
  image as a matte for a composite [bug 26048]

* Fixed failure in ramsize diagnostic [bug 28867]

* fl-diag will no longer report an error if the PFS is conigured to
  work with the yfs kernel module [bug 22694]

* Fixed behaviour of cached strips in interlaced formats [bug 28929]

* Fixed occasional crash when applying Scratchpad slots [bug 28668]

* Increased sensitivity of encoder when changing Blend Type via encoder
  on Blackboard 2 / Slate [bug 29054]

* Replaced unusable "Confirm Version" button with "Original Version" 
  for Scratchpad on Slate desks [bug 30305]

* Fixed failures when using Undo/Redo to re-create operators that use
  formats which no longer exist [bug 11868]

* Multi-Insert no longer treats movie files as proxies [bug 30370]

* Stereo (left+right track) renders now render the two tracks at the
  same time rather than using multiple passes through the scene. This
  should improve render speed for scenes using stereo colour matching
  [bug 25856]

* Input from desk trackballs, rings and encoders is now disabled when
  an edit box has focus [bug 29037]

* Allow renumbering of layers that span more than one stack 
  [bug 30636]

* ARRI metadata "CameraClipName" is now used to populate Clip metadata
  [bug 29596]

* Improved the read performance of temporally compressed movie files
  [bug 15023]

* QuickTime internal data references are no longer resolved, to avoid
  hanging when opening certain files [bug 28755]

* Fixed loss of alpha channels using Generate Proxies from the Job
  Manager [bug 30702]

* To address occasional issues with database permissions, all
  connections to job databases are now made as the 'filmlight'
  database user. The bl-fixdb command can be used to reset permissions
  on all scenes on a database host. When older scenes are upgraded to
  Baselight 4.4m1 their database ownership is changed to 'filmlight'
  [bug 30735]

* Baselight now reacts better if you overwrite a movie file that it is
  using, and will read the updated file for future images [bug 30799]

* Fixed crash when Importing/Exporting Chalk layouts on Mac OS X
  [bug 30669]

* Add minimum allowed OS check to Mac OS X installer [bug 30842]

* Fixed bug which prevented layer operator bypass from working if
  there was only a single operator in a layer and the layer had a
  matte [bug 29932]

* If the database it not running, the prerender service will wait a
  few seconds and re-attempt connection. Previously it would sometimes
  fail to start up at boot time [bug 31000]

* The prerender service will now restart itself after losing
  connection to the database, or any other type of error [bug 31004]

* Improved activation of tooltips when using a tablet [bug 28225]

* Fixed a bug where some QuickTime files opened on Mac listed internal
  fourcc codes as metadata [bug 28756]

* 10-bit Packed YUV QuickTime codecs on Linux ('v410' and 'v210') no
  longer automatically squashes the output image to legal range.
  Instead, a warning will be presented in the render panel if a full
  range colour space is selected [bug 26007]

* Fixed crash when subtitle xml file references a missing png file
  [bug 30965]

* Fixed an issue which could cause temporally compressed movies to
  decode with broken images [bug 30985]

* Browsing for an output directory on Render View now expands all %
  substitutions in the path (e.g. %J) [bug 31023]

* Fixed drag and drop from Cuts View not obeying the All, Primaries,
  Layer 0 drop-down [bug 31082]

* Fixed failures caused by the 'postgres' database user not being a
  superuser; added a diagnostic test to check this [bug 31094]

* Fixed crash in conform using "Apply Baselight Grades" when the scene
  uses a non-global working format [bug 31106]

* Fixed issue with Cuts View always redrawing during playing or shot
  jumping [bug 30592]

* Fixed error when importing cdl files into the CDL operator 
  [bug 31129]

* Fixed bug where BLG Export from the Shots View was not correctly
  setting the Viewing Colour Space [bug 31144]

* There is no longer a large performance drop when decoding RED
  material using CPU on a system that has a RED Rocket or RED-capable
  GPU installed, compared to systems without such hardware.

* Load nvidia driver before enumerating the GPUs [bug 30232]

* Improve NVIDIA driver version selection logic to allow for a
  maximum NVIDIA driver version for systems with FilmLight
  DVI2SDI or Framestore hardware [bug 31190]

* Inverted the CDL power parameter so moving up on any slider 
  reduces the value, and moving on the hue wheel has an inverted
  effect on the values [bug 31274]

* Fixed bug which would cause the first newly inserted Film Grade
  operator to have incorrect pivot/bump values if they had been
  changed from the defaults [bug 31326]

* Fixed Timecode 2 reported from Phantom camera .cine movies. It
  should now match what other software reports as the "time of day"
  timecode, taking the recording timezone into account. Timecode 1
  continues to report the definitive per-frame timecode stored in the
  file [bug 31367]

* Fixed calculation of sequence frame numbers for various source,
  working and viewing frame rates [bug 31357]

* Fixed crash when using Display and Timeline Cache "16 bit Floating
  Point RGB" on non-combiner systems BL4/BL8 [bug 31320]

* Fixed pasting layer 0 to include the format (if the resolution are
  the same) and the colour space information [bug 24817]

* Fixed audio playback via AJA Kona 4 SDI card [bug 31460]

* Subtitle painter correctly handles right-to-left written Unicode
  characters [bug 31448]

* Removed incorrect colour conversion applied to matte input of
  subtitle composite layers [bug 31449]

* Fixed bug when referencing a non-inside/outside layer's matte from a
  downstream reference strip [bug 31491]

* Fixed bug which would cause the wrong frames to be displayed for
  sequences with a speed change in resampling modes other than "Snap
  To Frame" [bug 31424]

* Fixed a bug that could cause a lengthy initial delay to commands
  such as fl-ls and bl-browse on some OS X systems [bug 31411]

* Fixed bug which caused Baselight to display an old file when a newer
  one was available on disk [bug 26208]

* Grades which have Clip enabled now clip the image even when the
  grade's settings make no other change to the image [bug 28368]

* The Orientation of the power control in CDL grade has been flipped
  [bug 31095]

* Fixed failures when working with very long R3D clips using many
  run-on .R3D files [bug 12724]

* File system usage information is now reported for cloud media and
  other volumes [bug 31588]

* Fixed a bug that caused custom bitrates for DCP and DCI MXF codecs
  to be interpreted as bits per second rather than megabits per second
  [bug 31606]

* Fixed colour space for VRW (Panasonic Varicam RAW) files [bug 31549]

* Fixed multi-insert to calculate correct file size for R3D files 
  [bug 31373]

* Fixed "output %d Nan" warning messages when generating cubes from
  a stack and added more informative error messages [bug 31680]

* Fix hang on shutdown in SDI output [bug 31736]

* Fix LUT export for files with spaces in the name [bug 31739]

* Fixed diagnostic test for NVIDIA driver version on systems with
  FilmLight DVI2SDI or Framestore hardware [bug 31776]

* Fixed RGB 4:4:4 12-bit SDI output via AJA Kona 4 [bug 31816]

* Due to an update to the ARRI SDK, ARRI-mode decoding of ARRIRAW
  files is no longer available on FLOS 2.1. If your system is running
  FLOS 2.1 and you need to use ARRI decoding of ARRIRAW files, you
  will need to upgrade to FLOS 6.4 [bug 31828]

* Fixed stereo display via AJA Kona 4 [bug 31689]

--------------------------------------------------------------------------

Baselight Release 4.4.7370 (2015-05-01)

Bug Fixes Since Baselight 4.4.7317
==================================

* Fixed problem with SDI setting options appearing blank in the
  Setups editor [bug 31857]

* Fixed compatibility issues reading and writing Avid DNxHR QuickTime
  files [bug 31877]

* Changing any of the SDI setup parameters in the Display panel of the
  Setups editor will not reset the other settings if those settings
  are still valid. For example, changing the SDI frame rate will no
  longer reset the Signal Format or Speed options [bug 30640]

* Added 'nodirect' option to volume.cfg to disable direct io on a
  per-volume basis (e.g. 'limit san_rt0 nodirect') [bug 31316]

* Fixed problem that could cause EXR files to be identified as plain 
  files rather than a sequence when copying [bug 31969]

* Fixed problems rendering to movie files when the system's hostname
  has been modified so it is not fully-qualified [bug 32297]

--------------------------------------------------------------------------

Baselight Release 4.4.7317 (2015-03-30)

Bug Fixes Since Baselight 4.4.7274
==================================

* Fixed failures when working with very long R3D clips using many
  run-on .R3D files [bug 12724]

* Fixed bug which could cause view layouts to be recalled from the
  Slate's numeric keypad when 'View' mode wasn't selected [bug 31349]

* Fixed bug which could cause tracked & keyframed shapes to move when
  their stack was split [bug 31468]

* Fixed a bug which caused bl-browse to show directories as symbolic
  links when real symbolic links exist in the directory being browsed
  [bug 31576]

* Fixed crash which could sometimes occur during tracking, especially
  at large resolutions [bug 30618]

* Fixed display of images on a Gen V BL4/8 without a combiner when
  using 16 bit caching [bug 31573]

* Fixed a bug that caused custom bitrates for DCP and DCI MXF codecs
  to be interpreted as bits per second rather than megabits per second
  [bug 31606]

* Changing the Sequence Browser "List" option now updates the text on
  all items in the browser [bug 31628]

* Fixed "sched_setaffinity" warnings on console when running on a
  system with only 2 CPU cores [bug 31566]

* Fixed bug introduced into fl-diag dpm SMART tests that showed as an
  incorrectly formated smartctl command line [bug 31601]

* Fixed problems with LUT generation where errors were not correctly
  reported [bug 31653]

* Fixed "Add Image" browser when editing a burnin [bug 31669]

* Fixed hang on exit in the SDI display code [bug 31471]

* Removed invalid "UltraHD 48p" setup [bug 31678]

* Fixed incorrect default SDI resolution for "HD 24p (Dual)" setup
  [bug 31688]

* Fixed diagnostic test for NVIDIA driver version on systems with
  FilmLight DVI2SDI or Framestore hardware [bug 31776]

* Changed the default SDI output signal format to "Progressive" for 
  the following built-in setups: "HD 23.98p (444)", "HD 24p (444)",
  "HD 25p (444)", "HD 29.97p (444)", "HD 30p (444)"  [bug 31770]

* Fixed HDMI output for high frame rate modes (48p, 50p, 59.94p, 60p)
  [bug 31780]

* Fixed progress output from command-line bl-render [bug 31786]

* Fix conform bug in subdirectory matching when using the pattern
  "%*" to match any directory [bug 31464]

* Fixed hang on startup when using 48p modes with the AJA Kona 4
  SDI output [bug 31818]

* Fixed AJA Kona 4 settings for PAL and NTSC setups [bug 31786]

* Fixed compatibility issues reading and writing Avid DNxHR MXF files
  [bug 31827]

--------------------------------------------------------------------------

Baselight Release 4.4.7274 (2015-03-09)

New Features Since Baselight 4.4.7262
=====================================

* Added support for reading big-endian 32-bit floating-point RGB TIFF
  files [bug 26656]

Bug Fixes Since Baselight 4.4.7262
==================================

* Relaxed bitrate limitations in the codec parameters for DCP and DCI
  MXF writing. It is now possible to specify any bitrate greater than
  zero [bug 31469]

* Fixed colour issues with very old Phantom cine files [bug 31352]

* Fixed failures caused by inserting removable media with a long name
  [bug 31473]

* Fixed bug which could cause an flfsd assertion error (have_handles)
  when changing the permissions of a file with missing pfs2 attributes
  [bug 31454]

* Fixed internal error in the disk performance diagnostic [bug 31507]

--------------------------------------------------------------------------

Baselight Release 4.4.7262 (2015-03-03)

New Features Since Baselight 4.4.7218
=====================================

* Added -u option to "fl-queuetool list" to make the queue list update
  continuously [bug 31036]

* Added option to set "Input Video LUT" in the "Update Avid AAF with
  Baselight Grades" EDL Export panel. This option allows you to
  specify a Legal-to-Full scale to be applied in Baselight for Avid,
  to counteract Avid's application of a Full-to-Legal scale to some
  RGB444 formats linked via AMA.

  To see the effect in Avid, you will need to install a recent
  version of the Baselight for Avid 4.4 beta (post 4.4.7217).

* The Input layer of Baselight for Avid effects written by the EDL
  Export View's "Update Avid AAF with Baselight Grades" option now
  contain the name of the shot from the Baselight timeline.

* Added support for reading embedded 2-bit dirt matte in 10-bit DPX
  images from Scanity [bug 22879]

* Added 50MB UHD sized file pass to flioinfo which is used by the
  fl-diag disk_performance test [bug 30984]

Bug Fixes Since Baselight 4.4.7218
==================================

* Fixed errors that arise when "Default container directory (high
  res)" is made empty in Setups editor [bug 31051]

* Fixed incorrect Reference Timecode frame rate when inserting
  material with discontinuous timecode, or with an ambiguous timecode
  frame rate [bug 31039]

* Fixed behaviour of "fl-queuetool tasks" when tasks lists is
  non-contiguous [bug 31121]

* Fixed incorrect behaviour when using Ctrl + Right Trackball Ring as
  Jog Wheel control on Slate desks [bug 30182]

* Improved the performance of sequence browsing and conform on slower
  filesystems such as SANs and external drives [bug 30972]

* Fixed errors loading the DNxHD library on some systems [bug 31179]

* Fixed instability when using RED decoding on GPU or RED Rocket,
  particularly on Baselight FOUR/EIGHT systems [bug 31137]

* Fixed crash which could occur on grabbing a new scratchpad entry
  after having closed another scene [bug 31064]

* Fixed Film Grade Balance Exposure behaviour when exposure is
  keyframed [bug 31294]

* Fixed a bug in the file/sequence browser that could cause
  directories to be given the wrong permissions or modes, and special
  files such as a FIFO might cause the browser to hang [bug 31303]

* Fixed support for 1920x1080 and 2048x1080 video modes at 47.95,
  48.00, 50.00, 59.94 and 60.00 Hz when using 1.5G-SDI and 3G-SDI
  Level B signalling on the AJA Kona 4 [bug 31333]

* Fixed 4K HDMI routing on the AJA Kona 4 [bug 31344]

* Fixed incorrect pixels on the left side of ProRes images when the
  image width is not a multiple of 16 pixels [bug 31309]

* Improved error message when attempting to use HDRx blending with GPU
  decoding; this is not supported by the RED SDK [bug 31340]

* Fixed start timecode written to QuickTime movies when timecode frame
  rate is 50@25 or 48@24 [bug 31378]

* DNxHR QuickTime movies tagged as "AVdh" are now correctly recognised
  by Baselight; DNxHR QuickTime movies written by Baselight are now
  correctly tagged as "AVdh" [bug 31423]

* Ensured that tcpmux-server has no connection limit [bug 29311]

* Fixed DNxHD failures on Baselight Kompressor [bug 31290]

--------------------------------------------------------------------------

Baselight Release 4.4.7218 (2015-02-13)

Bug Fixes Since Baselight 4.4.7170
==================================

* Fixed bug which could cause an flfsd assertion error (bad fileid)
  when files are moved between directories [bug 30553]

--------------------------------------------------------------------------

Baselight Release 4.4.7204 (2015-02-05)

New Features Since Baselight 4.4.7170
=====================================

* Updated to RED SDK v5.3. This addresses some issues in earlier SDK
  releases, and adds REDcolor 4 and DRAGONcolor 2 color spaces.

* Added support for reading and writing MXF and QuickTime movies in
  the new Avid DNxHR codecs:

  DNxHR 444 - 12/10-bit 4:4:4 RGB
  DNxHR HQX - 12/10-bit 4:2:2 high quality extended
  DNxHR HQ  - 8-bit 4:2:2 high quality
  DNxHR SQ  - 8-bit 4:2:2 standard quality
  DNxHR LB  - 8-bit 4:2:2 low bandwidth

  These codecs extend the existing DHxHD codecs by supporting
  unlimited resolution images.

  PLEASE NOTE: Avid's code requires CPUs supporting SSE 4.1. This
  means that DNxHR support is not available on Generation III and
  earlier Baselight systems.

Bug Fixes Since Baselight 4.4.7170
==================================

* Changes to ISIS mounts now correctly update cloud media [bug 30665]

* Fixed an issue where long QuickTime and MP4 files could take a long
  time to open. Particularly affected highly compressed H264 files
  [bug 30654]

* Fixed reading some DNxHD MXF files which reported "Unsupported
  flavour of DNxHD" [bug 30678]

* Fixed potential crash in Stereo Grade picking when stereo colour
  match was active in layer 0 [bug 30712]

* The scopes "Resolution when Playing" setting is no longer reset to
  Medium if you have previously set it to Low or Off [bug 26845]

* Fixed bug in conform which prevented multi-part R3D files (and
  sidecar RMD files) from being consolidated correctly [bug 30737]

* Fixed bug which allowed background services to create very large log
  files [bug 30613]

* fl-diag and fl-config-validate now detect and report duplicated
  volume names in volume.cfg [bug 30707]

* Fixed a shape issue where the "Find Stereo Correspondence" tool was
  failing with an active stereo colour match in layer 0 [bug 30713]

* Fixed problem with stereograde zero convergence point picks
  accumulating results from previous picks [bug 30767]

* Fixed a crash that could occur when rendering ProRes to Quicktime
  files on Linux [bug 30542]

* Fixed endless logging loop in flfsd (tcp: max = ...) [bug 30780]

* Fix problem with communications with FilmLight Framestore display
  hardware [bug 29947]

* Fixed issue in bl-config-video sending commands to FilmLight DVI2SDI 
  & framestore hardware [bug 29947]

* Fixed crash when resetting Button Action Slots in Chalk [bug 30719]

* Baselight's scene load time has been improved considerably, for very
  large scenes [bug 30446]

* Fixed error in rendering stereo scenes when they contained both 
  multiple track stacks and stereo strip stacks [bug 30787]

* Fixed Balance Exposure button moving cursor onto image when turning
  off [bug 30874]

* Fixed the default DCP title to be the scene name excluding job folders
  [bug 30201]

* XDCAM 422 encoded movies now write the same values to the MPEG2
  aspect ratio field that Sony XDCAM devices do [bug 30337]

* Fixed an flfsd assertion error (bad fileid) triggered by bad data
  [bug 30553]

* Errors caused by writing images to an unsupported resolution now
  correctly fail a render [bug 30920]

* Consolidate no longer reduces the number of frames it copies in
  situations where the Handles information in Shots View indicates
  that there are not enough frames on disk [bug 30794]

* Fixed incorrect automatic colour space assignment for Sony MXF files
  [bug 30938]

* Creation of invalid DCPs with uneven numbers of audio channels is
  now prevented [bug 29033]

* The default GOP size for H264 encoded QuickTime files rendered on
  Linux has been reduced from 250 to 64. This improves playback of
  these files in QuickTime Player on Windows [bug 29315]

* Fixed error introduced with SSD support causing dpm diagnostics to
  fail on early Gen I & Gen II machine equipped with 3ware 9500 or
  9550 RAID controllers [bug 30959]

* Fixed bug which caused the Baselight installer to fail due to AJA
  kernel module being in use [bug 30418]

* Added support for NVIDIA 346.35 driver.

* Fixed bl-genedl tool [bug 31013]

--------------------------------------------------------------------------

Baselight Release 4.4.7170 (2015-01-12)

New Features Since Baselight 4.4.7153
=====================================

* The bl-dvs-upgrade script can now be used on systems with Atomix LT
  cards. The DVS firmware & SDK has also been updated to the latest
  stable revision.

* Baselight disk-cache loading perfomance has been improved for very
  big caches. In addition, the cache load progress is shown in the
  Baselight splash screen [bug 13891]

* Added fl-queuetool for command-line inspection and modification of
  the Operations Queue [bug 30564]

Bug Fixes Since Baselight 4.4.7153
==================================

* Blur button for Layer 0 is now enabled on Blackboard 2 & Slate desks
  [bug 30312]

* A conform bug was causing the wrong movie to be selected when there
  were several alternatives with the same name but at a different
  filesystem path available [bug 30439]

* Fixed incorrect marks when splitting some strips (e.g. Text, Bars)
  [bug 30561]

* Fixed issue with saving cursor settings in a scene when the name of
  the Viewing Format contains unusual characters [bug 25278]

* Fixed an issue with 'Import EDL' which after selecting an XML file
  would fail when browsing for a subsequent file [bug 29828]

* Fixed empty dialog issue when attempting to duplicate masks and
  burnins in the Formats window [bug 30371]

* Fixed reading DNx444 MXF files from ARRI ALEXA [bug 30617]

* Fixed the 'blgwcspace' value in BLG files being incorrectly set. It
  is now set to the working colour space of the scene being exported
  from [bug 29444]

* fl-diag now no longer reports an error message when checking DVS
  fimware version [bug 30631]

* The Machine Control edit mode now defaults to auto-edit, which is
  more reliable and used on all modern VTRs [bug 28541]

* In some cases, VTRE operations would stall whilst locating. These
  have been found and fixed [bug 28327, 29288]

* The vtre-server now line-buffers its log output, so it can be
  monitored in real-time with "tail -f" [bug 26846]

* Fixed potential "overwriting global function log() with array" crash
  in vtre-server [bug 29329]

* Baselight will now tell you if you have an unsupported %-escape in a
  ingest/playout filename template [bug 28268]

* Fixed issue with large 'fl-cp' and 'flux' operations consuming
  resources and appearing to 'hang' [bug 30610]

* Fixed issue that was causing conform to fail if a new search directory
  was selected whilst a conform attempt was in progress [bug 29889]

--------------------------------------------------------------------------

Baselight Release 4.4.7153 (2014-12-19)

New Features Since Baselight 4.4.7137
=====================================

* Film Grade now has a neutral exposure balancing function. When the
  Balance Exposure button is pressed, picking a colour (or an area of
  colours) from the image will change the Exposure to make that colour
  neutral [bug 30487]

* Added support for ARRIRAW files from Alexa 65 camera (using
  Baselight decode only) [bug 30292]

* Scene Detect now has a Pixel Threshold slider. This adjusts the
  level of difference between corresponding pixels in adjacent frames
  which is necessary in order for the pixels to be counted as
  different. This can be useful on low-contrast material [bug 30442]

* When using the filter button in a browser, the filter text is now
  selected for text entry, saving you a click [bug 18010]

* The scroller buttons shown when tabs do not fit in a window now
  scroll the tabs left and right continually while the button is
  pressed [bug 30425]

Bug Fixes Since Baselight 4.4.7137
==================================

* Prevented custom colour spaces containing errors from causing
  crashes [bug 30455]

* Fixed Smart Dissolve to preserve strip caching and bypass states on
  both sides of the dissolve [bug 30461]

* Fixed right-click in the area below the last entry in a text list
  (e.g. on Jobs Manager) [bug 30428]

* Fixed crash when using a Tangent Element panel [bug 30364]

* Fixed bug which may have prevented picking on the image when a scene
  was initially opened [bug 30492]

* Fixed crash when enabling Anaglyph or Interlaced stereo display
  modes on Baselight FOUR/EIGHT systems using AJA Kona 4 display
  hardware [bug 30382]

* Fixed initialisation of Kona 4 SDI outputs when switching between
  between HD/2K, stereo HD/2K and 4K display modes [bug 30436]

* Fixed 12-bit stereo SDI output support on systems with AJA Kona 4
  display hardware [bug 30448]

* Fixed an issue where MXF OpAtom files written by Avid could not be
  read [bug 30472]

* Improved handling of conflicts between user/host/site preferences
  for control panels, user preferences now override host/site
  preferences [bugs 29660, 30432]

* Fixed render failure "Render swaps 200 tiles: only 100 tiles may be
  swapped" [bug 28314]

--------------------------------------------------------------------------

Baselight Release 4.4.7137 (2014-12-15)

New Features Since Baselight 4.4.7079
=====================================

* Updated to ARRI SDK v4.6. This adds support for the "ADA-5 SW"
  DeBayer Mode for ARRIRAW files.

* Added 32x playback speed option [bug 28785]

* Added support for Canon LUT formats.

* Added support for reading Panasonic Varicam VRW files [bug 28919]

* Added 'clip' option to Reference strips when used to reference a
  matte [bug 29965]

* Avid ISIS workspaces mounted on a Baselight system are now made
  available as Cloud Media [bug 27852]

* Blackboard Stack Manager can now access more than 5 Inside/Outside
  operators by holding <Ctrl> [bug 22737]

* A warning is now presented in the render UI when creating a DCP
  with a non-standard framerate [bug 28528]

* Digital Cinema Packages (DCP) can now be created either using the
  current SMPTE standard, or the older Interop standard. When creating
  a SMPTE package, the audio channel format label used can be
  configured in the codec parameters dialog [bug 28410]

* The version label used when creating DCPs can now be configured in
  Scene Settings under the Metadata tab [bug 29045]

* Added support for reading and writing OpenEXR files using DCT
  compression options.

* Updated to RED SDK v5.2. This addresses some issues in earlier SDK
  releases, and adds support for monochrome clips on RED Rocket-X.
  Updated RED Rocket-X firmware is included.

* 'Grab Poster' now grabs a new poster frame for the (DBS) shot being
  previewed when used with the 'View' key held down [bug 11645]

* Added support for Codex Action Cam RAW (.cdx) files [bug 29565]

Bug Fixes Since Baselight 4.4.7079
==================================

* Fixed renderer crash "m_pPhysical != __null" [bug 20611]

* Fixed crash changing Truelight on cursor [bug 26515]

* Fixed an issue where the frame rate calculation of some QuickTime
  files was slightly off on Mac [bug 29371]

* Fixed some issues with using apply onto source stack with dissolves
  [bugs 29319, 29038]

* Fixed TechGrade's starting contrast being 2.0 - it is now 1.0, a
  value which means that TechGrade's default values do not affect the
  image at all [bug 29349]

* Fixed problems editing long text in short text fields, notably in
  the Render View [bug 29221]

* Added progress panel when creating a new job [bug 29395]

* On a single-screen system, full screen mode now only hides the
  cursor until the mouse moves [bug 29466]

* The point tracker can now track cached material [bug 28095]

* Added an option 'show input' in the tracker, which determines
  whether Display View shows the tracker's input image or its output
  [bug 28714]

* Fixed errors rendering to movies containing '@' in their path or
  filename [bug 29512]

* Update xfs_repair to upstream version 3.2.1 [bug 28793]

* Fixed pfs-verify 'bad fsid in nfs handle' assertion [bug 29391]

* Consolidate now uses the cursor's proxy resolution, to fix issues
  when working with proxy-resolution material [bug 29408]

* Improved the error message reported when QuickTime movies fail to
  open on Linux [bug 29485]

* Updated the tooltip for the h.264 Quantizer parameter on Linux to
  reflect the actual default value [bug 29599]

* Fixed Consolidate of reversed sequences [bug 29634]

* Fixed crash when leaving an edited Six Vector [bug 29640]

* Conversion of grades to LUTs now forces the cubes to be reloaded in
  the new Truelight strips. Existing Truelight strips which use cubes
  that have been overwritten can be updated using the Reload option in
  the Truelight UI [bug 27802]

* Fixed reading of AVID RGBPacked Codec QuickTime movies on Baselight
  Kompressor [bug 29710]

* Fixed occasional crash when dragging actions onto buttons in Chalk
  [bug 27576]

* Toggle off curve grade animation on removal of last keyframe 
  [bug 28071]

* Fixed crop rectangle position drawn on Sequence Browser [bug 29772]

* Layer/Track option is no longer shown on Render View when rendering
  to cache [bug 29779]

* Fixed problem with conform panel and search directory choices from
  previous attempts being intermixed [bug 29796]

* Don't attempt to use SDI output devices on Mac if no SDI Display
  licence present [bug 29809]

* Fixed incorrect colours from Sony RAW MXF when using proxy
  resolution decoding [bug 29832]

* Fixed licence diagnostic expiry calculation which could be a day
  short due to daylight saving time [bug 29866]

* Fixed crash when moving DBS with 'Try' button held down [bug 24928]

* Fixed failure to set AudioConverter priming info when rendering AAC
  audio via Kompressor [bug 29788]

* Fixed thumbnails for some Sony RAW MXF files [bug 29923]

* Fixed an issue where DCPs were written using SMPTE XML metadata but
  Interop tags in the MXF files [bug 28455]

* Fixed crash when using the Blackboard to navigate around the 
  Layer View [bug 26127]

* Fixed behaviour of View 5 and View 6 when there are inactive tracks
  higher up the timeline [bugs 29933, 29560]

* Colour Space Journey View now indicates video LUTs applied on AJA
  card SDI output [bug 30121]

* Conforming 25@50 fps material could fail when an event has a
  timecode but no end timecode, and a speed of 0 [bug 30145]

* Conforming from a volume that is not the default would result in
  strips not having a %C container prefix [bug 30154]

* A race condition in the file scanner could cause it to exit with
  SIGPIPE when scanning was complete [bug 30024]

* Flux now allows browsing media connected to a UI host of a Baselight
  TWO/FOUR/EIGHT system [bug 30172]

* You are now prompted for confirmation when deleting an EDL Import
  View setting [bug 30194]

* User group and supplemental groups were not being applied when file
  browsing and conform [bug 30198]

* Fixed failures when using media on a removable drive connected to n0
  (on a Baselight TWO) or io (on a Baselight FOUR/EIGHT) [bug 30199]

* On Flos 2.1 systems the user's path now has the Baselight bin
  directory before the Truelight one [bug 27293]

* Fixed issues with image files with long numbers (e.g. 11 digits)
  [bug 30212]

* Fixed poor behaviour of file scanner when it encounters non-image 
  files that look like a sequence [bug 30204]

* Fixed bl-conform --container [bug 28200]

* Fixed support for using the Quadro K600 as a UI card on Baselight
  ONE systems [bug 30173]

* Added support for using Quadro K620 as a UI card on Baselight ONE
  systems. Requires NVIDIA driver 340.32 or later [bug 30265]

* Added support for using Quadro 410 as a UI card on Baselight ONE
  systems. Requires NVIDIA driver 304.117 or later [bug 30265]

* Fixed problem with SDI output synchronising when using stereo
  display modes via the AJA Kona 4 display card [bug 30153]

* Stereo HDMI output is now available when using the Stereo 1920x1080
  and Stereo 2048x1080 resolutions via the AJA Kona 4 display card
  [bug 30268]

* Fixed crash on switching to 9 up or showing version on the display
  [bug 30263]

* Fixed bl-config-xorg problem which prevented FLUX Store systems
  running FLOS 6.4 from performing rendering [bug 28317]

* Fixed fl-gpustresstest, fl-retracecountertest and fl-updowntest when
  running on FLOS 6.4 machines with NVIDIA driver 340.32 [bug 30079]

* Fixed fl-cp and fl-mv when using a subsequence or when renumbering
  [bug 30299]

* Fixed Soften strip insert action for Slate/Blackboard 2 [bug 28731]

* Fixed incorrect render of stereo scenes containing cached strips
  [bug 30336]

* Fixed crash when two desks are simultaneously marked as active in
  bl-prefs. An error message is now displayed [bug 29660]

* Fixed White Balance: Ignore File Values for Phantom.

* Fixed access to sequences on cloud media which are contained in
  resolution directories [bug 30340]

* Fixed Multi-Insert not adding %R [bug 30386]

* Fixed bug with grey border around the active image region when the
  image is zoomed/scaled down [bug 30193]

* Fixed crash at Baselight application startup on Linux when in a
  multiple monitor configuration [bug 30295]

* Fixed glitch in cursor rendering on the image display via AJA Kona 4
  display hardware [bug 30303]

* Fixed crash when inserting Audio Sequence via the Insert menu (no
  longer supported) [bug 29891]

* Fixed configuration of tablet buttons on Blackboard TWO and 2ONE
  hardware. The button nearest the tip of the pen is now equivalent to
  the middle mouse button, and the button further away from the tip is
  now equivalent to right mouse button [bug 27047]

* Fixed behaviour of worker service which would cause it to delete
  disk cache entries if a user's preferences had a larger disk cache
  size than the default setting [bug 30444]

* Fixed tape name reading in sequences without timecode [bug 30454]

* Fixed %W in conform to be case-insensitive [bug 30457]

* Fixed issues with flux and external drives [bug 30277]

--------------------------------------------------------------------------

Baselight Release 4.4.7079 (2014-11-11)

New Features Since Baselight 4.4.6964
=====================================

Consolidate
-----------

* Consolidate View allows the images and movies used by one or more
  scenes to be copied to a new location, optionally adding handles to
  image sequences, and optionally updating the scene(s) to use the new
  location. For example, consolidation can be used after conform to
  copy the necessary material onto local Baselight storage [bug 27407]

Conform
-------

* The conform process has been redesigned to be more efficient.

* Command line conform is supported via the bl-conform tool. The tool
  has a lot of help text built in, but its full use is documented in a
  separate FilmLight manual

Cloud Media
-----------

* Baselight can now access files stored on removable drives ("cloud
  media") connected to any Baselight system on the network, without
  having to configure shared volumes.

* Baselight can directly conform from EDLs and material on cloud
  media. Once the conform is complete, the Consolidate function can be
  used to copy only the used material [bug 27638]

Apple ProRes
------------

* Baselight now uses Apple's ProRes library for encoding and decoding
  Apple ProRes movies.

* QuickTime movies can now be written using the Apple ProRes XQ codec.

* Apple ProRes movies can now be decoded at half-resolution for speed
  (except where the movie has alpha channel data).

* Apple ProRes 4444 and Apple ProRes 4444 XQ QuickTime movies
  containing valid (non-opaque) alpha channel data are now indicated
  as such in the Sequence Browser.

AJA Display Output
------------------

* Baselight can now use AJA Kona 4 hardware for image display.

  The following video modes are supported via AJA hardware:
  - NTSC 720x486  at 29.97, 30 Hz
  - PAL  720x576  at 25 Hz
  - HD  1920x1080 at 23.976, 24, 25, 29.97, 30, 50, 50.94, 60 Hz
  - UHD 3840x2160 at 23.976, 24, 25, 29.97, 30, 50, 50.94, 60 Hz
  - DCI 2048x1080 at 23.976, 24, 25, 29.97, 30, 47.95, 48, 50, 59.94, 60 Hz
  - DCI 4096x2160 at 23.976, 24, 25, 29.97, 30, 47.95, 48, 50, 59.94, 60 Hz

  The SDI output can be configured as 1.5G SDI, 3G-SDI Level A or
  3G-SDI Level B.

  NOTE: 50, 59.94 and 60 Hz modes are only available using the Y'CbCr
  4:2:2 signal format, and are only available as progressive formats.

* Stereoscopic display via AJA display hardware is supported for HD
  1920x1080p/sF and DCI 2048x1080p display modes.

* Simultaneous HDMI and SDI output is available from the AJA Kona 4.
  The HDMI output can match the resolution of the SDI format, or can
  be configured as an HD downscale from the UltraHD or 4K signal being
  displayed via SDI.

* Audio output via SDI is supported on systems using AJA SDI display
  hardware. The following audio output options are available when routing
  audio via the AJA hardware:
  - 16 channels of audio are embedded in the SDI output
  - 16 channels of audio are available on the AES stereo outputs
    (as 8 stereo AES outputs)
  - 8 channels of audio are embedded in the HDMI output
  - 2 channels of analog audio available on phono connectors on the
    AJA SDI breakout box.

* The Baselight Setups editor has been modified to support editing
  settings for the AJA SDI output device. When running on a system
  with AJA SDI hardware, the Display tab will show a set of settings:

  - Resolution
      Allows you to choose the resolution of the display format.
  - Rate
      Allows you to choose the frame rate of the display format.
  - Signal Type
      Allows you to choose Progressive, PsF or Interlaced.
  - Speed
      For HD/UltraHD/DCI formats, this option allows you to specify
      the base SDI signal speed, choosing between 1.5G, 3G Level A and
      3G Level B.
  - Video Format
      Allows you to choose between RGB 4:4:4 or Y'CbCr 4:2:2.
  - Sync Source
      Allows you to choose internal or external sync.
  - HDMI Mode
      When the main SDI output format is 3840x2160 or 4096x2160, you
      can choose whether the HDMI output is the same resolution, or
      downscaled to HD/2K. The HDMI output will have the same frame
      rate as the SDI output however (it does not perform 2:3
      pulldown).
  - SDI Audio
      Allows you to choose to output audio via the SDI hardware (which
      also provides AES, HDMI and analog stereo output), or via the
      existing audio hardware (for example, via the USB optical audio
      interface or Hammerfall audio interface).

* Known issues with AJA Kona 4 SDI/HDMI output:
  - When using an UltraHD or DCI 4K display mode, and using the HDMI
    HD mode (which performs a downscale from UltraHD/4k to HD/DCI 2K),
    this currently only works when using a 4:2:2 SDI output. This will
    be fixed in a future release of Baselight.
  - SDI timecode output is not implemented yet.

* Please contact FilmLight support for details on upgrading your
  system to AJA Kona 4 display hardware.

* Please note that AJA Kona 4 SDI output requires an update to your
  Baselight licence.

DVI/HDMI/DisplayPort Output
---------------------------

* It is now possible to configure Baselight to use the DVI, HDMI or
  DisplayPort output on the main processing GPU to drive monitors or
  projectors.

  Baselight allows the resolution and refresh rate for the display to
  be selected in the Baselight Setups editor. These options are read
  dynamically from the attached display device.

  Note this option is not available on systems using FilmLight DVI2SDI
  or Framestore display hardware.

  This option requires NVIDIA driver 340.32 or later.

* "Primary Output Device":

  In the Baselight Setups editor, you can choose which display device
  to use on a per-setup basis. Most setups will use the "Default"
  device, which is governed by the "Default Display Device"
  preference.

  Available devices include:
    - AJA SDI display cards
    - FilmLight DVI2SDI or Framestore hardware
    - GPU DVI/HDMI/DisplayPort outputs

  This allows you to use SDI output for the majority of setups, but to
  switch to DVI/HDMI/DisplayPort on certain setups if required to
  drive a specific display device.

  On systems with AJA SDI hardware, AJA SDI is the default display
  device.

  On systems with FilmLight DVI2SDI or Framestore hardware, DVI2SDI or
  Framestore is the default display device.

* "Default Display Device" preference has been added to bl-prefs, in
  the Display->Output section. This allows you to choose the preferred
  image output mechanism.

  When a setup in the Baselight Setups editor is set to use the
  Default display device, Baselight

  There are the following options
  - Choose Automatically
      Allow Baselight to automatically determine the best display
      device to use for the image output. Baselight chooses in the
      following order:
      1. SDI hardware, if present
      2. FilmLight combiner/framestore, if present
      3. DVI/HDMI/DisplayPort from GPU
  - SDI (PCI Express/Thunderbolt)
      Default to using AJA SDI hardware via PCI Express if it is
      present.
  - FilmLight DVI2SDI/Framestore:
      Default to using FilmLight DVI2SDI/Framestore hardware, if it
      is present.
  - DVI/HDMI/DisplayPort from GPU:
       Default to use the DVI/HDMI/DisplayPort outputs from the main
       processing GPU.

  The default option is "Choose Automatically", which is the
  appropriate setting for the majority of systems.

R3D GPU Acceleration
--------------------

* R3D movies can now be decoded using the Baselight GPU. This is
  generally faster than using the CPU, and does not require RED Rocket
  hardware.

  GPU decoding of R3D movies requires
  1. An NVIDIA GPU which
    a. supports CUDA Compute capability 2.0 or higher
       (see http://developer.nvidia.com/cuda-gpus)
    b. has at least 3GB of RAM
  2. FilmLight OS 6.4 or later

  The GPU requirement means that this functionality is available on
  Generation V Baselight systems, or Generation IV systems with
  upgraded graphics cards. (Mac systems do not support GPU R3D
  decoding in Baselight at this time.)

  The "Decode" option on the R3D Params operator allows GPU decoding
  to be disabled, or to be chosen in preference to a RED Rocket.

  GPU decoding is not supported for scenes which use R3D Colour
  Science v2 "New Colour Science".

  When GPU decoding is available, the speed of CPU R3D decoding is
  impacted (just as it is when a RED Rocket card and driver are
  installed). A preference (under System/Render) allows GPU decoding
  to be disabled should you wish to continue using CPU decoding
  without a speed penalty.

Miscellaneous
-------------

* Support for 10-bit Y'CbCr 4:2:2 timeline cache.

  When dealing with the increased data rate and storage requirements
  of UltraHD at 59.94 or 60 Hz frame rates, it may be desirable to
  change the "Display and Timeline Cache" format in scene settings to
  use "10-bit Integer 4:2:2 Y'CbCr". This reduces the disk space, disk
  bandwidth and network bandwidth requirements for playing back
  UltraHD/60p material by 33%.

  UltraHD 50, 59.94 and 60Hz display modes use Y'CbCr 4:2:2 encoding,
  so there is no visual loss in quality when using this format.

  Selecting this format does not affect the chroma resolution when
  rendering to RGB or Y'CbCr 4:4:4 deliverable formats, as the image
  data will not be compressed to Y'CbCr 4:2:2 format when rendering to
  image/movie formats with higher chroma resolution.

* Updated to RED SDK v5.1. This addresses some issues in earlier SDK
  releases, and adds:
  - Support for Dragon Enhanced Blacks (D.E.B.) processing (not
    available on RED Rocket or RED Rocket X)
  - Low-pass filter metadata

* Added fl-vers and fl-service commands to Mac OS X

* Added ability to save the log for an operation [bug 28907]

* Automatic adjustment of the floating window option in stereograde
  now acts globally [bug 28990]

* Scrollable text items, for example on the right side of the Sequence
  Browser, can now be copied to the clipboard using a right-click
  menu [bug 29205]

* Added support for reading metadata for ARRIRAW files from Codex
  Vault XML files [bug 27374]

* When a render operation has multiple deliverables, Setup For Tape
  Playout now offers the choice of deliverable [bug 28824]

* When a scene has multiple deliverables, Setup For Rendered Scene now
  offers the choice of deliverable [bug 29284]

* Added bl-aja-upgrade tool for upgrading AJA Kona card firmware 
  [bug 29293]

* Added firmware version check for SDI diagnostic test [bug 29293]

* Add suport for 12-bit SDI output via Kona 4 for HD, UltraHD, DCI 2K
  and DCI 4K resolutions [bug 29369]

* In BLG Export, added additional 1/16, 1/32 and 1/64 proxy resolution
  options, to allow the creation of BLGs with much small file sizes.

* Baselight now requires 290.10 or later drivers for GPU rendering.
  If upgrading from 177.70, please use the latest Nvidia driver release
  from FilmLight [bug 29793]

Bug Fixes Since Baselight 4.4.6964
==================================

* Fixed bl-setups and bl-config-video on systems with FilmLight
  combiner, DVI2SDI or Framestore hardware [bug 28302]

* Fixed stereo display modes on FilmLight combiner, DVI2SDI and
  Framestore hardware [bug 28303]

* Fixed tearing on SDI output when using FilmLight combiner, DVI2SDI
  or framestore hardware [bug 28352]

* Fixed support for 3840x2160/50p video mode [bug 28774]

* Fixed crash in GPU renderer [bug 28019]

* Fixed bug that prevented using Truelight profiles on the cursor
  [bug 28621]

* Fixed support for DVI/HDMI/DisplayPort output on Baselight
  TWO/FOUR/EIGHT.

* Fixed dual-link 1.5G SDI support.

* Added support for 48p display modes at DCI 2K and DCI 4K resolutions
  on Linux.

* Added support for Dual 1920x1080 and Dual 2048x1080 stereo display
  modes, up to 4:4:4 30p and 4:2:2 60p [bug 27868]

* Fixed incorrect buffer capacity assertion in flfsd [bug 28891]

* Fixed bug in 59.94 conform from CMX3600 EDLs [bug 28806]

* Added support for NVIDIA driver 340.32 on systems with GTX 680 or
  GTX 780 GPUs [bug 28979]

* Fixed failure to recognise/read some DNxHD MXF movies [bug 28372]

* Changed Job Browser to indicate what product a scene was created
  with [bug 28837]

* Fixed issue where some error messages were truncated [bug 26889]

* Fixed scene detection failures when image/movie filenames contain
  unusual characters [bug 28986]

* Fixed behaviour of Colour Space Journey View when docked into a
  workspace [bug 29015]

* Fixed typo in Technical Manual pg_dumpall section [bug 27284]

* Fixed bl-conform to sanity check that the requested format exists
  [bug 28172]

* Fixed bug that showed a percentage on the 'Raw EDL' tab of the EDL
  Import panel [bug 28128]

* Fixed a bl-conform but that would not accept '.' characters in host
  names [bug 28179]

* Fixed the retrieval and display of scan statistics in the Baselight
  conform panel [bug 28129]

* Fixed error display for bl-conform when the required broker service
  is not available [bug 28198]

* Fixed default minimum conform percentage, raised from zero to 10
  percent. Can be overridden from the command line [bug 28159]

* Fixed problem with colour coding of access rights in the filesystem
  browser [bug 28407]

* Fixed problem causing sequences to be missing in browse results
  [bug 28393]

* Fixed problem using copy with sync option on raw frames for which 
  there is no internal writer available [bug 28953]

* Fixed license warning on FLUX Store systems [bug 29084]

* Select Missing Media now has a Cancel button [bug 28827]

* Fixed crash using AST file in Audio Sync [bug 29028]

* Fixed an issue preventing MXF files written by ASDCP from being
  read. Affects JPEG2000 and audio files used for e.g. DCPs
  [bug 29152]

* Reduced the number of partitions created when writing XDCAM MXFs.
  The large number of partitions previously created caused the file to
  open and read very slowly in Baselight [bug 29183]

* Fixed BLGs exported from stacks containing both layer blending and
  Truelight operators not containing the required cubes [bug 29216]

* Sony RAW Parameters are now initialised to use the Colour Primaries
  and Tone Curve which match the monitoring metadata in the MXF file
  [bug 28650]

* Fixed crash on Baselight Kompressor when /etc/hosts doesn't have
  configuration comments that are normally added by fl-config-master
  [bug 25949]

* Using a full-sensor-size format for Sony RAW media no longer fails
  with "Sequence Input Format is too large" [bug 29250]

* Support Quadro 600 card as a replacement for a GeForce 6200 to drive
  the Blackboard display on gen3 Baselight ONE systems running
  FilmlightOS 6.4 due to the GeForce 6200 driver crashing in this
  configuration [bug 29134]

* Fixed pfs-verify false positive warning "[file] has redundant sparse
  files" for zero-length round-robin file [bug 29252]

* Fixed incorrect black levels in the letterboxing area when rendering
  to ProRes [bug 29264]

* Fixed problem with Video grade lifting black when no parameters have
  been changed [bug 29196]

* When an AAF references the start of an image sequence in the FileName 
  column, this is turned into a descriptor for a likely sequence, and
  will be searched for when conforming [bug 29170]

* Fixed renderer crash on clusters ("Invalid internal buffer format")
  [bug 29008]

* Fixed upward shift when decoding some XDCAM MXF files, resulting in
  black lines at the bottom [bug 29325]

* Fixed flfsd tight retry loop (transmit failed: bad address) when an
  internally generated request was deleted prematurely [bug 29068]

* Fixed audio sync when playing 59.94fps scenes on a 29.97fps display
  devices [bug 29384]

* Fixed bug with Nvidia GPU Configuration diagnostic on systems with
  NVIDIA 340.32 driver [bug 29389]

* Fixed bug that could cause more than the correct number of conforms
  to be attempted when using 'Timecode location = Header' [bug 29374]

* Fixed crash on startup when running on a machine with NVIDIA 340.32
  drivers and FilmLight DVI2SDI or Framestore hardware [bug 29417]

* Fixed queued render failures with "Cannot fetch unparsed string"
  errors [bug 28693]

* Fix playback errors on systems with DVI2SDI or Framestore combiners
  [bug 29430]

* Fixed the export resolution dropdown doing nothing in the BLG Export
  dialog [bug 29372]

* Fixed problem with configuring "Sony 4K" and related video modes when
  using FilmLight DVI2SDI or Framestore hardware [bug 29623]

* Fixed flfsd assertion '((_length + 3) & ~3) <= capacity' [bug 29636]

* Fixed flfsd dropping reply packet when tcp connection is temporarily
  unavailable [bug 29643]

* Fixed problem with conforming rendered media [bug 29615]

* Fixed bad colours of "ph7" Phantom cine files. Existing scenes are
  unchanged; to update the behaviour of an existing scene, use the
  Update Sequence Behaviour button [bug 29697]

* Fixed an issue where some very old Baselight scenes could not be
  opened [bug 29765]

* Fixed problem with corrupt output via FilmLight Framestore hardware
  when using "Sony 4K" or "DCI 4096x2160 24p" video modes [bug 29782]

* Fixed artefacts in highlights in some Phantom cine files [bug 29839]

* Fixed problems with trackball sensitivity on newer Blackboard 2
  hardware which was causing text boxes to occasionally undo typing
  [bug 29410]

* Fixed issue with Blackboard 2 jog shuttle sensitivity on newer hardware
  which could occasionally cause playback to stop [bug 29746]

* Fixed problem with genlock at 23.976 and 29.97 frame rates on older GPUs 
  (8800/9800GT) when using newer NVIDIA drivers (290.10, 304.117 and newer)
  [bug 26598]

* Fixed a problem that could cause the movie reader to crash when reading 
  DCPs [bug 28999]

* Added check to installer to valid GPU hardware configuration before 
  allowing Baselight to install [bug 26598]

* Fix problem with communications with FilmLight Framestore display
  hardware [bug 29947]

* Disable PAT/MTRR Nvidia config patch for Baselight ONE systems using
  PCI Express UI GPUs [bug 26598]

* Fixed installer test on Gen 3 Baselight ONE with Quadro K600 
  [bug 26598]

--------------------------------------------------------------------------

Baselight Release 4.4.6964 (2014-09-08)

Bug Fixes Since Baselight 4.4.6933
==================================

* Fixed detection of Blackboard on Baselight ONE systems running
  FLOS 6.4 [bug 29004]

* Fixed a problem that the hotfix script would produce incorrect
  warnings on a Baselight ONE during installation [bug 29042]

* Fixed queued renders not using the GPU in some circumstances
  [bug 29035]

* Fixed bug which could cause some stacks to be incorrectly cached
  [bug 29174]

* Fixed bug which could cause some stacks to be incorrectly cached
  [bug 29174]

--------------------------------------------------------------------------

Baselight Release 4.4.6933 (2014-08-22)

New Features Since Baselight 4.4.6871
=====================================

* Added new substitutions to Gallery Autoloads, allowing more
  flexibility for those users who use folders to organise their work.
  The new substitutions are %1F, %2F etc up to %9F (F stands for
  "Folder" here). For example, say your project hierarchy is
  typically:

     <host>:<customer>:<colourist>:<date>:<scene>

  and you wish to have a fresh gallery for every combination of
  customer, colourist and date. In this situation, an autoload
  template of:

    %J_%1F_%2F

  would be suitable [bug 28554]

Bug Fixes Since Baselight 4.4.6871
==================================

* Fixed delay in starting playback when scene is set to 16-bit
  floating point caching [bug 28378]

* Fixed bug in Gallery where thumbnails could disappear when
  re-loading the gallery, if the input image path didn't contain a
  resolution directory [bug 22959]

* Fixed Y-Y curve grade on DNx444 movies [bug 28540]

* JPEG 2000 files without specified colourspace but with subsampling
  are now treated as YUV rather than RGB [bug 28534]

* Turning the jog wheel on a Blackboard 2 will now stop playback when
  in frame-step mode [bug 28512]

* Fix problem with configuring Baselight ONE systems to use DVI/HDMI
  output from main processing GPU on FLOS 6.4 [bug 28595]

* Fix problem that causes intermittently Baselight to fail to launch
  on Baselight ONE systems running FLOS 6.4 [bug 27501]

* Fix problem with selecting certain custom video modes added via the
  Available Video Modes option in bl-prefs [bug 28593]

* Fixed colour grading operations inside Layer 0 being incorrectly
  burnt into the "Source" layer of BLG EXR files [bug 28564]

* Fixed the "Source" layer of BLG EXR files not having the correct
  mapping applied when the input format was a different resolution to
  the working format [bug 28564]

* Fixed the "Source" layer of BLG EXR files sometimes having an input
  colour space to viewing colour space conversion incorrectly applied
  [bug 28564]

* Fixed BLG EXR files having the incorrect resolution (and sometimes
  aspect ratio) when the cursor viewing format was different to the
  scene working format [bug 28564]

* Fixed the Input Colour Space not being set in the Sequence when
  importing BLG EXRs onto the Timeline [bug 28564]

* For some image formats, Baselight is unable to write proxies (an
  example is ARRIRAW). This meant that if such a shot was grabbed to
  gallery and the original media went off-line, you would get an X in
  the gallery. This is no longer the case - the Gallery will now fall
  back to auto thumbnail generation in these cases [bug 25480]

* Fixed issue where filtered columns in file browsers could vanish
  when changing directories [bug 28603]

* Set hfsplus umask=0 to allow writing to Mac-formatted USB drives
  [bug 28037]

* Fixed fl-fsr 'file placed out of sequence' warnings caused by xfs
  driver failing to allocate from known free space [bug 28383]

* Fixed conform issue affecting fractional frame rates [bug 28648]

* Added support for %X (tape name as file name) and %Y (clip name as
  file name) in conform to aid prefiltering of sequences, useful in
  some workflows [bug 28648]

* Added support for filtering by ClipName in filename or path when
  using FCP XML [bug 28681]

* Fixed bug which could result in incorrect cache status reporting
  [bug 28676]

* Fixed failure to open scenes in bl-render after closing a scene
  using a scene-local output format [bug 28728]

* Resetting the cache on clusters was silently failing as a side
  effect of support for SSD's [bug 28730]

* Fixed crash when adjusting pivot points in Film Grade or Video Grade
  [bug 28754]

* Disable touch sensitivity on Wacom tablets [bug 28281]

* Add '-cache' option to fl-setup-pfs and fl-setup-3ware to limit
  actions to SSD-based array only [bug 28746]

* Add fl-check-product-version script for use by installer [bug 27520]

* Skip known SAN volumes when scanning for removable volumes at boot
  time [bug 28747]

* Disable network interfaces which are marked as 'off' in cloud.cfg
  [bug 28679]

* Added LSI RAID controller support to dpm.

* Fixed bug in 59.94 conform from CMX3600 EDLs [bug 28806]

* Fixed magenta stripes on letterboxed renders for certain movie
  formats [bug 28673]

* Fixed artefacts in highlights in some Phantom cine files [bug 28917]

* Fixed Phantom cine decoding which was slightly too dark. Note that
  this change only affects newly-inserted sequences; existing
  sequences are unchanged unless you use the Update Sequence Behaviour
  button [bug 28917]

* Reduced flfsd (pfs2 filesystem daemon) virtual memory consumption
  [bug 27953]

* Fixed ARRI Decode of ARRIRAW files on FilmLight OS 2.1 and Mac OS X
  [bug 28573]

* Fixed crash when using Cuts View Selection playback [bug 28945]

* Fixed a problem on systems other than a Baselight ONE that caused
  configuration files to not be properly linked [bug 28810]

--------------------------------------------------------------------------

Baselight Release 4.4.6871 (2014-07-16)

New Features Since Baselight 4.4.6814
=====================================

* Added LUT export formats Autodesk 1D half float (for Flame 2015),
  Colorfront 1D and Colorfront 3D.

* Added bl-reset-cache '-hardssd' option which can improve performance
  of the Baselight cache when it is hosted on a Solid State Drive
  array by secure-erasing the raw drives, hence restoring them to
  their factory state [bug 28009]

* Improved the information shown on colour space menus:
  - tooltips are now presented to describe each space
  - a warning icon indicates when a space is not ideal for use as a
    working/grading colour space
  - Cursor View warns when the viewing colour space does not match the
    full/legal setting of the Combiner SDI Output (when no Truelight
    is applied) [bug 28114]

Bug Fixes Since Baselight 4.4.6814
==================================

* Fixed occasional bright pixels in dark areas of Phantom cine images
  [bug 28164]

* Improved error message when trying to render FFMpeg ProRes at a
  resolution whose width and/or height is not even [bug 27512]

* Data in the timeline cache is now used where possible for RGB
  renders, when the cache has enough precision and the render settings
  match those of the cursor used to fill the cache [bug 20666]

* Scenes with long folder/scene names can now be opened as galleries
  [bug 26299]

* Fixed decode of ALEXA Open Gate material using ARRI SDK [bug 28254]

* Fixed a random crash on exit issue [bug 27900]

* Fixed Input Colour Space setting on conformed sequence, when Scene
  Setting specifies a named colour space [bug 28283]

* Fixed crash in EDL Import, which occurred when loading DLEDLs
  containing "DLEDL: PATH:" lines lying after an invalid CMX event
  [bug 22214]

* Fix for crash after deleting buttons in Chalk then switching layouts
  [bug 28165]

* Fixed issue where Slate screen updates could lag behind UI display
  [bug 28223]

* Fixed glitching playback when pressing "Ctrl" on Blackboard 2 or
  Slate desks [bug 27850]

* Fixed crash when driving Blackboard 2 from graphics card which does 
  not support glXSwapIntervalEXT [bug 28245]

* Improved startup time of many applications and tools when there are
  many Truelight profiles on the system [bug 28326]

* Improved appearance of tooltips [bug 28156]

* Fixed reading of some Avid legacy format MXF files [bug 28372]

* Added support for reading Apple ProRes 4444 XQ QuickTime movies on
  Linux [bug 28344]

* The About Baselight dialog now shows the current user [bug 28085]

* Fixed 'connection timeout waiting for nodes' error due to interrupt
  routing issues on Generation IV hardware running Flos 6.4. NOTE:
  this needs a full reboot of all nodes in a Baselight FOUR/EIGHT
  after installation [bug 27855]

* On Flos 6.4 systems the user's path now has the Baselight bin
  directory before the Truelight one [bug 27293]

* Fixed NVIDIA driver version diagnostic on systems without a Myricom
  NIC [bug 28131]

* Fixed crash on mouse left button click in the layer view [bug 28180]

* The strip name can no longer be edited when multiple strips with
  different names are selected [bug 22863]

* Fixed incorrect area picks in all keyers [bug 28355]

* Fixed playback stall on Baselight EIGHT [Bug 28382]

* Log DPX files are no longer assigned ADX Log colour space by default
  [bug 28427]

* Fixed crash report setup on new systems [bug 28438]

--------------------------------------------------------------------------

Baselight Release 4.4.6814 (2014-06-11)

Bug Fixes Since Baselight 4.4.6806
==================================

* Fix for issues where text entry becomes impossible due to phantom
  haptic encoder movement on Blackboard 2 desks [bug 24047]

* Fixed crash reading DNxHD QuickTime movies on Linux [bug 28141]

* Fixed green letterbox/pillarbox areas when rendering through a
  mapping to some movie formats [bug 28140]

--------------------------------------------------------------------------

Baselight Release 4.4.6806 (2014-06-06)

New Features Since Baselight 4.4.6767
=====================================

* Sequence Browser now allows Mark In/Out using Timecode or Timecode 2
  [bug 16240]

* Changed behaviour of Render Layer/Track options. "Input Only" now
  renders the input sequence, with no colour space conversion to the
  sequence Output Format, and no Grade Result Colour Space. "Layer 0
  Only" preserves the previous behaviour [bug 27121]

* Improved decode of Phantom cine files (existing sequences created in
  older Baselight releases are unaffected; these changes only affect
  newly-added sequences):
  - Added support for Flex4K
  - Fixed incorrect colours on some files
  - Improved colour
  - Added repair of bad pixels.

* Added "Soft Clip To Full" Video LUT option on Render View, to give a
  soft rolloff of values above 1.0 and below 0.0 [bug 25952]

* Added S-Gamut3, S-Gamut3.Cine and S-Log3 options to Sony RAW Params
  [bug 26423]

Bug Fixes Since Baselight 4.4.6767
==================================

* When loading a scene, the progress bar no longer goes from 0-100%
  twice [bug 27745]

* Improved the speed of submitting certain scenes for rendering, when
  the database server is using PostgreSQL 8.2 or later [bug 27693]

* Improved error message when an ARRIRAW sequence is replaced with
  a non-ARRIRAW sequence [bug 27778]

* Fixed failures in tracking when a shot's Comment metadata contains a
  string that can be interpreted as an escape sequence (e.g. "\005")
  [bug 27731]

* The render panel now only allows selection of audio sample rates
  that are actually supported by the corresponding codec [bug 27660]

* Reduced uneven playback behaviour of movies [bug 27551]

* Removed incorrect error message when opening DNx444 movies in
  QuickTime containers on Linux [bug 27437]

* Prevent nodemon from producing too much console output [bug 27575]

* Add support in flux for copying to target directories that contain a
  % character [bug 27747]

* Disabled support for writing the DNx100 codec to MXF container since
  the encoder is too unstable [bug 25918]

* Reduced time taken to update Slate desk screens over USB [bug 27773]

* Fixed crash with deleting a blend layer via the layer manager 
  [bug 27812]

* Fixed bug where "New Shape" button on Slate desks failed to respond
  to being pressed [bug 27684]

* Added Slate desk support for Matte Merge and added "Matte Merge"
  button to "Stack Manager" section of Chalk for Slate [bug 27827]

* Fixed brightness of Six Vector keyer mode display [bug 27871]

* Fixed crash when exporting a CMX EDL with pulldown [bug 27632]

* 'flint' parallel barrier driver can now use a shared interrupt
  [bug 27855]

* Slate connection diagnostic now returns a more meaningful message on
  failure [bug 27723]

* Fixed slow playback performance on multinode systems when using DPX
  files that have large headers [bug 27876]

* Removed access to Blackboard 2 specific buttons in Chalk for Slate
  [bug 27547]

* Fixed crash that could occur when rendering DNxHD to Avid OP-Atom
  MXF files [bug 27892]

* Fixed green mask area when rendering with Hard Black mask to most
  movie codecs [bug 27917]

* Fixed unwanted switch to Movies Video+Audio when changing movie file
  type on Render View [bug 27672]

* Fixed Colour Space Journey when the stack only contains one operator
  (e.g. a Blank) [bug 27933]

* Fixed initial values of Scene Settings set when upgrading scenes,
  which could cause changes in scene rendering [bug 27929]

* Updated xfs-repair to version 3.2.0 [bug 27642]

* Fix for crash when undo-ing changes involving deleted Custom Buttons
  in Chalk [Bug 26931]

* Fixed Low-res proxy option on Sequence Browser [bug 27995]

* Fixed crash due to 'unimplemented format conversion' when writing
  QuickTimes on Linux [bug 28035]

* Fixed incorrect orientation of some DPX files (e.g. from Flame 2015)
  [bug 28030]

* Fixed flio diagnostic utility 'no space left on device' error due to
  a full xfs allocation group [bug 27805]

* Fixed render failure using symbolic link option [bug 28084]

* Fixed bug with cursor not being drawn on the SDI output when using
  "Sony 4K" or "DCI 4096x2160" video modes [bug 27967]

* Fixed occasional hang in Sequence Browser when scanning several
  folders of movies [bug 28093]

--------------------------------------------------------------------------

Baselight Release 4.4.6767 (2014-05-16)

New Features Since Baselight 4.4.6757
=====================================

* Changed the R3D Params operator to offer general Linear output in
  any R3D Output Colour Space, in addition to the existing ACES Linear
  option. Both the Linear options cause the R3D decode to generate
  true linear floating-point images [bug 27848]

Bug Fixes Since Baselight 4.4.6757
==================================

* Fixed slow reading of some MXF files [bug 27832]

* Reading QuickTime movies with multiple sample descriptions no
  longer generates an error when opening the file [bug 27786]

* Improved speed of rendering movies to ISIS filesystems mounted on
  Linux [bug 27864]

--------------------------------------------------------------------------

Baselight Release 4.4.6757 (2014-05-09)

Bug Fixes Since Baselight 4.4.6753
==================================

* Fixed changes in behaviour when splitting or pasting a Dolby Vision,
  Image Transform Settings or Colour Space operator [bug 27769]

* Updated LUT generation from grades to handle colour space
  conversions within the stack [bug 27749]

* Fixed Remote Rendering in bl-render [bug 27728]

* Fixed rejection of some MXF files as "unindexed" [bug 27803]

--------------------------------------------------------------------------

Baselight Release 4.4.6753 (2014-05-07)

New Features Since Baselight 4.4.6689
=====================================

Chalk for Slate
---------------

* Chalk for Slate enables users to customise button layouts for Slate
  desks. Users can select between preset button layouts, make their
  own unique layouts and edit functionality of individual buttons.

  Each main Layout is comprised of one Home Layout and multiple Slate
  Layouts.

  The Home Layout offers access to per-strip buttons (e.g. Gang and
  Reset operators) and is used as a conduit to access the various
  Slate Layouts.

  Slate Layouts are used as a container for any type of button and a
  number of commonly used Slate Layout presets are provided: E.g. DBS,
  Keypad, Layers, Transport, etc.

  Layouts can be exported to a USB stick for easy transferring between
  facilities.

BLG and Baselight Editions
--------------------------

* Re-enabled "Update Avid AAF with Baselight Grades" and "Update FCP
  XML with Baselight Grades" options in the EDL Export panel, now that
  4.4 builds of Baselight for Avid and Baselight for FCP are available
  for testing.

* Added "Lock Grade" option to BLG Export, as well as to the "Update
  Avid AAF with Baselight Grade" and "Update FCP XML with Baselight
  Grades" EDL Export options. When set to "Yes", then any exported
  grades loaded into any of the Baselight Editions (Baselight for Nuke
  etc) will have the Layer Manager drop-down disabled and set to Layer
  0. This will allow the user to change the input/output colour space
  processing, but not examine or change the grade layers themselves.
  However, it should be noted that switching on this option will not
  prevent grades being visible when loaded into full Baselight.

Colour Spaces
-------------

* Added generalised colour space support to "Update Avid AAF with
  Baselight Grades" and "Update FCP XML with Baselight Grades",
  allowing the user whether or not to include Input Colour Spaces, the
  Viewing Colour Space or current Truelight setting in the Baselight
  grades written to the AAF/XML.

* Added generalised colour space support to the "Apply Baselight
  Grades" setting in the EDL Import view. Now, when Baselight Grades
  are detected in an EDL, a setting appears to the right of the Yes/No
  dropdown, allowing the user to specify which colour space settings
  (Sequence Input Colour Spaces, Cursor Viewing Colour Space, Cursor
  Truelight Settings) are to be applied. Having them all on should
  make the grade look identical to who it looked in the exported
  Avid/FCP/Baselight, so long as the media is the same. If the AAF/XML
  was exported from an NLE, then it is possible that each grade could
  have different Working Colour Spaces, Viewing Colour Spaces - in
  this situation, Baselight works out the most common value for each
  setting and assigns that, adding per-event warnings for those events
  whose values don't match.

* A new option on Scene Settings allows the Display Rendering
  Transform to apply only on conversions from scene-referred to
  display-referred colour spaces, having no effect for the reverse
  display-to-scene conversion. This is initially enabled for new
  scenes (via Setups) [bug 27295]

* The Scene Settings and Setups default Input Colour Space control now
  allows a specific colour space to be chosen [bug 26665]

* Added support for Display Rendering Transforms defined using
  functions instead of cubes [bug 27436]

* New Colour Space Journey View shows details of all colour space
  conversions in the current cursor's stack, and the colour space at
  the current cursor position [bug 27635]

File Formats and Codecs
-----------------------

* Unencrypted, non-stereoscopic DCP packages can now be created. The
  option lists as 'Digital Cinema Package' under the Movies Video Only
  and Movies Video+Audio categories in the render panel. Package
  title, creator and issuer are read from the scene settings metadata.
  Bitrates from 250 Mbit/s to 500 Mbit/s are supported by adjusting
  the codec parameters. Maximum reel file sizes can also be set [bug
  16821]

* Unencrypted, non-stereoscopic DCP packages can now be opened and
  read. The ASSETMAP file in the DCP directory is treated as if it was
  a movie file

* Added support for reading and writing unenctryped, non-stereoscopic
  DCI compliant MXF files containing JPEG2000 compressed frames.

* Updated to RED SDK v5.0. This addresses some issues in earlier SDK
  releases, and adds:
  - DRAGONcolor color space
  - REDgamma4 gamma option
  - Updated RED Rocket-X firmware and driver

* Added support for reading 16-bit planar TIFF images.

* Writing of compressed file formats now makes better use of available
  system resources, which improves speed [bug 24875]

* Timecodes in MXF files are now indicated with their correct frame
  rate in the Sequence Browser [bug 27257]

* The fabricated Timecode 2 from Phantom cine files now uses the same
  fps as the embedded per-frame timecode [bug 27375]

* Added support for reading DNxHD QuickTime movies with mixed codec
  settings. Files with more than one setting are shown as being
  compressed using the setting of the first frame, with an appended
  '+' to indicate that mixed settings occur in the file [bug 26652]

Miscellaneous
-------------

* fl-code now supports -m option to show metadata for image files as
  well as for movies [bug 27526]

Bug Fixes Since Baselight 4.4.6689
==================================

* Fixed crash in "Update Avid AAF with Baselight Grades" EDL Export
  option, which could occur when the "Input Filename" was an AAF which
  didn't match the conformed timeline [bug 26286]

* Fixed bug in EDL Import which could cause switching between multiple
  conform tabs to be slower and use more memory.

* Fixed bug in EDL Import in which the count of events containing was
  occasionally wrong.

* Fixed bug in EDL Export where removing strips based on categories
  didn't work for "Update Avid AAF with Baselight Grades".

* In EDL Import view, removed a now-spurious warning ("None of the
  possible formats for this event match the preferred input colour
  space.") which would appearing during conform using a working colour
  space which is different from the input formats'.

* Fixed typo in Technical Manual pg_dumpall section [bug 27284]

* Fixed excessive PostgreSQL warnings in log files [bug 27340]

* Fixed issue with database permissions [bug 27332]

* Fixed stereo rendering problem where upper eye track was failing to
  render correctly [bug 27406]

* Fixed EDL export missing the left eye in single stack stereo scenes
  [bug 27393]

* Allowed the scene compare to terminate when it's running in the 
  background if another operation has started [bug 27242]

* Rendering speed of ProRes encoded movies is now improved on Linux
  [bug 19384]

* When changing movie file type when rendering with audio, the audio
  codec is no longer left in an invalid state [bug 27109]

* Fixed crash when applying to a paste protected stack, with a matte
  [bug 27287]

* Remove hotfix which replaces /etc/mtab with a symlink to
  /proc/mounts because this breaks CXFS bind mounts. Modify fuse
  library to disable /etc/mtab updates since it uses invalid mount
  options which cause /pfs automount to fail [bug 27019]

* Fixed crash in Sequence Browser when using List Keycode option with
  sequences with invalid keycode [bug 27497]

* Fixed expansion of %{} keys in Truelight operators [bug 27449]

* Added confirm/cancel dialogue on close scene/quit if a conform is in
  progress [bug 27525]

* Fixed problem where audio timecode and metadata were not being set
  correctly when an audio file was added to a shot or to the timeline
  via the Sequence Browser [bug 27504]

* Fixed problem where changing the Audio FPS for a shot via Shots View
  was incorrectly changing the shot's audio timecode [bug 27504]

* Fixed crash loading DPX file containing Northlight alpha channel
  [bug 27529]

* Prevented new burnin creation from Cursor View overwriting an
  existing burnin with the same name [bug 27538]

* Improved performance of Blackboard 2 rendering [bug 22510]

* Fixed bug which could, on rare occasions, cause a scene to become
  unopenable [bug 27558]

* Fix for slow timeline refresh rate on Gen5 machines with a
  Blackboard 2 [bug 27450]

* Added latest version of Blackboard 2 One firmware (8.0.68.74)
  [bug 27453]

* Changes to Blackboard 2 Fan Speed in "Blackboard2 Setup" are now
  persisted across sessions [bug 27446]

* Replacing Inside/Outside layer operator with an "Add Grain" now
  shows "Add Grain" on Blackboard 2/Slate instead of "Grain2"
  [bug 26254]

* Enabled user editing of "Shift & Alt" Action slot in Chalk for
  Blackboard 2/Slate [bug 27186]

* Fixed bug which prevent image from being updated on initial slider
  drags of matte tool parameters [bug 27580]

* Fixed problem where the stereo eye mode was not toggling correctly
  when the render line was not in the bottommost stack [bug 27569]

* UI/Image/Tablet related buttons on Blackboard 2 One desks are now
  disabled if not applicable [bug 27346]

* DKey encoder parameters now display correctly on Artist Color desks
  [bug 26201]

* Moved display of "No current, single selection" on Blackboard 2 One
  desks by a few pixels to ensure it's not hidden behind physical
  blanking of screen [bug 25896]

* Fixed incorrect disabling of R3D Params controls when ACES Linear is
  selected then disabled, fixed ACES Linear controls enabled when
  using Automatic [bug 27625]

* Fixed pulldown removal [bug 27629]

* Fixed crash applying a deliverable set preset with Output Format:
  Use Input Format [bug 25473]

* Fixed crash that could occur when pressing "UI 1" or "UI 2" buttons
  on the Blackboard [bug 27577]

* Fixed crash when opening Shot View when scene contains a shot
  with audio but no valid audio timecode [bug 27552]

* Fixed text input issues related to some Blackboard 2 desks
  [bug 27355]

* Fixed bug which could result in the Scratchpad becoming unopenable
  due to undefined formats [bug 27652]

* Improved network performance diagnostic to capture link failure 
  statistics [bug 27070]

* Fixed crash when cancelling the "Add New Burnin" dialog [bug 27646]

* /vol automounter will use tcp when connecting to a remote pfs2
  server and pfs2 server will negotiate 1MB rsize/wsize nfs/tcp where
  possible [bug 26799]

* /vol automounter will negotiate 1MB rsize/wsize nfs/tcp where
  possible [bug 27261]

* Prepare For Review is now disabled when the disk cache is
  unavailable [bug 27395]

* Fix a 'division by 0' alert when conforming using RED material and
  overwriting the tape name [bug 22677]

* Fix for crash when pressing Ctrl + Escape with no desk attached
  [bug 27643]

* Fix for crash after using Layer View on Slate desks [bug 27687]

* Fixed bug which could cause the Blackboard's 'Undo' button to be 
  temporarily disabled immediately after a tracking operation
  [bug 27697]

* Fixed bug where timecodes were not read from some AAF files
  [bug 27611]

* Fixed bug where encoder displays on Artist Color desks were not
  showing [bug 26201]

* Fixed bug where some Shape buttons could fail to appear on Slate
  desks [bug 27704]

--------------------------------------------------------------------------

Baselight Release 4.4.6689 (2014-04-04)

Bug Fixes Since Baselight 4.4.6673
==================================

* Fixed crash when using a tracker on Baselight FOUR/EIGHT systems
  [bug 27476]

--------------------------------------------------------------------------

Baselight Release 4.4.6673 (2014-04-01)

New Features Since Baselight 4.4.6600
=====================================

* Updated to RED SDK v4.6. This addresses some issues in earlier SDK
  releases, and adds:
  - Support for ACES Linear output
  - Support for new Dragon OLPF
  - Rocket-X support for RED ONE clips
  - Rocket-X driver for FLOS 6.4
  - Additional metadata support

* Updated to ARRIRAW SDK v4.5. This addresses some issues in earlier
  SDK releases.

* The Operations Queue in Baselight and bl-render now processes
  renders submitted by all users, not just the user running the
  application (does not apply to Baselight PORTABLE).

* Added "Lock Y Positions" toggle to shape strips. This prevents
  shapes & edges from being dragged vertically on the image or
  moved vertically from the trackballs [bug 23514]

* Added horizontal left/right bumps for shapes to the numeric
  keypad (using the '8' and '/' keys respectively, to match stereo
  grade). These are available when 'Numeric Keypad for Grading' is
  enabled (from the 'Edit' menu). These bumps are also available on
  the middle Blackboard trackball reset/top row buttons.

  The bump amount can be set from the "Customise" menu and half bumps
  are available using the "Control" modifier [bug 23514]

* Translating shapes that have been stereo split now applies the 
  opposite change to the other eye's shape if grouped grading is
  enabled [bug 23514]

* Added functionality to support grading for Dolby Vision. This is
  beta functionality and is currently visible only to customers with
  an appropriate licence.

* Added option on Scene Settings (and Setups New Scene tab) to control
  the bit depth of the timeline cache and display pipeline. Switching
  to 16-bit floating-point increases the size of the timeline cache by
  50% which can impact performance. The default setting of 10-bit
  integer is recommended unless you are:
    1. grading HDR material and wish to pick negative or >1.0 colour
       values
    2. grading for Dolby Vision
  [bug 26094]

* A new option on the Display menu allows the brightness of mattes,
  shapes, control elements and the cursor to be reduced. This is
  useful on displays where the maximum brightness is uncomfortable to
  view. By default the brightness is scaled to the white point of the
  cursor's Viewing Colour Space. Please note this functionality
  requires a combiner or DVI2SDI box; it has no effect on Baselight
  PORTABLE [bug 26839]

Bug Fixes Since Baselight 4.4.6600
==================================

* Fixed incorrect rendering of Text and Burnin entries when one %
  expansion follows immediately after another [bug 27097]

* Fixed white thumbnails for OpenEXR files; if you continue to see
  white thumbnails, please use "bl-reset-cache -thumb" to clear the
  cached thumbnails [bug 26541]

* When changing movie file type when rendering with audio, the audio
  codec is no longer left in an invalid state [bug 27109]

* Fixed permissions on directories created when rendering to volumes
  hosted on Baselight Kompressors [bug 27099]

* Fixed an issue where QuickTime movies containing large blocks of
  NULL bytes took a long time to open [bug 27098]

* Reduced disk space required by operations queue, by compacting
  operations once they have completed [bug 26083]

* Fixed incorrect ICC profile information written into TIFF files
  using colour spaces without ICC profiles [bug 27162]

* Fixed crash when duplicating a mask or burnin [bug 27164]

* Fixed pfs2 service script failure on initial Baselight install
  [bug 27150]

* Increased speed of renders using "Link To Unchanged Input Files"
  option to create symbolic links [bug 26257]

* Fixed render corruption when loading the same (large) image multiple
  times per frame [bug 26477]

* Fixed problem with X server startup on Baselight nodes [bug 27137]

* Fixed problem that prevented access to text consoles on Baselight
  nodes whilst X server is running [bug 27183]

* Fixed problem with starting applications on Baselight workstation
  systems after running bl-config-xorg for the first time [bug 27154]

* Fix conforming by 'Tape Name in Header' when remote conform is
  active [bug 27182]

* VTRE no longer continuously attempts to reconnect to a server. It
  now waits 10 seconds between attempts [bug 27055]

* Fix sending of crash reports; it is now less verbose when reporting
  is turned off [bug 11257]

* sshfs-based network mounts now work on Flos 6 systems [bug 27210]

* Disabled Shuffle's 'Input 2' button when used in an Inside/Outside
  layer [bug 27212]

* Fixed issues with some operator presets (e.g. Add Grain) when a
  value was negative [bug 27095]

* Ensure graphical boot screen is finished before starting X server on
  nodes [bug 27223]

* Fixed occasional Server Failure errors when using file panel in
  directories containing dangling symbolic links [bug 27249]

* Fixed occasional crash when writing DNxHD movies.

* Fixed corrupt audio reading from MXF movie files with 1000/1001
  frame rates (such as 23.976, 29.97 and 59.94 fps) [bug 27211]

* Fixed support for integrated motherboard audio outputs [bug 27258]

* Fixed problem that prevented certain tools from using the correct
  GPU on Baselight ONE systems [bug 27259]

* Fixed command-line render submission using bl-render -queue ignoring
  a supplied frame range [bug 27290]

* Fixed problem with Blackboard tablet mapping after running
  bl-config-xorg on a UI host [bug 27345]

* Fixed rare diag warning for nvidia or combiner firmware caused by
  race condition [bug 27369]

* Fixed problem starting bl-render on Mac OS X [bug 27061]

* Fixed problem with error reporting in bl-config-video and
  bl-config-xorg [bug 27061]

* Fixed problem with bl-config-tablet not running. bl-config-tablet is
  responsible for mapping the tablet area to the primary UI monitor on
  startup/login [bug 27214]

* Fixed issue with applying to a blank in Replace mode causing a crash
  [bug 27234]

* Prevented some queued renders from repeatedly failing and restarting
  [bug 27401]

* Fixed "parse failed" errors when rendering using a mask [bug 27421]

--------------------------------------------------------------------------

Baselight Release 4.4.6600 (2014-03-06)

New Features Since Baselight 4.4.6570
=====================================

* Added the "ACES RRT 0.7" display rendering transform [bug 26841]

* ARRIRAW files now support crop rectangles, this is useful for ALEXA
  Open Gate files [bug 26738]

* The 'transfer characteristic' is read from DPX metadata and used
  where appropriate to set ADX Log as the 'From Metadata' colour space
  in the sequence operator [bug 26816]

* Added the parameter operators for DNG, Indiecam, Sony RAW, CineForm
  and RAW to the Insert menu, and to the optional operators for all
  layers [bug 26900]

* Added support for reading Fuji RAF file format. The decode of these
  files is currently very slow [bug 25733]

* ARRIRAW decode now gives a smoother histogram in the shadows instead
  of a sharp cut-off for the sub-blacks, which is a closer match to
  the ARRI render. The old decode is preserved for existing scenes
  [bug 26641]

* Added the Baselight 4.4 User Guide and Reference Manuals.

Bug Fixes Since Baselight 4.4.6570
==================================

* Fix false remote root access diag warnings [bug 25354, 27005]

* Fix the 'autofs' diagnostic on FLOS 6.4 [bug 26804]

* Fixed problem with the cursor not moving when switching from a
  stereo scene to a mono scene while still in a stereo viewing mode
  [bug 26825]

* Fixed bug which would cause keyframe bar to incorrectly switch the
  'Blending' mode when some layer operators were selected [bug 25999]

* Removed unwanted debugging print outs [bug 26856]

* Fixed the FromLinear function in the ADX Log colour space definition
  which had an offset error for (linear) values between 0.0013 and
  0.0019 [bug 26829]

* Fixed metadata read from some QuickTime movies [bug 26545]

* Prevented a stereo stack combine when a split strip is present in
  either of the 2 stacks [bug 26833]

* Fixed loading of OFX plugins with missing dependencies, such as
  Twixtor [bug 23389]

* Fixed reporting of relink errors from Modify AAF/XML commandline
  renders [bug 25437]

* Fixed spurious "xinput-stub" debug messages on FLOS 2.1 [bug 26875]

* Fixed detection of RED Rocket card in FLOS 6.4 [bug 26418]

* Fixed render to muxed problem where only 1 eye would be rendered
  [bug 26877]

* Fixed crash when separating stereo stacks with a single operator
  strip [bug 26877]

* Fixed an issue where some RAW files would fail to decode with a
  message about unexpected size [bug 14509]

* Fixed incorrect duration shown for BLG files in Sequence Browser
  [bug 26917]

* Fixed bug which could cause Baselight to crash with an incomplete
  stack containing a temporal effect [bug 26933]

* Fixed overlapping strips problem with dragging and dropping to a 
  protected stack [bug 26905]

* Fixed potential crash when popping up layer number selector 
  [bug 26930]

* Optimize pfs2 access to 12-bit filled dpx images [bug 25697]

* Fix for quantization problems with stereo display modes [bug 26894]

* Fixed missing metadata information from burnins applied to masked
  renders [bug 26944]

* Fix for crash when using "Delete Keyframes" Chalk action when no
  current scene is open [bug 25575]

* Fix bug that caused conform to compare tapenames and filenames with
  case sensitivity [bug 26956]

* Fix for Undo desk button being disabled after adding an new Area
  Shape Track [bug 26675]

* Fix for crash that could occur using certain parameters when reading
  EXR files [bug 26402]

* Both links to a dual 10ge kompressor are now tested in the 'netperf'
  diagnostic test. Kompressors are tested from within the zone that
  they belong to [bug 26908]

* Fix bug that caused some Arri RAW files to generate a 'Truncated
  file' error message when read [bug 26993]

* Blackness level changes in Stereo Grade now obey group grading
  [bug 26992]

* Entries on "This Deliverable" and "Deliverable Set" menus are now
  sorted alphabetically [bug 27001]

* Fix a UI stall when a vtre client's hostname is slow to resolve over
  DNS [bug 27034]

* Fixed bug which could result in layer matte overlays being drawn 
  in the wrong place if a stack contained a downstream transform
  [bug 27042]

* Corrected the "sRGB Legal" colour space which had a minor error in
  one direction of the transfer function (affecting the blacks in
  conversions to sRGB Legal) [bug 26425]

* Fixed Sequence Browser preview of files with backslashes in their
  filename [bug 27039]

* Phantom Cine files which have colour metadata now use the Rec.709
  Linear colour space when From Metadata is selected [bug 24345]

* Fixed problem that prevent bl-benchmark from running on Baselight
  ONE hardware running FLOS 6.4 [bug 26922]

* Added support for Quadro K600 UI cards [bug 26406]

* Fixed a problem that would cause conform to fail when using XML 
  based conform with events that have no filename [bug 27060]

* Fixed unwanted boxes being drawn at the end of Text and Burnin
  entries [bug 27097]

* Fix GPU upload speed & texture text diagnostics [bug 26879]

--------------------------------------------------------------------------

Baselight Release 4.4.6570 (2014-02-19)

New Features Since Baselight 4.4.6441
=====================================

* Baselight now supports FilmLight OS (FLOS) 6.4.

* Baselight no longer supports FilmLight OS (FLOS) 1.3.

* Added colour space "Sony S-Log3 SGamt3.Cine" and support to recognise
  this space in the metadata of Sony XAVC files [bug 26423]

* Added support for conforming filtering by clip name [bug 25695]

* Added support for reading clip names from AAF files. Note that
  Baselight 4.3 used the clip name as the filename, which wasn't right
  as some AAF files have the filename stored in the filename field,
  and others have the filename in the clipname field. Baselight now
  supports reading both fields and conforming by either [bug 25695]

* Added colour space "Adobe RGB (1998)" [bug 26522]

* TIFF and JPEG files with embedded ICC profiles now show the profile
  name in the Sequence Browser. If the profile is Adobe RGB (1998),
  sRGB or Facebook's "c2" (sRGB equivalent) then the corresponding
  colour space can be automatically associated with the image in the
  Sequence operator [bug 26522]

* ICC profiles are written into TIFF and JPEG files when rendering to
  Adobe RGB (1998) or sRGB colour spaces [bug 26591]

* Additional Exif information is now shown for digital camera files.
  Exif information is now read from TIFF files [bug 18633]

* Exposed Stack Manager controls for matte manipulation as Chalk
  Actions in "Layer Mattes" category.

    - Matte 1 - Select Shape
    - Matte 1 - Reset Shape
    - Matte 1 - Select DKey
    - Matte 1 - Reset DKey
    - etc [bug 26606]

* The Operations Queue (shown in Baselight's Queue Monitor, bl-render
  and fl-queue) now has an optional column indicating the size that
  each operation occupies in the database. Archiving or deleting an
  operation reduces its size.

* Added support for writing DNxHD encoded QuickTime files on
  Linux [bug 25779]

* A new fl-diag module, "runlevel", will check each machine is running
  at the proper runlevel [bug 26714]

* The Grade Result Space option "From Working Colour Space" is now
  named "From Stack" to more accurately reflect its behaviour.

* Added support for reading and writing 60@30 timecode to and from
  QuickTime movies, mimicking the way it is handled by Final Cut Pro
  [bug 26426]

* Edit Left & Right keyframing modes no longer automatically add
  keyframes unless the preference "Automatically add keyframes in
  Edit Left/Right modes" (on the Plugins tab) is enabled [bug 26728]

* Added a counter for Shot Comment. This counter supports long
  comments and will wrap to 80 character width [bug 26794]

* Added scale factor display for remove border in stereograde 
  [bug 26808]

Bug Fixes Since Baselight 4.4.6441
==================================

* Fixed a crash caused by reading certain TIFF files [bug 26251]

* Fixed a problem where variable rate QuickTime movies could be
  misinterpreted to have too high frame rates [bug 26357]

* Fixed a crash that could occur when reading audio from certain MXF
  movie files [bug 25398]

* Fixed "flix write: <filename>: Invalid argument" error when writing
  to a cxfs volume [bug 26472]

* Fixed several issues with OFX plugins: 1. removed incorrect
  application of DRT; 2. fixed white-point clipping of images passed
  to plugins; 3. fixed format of images passed to plugins to use
  floating-point where possible [bug 26381]

* Fixed problem with reading audio from MXF files at 1.001 frame rates
  (such as 23.976, 29.97, 59.94 fps) [bug 26428]

* Fixed problem with image store and root filesystems appearing in a
  users trashbin - a diagnostic will now fail if this occurs, and a
  hotfix will remove incorrect entries at login time if it is detected
  [bug 20911]

* Fixed show disparity pick not taking current convergence value into 
  account in stereograde [bug 26542]

* Fixed conform of MXF material when there are audio and video files
  sharing the same material UID [bug 26549]

* Fixed failures when rendering with Output Format: Use Input Format
  [bug 26554]

* Fixed crash in EDL Import, which could occur with ", as frame
  numbers relative to the matching sequence/movie start" set to "Yes"
  [bug 26544]

* Fixed bug in reference strip where Blackboard alpha "Invert" button
  would incorrecly remain available in some modes, causing Baselight
  to crash if pressed [bug 26547]

* Fixed bug which would cause shape control point to be selected when
  enabling custom inner/outer curves [bug 26568]

* Added Nvidia driver 319.60 and 319.76 as acceptable to installer and
  diagnostic tests [bug 26589]

* Fixed bug which would cause an error when changing video modes on
  newer video cards (GTX 680, GTX 780 Ti) [bug 26589]

* Improved UI/system performance when playing through complex stacks 
  (particularly those containing explicitly cached strips)

* Fixed problem with a reference strip not updating its layer
  selection thumbnails [bug 26594]

* Fixed repeated 'Select failed; error code 9' errors on console when
  a PosgreSQL database server stops [bug 26584]

* Operations can now be restarted from the fl-queue application, as
  they can in Baselight and bl-render [RT 45028]

* Improved behaviour of prerender service and rendering when the
  system has no network connections and its hostname is unresolvable
  [bug 26566]

* Fixed stereo grade edge softness not reseting to default value 
  [bug 26610]

* Fixed a crash reading corrupt AvidRGB MXF [bug 26504]

* Fixed issue when copying some AT data from a shape or a transform
  into an other shape/transform [bug 26638]

* Fixed bug which could cause crash when blening layers in stacks
  with missing strips [bug 26508]

* Fixed missing shot metadata in burnins when the image does not cover
  the area of a node on a FOUR/EIGHT [bug 26611]

* Fixed inability to join split sequence strips after save and reload
  of the scene [bug 26639]

* Fixed a small offset error in the sub-blacks region of the
  convertToLinear functions of the Sony colour spaces [bug 26502]

* DPM diagnostic no longer erronously reports PASS if there is no
  3ware hardware on the machine [bug 24262]

* fl-diag now checks for the correct Myricom driver version when using
  an Nvidia GTX 580 or newer GPU [bug 21483]

* pfs-verify will recreate a missing zero-byte file on a node if all
  its siblings are zero-byte files [bug 16265]

* Fix X11 server config on systems with GTX285 GPUs [bug 26635]

* Fixed a crash reading corrupt Avid RGB MXF files [bug 26504]

* Changed test for xorg service in bl-config-video [bug 26654]

* Fixed crash opening Chalk [bug 26553]

* Fixed crash in bl-config-xorg and bl-config-video when running on
  older GPUs (7600 GT, 9800) [bug 26663]

* Fixed unclosable panel after using Prepare For Review on an empty
  scene [bug 26633]

* Removed -colourspace option from bl-shots since it was only correct
  when the Input Colour Space was set to From Format [bug 26667]

* Fixed problem that prevented user changing the Timecode Frame Rate
  for the Reference Timecode in Shots view [bug 26705]

* Fixed problem with layer view with no scenes open [bug 26711]

* Fixed Bypass categories not working with split strips [bug 26034]

* Fixed Replace paste mode with protected categories not removing
  unprotected strips [bug 25887]

* Fixed render commandline printed when using Modify AAF [bug 26723]

* Fixed crash reading subsampled JPEG2000 files [bug 26732]

* Fixed a problem modifying AAF files with reduced handles on fast
  reverse clips [bug 25277]

* Fixed issue with incorrectly interpreting speed changes during
  conform [bugs 25691, 25343]

* Fixed issue where AAF relinking moved content around on contingent
  clips when rendering both clips with the same grade [bug 26278]

* Fix issue conforming AAF files where the EDL contains multiple
  paths, but the content to conform against is in a single directory
  [bug 25904]

* Fixed permissions issues when working with newer database servers
  (e.g. on FLOS 6) [bug 23696]

* Fixed failure to export jobs containing a folder or scene whose name
  includes a ' character [bug 26696]

* Improved speed of some fl-cp/flux copies [bug 25863]

* Fixed crashes splitting and joining some sequence strips [bug 26719]

* Fixed potential crash when closing scene while playback in progress
  [bug 20974]

* Fixed crash rendering with pulldown [bug 26806]

* Added bl-power support for Flos 6.4 clusters [bug 26758]

* Fixed problem with Multi-Pasting BLG files where the difference
  between the start & end frame number doesn't match the difference
  between start & end timecodes [bug 26814]

* Added Flos 6.4 support to fl-node-repair [bug 26716]

* Fix for crash when starting application with Slate specified in 
  preferences but no desk attached [bug 26761]

* Fixed bug where Add Grain would fail to animate from frame to frame
  [bug 26872]

* Fixed crash when pasting a matte from the Blackboard [bug 26874]

* Fixed layer result blending slider colour space bug 
  ("Blend/Composite In Linear Space" Customise menu option was being
  incorrectly evaluated) [bug 26928]

--------------------------------------------------------------------------

Baselight Release 4.4.6441 (2014-01-09)

New Features Since Baselight 4.4.6396
=====================================

* Added support for Quadro K600 and Geforce GTX 780 Ti graphics cards
  [bug 26406]

* Added access to "Wipe" and "1x1" display modes via buttons above
  left trackball when in View mode on Slate desks [bug 26326]

* Added Gang Cursors button to Display Slate layout [bug 26227]

* Added Show Versions button to Keypad Slate layout [bug 26329]

* Changed Setups so that the default Input Colour Space for new scenes
  is now "No Conversion". To return to previous Baselight 4.4
  behaviour change this to "Automatic/From Metadata"; to emulate
  Baselight 4.3 behaviour change it to "From Input Format" [bug 26246]

Bug Fixes Since Baselight 4.4.6396
==================================

* Fixed issue where Slate could appear unresponsive if the same Slate
  Layout was activated simultaneously on both sides of the desk
  [bug 26321]

* Fixed issue where tracking was slow with some large resolution 
  material [bug 26393]

* Fixed occasional Slate-related crash when opening and closing "DBS" 
  Slate Layout [bug 26321]

* Fix for crash when undoing stereo splitting of strip [bug 26221]

* Fixed crash when an image thumbnail is missing in the layer view
  [bug 26213]

* Fixed crash deleting a matte from the matte selector [bug 25729]

* Corrected the sRGB colour space which had a minor error in one
  direction of the transfer function (affecting the blacks in
  conversions to sRGB) [bug 26425]

* Fixed hang in Baselight when reading images from movie files or
  round-robin files on cluster systems or via the network [bug 26463]

* Fix for incorrect updating of Slate FilmGrade trackball reset
  buttons when panel not in "Home" mode [bug 26429]

* Fixed crash when bl-shots is run on a scene with single input and
  use matte turned on [bug 26358]

* Fixed LUT export when the scene's working colour space is not the
  working format's default [bug 26369]

* Fixed failure to render certain gallery thumbnails due to a colour
  space error [bug 26484]

* Fixed black/white point lines on histogram not moving when cursor
  colour space changes [bug 26166]

* Fixed a small offset error in the sub-blacks region of the
  convertToLinear functions of the Sony colour spaces [bug 26502]

--------------------------------------------------------------------------

Baselight Release 4.4.6396 (2013-12-19)

New Features Since Baselight 4.4.6371
=====================================

* Counter settings are now included in the scene/job cursor settings
  saved from Cursor View [bug 26384]

* Audio files alongside image sequences are now automatically added
  when the audio filename matches the first frame of the sequence
  (excluding their extensions) [bug 26394]

* Added "Grading Workflows With Generalised Colour Spaces" document
  (accessed from Help menu).

Bug Fixes Since Baselight 4.4.6371
==================================

* Fixed filename set in Sequences when conforming material whose
  filenames contain the scene's container in a subdirectory, for
  example /vol/bl-images/project/vol/bl-images/... [bug 26354]

* Fixed "Tape Name From Strip Name" and "Clip Name From Strip Name"
  options [bug 26228]

* Fixed problem with the video grade jumping to extreme valeus on 
  switching between Y'CbCr and RGB tabs [bug 25683]

--------------------------------------------------------------------------

Baselight Release 4.4.6371 (2013-12-11)

New Features Since Baselight 4.4.6317
=====================================

* Added "Pick Corners For Manual Adjustment" button to Stereo Fix
  semi-automatic page for picking the 4 image corners for manual
  adjustment.

* Added "Metadata" tab to Scene Settings, to allow scene metadata to
  be edited. The default values for scene metadata can be set in the
  job from Scene Settings. Initially the only metadata controlled from
  this tab is the Project written into Avid MXF files [bug 17524]

* Added new 'Blend Grade Source' layer mode. When selected, the
  layer's grade operators are applied to the blend source (when this
  mode is selected, the 'Blend Source' dropdown moves up to sit below
  the 'Layer Mode' dropdown to indicate that the layer's operators are
  applied to it) [bug 26147]

* Added options to show Viewing Colour Space and Display Rendering
  Transform as metadata on Gallery View [bug 26149]

* On Slate <Ctrl> + <Layer 0> now selects Layer 31 [bug 26051]

* On Blackboard 2 <Ctrl> + <Layer 0> now selects Layer 21 [bug 26051]

Bug Fixes Since Baselight 4.4.6317
==================================

* Fixed functionality of trackball reset buttons on Tangent panels
  [bug 26072]

* Fixed failures copying image sequences from non-/vol locations to
  /vol/images on a Baselight FOUR or EIGHT [bug 26084]

* Removed the fixed width restriction on the System column in
  "fl-systemmonitor -live" output [bug 26089]

* Fixed occasional crash when dealing with certain Truelight profiles
  on display [bug 25598]

* Fixed premature exit from commandline (non-queued) bl-render when
  rendering to more than one movie (e.g. with %L or %E) [bug 26112]

* Fixed crash when using blur and very large transform scales; also
  restricted available transform scale [bug 26110]

* Fixed memory leak, render cancellation and render hang issues on
  Baselight FOUR/EIGHT systems [bugs 26071,25974,25847,25781]

* Fixed occasional commandline (non-queued) bl-render hangs when
  rendering to movies [bug 25982]

* Fixed crash when changing the frame rate of Reference Timecode on
  Shots View [bug 26064]

* Fixed bug in Stereo Fix strip's "Show Input" mode when in a stack
  with upstream transforms & cached strips (the transforms could be
  applied twice) [bug 26122]

* Fixed issue with artifacts in underexposed RAW files [bug 25786]

* Fixed crash reading interlaced VC-3 (DNxHD) MXF files [bug 26137]

* Fixed Multi-Insert of split-file MXF movies (e.g. C300) [bug 26144]

* Fixed read failure of intra-frame encoded MPEG MXF files such as
  D-10 IMX [bug 26143]

* Fixed incorrect gallery images when the stack has cached strips and
  the stack was grabbed from a scene with a different working format
  from the gallery scene [bug 23197]

* Fixed various issues with gallery grabs resulting in incorrect
  colour spaces being applied when previewed on the display monitor
  [bug 25620]

* Fixed the top-left thumbnail shown in Cuts and Gallery View
  occasionally using the wrong colour space.

* Fixed incorrect gallery images when the stack was grabbed from a
  scene with a different DRT from the gallery scene.

* Fixed various issues with Gallery Current Cursor mode.

* Fixed occasional flickering rear and button screens on Slate desks
  [bug 26150]

* Fixed crash when recalling from or to a stereo split sequence
  operator [bug 26047]

* Fixed BLG export of stacks containing Look operators with no look
  selected [bug 26151]

* Fixed errors overwriting gallery files due to restrictive file
  permissions on original files [bug 26165]

* Fixed crash in stereo grade [bug 25840]

* Fixed incorrect application of Truelight profiles on the cursor when
  they only contain a 1D LUT [bug 26162]

* Fixed bug which could cause the incorrect keyframe to be highlighted
  on keyframe bar in edit left/right modes [bug 26000]

* Fixed errors when double-clicking on a scene in the Save As dialog
  [bug 26199]

* Fixed problem with combiner genlock at 4096x2160 on GTX 680 GPUs
  [bug 25923]

* Fixed problem with audio-related metadata not appearing in Shots
  View or ALEs exported from Shots View [bug 25837]

* Fixed crop rectangle read from Canon HRAW (.RMF) files [bug 26220]

* Fixed render failure "Insufficient tiles to complete this render"
  [bug 25668]

* Fixed problem with more than 2.1 billion repeated lines causing log
  files to become too large [bug 26232]

* Fixed Modify AAF renders never being shown as completed [bug 26239]

* Fixed an issue that caused short H.264 QuickTime movies on Linux to
  be empty [bug 25942]

* Fix for issue when <Alt>+<Tab>-ing from and to Baselight which
  resulted in the Slate desk displaying buttons as though the <Alt>
  key was still held [bug 26216]

* Reordered input devices in Preferences->System [bug 25898]

* Fixed bug which left Blackboard undo/redo buttons temporarily
  disabled after a Curve Grade encoder control point adjustment
  [bug 26264]

* Fixed "phantom" trackball movement on Slate desks which could
  prevent caching from working correctly [bug 26209]

* Updated Blackboard 2 firmware (1.1.44.60) to improve response time
  of button presses (now updates at 200Hz as opposed to 33Hz). Install
  new firmware by running "/usr/fl/baselight/bin/bl-update-bb2" at the
  command line [bug 26183]

* Fixed race condition in renderer that could cause black stripes to
  be visible in on clusters [bug 26197]

* Fixed recall of cursor Colour Space when loading scene [bug 26296]

* Fixed a logging problem with long-but-different lines being considered 
  to be the same [bug 26232]

* The operations queue database is now vacuumed overnight prior to the
  database backup, which should improve performance [bug 25844]

* Fixed errors in View 5-9 modes when using cached strips [bug 26081]

* Fixed excessive memory usage on render-to-cache [bug 26319]

* Fixed bug which could cause crash with some burnin settings in 
  stacks with explicitly cached strips [bug 26336]

--------------------------------------------------------------------------

Baselight Release 4.4.6317 (2013-11-13)

Bug Fixes Since Baselight 4.4.6309
==================================

* Fixed a problem that could cause commands with a lot of console
  output without a newline (such as fl-cp progress information) to
  lose some output [bug 26106]

* Fixed crashes in flfsd, the service which controls the PFS on a
  Baselight FOUR/EIGHT [bug 26103]

--------------------------------------------------------------------------

Baselight Release 4.4.6309 (2013-11-05)

New Features Since Baselight 4.4.6262
=====================================

* Added Swap For Blank button to reference strip [bug 25481]

* Added Do Not Read Cache option to Render View, and restored the
  -nocacheread option to the bl-render command line [bug 25422]

* Added support for a length number with % substitutions in Shots View
  when editing Tape, Clip or Name fields. For example %8W gives the
  first 8 characters of the input filename template, and %6N the first
  5 characters of the tape name [bug 21263]

* Added Cache All Cursors command (on Cursors menu). This waits until
  every cursor is fully cached, and can be used to prepare a number of
  scenes for playback.

* Added Clamp Negative Values option to Image Transform Settings
  operator (and correspondingly to Scene Settings and Setups). This
  option can be used to correct artefacts caused when transforming
  images containing negative pixel values [bug 25897]

* Sequence Browser now allows viewing the alpha channel of ProRes 4444
  movies [bug 25494]

* The Scene Settings Input Colour Space option now allows selection of
  "No Conversion" to better support old-style workflows [bug 25326]

* The Scene Settings Input Colour Space: Automatic/From Metadata
  (where applicable) option now sets sequences to Input Colour Space:
  No Conversion when the colour space cannot be determined
  automatically, and the default colour space of the sequence's Input
  Format is a historic (Baselight 4.3) colour space [bug 25838]

* Additional DRT .fltransform files and their cubes should now be
  located in /usr/fl/etc/colourspaces [bug 24355]

* Added diagnostic for Slate desks to check if high speed USB 2
  connection is available [bug 25850]

* Added Delete All Keyframes action to Chalk for use on Blackboard 2
  desks [bug 25747]

* Added Fixup Tape command to Shots View, to update the Tape metadata
  for selected shots [bug 22966]

* Multi-Paste of Layer 0 now pastes the Orientation (flip/flop) into
  Sequences [bug 25892]

* ARRIRAW Parameters is now available on the Insert menu and can be
  added as an operator to layers.

* Render To Cache (or bl-render -tocache) and Prepare for Review now
  both perform the same operation as background caching in Baselight:
  they quickly check the cached files, and cache every explicitly-
  cached strip plus the bottom of the stack. In order to do this
  correctly you must now specify whether the cache is for a
  progressive or interlaced display [bug 25849]

'랜더 투 캐쉬'(또는 bl-render -tocache)와 '리뷰 준비' 둘 다 베이스라이트에서 백그라운드 캐싱이라는 동일한 작업을 수행합니다. 
두 작업 다 빠르게 캐쉬된 파일을 확인하고, 캐시된 스트립에 추가적으로 스택의 아래까지 캐싱 작업을 합니다. 이 작업을 진행할때 프로그레시브와 인터레이스 디스플레이를 올바르게 선택해야 합니다.  



* Waveforms now have an "Auto" Legal Overlay option, that sets the
  overlay to full or legal depending on the viewing colour space
  [bug 25476]

Bug Fixes Since Baselight 4.4.6262
==================================

* DPM tests hang on a deskside ONE [bug 25780]

* Fixed Reset button on Blackboard on operators including Soften 
  [bug 25744]

* Added support for Generation V Baselight ONE systems configured with
  both SSD and HDD RAIDs [bug 25740]

* Optimize pfs2 access to 12-bit filled DPX images [bug 25697]

* Fixed over-sharp ARRIRAW images at proxy and thumbnail resolutions
  [bug 25795]

* Improved error messages when DRT cube files are missing [bug 24355]

* Fixed bug which would produce a black and white image when bypassing
  an input strip containing an ARRIRAW sequence [bug 25794]

* The Resolution Filter in flux is no longer persistent; it is now
  turned off each time flux starts [bug 14710]

* Fixed expansion of many substitutions such as %{ISODate} in render
  directory/filename templates [RT 42971]

* Cached images from explicitly-cached strips are now read when
  rendering to all deliverable types, including movies and 16-bit
  image sequences [bug 25422]

* Deliverable presets cannot now be deleted by mistake [RT 42977]

* Fixed "Unknown hardware" splash screen message on some Generation II
  systems [bug 25829]

* Fixed full-range video warning messages for ProRes rendering.

* Fixed bug where HueShift rear screens on Blackboard desks would
  still be displayed after selection moved to another strip
  [bug 25790]

* Added support for Soften and Add Grain strips to Slate desks
  [bugs 25767, 25803]

* Fixed unpredictable behaviour of decimal places on Blackboard 2 and
  Slate readout screens when switching between tabs on Videograde and
  Filmgrade [bug 25805]

* Increased sensitivity of Slate trackball rings [bug 25804]

* Prepare for Review now takes account of the disk space required for
  caching explicitly-cached strips.

* Speed of Blackboard 2 ONE USB connection is now reported accurately
  during diagnostics if it is insufficient to handle bandwidth
  required [bug 21575]

* Fixed Strip Name counter [bug 25854]

* Prevent console output log from filling with repeated warning lines
  [bug 25388]

* Fixed occasional hang during rendering [bug 25878]

* Fixed bug that could cause a crash when encoding high resolution
  ProRes QuickTime movies on Linux [bug 25825]

* EDL Import now uses the Scene Setting for Default Input Colour Space
  [bug 25881]

* Film Grade's numeric keypad and Blackboard bumps now work on key
  down rather than key up [bug 25407]

* Fixed crash in sequences when using %W [bug 25879]

* Fixed Grouped Grading of several decode parameters operators
  including ARRIRAW Parameters and Sony RAW Parameters [bug 25891]

* Fixed hang when exiting with a MCS Spectrum panel enabled in prefs
  [bug 25861]

* Fixed crash in large gallery view [bug 25894]

* Addressed histogram errors when image frame is empty. Reduced
  differences between different histogram resolutions. Histogram
  resolution options now match those in the scope views (Stopped,
  Playing, Grading) [bug 25246]

* Movie codec is no longer reset when changing from Movies Video Only
  to Movies Video+Audio [bug 25902]

* Corrected issue in header of rendered 16-bit RGB DPX files to
  prevent rejection by ARRILASER 2 [bug 25901]

* Fixed error reporting from bl-render commandline [bug 25906]

* Addressed issue with red/blue noise in very dark/underexposed
  high-speed Phantom material [bug 22110]

* Fixed output of frames where there are no strips to use the black
  level of the viewing colour space [bug 25927]

* Preserved red "illegal" overlay when coloured mode is disabled
  in Luma/RGB/YCbCr scopes [bug 25915]

* Strip caching is now taken into account to speed up the Area Tracker
  [bug 22637]

* Fixed issue which was slowing down the area tracker when the
  material format and the scene format were different [bug 25916]

* Fixed an issue which caused 444 Cineform QuickTime movies to decode
  incorrectly on Mac [bug 25875]

* Fixed occasional hang in RED Rocket reading [bug 25943]

* Fixed crash selecting the matte tool with a slate that's
  disconnected [bug 22844]

* Fixed some slightly inaccurate colour values of the SMPTE charts
  supplied by the Bars operator. Note that since the chart is
  generated to 10-bit accuracy, the +I, -I and +Q patches are (still)
  not represented exactly [bug 25495]

* Fixed the position of the white-point histogram marker with the
  "Rec. 709 Video Legal" colour space [bug 25929]

* Fixed an issue that could cause failure when reading some OpenEXR
  files, with messages about truncated files or internal
  inconsistencies [bug 25111]

* Fixed performance issues while prerendering and rendering large
  scenes, due to database issues [bug 25968]

--------------------------------------------------------------------------

Baselight Release 4.4.6262 (2013-10-09)

Bug Fixes Since Baselight 4.4.6259
==================================

* Add Grain operator no longer appears blue when initially added to an
  inside/outside layer [bug 25558]

* Fixed memory leak when reading OP-1a MXF files [bug 25761]

--------------------------------------------------------------------------

Baselight Release 4.4.6259 (2013-10-08)

New Features Since Baselight 4.4.6237
=====================================

* Added the option to decode ARRIRAW files using the ARRI SDK. This is
  slower than using the Baselight decode, but should enable matching
  to the decode from other applications.

  To simplify operation, the Sharpen which is added to the Baselight
  decode is now controlled from the ARRIRAW Decode operator.

  PLEASE NOTE: The ARRI SDK is not supported on Mac OS X 10.5. This
  means that ARRIRAW files accessed by or via a Baselight Kompressor
  running Mac OS X 10.5 will not support decoding using the ARRI SDK
  [bug 25673]

* Added keyframe indicators for layer blend amount slider to keyframe
  bar [bug 25497]

* Added support for reading MXF files containing 2K Sony F5 RAW and
  2K Sony F55 RAW [bug 25439]

* Added ACES RRT 0.2.1 as an option for Display Rendering Transform.
  This is the recommended DRT to use for most situations, and is now
  the default DRT for new scenes (edit this in bl-setups or the
  Baselight Setups window) [bug 25614]

* Added No Conversion option for Output Colour Space on Render View.
  This causes no colour conversion to be applied during rendering, by
  setting the output colour space to be the same as the Grade Result
  Colour Space [bug 25701]

* Added support for decoding XDCAM HD, XDCAM EX and XDCAM HD422 in
  QuickTime movies without requiring a Baselight Kompressor, and for
  encoding XDCAM HD422 into QuickTime on Linux.

Bug Fixes Since Baselight 4.4.6237
==================================

* Fixed bug which would cause animated layer blend amount keyframes to
  be incorrectly positioned after a strip had been split [bug 25642]

* Fixed problems creating the database user on OS X when the user name
  includes upper case characters [bug 25633]

* Fixed problem with selecting the display menu with no scene open
  [bug 25651]

* Fixed problem with Stereo Grade not setting the keyframe mode on the
  other eye [bug 25655]

* Improved RED Rocket-X support [bug 23716]

* Fixed problem where convergence was getting set to the same value in
  both eyes [bug 25662]

* Stereo Grade now auto-splits on a group-graded action [bug 25665]

* Rendering using Both Eyes now always renders from the bottom of the
  other eye stack [bug 25680]

* Fixed slow performance caused by Video Grade continually updating
  the Blackboard graph selector [bug 25631]

* Fixed Apply of a single blend layer [bug 25479]

* Fixed failures caused by QuickTime files with bad timecode data that
  has no frame rate [bug 25607]

* Fixed bug where incorrect functions could occasionally be activated
  when using the 'Ctrl' modifier on Blackboard desks [bug 25682]

* Fixed orientation of rear screens and incorrectly displayed buttons
  on Blackboard 2 ONE [bug 25623]

* Fixed crash at end of commandline bl-render -tocache [bug 25699]

* Fixed Queue Monitor incorrectly displaying "Rendering suspended"
  [bug 25703]

* AAF relink failures now cause a render to be marked as failed.

* Fix for values in Video Grade occasionally jumping to extreme values
  [bug 25683]

* Fixed invalid right eye cache produced by bl-render -tocache on
  single-stack stereo scenes [bug 25707]

* Fixed bug in grouped grading of keyframed blend amount slider
  [bug 25715]

* Fixed a bug where invalid 'edts' atoms in QuickTime movies could
  result in different reported lengths on Linux and Mac [bug 25602]

* Fixed occasional unnecessary re-caching of stacks using Sony RAW,
  R3D or ARRIRAW material with Automatic colour space [bug 25707]

* Fixed broken rendering of glow strips when using the 'Dark Glow'
  effect [bug 25752]

--------------------------------------------------------------------------

Baselight Release 4.4.6237 (2013-09-25)

New Features Since Baselight 4.4.6234
=====================================

* The Render View now warns when OpenEXR files are being written using
  a non-linear colour space [bug 25586]

* OpenEXR files written using the ACES Linear Output Colour Space now
  contain the correct metadata to indicate their use of the ACES
  primaries [bug 25586]

* OpenEXR files using ACES primaries are now recognised as using the
  ACES Linear colour space [bug 25427]

* MXF Capture Gamma metadata is now used to automatically set the
  colour space for many MXF files, notably XAVC [bug 25576]

Bug Fixes Since Baselight 4.4.6234
==================================

* Fixed render failure after exporting a CMX3600 EDL [bug 25585]

* Sequences with crop resolutions (e.g. Canon RMF) can now be
  correctly conformed using the format of the crop resolution rather
  than requiring the full RAW sensor resolution [bug 25581]

* Fixed incorrect identification of some ARRIRAW files as containing
  black+white images [bug 25597]

* Fixed an issue where intermittent decode failure of random frames
  could occur for some QuickTime files on Linux [bug 25565]

* Fixed bug where bypassed background replacement composite layers
  rendered the wrong image (ie. the background rather than the
  foreground) [bug 25601]

* Fixed bug where shape-based background replacement composite layers
  were not inverting the matte (fix only applied to newly created
  layers) [bug 25584]

* Fixed rendering ignoring the chosen Output Colour Space when the
  scene uses a Grade Result Colour Space [bug 25609]

--------------------------------------------------------------------------

Baselight Release 4.4.6234 (2013-09-20)

New Features Since Baselight 4.4.6201
=====================================

* Added support for the new Slate control surface. Slate uses the same
  technology as the Blackboard 2 but in a smaller, more portable form.

  The soft-mappable buttons are used to allow Slate access to the
  breadth of Baselight features. The left and right panels, each
  consisting of 24 buttons, can be quickly switched between a
  selection of with Slate Layouts. The initial set of Slate Layouts
  consists of:

   - Keypad
   - Layers
   - DBS
   - Display
   - Stack
   - Transport

  Buttons relating to the current strip are displayed when no Slate
  Layout is active.

  Undo/Redo, Copy/Paste, UI/Image, Layer Up/Down, Keyframe Toggle and
  playback controls are present above the trackballs, along with the
  trackball/ring reset operators.

  The Slate encoder push buttons function as reset buttons.

* Added a new "Merge events around CMX3600 dissolves" option in the
  "Timeline"->"Conform" tab in the Baselight preferences. CMX3600 EDLs
  often have the incoming or outgoing events in a dissolve split into
  two. If the option is on (the default, matching the previous
  behaviour), Baselight will attempt to merge events with matching
  tape name and timecode, so that the user doesn't need to merge
  manually. However, this is not always appropriate, especially in
  situations where the source timecode is monotonically increasing.
  Switching off this option disables the merging behaviour.

* Blackboard 2 encoder push buttons now reset the associated values
  instead of toggling the "gang" state.

* Add Grain can now be added as a layer operator.

* If you have set a Grade Result Colour Space, this is now used as the
  initial Render Colour Space in the Render View [bug 25369]

* Updated to RED SDK v4.5. This addresses some issues in earlier SDK
  releases, and adds:
  - Support for the RED Rocket-X accelerator board (note that RED ONE
    clips are not supported on RED Rocket-X) - please note this has
    not yet been tested by FilmLight; if you have a Rocket-X please
    contact baselight-support@filmlight.ltd.uk to report any issues
  - Support for the RED 6K Dragon sensor (not supported on RED Rocket;
    note that DRX has no effect for Dragon)
  - Support for the RED Motion Mount

  Users of RED Rocket cards installed in Baselight Kompressor systems
  will need to:

  1. update the Rocket driver using the installer package
  REDrocket_Driver_OSX_v1.4.36.0.pkg that can be found in the
  /Applications/Baselight/Current/Utilities/Resources/etc folder.

  2. update the RED Rocket card's firmware using the rocketup_1.1.17.3
  utility included with Baselight.

  Ensure the Kompressor is shut down and restarted after updating the
  firmware.

* Added display of Capture Rate and Playback Rate metadata for Canon
  RMF files [bug 25528]

Bug Fixes Since Baselight 4.4.6201
==================================

* Fixed crash when applying Baselight Grades which had been exported
  from a Baselight Edition in CPU rendering mode [bug 25444]

* Fixed crash in Render View when switching to use QuickTime Movie
  rendering via a Baselight Kompressor [bug 25446]

* Fixed Northlight Alpha issues on multinode systems, and Baselight
  TWO systems with dual network interfaces [bug 25438]

* The colour space of OpenEXR files is now automatically set to
  Rec.709 Linear [bug 25427]

* Fixed crash due to overlapping strips caused by switching eyes
  during a second conform [bug 25448]

* Renamed the "Gallery" keypad mode to "Recall" on the Blackboard 2
  [bug 25304]

* Fixed crash when switching to the matte selector after deleting a
  matte operator [bug 25275]

* Fixed crash after closing scene and pressing 3D button [bug 25181]

* Fixed Layer view and layer selector showing only  matte channels
  [bug 25330]

* Added support for Telecine Grade on MC Color and Tangent desks
  [bug 25177]

* Blackboard 2 and Slate keypad now display correct Scratchpad slot
  number when "Next Page" is active [bug 25243]

* Improved Tangent Element support for Film Grade and Curve Grade
  [bugs 22536, 22719]

* Fixed problem where Blackboard 2 desks could lose their brightness
  setting [bug 24514]

* Fixed crash applying a deliverable preset with Output Format: Use
  Input Format [bug 25473]

* Fixed problem with the display mode when switching between a stereo
  and mono scene. This was also causing the cursor not to move in the
  mono scene on playback [bug 24916]

* Fixed bug where tracks were not being added to a tracker strip when
  a tracked shape/transform strip was stereo split [bug 23640]

* Fixed bug on a Blackboard One which could cause the blend encoder to 
  be enabled even when the Inside/Outside key was not held down
  [bug 25499]

* Fixed suprious 3ware diagnostic failure on Baselight ONE Deskside
  systems [bug 25492]

* Fixed Prepare for Review [bug 25519]

* Fixed problem where combine stereo stacks was going into an infinite
  loop [bug 25550]

* Added warning dialog when attempting to reset a Chalk layout
  [bug 25526]

--------------------------------------------------------------------------

Baselight Release 4.4.6201 (2013-09-03)

New Features Since Baselight 4.3.6187
=====================================

Single Stack Stereo
-------------------

* Single stack stereo is a new way of organising the timeline when
  dealing with stereo projects. It removes the need to have two
  separate stacks, one for each eye. Single stack stereo allows there
  to be only one stack, where each strip that needs to be different is
  "split", allowing changes to occur separately per eye.

  To put a scene into single stack stereo mode, use the Stereo tab on
  the Scene Settings View. There are four stereo modes:
    - Not Stereo
    - Left Eye on Top
    - Right Eye on Top
    - Single Stack Stereo
  Eye on top modes allow a mixture of single stacks and split stacks,
  (still obeying the old rules for stereo). Single stack only allows
  single stacks, while still being allowed to join two different
  stacks.

  Each cursor now has an eye mode (Left or Right) in stereo scenes.
  This mode is displayed on the switching button in the cursor view,
  on the menu bar and also in the Pane Description when the mode is
  switched.

  An inside/outside layer or strip can be split using the "3D" button
  next to the bypass button. There is also an indicator of the
  operator's stereo status inside the grid selector and on the
  timeline strip. Both operators and strips can be split with the
  exception of a few special cases Reference and Audio.

  The Sequence can also be swapped right eye for left and vice versa,
  using the Swap Eyes button.

  In the Edit menu the new Combine/Separate Stereo Stacks command
  allows the combination or separation of the selected stacks. This
  can be used to batch combine a conformed scene containing two
  separate tracks, or to separate a stack that has become complex and
  needs to be processed with one stack per eye.

  Shots View now follows the cursor's active eye.

  The Gallery can now store single stacks and recall to both single
  stacks and dual stack stereo stacks.

Layer Blending and Compositing
------------------------------

* Every (Inside/Outside) layer in Baselight now has additional
  controls that allow you to easily blend the output of that layer
  with other layers further up the stack. You can also blend a layer's
  output with a different grade not currently in the stack, or even a
  completely different source sequence. The amount of blending to
  apply can be varied as well as the blend mode to use.

  The Result Blending section for each layer is located below the
  grade selection grid and consists of three controls:

  - A slider for adjusting the amount of blending to apply.
  - A 'Type' menu for selecting the blending operation to use.
  - A 'Source' menu for selecting what the output of the layer is
    to be blended with.

  On a Blackboard 2 the slider is always mapped to the encoder between
  the centre and right trackballs. On a Blackboard 1 holding down the
  'Inside/Outside' button will temporarily take over the second screen
  and its encoders/buttons, with the rightmost encoder mapped to the
  blend amount slider.

  By default, the blend type is set to 'Mix' and the source is set to
  'Input Image'. This means that changing the amount slider will mix
  between the output of the layer and the input to that layer. This is
  useful for quickly de-emphasizing the grade operations within a
  layer without having to go through each one adjusting its parameters
  individually.

  The Result Blending 'Source' menu is for selecting what the output
  of the layer is to be blended with. It has four options available:

  Input Image    - The result of the layer is blended with the input
                   to the layer (the default).

  Raw Image      - The result of the layer is blended with the raw,
                   ungraded image at the top of the stack.

  Numbered Layer - The result of the layer is blended with another
                   numbered layer number from further up the stack.
                   Selecting this option adds an additional button
                   which, when pressed, will pop up a thumbnail menu
                   for selecting the layer to blend with.

  Second Input   - Selecting this option adds a new Reference strip
                   above the layer titled 'Blend Source'. This strip
                   is used exclusively for blending with the layer.
                   New grade strips may be added (or pasted) directly
                   below this strip to create a different look not
                   currently in the stack for blending with the layer.

                   By default, the blend source strip is a reference
                   to the raw sequence, but it can easily be swapped
                   for a different sequence to blend into the layer (a
                   texture, for example). To do this, select the blend
                   source strip and press the 'Swap For Sequence Strip'
                   button. This will bring up the Sequence Browser for
                   selecting the new sequence to blend with.

  By default, the result/output of the layer is blended with the
  entire blend source image. However, if the layer has a matte
  associated with it, the blending can be forced to occur only through
  the layer's matte using the 'Use Matte: For Blend' toggle button.

  On a Blackboard 2 (in standard layout) there is a dedicated 'Blend
  Controls' button next to the right trackball that, when pressed,
  latches the second screen (and its buttons/encoders) into a mode for
  adjusting blend paramters. In this mode the right screen's buttons
  can be used to select the current blend source and inside grade
  source (see below). Also, the rightmost encoder can be used to
  select the blend type. Pressing the 'Blend Controls' button again
  cancels the mode.

  The Blackboard 1 has similar controls, but these are only available
  while the 'Inside/Outside' button is held down.

  The 'Inside Source' Menu
  ------------------------

  This option is only available for layers which have a matte.

  Previously in Baselight, grading stacks were typically constructed
  by cascading grades one layer below another. However, it is
  sometimes desirable to not grade over the result of the previous
  layer, instead choosing a layer further up the stack as a grade
  source. The 'Inside Source' menu is used for selecting that source.

  By default 'Inside Source' is set to 'Input Image'. This means that
  all the grading operators in the 'Inside' column will be applied to
  the input of the layer (the same source as the 'Outside' column). In
  this confuguration layers behave the same way they have in previous
  versions of Baselight.

  However, selecting one of the other menu options will change what is
  used as the source for the inside grade operators, effectively
  "punching a hole through the matte" up the stack to the layer
  specified.

  The 'Layer Mode' Menu (For Grading/Compositing)
  -----------------------------------------------

  Layers can now be classified as either 'Inside/Outside' (grading)
  layers or 'Composite' layers. An Inside/Outside layer grades either
  an entire source image or an area of a source image specified using
  a matte. A compositing layer takes foreground and background images
  and uses a matte to replace one with the other. By default, layers
  are configured as Inside/Outside layers. This menu lets you quickly
  change this, setting up layers for a number of different compositing
  scenarios described below.

  Background Replacement:

   Matte From Key   - This option may be used where the stack contains
                      a sequence with areas you wish to replace with
                      another (e.g. a classic 'sky replacement') using
                      a keyer to isolate those areas. Selecting this
                      option reconfigures the layer to contain a keyer
                      and launches the Sequence Browser to select the
                      new (background) replacement sequence. Once this
                      is done, the keyer strip will be automatically
                      selected, ready to pull a key on areas to be
                      replaced in the foreground sequence.

   Matte From Shape - As above, except a Shape strip is inserted to
                      isolate areas of the foreground to replace.

  Composite:

   Matte From       -  This option may be used when the stack contains
   Foreground Key      a background sequence onto you wish to
                       composite a different foreground sequence (e.g.
                       a green screen sequence). Selecting this option
                       will reconfigure the layer to contain a keyer
                       and launch the Sequence Browser to select the
                       foreground. Once this is done, the keyer strip
                       will be selected ready to pick/remove
                       transparent areas of the new foreground.

   Matte From        - As above, except a Shape strip is inserted to
   Foreground Shape    isolate areas of the foreground sequence.

   Matte From        - This option may be used where the stack
   Foreground Alpha    contains a (background) sequence on top of
                       which you wish to composite another
                       (foreground) sequence that has already has an
                       emebedded alpha channel to specify areas of
                       transparency (e.g. a TIFF title sequence).
                       Selecting this option will reconfigure the
                       layer and launch the Sequence Browser to select
                       the foreground. Once this is done, a reference
                       strip will be inserted to enusre the embedded
                       alpha is used as a matte for the layer.

                       Note: If the foreground sequence image data has
                       already been multiplied by its alpha, ensure
                       the 'RGBA: Premultiplied' toggle button is
                       enabled in the foreground sequence strip for
                       correct results.

   Matte From        - This option is only available if the top
   Background EXR      sequence in the stack is OpenEXR. It can be
   Channel             used when that single sequence contains
                       multiple (image) tracks and mattes (alpha
                       channels) for layered compositing. Selecting
                       this option will launch a dialogue for
                       selecting the foreground track and alpha channel
                       from that OpenEXR. Once this is done, two
                       reference strips will be added above the layer;
                       one referencing the alpha channel and one
                       referencing the track/fill.

  If there is a stack above the current stack, an additional toggle
  option 'Use Stack Above As Background' will be available which, if
  enabled, will *not* prompt for a new foreground sequence when a
  compositing option is selected. Instead, the stack above will be
  used as the background sequence, and the current stack as the
  foreground.

  Once in 'Composite' mode, the layer itself has different options and
  behaviour from 'Inside/Outside' mode: The Inside/Outside grade
  columns become Foreground/Background grade columns. Additional
  transforms are automatically added to these columns allowing the
  foreground and background elements to be repositioned relative to
  each other. Also, the blend amount slider is replaced with a
  Foreground Opacity slider. There is also a toggle button (on by
  default) that ensures any foreground transforms applied are also
  applied to the layer's matte input.

  Additional Notes
  ----------------

  For options above which automatically insert a keyer, the default
  keyer to use can be set from the Inside/Outside's 'Customise' menu.

  Some of these options are only available if the strips above that
  contribute to the layer are horizontally aligned on the timeline.

  Options to toggle a layer's composite mode off/on without adjusting
  the stack in any other way are available from the 'Layer Mode' menu
  via the Shift modifier. These options should only be used if you're
  comfortable with manually moving/inserting strips to obtain a valid
  stack.

Reference Strips
----------------

  Reference strips now support more options for referencing strips
  from further up the stack. Also, the controls have been reorganised
  to simplify the options available, only presenting certain controls
  when appropriate.

  The 'Reference' menu is always available and is used to select the
  type of reference the strip makes. The options available in this
  menu may change depending on the strip's position in the stack (for
  example, a reference on the foreground input of a composite layer
  will have more options than one used in a simple keyed grade layer).

  Depending on the type of reference selected, the options on the
  'Using' line will change (or the line may disappear altogether).

  Some example new reference options available are:

  - The ability to reference any numbered layer above the current
    one in the stack.
  - The ability to reference tracks and channels from OpenEXR
    sequences at the top of the stack.

Colour Spaces
-------------

* Baselight now supports generalised colour spaces, defined by their
  RGB primaries and tone curve.

  Earlier versions of Baselight supported only a fixed set of "colour
  spaces" (Log, Linear, Video etc) which only affected the tone curve,
  having no defined RGB primaries. These colour spaces continue to be
  supported, and are now defined to use Rec.709 (sRGB) primaries.

  Colour space conversions are automatically applied where necessary.

  A Convert Colour Space strip is available to perform an explicit
  colour space conversion. For information on how to access this strip
  please contact baselight-support@filmlight.ltd.uk.

  Custom colour space definitions can be added to Baselight when
  required. Please contact baselight-support@filmlight.ltd.uk if you
  are interested in using a colour space that is not currently
  available in Baselight.

* Legacy (pre-Baselight 4.4) colour spaces are shown in orange and are
  not available in new scenes, except when using old formats which use
  them.

* The colour space set in a format can now be overridden in the
  Working Format, the cursor's Viewing Format, the Render View's
  Output Format and the Sequence's Input Format. This will reduce the
  number of formats that need to be created.

* The scene's Working Colour Space (the colour space used in a scene)
  can be overridden in Scene Settings. The Working Colour Space for
  new scenes is configured in Setups.

* The colour space assigned to the input data of a Sequence can now be
  changed using a menu beside the Input Format menu:

  Automatic        - For certain image formats (currently RED R3D,
                     Sony F5/F55/F65 RAW, ALEXA ARRIRAW, DNG)
                     Baselight can fix the Decode settings to generate
                     image data in a known colour space, which is then
                     converted to the output format's colour space.
                     Some Decode settings are disabled when using this
                     option.
  From Metadata    - For certain image formats (e.g. ProRes QuickTimes
                     written by an ARRI ALEXA) Baselight can guess the
                     the correct colour space using metadata in the
                     file.
  Use Input Format - The image data is converted from the input
                     format's colour space to the output format's
                     colour space.
  No Conversion    - No input-to-output colour space conversion is
                     applied. The image data is assumed to be in the
                     output format's colour space.
  Named space      - The image data is assumed to be in the named
                     colour space, and is converted from that to the
                     output format's colour space.

* A default setting has been added to the scene and setups to specify
  what the input space should be, either Automatic or From input
  format. This allows the Automatic setting to be turned off if it is
  not desirable.

* The colour space used by each Baselight cursor can now be changed to
  be different from that of the viewing format. Typical usage will be
  to use a display colour space (e.g. DCI X'Y'Z', P3, Rec.709 Video,
  sRGB).

* The default colour space for cursors can be stored with the initial
  cursor behaviour for the scene or job using the menu on the Cursor
  View.

* A display transform (such as an ACES RRT) can be set in Scene
  Settings. This is applied whenever the colour space changes from a
  scene-referred colour space to a display colour space (or vice
  versa). The display transform for new scenes is configured in
  Setups.

* The Cuts View now ignores the viewing colour space and Truelight
  settings of the current cursor and instead renders the thumbnails to
  the sRGB colour space which is suitable for UI monitors. The old
  behaviour can be restored using the right-click menu in the Cuts
  View. sRGB viewing can also be enabled for Gallery Views using the
  right-click menu.

* The Sequence Browser now allows colour management of the images it
  displays.

* A 'Grade Result' colour space may be specified in the Scene Settings
  (and a default value for new scenes in Setups).

  By default, Baselight expects the output of a scene's grade stacks
  to be in the working colour space of the scene itself. Baselight
  will then apply an appropriate transform from the working colour
  space to the (cursor's) viewing colour space for display.

  However, it can sometimes be preferable to manually apply a grade to
  convert from the working colour space to the viewing colour space in
  the grade stacks themselves (grading the image to look 'right' on
  the display without explicitly specifying a viewing colour space).
  For this workflow, the 'Grade Result Space' option should be used to
  tell Baselight the colour space the scene has been graded into.

  On initial selection of a new grade result colour space Baselight
  will set the cursor's viewing colour space to match. As the two
  colour spaces are the same, no conversion is necessary and the image
  will not change. Once the image has then been graded into grade
  result space, Baselight will then correctly apply appropriate
  downstream conversions where necessary (when rendering out different
  deliverables, for example).

Rendering
---------

* The Render View (also used in bl-render) has been simplified so that
  most options are hidden until you change them.

* Multiple deliverables can now be specified and rendered together in
  an efficient manner. The render presets used in Baselight 4.3 are
  now known as "Deliverable Presets". New "Deliverable Set Presets"
  allow groups of deliverables to be stored and recalled as presets.

* Renders are now submitted to a queue which is processed by Baselight
  and bl-render. You can submit renders to any queue in your Baselight
  network. The queue is persistent (i.e. it retains its contents after
  quitting Baselight).

* Submitting a scene for rendering takes a snapshot of the scene; you
  can continue to edit and work on the scene while the snapshot is
  rendered. You can even delete the original scene.

* You can monitor the progress of renders in the queue from Baselight
  (in the new Queue Monitor View), from bl-render (push the Operations
  button at the bottom if it's not visible) or from the new standalone
  fl-queue application. When you're in Baselight you can jump to
  frames where warnings or errors occurred.

* From the queue monitor in Baselight or bl-render, you can re-open a
  scene, with the render settings used for a given render, by
  double-clicking on the entry in the operations list, or using the
  Open/Edit button beneath.

* A completed or failed render may be restarted using the Restart
  button.

* bl-render commandline does not use the render queue unless you use
  the new -queue option to specify a zone name.

* bl-render supports rendering on remote systems as well as on the
  local system; this is required for rendering on a headless FLUX
  Store for example.

* Quitting rendering while output movies are in progress will cause
  those movies to be discarded and later restarted by the next
  renderer which starts; you are warned about this in Baselight.

* Baselight will only process renders queued by the current user; any
  renders added to the queue by other users will not progress until
  Baselight is run as that user, or bl-render is run as any user.

* The Q menu on the Baselight menu bar allows queue rendering to be
  paused and resumed.

* Rendering of the queue has lower priority that background caching;
  you may wish to pause background caching to allow rendering to
  proceed.

File Formats and Codecs
-----------------------

* The Decoder Pack One licence is no longer used; all the formats for
  which it was previously needed are now read natively in Baselight:
  - MPEG MXF, including XDCAM HD
  - AVC-Intra MXF, including Panasonic P2
  - JPEG2000 codestream (.j2c)
  - Long-GOP MPEG2 MP4 (e.g Sony F3)
  - Codex Digital JPEG2000-compressed DPX

* The Sequence operator now allows the Medium and Low resolutions of
  many movie decodes to be chosen for decode quality, rather than
  using the medium/low proxy resolution from the Input Format.
  Typically this will use half-resolution for Medium and
  quarter-resolution for Low. This is useful, for example, with R3D
  media which is commonly used at half-resolution for speed.

* The alpha channel of a ProRes 4:4:4:4 QuickTime movie can now be
  read without using a Baselight Kompressor [bug 24154]

* Added support for reading Sony FS700 RAW files [bug 24002]

* Rendering of H264 QuickTime movies on Linux now uses multiple
  threads, to greatly improve encoding speed [bug 22425]

* Added support for reading ProRes MXF files [bug 20476]

* Added support for images with premultiplied alpha, using the
  Premultiplied button on the Sequence operator.

* Added support for reading Avid IMX codec in QuickTime [bug 23930]

* Updated to latest Sony-supplied white balance colour transforms for
  Sony F5 RAW and Sony F55 RAW. Note that this will result in small
  colour changes in this material compared with Baselight 4.3.

* Added support for writing DCI compliant JPEG2000 files. Valid
  resolutions for 2K compliant files are:
  - 2048 by 1080 or less
  - 2048 or less by 1080
  Files matching these resolution criteria will be created with DCI 2K
  profile markers. Valid resolutions for 4K compliant files are:
  - 4096 by 2160 or less
  - 4096 or less by 2160
  Files matching these resolution criteria will be created with DCI 4K
  profile markers. Maximum file sizes will be determined using the
  output format frame rate and the selected bitrate.

  Three different bitrates are provided:
  - 250 Mbit/s, corresponding to the Digital Cinema System
    Specification, Version 1.2
  - 125 Mbit/s, which is half of the above rate to be used for left or
    right eye stereoscopic sequences
  - 500 Mbit/s, corresponding to the High Frame Rates Digital Cinema
    Recommended Practice

  The output colour space must be set to DCI X'Y'Z' for the produced
  files to be DCI compliant.

* Added support for writing DCI compliant JPEG2000 files at
  resolutions 2048x1080 and 4096x2160. The output colour space must be
  set to DCI X'Y'Z' for the produced files to be DCI compliant.

* Added support for reading ARRIRAW Black+White files [bug 24777]

* Updated to RED SDK v4.4, RED Rocket driver v1.4.33.0 and RED Rocket
  firmware v1.1.17.3.

  This adds:
  - Support for the Mysterium-X Monochrome sensor in the Epic-M
  Monochrome and Epic-X Monochrome cameras (only with RED Rocket
  disabled at this time)
  - DRX is now available on the RED Rocket
  - Additional metadata support, including user-defined metadata

  Users of RED Rocket cards installed in Baselight Linux systems will
  need to update the RED Rocket card's firmware using the
  rocketup_1.1.17.3 utility included with Baselight. Ensure that all
  systems hosting the RED Rocket cards are shut down and restarted
  after updating the firmware.

  Users of RED Rocket cards installed in Baselight Kompressor systems
  will need to:

  1. update the Rocket driver using the installer package
  REDrocket_Driver_OSX_v1.4.32.0.pkg that can be found in the
  /Applications/Baselight/Current/Utilities/Resources/etc folder.

  2. update the RED Rocket card's firmware using the
  rocketup_1.1.16.11 utility included with Baselight (be aware that
  a bug in this utility causes it to report the wrong version
  number while it is running; do not be alarmed by this).

  Ensure the Kompressor is shut down and restarted after updating the
  firmware.

* ProRes QuickTime movies read by Baselight now produce full-range
  data (in Baselight 4.3 and earlier they produced legal-range data)
  [bug 24939]

* Added support for reading AVC-Intra (non-avc1) QuickTime movies on
  Linux [bug 23928]

* The QuickTime ProRes codecs now expect to be given full-range images
  (in Baselight 4.3 and earlier they expected legal-range data). You
  should ensure this by using either a full-range Output Colour Space
  (such as Rec.709 Video) or the Legal to Full Scale Video LUT. The
  Render View will warn if it appears you are using inappropriate
  settings [bug 24939]

Disparity Histogram
-------------------

* There is a new view called disparity histogram. It shows you your
  disparity/depth distribution in your stereo scene. Only works with
  stereo scenes. Disparity histogram is useful for stereoscopic QC or
  in general for verifying your depth budget.

  The scene setting allows you now to specify a so called "comfort
  zone" which corresponds to the disparity zone that is usually
  associated to a pleasant stereo viewing experience. The zone range
  is specified in percentage of scene format width and is displayed in
  the histogram by two dotted red lines.

  The disparity values in the histogram are in cinema space.

  The histogram allows two different sampling methods:

     Regular = samples are taking on a regular grid and the grid size
               is specified by the sampling rate the lower the rate
               the tighter the grid.

     Edge based = Sample points are taken on image edges that have
                  been detected using an edge filter. Image edges
                  usually correspond to sample points with very high
                  confidence.

  The confidence of the overall result is encoded in the colour of the
  graph. A white graph means high confidence (>70%), yellow graph
  means medium confidence (>= 20% < 70%) and finally a red graph means
  low confidence (<20%).

  If the graph is red it can be a indication there is a problem in
  your stereo setup potentially a large vertical misallignment or
  timing mismatch between the two eyes.

Stereo Colour Matching
----------------------

* Added Stereo Colour Matching operator. It is accessible either from
  the 'Insert' menu or from Inside/Outside.

  It corrects colours locally on one eye, by taking from the other one in
  order to minimize the colour differences between the stereo pair.
  Only works with stereo scenes. It can correct the colour on
  the left eye, the right eye or using a second image input for
  the Dual Stack mode. It uses the following parameters:

   - Quality: Specifies the amount of processing. Increasing the
     quality will increase both the precision and the processing time.

   - Correction Type: Determines the desired treatment localness. It
     can be set to Localized, Intermediate or Global.

   - Border: This option applies a specific treatment on the image
     boundaries. It allows to exclude problematic regions on the
     boundaries where occlusions can append. The chosen region is
     represented by a red rectangle, which can be specified using the
     mouse, or can be set up to one of the default settings.
    (Default or Current Cursor Mapping).

StereoGrade
-----------

* StereoGrade blackboard controls have been reworked to allow an
  easier and more streamlined control on the floating window. Users no
  longer have to be aware on which eye they are currently located on
  as the trackball controls adapt automatically to the selected eye
  and therefore always act the same way.

  New blackboard trackball behaviour is as follows:

      Left Trackball Y-Axis moving downwards will pull left floating
                     window towards the viewer
      Left Trackball Y-Axis moving upwards will push left floating
                     window away from the viewer

      Middle Trackball Y-Axis moving downards will increase the
                       convergence pulling the scene towards the
                       viewer
      Middle Trackball Y-Axis moving upwards will decrease the
                       convergence pushing the scene away from
                       the viewer

      Right Trackball Y-Axis moving downwards will pull right floating
                     window towards the viewer
      Right Trackball Y-Axis moving upwards will push right floating
                     window away from the viewer

* Automatic floating window adjustment when changing convergence can
  be switched on/off

* Convergence can now applied to only a single eye if desired
  (hero eye mode)

* Pick mode now reflects the correct internal state of the strip

* Added additional blackboard control surface buttons to
  increase/decrease left/right floating window by one pixel

* Added the ability to soften the floating window edge

* Added ability to change the sensitivity of the blackboard trackballs

* Have a quick small/medium/large floating window preset for left/right
  floating windows

* Added numerical keypad for grading support:
      KeyPad-NumLock Decrease left floating window by 1 pixel
      KeyPad-Home    Increase left floating window by 1 pixel
      KeyPad-Left    Reset left floating window
      KeyPad-/       Decrease convergence
      KeyPad-Up      Increase convergence
      KeyPad-5       Reset convergence
      KeyPad-*       Decrease right floating window by 1 pixel
      KeyPad-PgUp    Increase right floating window by 1 pixel
      KeyPad-Right   Reset right floating window
      KeyPad-End     Set preset small left/right window
      KeyPad-Down    Set preset medium left/right window
      KeyPad-PgDown  Set preset large left/right window
      KeyPad-Insert  Toggle between left/right window

Miscellaneous
-------------

* Baselight no longer supports 32-bit operating systems.

* Added support for redesigned hardware encoders between trackballs on
  newer revision Blackboard 2 desks.

* Added "Magnify Values At Wheel Centre" option to "Customise" menu of
  video and film grade operators. When enabled, small offsets at the
  centre of the colour wheel are magnified, making it easier to spot
  grade changes when quickly navigating the timetime.

* Proxy containers can now be seen on Scene Settings without having to
  change a preference [bug 23109]

* Added new Baselight formats for ARRI ALEXA, for ARRIRAW and ProRes
  material [bug 23536]

* Added 1.5x speed to Play Controls [bug 22846]

* Baselight now attempts to create PostgreSQL database users where
  necessary.

* Added a Bypass button to the inside/outside to allowing individual
  operators to be bypassed. There are also controls on the Blackboard
  and Blackboard 2.

* Background caching can now be paused/resumed by clicking on the
  progress spinner in the timeline (or menu bar) [bug 20643]

* Added Tangent and Euphonix desk support to StereoGrade and Stereo
  Fix [bug 24346]

* Added Chalk action for Align Timeline Vertically command [bug 24168]

* Added Video LUT "Full to Legal Scale (Unclipped)" option for
  rendering to a legal-range output but without clipping the scaled
  pixel colour values to legal range [bug 24944]

* Added Y vs Y (luma) curve to curve grade. This curve works in YCC
  colour space downstream of all the other curves. Unlike the RGB
  master curve, it allows you to make luminance changes to an image
  without affecting the saturation/colour balance [bug 25048]

* Added 2 new control groups to FilmGrade for bumping overall contrast
  and overall saturation [bug 24380]

* For the initial release of Baselight 4.4, we have disabled the 
  "Update FCP XML with Baselight grades" and the "Update Avid AAF with
  Baselight grades" EDL Export options. This is simply because the
  release of the 4.4 release of the Baselight Editions for FCP7 and
  Avid Media Composer/Symphony will slightly lag the 4.4 release of
  full Baselight. These options will be restored once the 4.4 versions
  of the Editions are restored.

* In EDL Import, when the Time Type is "Source", a new option appears:
  "Source, as frame number relative to matching sequence/movie start",
  with possible values of "No", "Yes", and "<Try All Options>". This
  conform option is useful when your EDL's frame numbers or timecodes
  represent an offset into a sequence or movie, rather than an absolute
  frame number or timecode. This often occurs in workflows where
  editorial are liasing with VFX vendors, who often re-number
  sequences and lose metadata. When your source times are timecodes,
  the timecode hour the start timecode hour is treated as 0, where as
  the ending timecode hour is reduced by the same amount.

Bug Fixes Since Baselight 4.3.6187
==================================

* Baselight would occasionally freeze on older Supermicro H8QM3
  systems. This release adjusts the MTRR register on such systems to
  avoid the freeze [bug 24723]

* Fixed small colour shift in QuickTime movies using ProRes and some
  other codecs, when read or written on Mac OS X (e.g. via a Baselight
  Kompressor) [bug 22366]

* Fixed crash reading some JPEG2000 DPX files [bug 18277]

* Fixed error handling of damaged frames in H264 and MPEG QuickTime
  movies on Linux [bug 22086]

* Fixed issue where some Blackboard 2 ONE buttons were labeled 
  incorrectly [bug 23708]

* Fixed failure to read remote images containing '@' in the filename
  [bug 23140]

* Format mappings that only apply a fixed-pixel crop or translation
  (with no scaling, and no sub-pixel translation) no longer cause an
  image transform to be applied [bug 21304]

* "option kompressor" in cloud.cfg now correctly sets the current zone
  to use no Kompressor [bug 22798]

* Encoder readout values on Blackboard 2 now display same number of
  decimal places for negative values, and added +/- signs when value
  could be above or below zero [bug 23869]

* Support for QuickTime movies with edits described by edts-atoms has
  been improved on Linux. Video offset and trimming are now handled,
  and support for audio offset has been added for movies with single
  track audio. Apparent length and frame rate of affected movies will
  change to better match QuickTime on Mac [bug 22276]

* The handling of QuickTime movies with variable frame duration has
  changed to avoid frame repetition and skipping where possible. For
  movies with significant speed changes, e.g. those shot by mobile
  phones, an option to read the movie in 'frame by frame' mode will
  now appear in the sequence panel. This change can alter the frames
  displayed and affect the apparent length and frame rate of movies
  with variable frame duration [bug 21844]

* Image files whose filenames contain the } character can now be
  copied using flux and fl-cp [bug 23908]

* Hidden formats are no longer shown in the Mappings section of the
  formats editor unless Show Hidden is enabled [bug 23933]

* Changing the screen layout while running Baselight or any related
  application no longer causes a crash on Mac OS X 10.7 Lion or later
  [bug 23935]

* Encoding QuickTime movies on Linux using Motion JPEG A codec no
  longer squeezes progressive material into the top half of the frame
  [bug 22351]

* Multipaste now retains the explicit caching setting of any strips
  copied [bug 22667]

* Fixed bug which prevented toggling of strip caching/bypassing when
  more than one strip selected [bug 22667]

* Fix for crash when selecting "Control Raw Video I/O" via Machine
  Control icon when Tangent Element/Wave desk is attached
  [bug 24079]

* Removed 10 Area Track limitation per strip [bug 22974]

* Changed the Area Track overlay's behaviour. Holding 'Ctrl' or
  'Shift' allows to select the dotted rectangle using the mouse when
  this one is behind the plain rectangle. The rectangle selection
  using the mouse is now only performed from its edges [bug 21632]

* Increase maximum number of disk cache entries [bug 22239]

* Removed various engineering debug preferences [bug 22640]

* Fixed width of codec parameters dialogs [bug 24224]

* Cuts View now updates when formats are edited [bug 11693]

* Fixed Blackboard 1 desk functionality where strip marks of different
  categories can be toggled by holding Mark button and using numeric
  keypad buttons specified in preferences panel [bug 22772]

* Fixed crash which could occur if the trackballs were nudged while
  moving strips [bug 20532]

* Fix for issue where prolonged usage of Tangent Element or Wave desks
  could lead to out of memory errors [bug 24426]

* 8-bit PNG images are no longer converted to 16-bit when copied using
  fl-cp or flux.

* Fixed image corruption which occured when transforming a Northlight
  Alpha Channel [bug 24509]

* Fixed potential crash when moving strips immediately after deleting
  a layer from the Blackboard [bug 24523]

* Enabled 'Remote Conform' to be the default mode of operation for
  conform, ensuring less memory use on the host [bug 10869]

* Fixed reading RMD files with unusual HDR data [bug 24586]

* Improved speed of copying movie files onto a Baselight FOUR/EIGHT.

* Fixed stereo display of blanks on multinode systems [bug 24778]

* Older Phantom Cine files which have no colour matrix stored in the
  file now have the camera's default colour matrix applied, which
  should bring them to Rec.709 primaries [bug 24345]

* Fixed crash opening Spirit view when system has a Blackboard ONE
  or Blackboard TWO control surface [bug 24003]

* Fixed render failure with error "Insufficient tiles to complete
  render" [bug 24895]

* Fixed crash which could occur when rendering QuickTimes on Linux
  using the ffmpeg_mpg4 codec [bug 17089]

* R3D decode parameters are no longer shown on Sequence parameters in
  scenes that were created in Baselight 4.1 [bug 24958]

* Fixed bug which could cause a crash when disabling scratchpad
  "Show Versions" mode if simultaneously moving a trackball
  [bug 24176]

* Fix for slider bars for Hue Angle and Six Vector appearing at the 
  wrong size on Blackboard 1 & 2 rear screens [bug 24952]

* Fixed crash when verifying or performing an AAF relink following a
  render [bug 23534]

* Added %L for strip name as an option for file names when generating
  LUTs from grades [bug 22139]

* Ensured bl-render and the render view within Baselight always check
  for updated Truelight profiles or cubes when submitting a render
  [bug 22780]

* Fixed occasional crash on exit [bug 20972]

* EDL conform now warns when media is ignored because there are no
  formats for its resolution [bug 24996]

* Reduced memory usage when generating proxies from the Job Manager
  [bug 19661]

* Improved speed of caching when playing short sequences [bug 24577]

* The psql utility bundled with Baselight now includes readline support
  [bug 21695]

* The system precompiles shaders via a background service to avoid a 
  delay in the first start of Baselight after installation [bug 25066]

* Fixed bug which would stop grouped grading from working if the
  cursor was parked past the end of the currently selected parameter
  strip [bug 25115]

* Fixed a problem on the pre-render service on OS X that would create
  too many log files [bug 25060]

* Fixed timecode reported from QuickTime movies which claim to have
  60fps drop-frame timecode [bug 25133]

* Changing the name or length of a strip no longer forces the strip's
  frames to be re-cached [bug 23182]

* OpenEXR images are defragmented as sequences; previously they were
  treated as individual files [bug 22870]

* flood filesystem driver uses no more than 1/8 of physical memory
  (and at most 2GB) for its internal buffers [bug 21526]

* Fixed gallery grab of sequences using custom Track settings, notably
  BLG files inserted onto the timeline [bug 25018]

* fldm (X window manager) recognises FLUX Store and starts X without a
  connected display [bug 23709]

* Fix xfs attribute maintenance [bug 25219]

* Fix issue with copying tracking data between two shapes [bug 25251]

* Fixed crash issue with colour space parser [bug 25426]

--------------------------------------------------------------------------

Baselight Release 4.3.6187 (2013-08-20)

New Features Since Baselight 4.3.6117
=====================================

* Added the ability to load/save Baselight grades from/to Avid
  AAF files. This enables an easy, render-free round-tripping
  workflow with Baselight for Avid within Media Composer/Symphony.
  
  To load Baselight for Avid grades from an AAF, simply set
  "Apply Baselight Grades" to "Yes" in the EDL Import panel and
  conform as normal.
  
  To save Baselight grades into an AAF file, simply select
  "Update Avid AAF with Baselight Grades" in the "Export Format"
  dropdown in the EDL Export panel. This export option has the
  following options:
  
    Input Filename: The AAF file originally used to conform
      the timeline.
    Output Filename: The name of the AAF file to be generated.
      The generated AAF will be identical to the input AAF
      in structure, other than containing Baselight for Avid
      metadata in every shot.
    Remove Avid CCs: Used to remove Avid colour corrections.
    Remove Strips of Category: Used to remove strips tagged
      with a given category. This is typically used to
      remove Transforms applied during EDL Import so that the
      transformn doesn't get applied twice back in Avid.
    Continue on Error: Whether or no the EDL Export should
      abort if any shot can't be exported.

  The only Baselight grades which can't be exported to Avid
  are those stacks which include temporal effects (eg Temporal
  Degrain, Motion Blur, DSpot etc) or those stacks with split
  strips.

* Improved the "Modify AAF" workflow in several ways:
    - Failures to relink a single clip no longer cause a hard
      failure to generate a modified AAF. Instead, as many clips
      as possible are relinked with detailed error reporting
      for any clips which failed.
    - The actual AAF modification is now done in a separate
      process, meaning that crashes in the Avid AAF library
      no longer crash Baselight and prevent a modified AAF
      being written. Instead, Baselight detects a crash in the
      sub-process and redoes the modification, simply omitting
      the problem clip.
    - AAFs in which clips failed to relink are now automatically
      sent to FilmLight for analysis, along with sufficient 
      metadata to reproduce the issue.
    - Improved AAF speed change conform handling to only show
      warnings when variable speed change encountered plus better
      handling of Avid MC timewarps.

* Changed filename conform to initially try conforming using a common
  base directory, then if that fails to find anything, it assumes all
  media is in a single directory.

* Changed AAF conform to handle MXFs slightly differently.  Previously
  if a clip spanned two MXFs, the conform split this into two clips.
  Now the conform handles this as a single clip.

* Added FCP Flip/Flop support.

* Add the ability to set the keyframe interpolation mode for Transforms
  added by EDL Import [bug 25054]

* Added support for NVIDIA Quadro NVS 510 graphics card for UI hosts
  [bug 23507]

* Added support for reading AVC-Intra MXF files written by Avid
  products [bug 14622]

* Updated to RED SDK v4.4, RED Rocket driver v1.4.33.0 and RED Rocket
  firmware v1.1.17.3.

  This adds:
  - Support for the Mysterium-X Monochrome sensor in the Epic-M
  Monochrome and Epic-X Monochrome cameras (only with RED Rocket
  disabled at this time)
  - DRX is now available on the RED Rocket
  - Additional metadata support, including user-defined metadata

  Users of RED Rocket cards installed in Baselight Linux systems will
  need to update the RED Rocket card's firmware using the
  rocketup_1.1.17.3 utility included with Baselight. Ensure that all
  systems hosting the RED Rocket cards are shut down and restarted
  after updating the firmware.

  Users of RED Rocket cards installed in Baselight Kompressor systems
  will need to:

  1. update the Rocket driver using the installer package
  REDrocket_Driver_OSX_v1.4.32.0.pkg that can be found in the
  /Applications/Baselight/Current/Utilities/Resources/etc folder.

  2. update the RED Rocket card's firmware using the
  rocketup_1.1.16.11 utility included with Baselight (be aware that
  a bug in this utility causes it to report the wrong version
  number while it is running; do not be alarmed by this).

  Ensure the Kompressor is shut down and restarted after updating the
  firmware.

* Modified AAF relinking after render to check that the AAF file
  didn't change since conform. Baselight will no longer relink to a
  changed AAF file [bug 25212]

* Made improvements to the "Overwrite Tape Name" EDL Import setting:
    - Added the "With Filename" option, which allows you to overwrite
      the tapename with the first <n> characters of the event's
      filename. 
    - Removed the "<Try All Options>" option, as it generated a lot
      of spurious conform tabs which very rarely helped, as the
      default number of leading characters (16) was usually wrong
      [bug 25313]
  
Bug Fixes Since Baselight 4.3.6117
==================================

* Fixed crash handling very large shapes [Bug 20799]

* Fixed render hang on rendering movies on BL8 [Bug 24605]

* Allow yfs filesystems for /mnt/disk1 on some systems [bug 22694]

* Fix crash on startup in Baselight [bug 23131]

* Ensured custom film grade page configurations setup in Baselight
  version 4.4 don't crash version 4.3 [bug 25056]

* Ensured formats using new Baselight 4.4 colour spaces are
  unavailable and do not cause issues [bug 25067]

* Fixed crash when exporting BLGs from a scene whose Working Format is
  not defined in global preferences [bug 25063]

* Playback monitor improvement, pending reads replaced with completed
  reads. The read monitoring now takes into account the position in
  the playback queue of the read request [bug 24674]

* Fixed the 'Zones' diagnostic to be less likely to hang when systems
  in the cloud are unreliable [bug 23970]

* Fixed mix and transitions not working together when doing an AAF
  conform [bug 16108]

* Fixed issue with AAF reading crashing - patch to AAF library
  [bug 19953]

* Fixed issue with XF305 MXF files containing subclips [bug 22968]

* Modified AAF conform to conform filenames correctly [bug 20970]

* Fixed a problem with the SMPTE-352 payload identifier packet that
  upset Panasonic plasma displays [bug 24991]

* Baselight would occasionally freeze on older Supermicro H8QM3
  systems. This release adjusts the MTRR register on such systems to
  avoid the freeze [bug 24723]

* Fixed issue conforming MXF files containing subclips [bug 25049]

* Fixed crash when applying to stack in replace mode with copy 
  protected categories [bug 25161]
  
* Fixed issue with timeline rippling when inserting Baselight grades
  into AAF files [bug 25217]

* Fixed issue with incorrect xfs attributes [bug 25220]

* Modified AAF relinking to add a version number so that future
  relinking can be compatible with conforming in earlier versions.
  Anything without a version number is assumed to be prior to this
  release [bug 25212]

* Fixed issue where views would turn white after switching workspaces
  [bug 24218]

* Fixed failure to recognise Sony RAW MXF files with a zero-sized
  marker rectangle [bug 25269]

* Multi-Insert of movies which span multiple MXF files now inserts
  only one copy of the movie [bug 25261]

--------------------------------------------------------------------------

Baselight Release 4.3.6117 (2013-07-05)

Bug Fixes Since Baselight 4.3.5996
==================================

* Changed the STATD_OUTGOING_PORT in /etc/sysconfig/nfs to 659.
  Previously it would be randomly selected, and could potentially
  clash with other services on the LAN [bug 24303]

* fl-diag no longer warns about network link speed when a Baselight
  ONE is directly connected to a combiner [bug 20454]

* fl-diag no longer warns about network link speed when a Euphonix
  panel is directly connected to the Blackboard port [bug 19279]

* Fixed crash report generated when running bl-upgrade [bug 24306]

* Fixed incorrect render of cached movies on clusters when movie
  resolution differs from scene resolution [bug 23816]

* Worked around a problem in the Avid ISIS file system driver on Mac
  OS X 10.6 Snow Leopard that was limiting browse and conform to 13
  sequences [bug 23513]

* Fixed incorrect Sony F5/F55/F65 colour balance in Cuts View, Gallery
  View and CPU renders [bug 24402]

* Fixed failure to read single-frame R3D movies [bug 24421]

* Relaxed the Myricom driver version test for Leopard based 
  Kompressors to version 1.3.1 [bug 24429]

* Fast Start option is now available when rendering to QuickTime Movie
  via Kompresor [bug 24565]

* Fixed failure to read AAC encoded audio from QuickTime movies on
  Linux and mp4 files on Mac [bug 24575]

* Fixed the behaviour of the 'up' directory button in Flux [bug 24741]

* Fixed flux/fl-cp of BLG OpenEXR files [bug 24758]

* Fixed a delay in cancelling conform searches [bug 24531]

* Fixed issue with bl-config-xorg not assigning the correct GPUs for
  UI and rendering on Gen5 Baselight ONE systems [bug 24633]

* JPEG 2000 images with a .J2K extension are now treated as codestream
  data and require a Decoder Pack 1 license to read [bug 24860]

* Metadata for Source File, File and Slate is now read from DPX files
  and is available for burnin using %{Source File}, %{File} and
  %{Slate} [bug 24863]

* Improved Job Manager behaviour when using jobs containing thousands
  of scenes [bug 24887]

* Shots view will now correctly display the ALEXA camera ID in its
  Camera column when using ARRIRAW material. Note that handling of
  ARRI ALEXA metadata has been updated to match the settings available
  on the camera. In particular the 'Cinematographer' metadata item is
  now called 'Cinematographer' in Baselight, rather than the previous
  name of 'DoP' [bug 24116]

* Fixed bug when rendering to 16-bit images with a mask or transform
  starting on an odd column of pixels, causing colour fringing on the
  left edge [bug 24398]

--------------------------------------------------------------------------

Baselight Release 4.3.5996 (2013-05-29)

Bug Fixes Since Baselight 4.3.5962
==================================

* Fixed occasional hang on Baselight PORTABLE when rendering to movies
  using "Prefer Source Codec" and/or "Frame Rate From Source Movies"
  [bug 23196]

* Fixed crash in thumbnail rendering on the Mac for stacks containing
  certain HueShift 3 values [bug 24147]

* Fixed hang in "fl-systemmonitor -live" and possibly other command
  line utilities [bug 23969]

* Improved speed of movie decoding (e.g. R3D) on systems with more
  than 16 processor cores [bug 24198]

* Fixed fl-rm when specifying a frame range with leading "0" digits
  [bug 23602]

* Fixed creation of scenes with invalid names through pasting into the
  New Scene dialog [bug 24263]

* Fixed middle-button paste into text fields [bug 14]

* Worked around a bug in the Avid ISIS filesystem that prevented
  conform from finding all relevant files [bug 23604]

* Fixed occasional crash when clicking the "Edit" menu, if the
  Multi-Paste setting was in "BLG" mode [bug 24264]

--------------------------------------------------------------------------

Baselight Release 4.3.5962 (2013-05-10)

New Features Since Baselight 4.3.5900
=====================================

Baselight Grade Files (BLGs)
----------------------------

* This releases marks the introduction of the Baselight Grade (BLG)
  format. BLG files are a new mechanism for storing Baselight grades,
  allowing them to be easily loaded and exported to/from full
  Baselight, the various Baselight Editions and FLIP.
    - BLG files are essentially OpenEXR files. They contain 3 image
      layers:
        Default: An image displaying a wipe between the graded and
          ungraded versions of the image. This makes it easy to see
          in a glace the effect of a grade.
        Source: The ungraded input image, in its native colour space.
        Graded: The graded image, in its native colour space.
      Having both the input and the result available in a single images
      is very useful, as it make it easy to construct a LUT which
      represents simple grades on non-Baselight systems.
    - BLG files also contain all the metadata required for Baselight
      to reconstruct the grade stack in its entirety, including
      spacial operations like blurs and shapes, which cannot be
      represented by simple LUTs.
    - BLG files also (optionally) contain all the keyframes of the
      exported grade, allow them to contain the intent of a complex,
      dynamic colour correction.
    - If a grade requires external resources to achieve its look, then
      the external files are compressed and included within the BLG -
      typical examples would be LUTs and Truelight profile, looks etc.
    - Each BLG has the "BLGName" attribute, which is simply the name of
      the BLG file without the ".blg.exr" suffix.
    - Each BLG also contains the "BLGID" attribute, which is a 32-digit
      string derived from the contents of the source image and the
      Baselighr grade applied to it. This make it an excellent piece
      of metadata to use to match grades to shots, as BLGIDs are
      *extremely* likely to be unique within a project.

* To generate BLG files, select the shots you what BLG equivalents
  of and select the new "Export BLGs..." option in the "Actions" menu
  at the bottom-right of the Shots View. This launches a dialog with
  the following settings:
    - Directory: The directory into which the BLGs are to be exported.
    - Template: A template defining how the exported BLG files are to
      be named. Most of the standard Baselight text substitutions (eg
      %N for tape name etc) can be used. To see all the possible
      substitutiosn, click the "?" button to the right of the template
      edit field.
    - Scale: Resolution of OpenEXR files you wish to generate: Full,
      Half, Quarter etc. This option is used to make BLG files smaller,
      but whatever the resolution they are exported at, they will
      still behaviour like full resolution images when imported back
      into Baselight.
    - Frame: Whether to use the first frame or the poster frame as the
      representative frame of the shot.
    - Keyframes: Whether or not you wish the BLG file to contain
      keyframes. If "No" is selected, then the grade will be sampled
      at the "Frame" position and will contain no keyframes. If "Yes",
      then the BLG will contain all keyframes and they will be imported
      when the BLG is loaded by Baselight.
    - Preview Image Transform: The color space of the "Default" (wipe)
      layer of the OpenEXR file. "Linear" means that the preview will
      be expressed in a true linear colour space - this option is good
      if you wish to import BLG files into something like NUKE.
      "Linear (Mac OS X compatible)" means that an additional correction
      factor is applied to the preview to make it look correct when
      viewed in the Finder or Preview on Mac OS X - this is required
      because Mac OS X doesn't appear to treat true linear images
      properly.

  Once, you're happy with the settings, simply click "Export".

* A single BLG file can also be quicky exported via the "BLG Quick
  Export" command, which is mapped to the Alt+e accelerator. The BLG
  file will be written to the directory specified by the "BLG Quick
  Export Directory" preference (located in the "BLG" section of the
  "System" tab). The filename of the BLG will take the form of:
     YYYYMMDD_HHHMM_SS.blg.exr

* The Sequence Browser has been updated to include BLG file support:
   - BLG files found within a directory listing have a coloured icon
     beside them to make them easy to spot.
   - A selected BLG file will display the timecode/keycode ranges
     the BLG file represents, even though the OpenEXR file contains
     a single image. The ranges shown are the ranges of the original
     shot the BLG was exported from. Also displayed are the BLGName
     and BLGID attributes which every BLG file contains.
   - The "Default" (wipe), "Source" and "Graded" layers can be viewed
     by selecting the appropriate layer in the dropdown beneath the
     metadata section.
   - Like any other type of image, BLG files can be inserted/multi-
     inserted into a timeline, by clicking "Insert at Cursor" (this
     button was previously called "Insert Below") or "Multi-Insert".
     BLG files inserted onto the timeline will have exactly the same
     shot lengths, metadata and keyframes as the shots they were
     originally exported from, simply applied to the "Source" layer.
   - When other strips in the Timeline View are selected, then the
     button changes to "Insert BLG Grade Below". Clicking it will
     result in the grading stack represented by the BLG being inserted
     below the bottom-most selected strip in each selected shot.
     The "Include Layer 0 Operations" paste option is obeyed, allowing
     any Layer 0 operations present in the BLG (debayering operators
     for example) to be applied to the selected stack.
   - If a resource contained within the BLG (eg a Truelight profile)
     has the same name as an existing resource, then a dialog will
     pop up, asking the user how they wish to resolve the conflict.
     There are three possible resolutions:
        Rename: Import new version under a new, non-conflicting name.
        Replace: Replace the version on this machine with the version
          from the BLG file.
        Original: Use the version on this machine instead of the
          version from the BLG file.

* The new Multi-Paste View includes BLG support, allowing the user to
  quickly paste grades from a directory of BLGs onto shots with
  matching metadata. See below for details.

* The EDL Import View is now able to read BLGName and BLGID metadata
  out of the comment field of any EDL type. Syntax examples:

     BLGNAME=my_example_blg
     BLGID=7e07c10ac51b276ef35875941f53cfbc
     BLGNAME=my_example_blg, BLGID=7e07c10ac51b276ef35875941f53cfbc

  This functionality is very useful in associating a look with a
  shot, as after an EDL is imported, the new Multi-Paste view can
  be used to apply the appropriate grade, simply by matching against
  BLGName or BLGId.

* BLGName and BLGID columns have been added to the Shots View, allowing
  the user to see what looks have been associated with each shot.

* The fl-imageinfo now supports BLG files and will emit BLG-specific
  metadata in addition to the normal OpenEXR data.

* Added bl-applyblg utility to apply a BLG to a sequence or movie.
  Run "bl-applyblg -i" for usage information.

Strip Categories
----------------

* Paste Protection Category:

  A new category type has been added which allows the protect of
  strip from being changed during a paste action. Layers containing
  strips that have a no paste category will not be modified during
  any paste action. They will not be removed, written over or have
  their mattes changed. This category is labelled "Don't paste over
  strips of category".

  Note: This use of categories replaces the "NO_PASTE"-in-strip-name
  hack available in previous releases. It has now been removed.

* Copy Inhibit Category:

  A new category type has been added which allows a strip to be
  inhibited from being included in a copy action. Layers containing
  strips that have a copy inhibit category will not be included in any
  paste action when they are present in the source stack and
  protected by the copy inhibit category. This category is labelled
  "Don't copy strips of category".

* Both are used in Apply actions, Blackboard copy and paste, and 
  keyboard or Edit Menu copy and paste. Copy inhibit and paste
  protect will only work for strip categories - using a mark on
  a strip will have no effect on copy and paste.

  Existing categories can be added and removed to the new types via
  the preference or scene settings. The category groups found in Scene
  setting "Category Group" tab allow the categories types to be set on
  a per scene basis. Existing categories can be added and removed to
  the new types. Category groups can also be set up via the
  preferences panel, under the "Timeline" tab, to work across scenes.

Multi-Paste View
----------------

* Baselight's Multi-Paste functionality has been extended and is
  now accessed from the Multi-Paste View (View menu). This new
  view contains the following settings:
    - Source: Specifies where the source grades are to be obtained:
        Current Copy Buffer: The current contents of the copy buffer.
          This is the equivalent to the multi-paste source in previous
          versions of Baselight.
        Multiple Scenes: Allows the user to select multiple scenes
          by clicking "Select Scenes", which will launch a job
          browser. This brower allows the user to add/remove scenes
          to/from a list via the "Add Selected Scenes" and "Remove
          Selected Scenes" buttons. All the scenes in a job can be
          added by selecting a job and clicking "Add All Selected
          Scenes In Job".
        BLG Files: Allows the user to paste the grade stacks contained
          within a directory of BLG files. This is an excellent way
          of restoring the grade pre-visualised on set using FLIP
          at the start of the final grade.

    - BLG Directory: When pasting BLG files, specifies the directory
      where they are to be found.

    - Resolve BLG Resource Conflicts By: Specifies how Baselight is
      to resolve file naming conflicts caused by inporting resources
      containing within a BLG file (Truelight profiles, cubes, looks
      etc). There are three possible strategies:
        Replace Existing Resources with BLG Versions: If there is
          already an existing resource with the same name as the
          resource contained within the BLG file, then the existing
          resource will be overwritten by the BLG's version.
        Use Existing Resources with the Same Name: If there is
          already an existing resource with the same name as the
          resource contained within the BLG file, the existing
          resource is used in the grade stack. In this case, the
          BLG's resource will not be imported.
        Import BLG Resources Under a New Name: If there is a naming
          conflict, then the BLG's resource will be imported using
          a name which doesn't conflict and the grade stack updated
          to reflect this.

    - Match Shots By: Allows the user to specify the metadata by
      which shots are matched with one another.

    - Paste: Specifies whether or not operators from layer 0
      (the top of stack) in the source shot are copied to layer 0
      in the destination shot:
        Stack Only (exclude Layer 0): Copy the source stack,
          but do not copy layer 0 operations - this matches the
          behaviour of multi-paste in previous versions of Baselight.
        Layer 0 and Stack: Paste *both* the source stack and
          the source layer 0 operators.
        Layer 0 Only: Paste *only* the layer 0 operators.

      When pasting of layer 0 operators is enabled, a dropdown
      appears allow the user to specify what happens to the existing
      operators in layer 0:
        Overwrite Layer 0 Operators: All destination layer 0
          operators are overwritten, other than "Sequence" and
          "Audio" operators.
        Append To Existing Layer 0 Operators: All destination
          layer 0 operators are retained and the copied operators
          are appended at the bottom, unless an operator occurs in both
          source and destination and the destination operator is in
          its default state - in that situation, the source operator
          will overwrite the destination operator in its existing
          location.

    - Source Stacks: Specifies what strips are to be copied from the
      source shots:
        Copy All Strips: All strips will be copied from the source
          stack.
        Copy All Strips Except Of Category..: All strips will be
          copied, except those tagged with one or more of the
          categories specified by selecting options in the "Choose"
          dropdown menu. Note that tagging a grade strip with
          an excluding category will result its matte also being
          excluded and vice versa.
        Copy Only Strips Of Category..: Only those strips tagged
          with one or more of the specified categories will be
          copies.

    - Destination Stacks: Specifies what strips in the destination
      shot, if any, are to be retained:
        Overwrite All Strips: All strips in the destination stack
          are to be removed prior to the paste.
        Overwrite All Strips, Except Strips Of Category..: All
          strips are to be removed, except those tagged with one or
          more of the categories specified.
        Retain All Strips: All strips will be retained.
        Retain All Strips, Except Strips of Category..: All strips
          will be retained, except those tagged with one or more
          of the categories specified.

    - When there is a chance of strips being retained in the
      destination stack, a dropdown appears allowing the user to
      specify where the new strips should be pasted, relative to the
      existing stack:
        Paste Above Existing Strips
        Paste Below Existing Strips

      KNOWN ISSUE: It is not currently possible to merge the layers of
      the source and retained destination stacks, the copied strips
      will all lie either above or below the retained strips. This
      merge functionality will be added in a future release.

    - Shred Composites Into Separate Shots: A single-stack composite
      is a composite where the timeline extent of the top side of the
      composite completely matches or overlaps the bottom. A standard
      foreground/background chroma-key would be a good example,
      whereas a dissolve transition would not.
      This setting specifies how these should be treated:
        No: The entire compositing
          stack will be treated as a single shot, with the metadata
          coming from layer 0 (top of stack).
        Yes, Except For Composites Of Category..: Each individual
          element of the composite will be treated as a separate shot
          and will be pasted separately, unless the compositing
          operator has been tagged with one or more of the categories
          specified. If a composite is shredded, the compositing
          operator which combines the shot will *not* be pasted. This
          is useful if the destination scene has an existing
          compositing structure and you simply wish to paste the
          grades.

    - Treat External Mattes As Individual Shots: Specifies whether or
      not external matte sequences (eg rotoscopes) are to be treated
      as separate shots, rather than being included as part of their
      top strip's shot. This is useful when the destination scene has
      an existing external matte structure (eg automatically generated
      scenes for CG animated movies) and you simply wish the copy the
      grades.

* Pressing "Multi-Paste" in this view will perform the multi-paste
  according to the settings specifies, with feedback being provided in
  the progress area. If multiple source scenes are specified, each
  source will be opened in order, a multi-paste performed and the
  scene closed. Once a shot has received a grade from a source scene,
  it will *not* accept a grade from any other subsequent scene.

* The Multi-Paste View now provides detailed feedback as to which
  destination shots had grades successfully pasted onto them and where
  those grades came from. Simply clicking on individual lines in the
  progress area will wrap the current cursor to the appropriate
  source/destination location. In the case of BLG file sources, then
  the Sequence Browser will be opened to display the BLG file in
  question. Pastes where there was no ambiguity will be marked in
  green. Pastes where multiple source shots matched a destination shot
  will be marked in orange, encouraging the user to check them
  carefully. If the source shot lies in a closed scene, the scene will
  be opened into a new cursor.

* Much like Timeline Sort, multiple tabs of different Multi-Paste
  settings can be stored in tabs of the Multi-Paste view.

* The Ctrl+m shortcut (Cmd+m on Mac) now simply applies the current
  Multi-Paste Views's settings without needing the view to be visible.
  The "Multi-Paste Mode" sub-menu in the "Edit" menu from previous
  versions of Baselight has been removed - all multi-paste settings
  are to be edited using the Multi-Paste View.

* The Multi-Paste View can be popped up/popped down using the Win+m
  accelerator (Ctrl+m accelerator on the Mac).

* Added a number additional filter types to Multi-Paste:
   - BLGName
   - BLGID
   - Clip Name
   - Avid UID: Very useful when multi-pasting between two
       different AAF conforms. Avid's media management
       is based around the concept of tagging media with unique
       identifiers (the UID), so the same media referenced by two
       different AAFs will typically have the same UID.
    - Case-invariant variations of a number of existing filters.

Timeline Sort
-------------

* Changed the appearance of the "Remove Strips Of Category" option to
  match the appearance of other category-related settings in other
  views.

* Renamed the "Composites" setting to "Shred Composites Into Separate
  Shots", and changed its options to match those in Multi-Paste View.
  Just like Multi-Paste View, it is possible to prevent a composite
  being shredded by specifying one or more categories from the
  "Choose" menu.

EDL Import
----------

* The "Copy Grades" setting has always used multi-paste internally to
  do the copy, and this is still the case. However, its behaviour has
  been changed slightly in light of the possibilities offered by the
  new multi-paste. When active, it now behaves like a multi-paste with
  the following settings:
    Layer 0: Paste Layer 0 and Stack.

    Source Shots: Copy All Strips

    Destination Shots: Overwrite All Strips

    Shred Composites Into Separate Shots: No

    Treat External Mattes As Individual Shots: No.

* Copying grades using different settings will need to be done as an
  explicit multi-paste using the Multi-Paste View.

Audio
-----

* Added support for AAC audio decoding from QuickTime files. This
  requires an additional license option, which is available at no
  extra charge. Please contact Baselight support for an updated
  license [bug 15471]

* Added support for AAC audio encoding when rendering to QuickTime or
  MP4 on Linux. This requires a additional license option, which is
  available at no extra charge. Please contact Baselight Support for
  an updated licence [bug 15471]

* Added support for discrete audio tracks when rendering to QuickTime
  or MP4 movies. In this mode, each audio channel is placed into a
  separate track in the movie file [bug 22018]

* Added support for specifying surround-sound channel layout when
  rendering to QuickTime movies with discrete audio tracks.

* Added constant offset parameter to Audio Sync view. This is a value
  in frames (accurate to one tenth of a frame) which is added to the
  audio offset when synchronising based on timecode. It allows for a
  constant delay between the audio and video to be compensated for
  during the automated Audio Sync process.

* Improved Shot Timecode, File Timecode and File Timecode 2 audio sync
  modes where audio file starts after the start of the image sequence.

* Added support for adjusting the Audio Offset for multiple selected
  shots via the Waveform View when Grouped Grading is enabled. This
  works for sliding the offset offset by dragging in the Audio
  Waveform view, and also when using the Nudge Audio Left/Right
  keyboard shortcuts.

Rendering
---------

* Rendering of H264 movies will now default to using multiple threads
  on machines with multiple cores [bug 22425]

* Added option to use Clip name from Shots View as the Tape name when
  rendering.

* Added %n and %{FrameCount} to render filename template; this is a
  counter which starts at 0 and increments regardless of the frame
  range(s) being rendered [bug 18642]

* Added support for file numbering expressions in Render View and
  bl-render. This extends the existing numbering options:
   %F - timeline frame number                - %{TimelineFrame}
   %T - timeline timecode                    - %{TimelineTimecode}
   %G - shot frame number                    - %{ImageFrame}
   %H - shot timecode                        - %{ShotTimecode}
   %E - timeline frame number at shot start  - %{ShotStartFrame}
   %U - shot timcode at shot start           - %{ShotStartTimecode}
   %n - rendered frame count                 - %{FrameCount}
  by allowing a mathematical expression to be used instead.

  Examples:
   %.6{F+2000}  - first frame on timeline renders to 002000
   %.7{F-E}     - each new shot starts numbering at 0000000
   %{F-E+1}     - each new shot starts numbering at 1
   %.5{F*2+100} - 00100, 00102, 00104 etc
   %.6{10001+n} - 010001, 010002 etc, regardless of frame range

File Formats and Codecs
-----------------------

* Added support for concatenating Canon C300 and Panasonic P2 clips
  that are spread across several MXF files [bug 23307, bug 22513]

* Sony F65RAW MXF files can now be decoded at 8192x4320, 7680x4320,
  8192x2160 and 6144x3240 resolutions, by setting an appropriate input
  format (note that this will be slow) [bug 22701]

Miscellaneous
-------------

* Added support for controlling which Baselight Kompressor (if any) to
  use when decoding QuickTime movies for images and audio:
    - Scene Settings View allows the Kompressor used by a scene to be
      changed.
    - Setups controls the setting for new scenes, and this setting is
      also used in the Sequence Browser and bl-browse [bug 15160]

* It is now possible to slide away the operator selection section of
  the Grade and Matte tabs to get more screen real estate on smaller
  displays. Simply click the small triangle to the left of the
  operator section.

* Added the ability to "Remove Strips Of Category" to the "Update FCP
  XML with Baselight Grades" Export panel. This is useful to remove
  Transform strips added as part of EDL Import, which we don't include
  when updating an XML, as it would result in the transform being
  applied twice (once by FCP itself and once by the Baselight plugin).

* The Machine Control view is now toggled up/down using the Win+v
  shortcut (Ctrl+v on the Mac).

* Added Circle Take column to Shots view. Circle Take data is read
  from ALEs when imported into Baselight, and can be written into
  ALEs. The value of the Circle Take column is also available in the
  burn-in editor using the %{SrcCircleTake} variable.

* Added support to Burn-Ins for original conform CDL values and
  current CDL values when using CDL-compatible video grades. The
  variables %{ConfASCSOP} and %{ConfASCSAT} can be used to burn-in the
  original CDL values taken from a CDL or ALE. The variables %{ASCSOP}
  and %{ASCSAT} contain the current CDL grade values being applied.

* Sony F65RAW MXF files now show the filename as both Clip and Tape
  metadata.

* Added support for using %U and %.#U when naming movie files to allow
  the shot start timecode, converted to frame number, to be used to
  generate a name for a movie file.

* Fixed "Add All Scenes in Folder" button in Multi-Paste source scene
  selection dialog so that scenes in all subfolders are also add to
  the list of source scenes.

* Added "Remove All" button to Multi-Paste source scene selection
  dialog.

* Added DVI 1920x1080 24p and DVI 1920x1080 25p video modes for
  DVI-only operation.

* The Sequence Browser "Insert Below" button has now been relabeled
  "Insert At Cursor" to better reflect its actual behaviour.

* The fl-ls tool has a new option -M, which displays all metadata from
  the listed sequences. The existing option -m is unchanged.

* "Raw Image Alpha Channel" is now an option in Preferences for the
  Reference default mode [bug 23477]

* Added support for Tangent panel trackball controls to Transform
  [bug 22688]

* Added "RGB Overlay" mode to the RGB Parade. This overlays the three
  waveforms over one another rather than side by side. This mode
  cannot be used simultaneously with the Luma Waveform or YCC Parade.

* Added "Overlay Intensity" to the Luma Waveform, RGB Parade, YCC
  Parade and Vectorscope. This allows you to change the
  brightness/intensity of the overlay.

* View layouts accessible through Blackboard numeric keypad "Views"
  mode are now available as individual Actions in Chalk [bug 22751]

* fl-rm now allows deletion of individual frames of a sequence, using
  the form fl-rm /vol/images/.../%.7F.dpx:100 [bug 23602]

* The Baselight version used to create and save scenes (where this is
  known) is now shown on the Job Manager.

* Added Chalk actions for Save, Save As and Close [bug 23803]

* Added new bl-timecode utility to report a scene's timeline start
  timecode [bug 23915]

Bug Fixes Since Baselight 4.3.5900
==================================

* If you cannot open a scene because all 9 cursors are active,
  Baselight now warns you before opening the scene [bug 23039]

* Fixed crash exporting FCP XML from a scene with a scene-local
  working format [bug 22278]

* Added names for several previously unrecognised decks, including
  XDCAM BluRay [bug 23250]

* Fixed memory leak with OFX plugin on-demand renders [bug 23313]

* Fixed bug in Timeline Sort where it wasn't possible to construct
  a "Sort By" order of "Directory", "Filename", "Frame Number".

* Removing strips from within a stack now deals much better with
  gaps between strips. Previously, gaps were never removed, leaving
  spurious space below remaining strips in the stack.

* Grabbing to the gallery no longer incorrectly grabs only the input
  layer if "Layer 0 Ops" is selected.

* "Include Input Strip" has been renamed to "Include Layer 0 
  Operations" to match cutview.

* fl-ls now gives the same results when invoked on a single image or
  movie as on a directory containing that file [bug 23372]

* Fixed crash in video grade when set to CDL mode and hitting reset on
  the Blackboard [bug 21533]

* Fixed compressor name for QuickTime movies written from Linux as
  shown in QuickTime Player's "Format" field [bug 21836]

* Fixed problem conforming against image sequences [bug 22202]

* Fixed behaviour of Decode operators (e.g. Sony RAW Decode) when
  copied and pasted into other shots [bug 23383]

* Fixed memory leaks that could occur in the DKey, Matte Tool and
  Tracker rops [bug 23423]

* Fixed crash in multi-paste which could occur if the copy data
  contained strips which had been deleted after the copy was done
  [bug 23426]

* Audio file types are no longer listed in the "File Types" dropdown
  in the EDL Import View.

* The "48@24fps" and "50@25fps" frame rate options no longer appear
  in the EDL Import panel when importing 24 and 25 fps ALE edls.

* fl-cp now reports the filename causing a "too many levels of
  symbolic links" error [bug 23425]

* Removed display of Tangent-specific desk layouts from Chalk tool, 
  selecting them would cause unexpected behaviour on Blackboard 2
  [bug 23424]

* Fixed crash when a filename template contains a very large field
  padding [bug 22516]

* Baselight now rejects filename templates with field padding more
  than 99 [bug 22516]

* Fixed crash when turning on mask and burnin, when gallery scene
  format doesn't have a mask of the same name [bug 23458]

* Updated firmware for 3ware cards 9650se and 9750 [bug 15234]

* Baselight ONE systems now run the raid3wareconfig diagnostic

* Diagnostics on Kompressors now warn if the myricom driver is
  older than version 1.3.3 [bug 23449]

* Fixed render failure in Sharpen through a matte when gain is zero
  [bug 23532]

* Fixed diagnostic hang on Mountain Lion kompressors. Note that Mountain 
  Lion is not yet a fully supported platform [bug 23565]

* Update 3ware toolset to 3w-9xxx.9.5.5.1 [bug 22557]

* The colour of some RAW-format files, such as Canon CR2, was
  previously occasionally stretched to fill the 16-bits available.
  This could cause flickering between frames. New scenes with these
  files now decode the images without scaling [bug 23443]

* Fixed crash reading some QuickTime files on Mac [bug 23574]

* Fixed caching of first frame of scene after deletion of source
  material [bug 23503]

* Fixed bug where taking finger off Ctrl first when splitting a strip
  with Ctrl+I(Toggle Mark) on Blackboard desks would also incorrectly
  drop a mark [bug 22940]

* Fixed incorrect interpretation of quicktime edit lists on Linux
  causing incorrect calculation of movie length, offset and frame rate
  [bug 22458]

* Fixed "Invalid audio channel layout index" error when rendering to a
  movie with audio.

* Fixed SSDs not having a SMART seek error count [bug 23296]

* Made flioinfo figures more consistent by replacing the fixed file
  count with one relating to the measured IO performance [bug 6449]

* Fixed issue where opening certain quicktime files would take a long
  time and produce lots of "skipping corrupted frame" errors in the
  console [bug 23680]

* Fixed crash when using %f in a sequence template [bug 23654]

* Added the profile or cube name to the error reported when loading
  the profile failed [bug 23720]

* Improved memory usage when an OFX plugin uses many images in an
  analysis pass [bug 23313]

* Fixed kOfxImagePropUniqueIdentifier in OFX plugins [bug 22475]

* Fixed crash on quit when multiple shots are selected in Cuts View
  and an overlay is active [bug 23679]

* Fixed shearing in Sony F5/F55 thumbnails in flux [bug 23463]

* Fixed initial selection in file panels, e.g. when browsing to
  replace stem audio files from Scene Settings [bug 23737]

* Fixed issue where the last frame in some MXF files would fail
  to decode [bug 23742]

* Fixed issue where Chalk-remapped left trackball bottom-left and
  bottom-right buttons stop working when a Shape strip is active
  [bug 23142]

* Fixes issues with scene creation (and Save As) in an imported job
  [bug 20762]

* Fixed crash opening System Monitor on Baselight PORTABLE [bug 23766]

* Fixed cancel button on OFX progress dialogs [bug 23767]

* Critical syslog errors are displayed in the Baselight alert panel
  [bug 13327]

* Fixed crash viewing gallery shots that were dragged from Cuts View
  [bug 23368]

* Fixed meta data of cached strips on clusters [bug 23818]

* Fixed UI issues preventing changing the channel list using the Channels 
  popup in the Audio Waveform view.

* Fix memory leak when rendering an audio file to a remote Baselight
  system [bug 22652]

* Fixed crash which could occur when scrubbing a thumbnail after
  grabbing to the Gallery via a drag [bug 23368]

* When user attempts to insert or appy a BLG created by a newer,
  incompatible version of Baselight via the Sequence Browser,
  Baselight will present a dialog box explaining that the BLG grade
  data cannot be loaded. The EXR image sequence will still be inserted
  into the timeline however [bug 23865]

* Fixed System Information diagnostic which was not including all 
  required information [bug 23866]

* XFS diagnostic checks the syslog for filesystem warnings which have
  appeared since xfs_repair was last run [bug 13327]

* Improve reliability of purr automatic wake-up of UI host [bug 22649]

* Added scrollbar to the Mark/Strip Categories preferences editor, to
  fix issues when there are many categories defined [bug 23894]

* Fixed transport controls on Avid Transport panels [bug 23872]

* Fixed crash in Audio Waveform view when the user attempted to adjust
  the audio offset by Ctrl-dragging in the audio waveform view with no
  active audio sequence in the timeline [bug 23902]

* Fixed "movie is not open" errors when rendering from a Baselight ONE
  to a global "mount" volume which is mounted on the same Baselight
  ONE [bug 23492]

* Fixed incorrect colours on some (e.g. yuv2 codec) QuickTime movies
  read by a Baselight Kompressor from a volume not hosted via a
  Baselight Kompressor [bug 23906]

* Fixed occasional failures to import scenes [bug 23974]

* Fixed memory leak when reconnecting to Blackboard 2 [bug 23123]
 
* Fixed Telecine Grade trackball reset buttons not being labeled on
  Blackboard 2 desks [bug 22669]
 
* Fix for incorrect trackball reset button behaviour on Tangent
  Element/Wave desks when editing parameters in triple slider mode
  [bug 23222]
 
* Fixed crash when holding the Mark key on Blackboard 1 [bug 22772]
 
* Reduced time taken to update Blackboard 2 ONE screens [bug 23262]
 
* Fixed error with Truelight profiles using lutLength{2} with
  outputDisplay [bug 22699]
 
* Updated Truelight library for improved handling of LUT files in
  non-Truelight formats [bug 23358]
 
* Fixed bug in StereoGrade which prevented picking to set the
  zero-convergence point when in Anaglyph, Interviewed, Checkerboard
  or Difference display modes [bug 22948]
 
* Fixed minor bug in bl-shots' "-replace" mode where it would
  incorrectly report the number of mappings it had read from stdin.
 
* Increased timeout checking licences at startup [bug 22555]
 
* Fixed broken behaviour of "+" and "-" buttons on Blackboard 2 soft
  keyboard numeric keypad [bug 22976]
 
* Fixed crash when pressing <Layer Matte> on Blackboard desks in
  Truelight Player application [bug 22771]
 
* Fixed CtrlLock on Blackboard 2 desks, now modifies encoder
  behaviour for fine-tuning values [bug 22849]
 
* Free space on pfs is now calculated as (number of nodes x minimum
  space on any node) to better reflect the usable space [bug 23069]
 
* Busy services can now be stopped more reliably, especially at
  shutdown [bug 23302]
 
* 3ware statuses of 'SMART-FAILURE' will now be reported in the
  appropriate diagnostic module [bug 23297]
 
* Fixed cache rechecking after an OFX plugin button press [bug 23270]
 
* Fixed some keyboard shortcuts on Baselight PORTABLE, notably
  anything using shifted number keys [bug 23021]
 
* Added support for OfxParamPropStringFilePathExists in OFX plugins
  [bug 22395]
 
* Changes to Render View presets are now saved immediately [bug 22990]
 
* The "Grouped Grade Stacks Above/Below" setting is now persistent
  [bug 22364]
 
* Fixed crash if the Gallery "Display UI Controls" preference was
  turned off [bug 22321]

--------------------------------------------------------------------------

Baselight Release 4.3.5900 (2013-03-28)

Bug Fixes Since Baselight 4.3.5877
==================================

* Fixed bug which could occasionally cause scene corruption after a
  grade containing external mattes was pasted from a large Gallery
  into a smaller scene [bug 23555]

* Fixed issue with rendering to 16-bit formats or using strip caching
  in conjunction with a transform or format mapping [bug 22764]

--------------------------------------------------------------------------

Baselight Release 4.3.5877 (2013-03-14)

New Features Since Baselight 4.3.5769
=====================================

File Formats and Codecs
-----------------------

* Added support for reading Sony F55 RAW and F5 RAW files [bug 21942]

* Added support for Linear RAW DNG files (e.g. Ikonoskop) [bug 22973]

Input Devices
-------------

* Added support for Tangent and Euphonix/AVID panels to Technical
  Grade [bug 22650]

* Added trackball support on Pan & Scan for Tangent and Euphonix/AVID
  panels [bug 22688]

* Added support for Tangent and Euphonix/AVID panels to Matte Tool
  [bug 22753]

Miscellaneous
-------------

* Added System Monitor View to monitor FilmLight applications
  accessing the disks on the local system [bug 23056]

* Added the ability to generate sequence thumbnails from the medium-
  or low-resolution proxy images, for use in workflows where the
  high-resolution sequences are not available. This is set in Scene
  Settings View; new scenes take this setting from the current Setup
  [bug 20820]

* Added support for variables such as %{Job} and %{Scene} in Truelight
  strip commands [bug 21104]

* Added the ability for grabs to the Gallery to be made when running
  at Medium/Low proxy resolutions, when the High resolution media is
  missing [bug 22810]

* Added -E option to pfs-verify to fix OpenEXR files previously
  rendered to a remote Baselight FOUR/EIGHT [bug 22803]

* Added support for reading packed 12-bit DPX files [bug 5458]

* Updated ALE export to support the the following new keycode gearings:
     35mm 4 perf frame offset (35.1)
     35mm 2 perf (35.2)
     35mm 8 perf (35.8)
     35mm 12 perf (35.12)
     16mm 40 perfs/foot (16.40)
     65mm 4 perf (65.30)
     65mm 5 perf (65.24)
     65mm 8 perf (65.15)
     65mm 10 perf (65.12)
     65mm 15 perf (65.8)
  The number in brackets is what will be written into the "KN Film"
  column for each gearing. Since the ALE spec has never supported any
  of these gearings, we had to invent these values by extrapolating
  from the existing keycode gearings:
     35mm 4 perf (35.4)
     35mm 3 perf (35.3)
     16mm (16.20)
  We did these using the following rules:
    - 35mm formats: 35.<perfs per frame>, other than 35mm 4 perf frame
      offset, which is a special case where frames are written into
      the DPX header's perf field by some scanners.
    - Other formats: <gauge>.<frames per foot>.

* Gallery grabs no longer fail if one or more of the input images are
  not present. This restriction was loosened to stop bypassed external
  mattes pointing to non-existant material preventing gallery grabs
  [bug 22908]

* Added support for Nvidia GTX650 and GTX680 GPUs [bug 21259]

* Added Truelight profile support to stereo viewing modes (interleaved,
  anaglyph, chequer & difference) [bug 22905]

* Shots View can now be sorted by strip name [bug 22933]

* Improved speed of reading unstriped image files (e.g. ARRIRAW) on
  Baselight FOUR/EIGHT systems [bug 22931]

* Baselight will automatically apply the correct audio resampling
  ratio when rendering a scene to a movie where the final movie frame
  rate differs from the output format frame rate (ie 23.976p movie
  from a 24.000p scene) [bug 22817]

* The on-disk image cache size preference can now be set as high as
  50TB [bug 22991]

* Updated combiner firmware for DVI2SDI, Reduced Four Port Combiners,
  Framestores and Original Four Port Combiners to support GTX 680 and
  GTX 650 GPUs. Systems with these GPUs will require the latest
  firmware installed on the combiners and framestores.

* Added option '-A' to pfs-verify to fix or regenerate pfs2 internal
  handle attributes [bug 22975]

Bug Fixes Since Baselight 4.3.5769
==================================

* Added additional node memory and cpu logging [bug 22588]

* Kill processes if machine is using half the available swap space

* Improved Gallery data structures to greatly improve grab speed in
  large galleries. Old galleries are updated to the new gallery
  structure when they are loaded into this version of Baselight. This,
  however, means that loading new-style gallery scenes into older
  versions of Baselight will result in the viewing format of
  thumbnails in the gallery being incorrect, if they were different
  from the gallery's native format [bug 20521]

* Prevented R3D thumbnails from being rendered using a RED Rocket,
  which will improve performance when playing and also addresses some
  thumbnail corruption issues [bug 21514]

* Fixed "Select" -> "Select By Strip Category" submenu category list
  (previously showed categories relevant only to marks) [bug 22615]

* Fixed potentially unlimited memory usage in image servers if network
  send is slower than data generation [bug 22652]

* Fixed reference counting in image servers that prevented render
  cancellation [22652]

* Fixed memory leak in GPU renderer [bug 22652]

* Fixed incorrect red stripe icon shown in Sequence Browser for
  OpenEXR files on Baselight FOUR/EIGHT systems [bug 22702]

* Fixed error in Matte curve which was causes a colour shift when a
  matte operator followed [bug 21245]

* Fixed problem that prevented -omit_last_recovery_delta from working
  if the last delta could not be processed [bug 22767]

* Fixed race condition that could cause Baselight to crash during
  startup [bug 18754]

* Fixed issues with on-demand rendering in OFX plugins [bug 22785]

* Fixed incorrect decode of RAW stills shot in rotated orientation
  with an odd number of pixels in one dimension [bug 22711]

* Fixed sensitivity of Tangent panel trackballs when editing shape
  parameters [bug 22752]

* Fixed reading Phantom Cine files with missing image header
  information [bug 22811]

* Fixed reading MPEG2 MXFs from nanoFlash [bug 22814]

* Fixed memory usage when reading some movies, notably R3D files read
  using a RED Rocket [bug 22744]

* Input focus handling has changed. The text entry caret and selection
  highlight should no longer disappear [bug 22047]

* Fixed "missing image" errors after switching the Input Format of a
  sequence to change resolution from high res to proxy or vice versa.
  Newly-inserted material should behave correctly; to fix existing
  sequences use the Update Sequence Behaviour button [bug 20820]

* Fixed corruption of Northlight alpha data when copying or rendering
  DPX file to a remote Baselight FOUR/EIGHT [bug 22687]

* Fixed creation of damaged OpenEXR files when rendering to a remote
  Baselight FOUR/EIGHT. In addition, Baselight can now read these
  damaged files without error [bug 22687]

* Fixed bug where pressing and holding the directional keys on
  Blackboard desks didn't scroll the DBS [bug 22488]

* Fixed problems with audio when playing 23.976 fps scenes on a
  24.000 fps display device [bug 21414]

* Fixed bug in Timeline Sort's "Sort By" setting, causing weird
  behaviour when attempting to use multiple sort criteria.

* Fixed bug that prevented fl-diag from completing when one or mode 
  nodes are down [bug 22707]

* Upgraded to libsamplerate 0.1.8, which improves audio resampling
  performance [bug 22815]

* Fix crash on startup when Tangent panels are enabled [bug 22749]

* Fixed colour shift on files from older Phantom cameras [bug 22840]

* Increased timeout for clients connecting to a licence server, to
  reduce errors under load [bug 22555]

* Fixed a bug in Timeline Sort's "Stack Repeats Vertically" which was
  causing the full merged extent of all repeats to not be included
  [bug 20986]

* Fix bl-nodemon which could wrongly show a node as unavailable 
  [bug 19484]

* Fix bl-nodemon which could consume memory when left in display mode
  for a long time [bug 22420]

* Updated to xfs_repair-3.1.9 [bug 22703]

* Fixed issue with TangentHub service that could prevent Tangent
  control panels from functioning on Linux systems [bug 22857]

* Fix crash when picking on an image with a Truelight profile enabled
  which did not load for some reason (error in profile or licensing)
  [bug 22827]

* Increased range of scope gain control [bug 22934]

* Renamed scope gain control to intensity and increased range. Added
  scale control (equivalent to gain control on hardware vectorscope)
  [bug 22934]

* Separated scopes playing and grading resolutions. Playing resolution
  will take priority when playing & grading [bug 22972]

* Fixed problem with Nvidia Version diagnostic failing to work on
  systems with 177.70.33 drivers [bug 22930]

* Fixed issue with installer complaining when installing on systems
  with new Nvidia driver versions [bug 22929]

* Fixed reading 50@25 and 60@30 fps timecode from MXF [bug 22422]

* Fixed /vol/images reads failing with an IO error if a processing
  node returns an invalid nfs reply [bug 22954]

* Fixed UI lock-up in flux, bl-browse etc when dragging a slider and
  moving the mouse beyond the edge of the window [bug 22881]

* Fixed problem in Scene Compare when comparing with cached strips. It
  no longer flags an error when strips are cached. However strips that
  are cached will be flagged if the corresponding strip is uncached as
  this could cause render differences [bug 22876]

* Fixed crash when using scene compare with an empty scene [bug 22946]

* Fixed Render View not updating scene name after Save As [bug 22964]

* Fixed issue in "Modify AAF" workflow, where large speed changes were
  combined with very small handle sizes, resulting in errors like
  "Unable to replace MXF clip in AAF file: Clip extent (xxx frames)
  too small" when producing the modified AAF. Timeline Sort now adds
  sufficient extra handles to speed-changed shots to ensure that they
  can be rendered and updated properly [bug 22666]

* Fixed issue with flickering black lines on Baselight FOUR/EIGHT
  combiner/framestore output when using GTX 680 GPUs [bug 22984]

* Fixed AAF relinking with swapped out clips, when the swapped in clip
  has different tracks from the conformed MXF [bug 21761]

* Fixed bug that would remove progress logs of processes that were
  running for more than 30 days [bug 22907]

* Fixed combiner firmware diagnostic check to validate correct
  firmware is installed when using GTX 650/680 GPUs [bug 22963]

* Fixed bug where using "Change" in the Sequence UI to swap in a new
  movie/image sequence (eg dropping in a VFX shot) would cause the
  Modify AAF workflow to fail [bug 21761]

* Removed the Audio Parameters and Audio Ratio menus from the Render
  View [bug 22817]

* Fixed the AVID Artist Color panel so that the transport buttons now
  work [bug 22822]

* Fixed behaviour of pop-up menus which cover the button that causes
  them to appear [bug 22953]

* Fixed application hang and large memory usage when scanning some
  AIFF and WAV files [bug 22926]

* Fixed caching of scenes after "Save as" [bug 23010]

* Fixed slow copying of uncompressed OpenEXR files [bug 22740]

* Fixed diagnostic that checks network switch configuration [bug 23037]

* Scenes using movies now begin playback more smoothly and shouldn't
  stutter [bugs 21005, 23059, 23138]

* Fixed importing FCP EDLs with empty clip names [bug 22823]

* Added support for Revision C of HP S5820X SFP+ switch [bug 23075]

* Added warning to fl-cp when copying OpenEXR files which aren't
  suitable for fast access in Baselight (RGB or RGBA half-float
  uncompressed with equal data and display windows) [bug 22740]

* Added additional debugging to detect spurious license failures
  [bug 22555]

* Fixed dotted line along left edge of CPU demosaic [bug 23117]

* Fixed hang in fl-cp when copying a directory tree containing several
  copies or versions of the same MXF media [bug 23190]

* Fixed delay starting up fl-ls [bug 23165]

* Fixed problem with configuring video modes when starting Baselight
  [bug 23187]

* On Supermicro H8DAi-2 systems, the hotfix service will now set up a
  MTRR register for NVIDIA graphics cards. This should improve
  reliability on this platform, after the next reboot [bug 22947]

* Improved memory usage after pressing play and then stop in the
  Sequence Browser [bug 23206]

* Improved stablity when grouped grading many R3D movies [bug 23216]

* Fixed handling of RGBA OpenEXR files loaded from PFS [bug 23247]

* Handle errors checking licences caused by unreadable .flic files in
  the licence directory [bug 22555]

* Fixed occasional connection failures in fl-diag [bug 23284]

* Fixed renderer crash with "Insufficient tiles to complete this
  render" [bug 22782]

* Fixed hang when scanning certain Phantom Cine files [bug 23405]

* Fixed crash in audio resampling code that could occur during
  playback when scene frame rate and display frame rate do not match
  [bug 23133]

* Fixed failure to generate thumbnails and/or low/medium resolution
  proxy images for input files supporting marker rectangles (Canon RMF
  and Sony RAW) [bugs 22775, 23257]

* Fixed crash scrubbing an empty thumbnail in Cuts View [bug 23408]

* Adjusted cache parameters for flood filesystem to improve
  performance on gen3 hardware [bug 23363]

--------------------------------------------------------------------------

Baselight Release 4.3.5769 (2012-12-20)

New Features Since Baselight 4.3.5720
=====================================

* Added support for Tangent Element and Tangent Wave desks. 

   Element Bt
   - Has two 12 button layouts [General] and [DBS] toggled with <B>
   - [General] contains Copy/Paste, Undo/Redo, Keyframe and Mark
     manipulation controls
   - [DBS] provides buttons for selecting and applying looks from
     the Gallery and Cutview

   Element Tk
   - 3 trackballs & rings with reset buttons map to colour wheel and
     master values in active strip

   Element Kb
   - 12 push button encoders map to values in active strip

   Element Mf
   - Transport controls
     - Hold <Stop> button and tap <Play> and <Reverse> for frame skip
   - Ring of trackball acts as shuttle control
   - Keypad can be latched to select Scratchpad slots, Cursors and
     Timecode values

   Wave
   - Transport & Shuttle Controls
   - 9 push button encoders map to values in active strip
   - 3 trackballs and master dials map to 2D values in active strip
   - Up/Down buttons move position of render row
   - Function buttons:
     - F1 Undo
     - F2 Redo
     - F3 UI/Image Screen Toggle
     - F4 Copy
     - F5 Paste
     - F6 Move Keyframes
     - F7 Previous Keyframe
     - F8 Next Keyframe
     - F9 Set/Unset KeyFrame

* Added selection of higher layers through double, triple, quadruple,
  etc. taps of desk Layer buttons.

  The number of layers skipped depends on the number of buttons active
  in the layout. E.g.

  Blackboard 1 desks (6 Layer buttons)
   - Double tap Layer 6 to get Layer 12
   - Triple tap Layer 6 to get Layer 18

  Blackboard 2 desks (standard Chalk layout - 10 Layer buttons)
   - Double tap Layer 6 to get Layer 16
   - Triple tap Layer 6 to get Layer 26

  Note: This feature is disabled by default. Enable and alter
  sensitivity of the tap behaviour with Blackboard Setup -> Layer
  Selection [bug 21421]

* Blackboard 2 Display View buttons (1x1, 2x1, etc.) now show the
  current mode they are in e.g. "2x2 Butterfly". The various modes are
  iterated through by using <Ctrl> + <1x1>, <Ctrl> + <2x1>, etc.

  The <1x1> button is now also used to swap between the various stereo
  modes (line interlace, checkerbox, etc.) when in a stereo scene.
  Stereo modes are unavailable in non-stereo scenes [bug 18824]

* Blackboard 1 & 2 - Extended "Shots" button to toggle between 
  various Play Range modes and the full scene.
   - No Modifier      - Current Shot
   - <Shift>          - Between Marks
   - <Ctrl>           - Selected Shots
   - <Shift> + <Ctrl> - Review Range [Bugs 19680 & 22184]

* Added support for rendering to MPEG-2 XDCAM HD 4:2:2 50Mbps using
  the "Sony MXF" filetype.

* Render View now has a button to copy the "First File" path to the
  clipboard.

* Added "Set Keyframe Toggle" action to Chalk [bug 22387]

* Added support for reading 4-channel ADX files (please note that the
  fourth channel is ignored) [bug 22431]

* Improved Mac OS 10.7 Kompressor performance when rendering to
  Baselight volume [bug 21751]

* Improved performance of Curve Grade & Video Grade when using custom
  curves [bug 22327]

* Cursor View now allows the current cursor's viewing format,
  resolution, mask, guide and Truelight profile to be set as the
  initial settings for the current scene and/or job [bug 17382]

* Added "Review Range" to Blackboard desks. Activate by pressing
  <Ctrl> + <Shift> + <Shot>. Also available as an action in Chalk
  [bug 19680]

* Improved debugging of image server processes. If the file
  "/usr/fl/etc/is_log" exists on a machine then details of the last
  2500 image server requests will be logged. If an image server
  process crashes this information will be sent back to FilmLight with
  the crash report [bug 22140]

Bug Fixes Since Baselight 4.3.5720
==================================

* bl-delete now works with scenes in folders [bug 22207]

* The rendering spinner on the Baselight menu bar no longer continues
  spinning after an aborted flip to the other eye [bug 22430]

* Image Transform Settings are now applied under an explicity-cached
  strip (from the Scene Settings or from an Image Transform Settings
  strip placed beneath the cached strip), to control the transform
  from the Working Format to the Viewing Format. Note that Image
  Transform Settings set above an explicitly-cached strip have no
  effect when the Input Format matches the resolution of the Working
  Format [bug 22433]

* Controls under the mouse now correctly react when they are moved,
  typically by the scroll wheel [bug 22105]

* Fix for crash when adding a custom button in Chalk after moving a
  workspace view while holding Windows key [bug 22403]

* Fixed bug which could cause a crash when switching between shape
  strips during playback [bug 16592]

* Fixed scene corruption bug when applying from gallery with blur in
  input strip [bug 22470]

* Fixed bug where it was possible to export Chalk layouts to non-
  existent USB sticks [bug 22254]

* "Switch Eyes" button on Blackboard 2 keypad when in Cursor mode is
  now disabled when in a non-stereo scene [bug 21890]

* Improved formatting of numbers on Blackboard 2 encoder readouts
  [bug 22434]

* Fixed some buttons being incorrectly labeled on Blackboard 2 ONE
  desks [bug 22479]

* Fixed bug where pressing and holding the directional keys on
  Blackboard desks didn't scroll the DBS [bug 22488]

* Fixed bug on Blackboard 2 where <Keyboard> toggle can disappear when
  in latched mode [bug 22535]

* Fixed colour of Phantom cine files from Miro cameras [bug 22562]

* Fix for slow clockwise encoder movements on Blackboard 2 & ONE desks
  not being reported. Run "bl-update-bb2" or "bl-update-bb2one" to
  upgrade desk firmware to latest version [bug 22564]

* Fix for <Ctrl Lock> + <Layer Up/Down> to change between stacks on
  Blackboard desks not working [bug 22496]

* Fixed OFX plugin progress dialogs [bug 22573]

* Fixed bug with .exr copy to PFS which created an invalid image if
  its height was not a multiple of the node count [bug 22070]

* Fixed crash rendering complex scene to EXR files [bug 20589]

* Fixed 100% CPU usage in image server processes [bug 22375]

* Fixed 'xinetd flood reader is not responding' errors caused by a
  too-short timeout in the pfs2 diagnostic [bug 21553]

* This release will disable NVIDIA PAT on Supermicro H8DAi-2/H8DA3-2
  motherboards running Flos 2.1. PAT could trigger occasional node
  freezes with this combination of hardware & software [bug 21644]

* Fixed failure to get licences from a licence server under heavy
  load; added additional debugging to report licence server errors
  [bug 22555]

* Optimised MXF multi-track audio reading [bug 22458]

* Prevented R3D thumbnails from being rendered using a RED Rocket,
  which will improve performance when playing and also addresses some
  thumbnail corruption issues [bug 21514]

* Fixed hang when using fl-cp to copy folders containing sequences
  with '%' in their names [bug 22617]

* Fixed hang when rendering some long scenes to movies [bug 21951]

* Fixed OFX plugin path on Mac OS X [bug 22556]

* Fixed conforming new Avid flip/flop effects [bug 20362]

* Blackboard 2 Button Demo now works again [bug 22574]

* Fixed behaviour of JL Cooper MCS3 and Spectrum panels [bug 22471]

* Improved Blackboard 2 Jog Shuttle timeline navigation. Frame Step
  mode has no notch resistance by default and is more responsive at
  low speeds [bug 22478]

--------------------------------------------------------------------------

Baselight Release 4.3.5720 (2012-11-19)

New Features Since Baselight 4.3.5617
=====================================

Chalk - for Blackboard 2
------------------------

* A customisation tool for use with the Blackboard 2 control surface
  to control the position and functionality of buttons. It allows
  users to select between preset layouts, create their own unique
  layouts and edit the functionality of individual buttons.
  
  Layouts can be transferred between systems via USB storage devices.
  
  The Chalk tool is opened via "Chalk - for Blackboard 2" in the
  "Baselight" menu.
  
  For detailed user instructions please refer to "Chalk Setup" in
  Chapter 5 of the Baselight Reference Manual.
  
ALE Functionality
-----------------

* Conform from Avid Log Exchange (ALE) files is now available on all
  Baselight systems (and no longer requires a preference change to
  enable it).

* "Lab Roll", "Camera Roll", "Camera", "Shoot Date" and "Comments"
  columns are now read from ALE files.

* There is now an option for a "Duration" column to be written in ALE
  files. The duration is the timecode difference between the "Start"
  and "End" columns.
  
Scene Compare View
------------------

* There is a new view, Scene Compare, which compares 2 scenes for
  differences in the render. This can be used as a QA tool to find
  shots that changed in different versions of a scene. You can select
  different rendering modes and categories to include or exclude.

  For detailed user instructions please refer to "Rendering and
  deliverables" in Chapter 4 of the Baselight Reference Manual.

Miscellaneous
-------------

* Baselight software on Mac OS X (Baselight PORTABLE and Baselight
  Kompressor) is now 64-bit.

* Added burnin metadata for shot length in frames (i.e. the length of
  the topmost strip in the stack).

* Added support for reading and writing MXF movies using the DNxHD
  "DNx100" codec.

* Shots View's "Fixup" operation fixes up a Sequence strip's Timecode
  and Keycode by reading the file headers of a sequence of images. It
  is now statistical in nature, determining all the chunks of timecode
  and keycode within a sequence of frames and picking the largest ones
  to apply to the entire strip. This is especially useful in film
  dailies workflows, where the first few frames of a clip may have
  invalid keycode, due to the time taken for the scanner's keycode
  reader to switch between camera rolls.

* Timecode 2 is now generated for Phantom cine movie files, using the
  same time-of-day algorithm as other sofware. However the Resolve
  timecodes vary depend on the frame rate of the project. At present
  Baselight always generates 30fps timecodes. A future Baselight
  release may allow this to be adjusted.
  
* Timecode frame rate for movies (when it is known, for example for
  Phantom cine) is now shown on the Sequence Browser.
  
* Avid MXF exports now include Labroll.

* Added the option to set a movie's Clip name from the Camera Roll
  metadata.

* Added options to select marked frames by category on Render View and
  in bl-render.

* Added support for writing AVI movies using the "10 bit packed YUV
  4:2:2 (v210)" codec.
  
* Added ability to playback just the selected shots.

* Updated four-port combiner firmware adds support for 720p at 30,
  29.97, 25, 24, and 23.976 fps. Use the bl-combiner-upgrade
  tool to upgrade the firmware if you require this functionality.
  
Bug Fixes Since Baselight 4.3.5617
==================================

* Baselight and Truelight Player no longer crash when run on a
  Baselight Kompressor [bug 21855]

* Fix potential crash in stereo geometry fix when input format and
  scene format are very far apart in width & height [bug 21571]

* Licence diagnostic no longer warns about using "master" as a server
  name [bug 21723]

* Using the "Change" button to replace a sequence no longer prevents
  it from being used with Modify AAF/XML workflow [bug 21761]

* Tetrahedral Interpolation mode in Truelight strips can now be
  updated using Group Grading [bug 21217]

* Added a Disable switch to the Truelight controls in the Cursor view.
  This allows enabling and disabling of an active profile or cube
  without having to change the list selection [bug 21700]

* Fixed bug where pressing the UI/Image button when starting Baselight
  could cause the application to crash [bug 21496]

* Fixed crash using Mattetool with Euphonix desk [bug 21451]

* Fixed crashes caused by Cuts View retaining control over the
  Blackboard balls after finishing a preview [bug 21719]
  
* Fixed right-click Reset Operator Entry on the current selection in
  Inside/Outside [bug 21391]
  
* Matte Tool now selects a newly-created stage [bug 21378]

* Fixed crashed caused by switching between Matte Tool while changing
  values on the Blackboard [bug 21166]
  
* Fixed bug which could cause a crash if 'trying' a grade from the
  Cuts View/Gallery while simultaniously adjusting an encoder from the
  Blackboard [bug 20945]

* Fixed crash when selecting a new preset for a strip with grouped
  grading enabled [bug 20981]

* Fixed bug which could cause crash on 'Try' key from the Blackboard
  [bug 21601]
  
* Fixed bug which could cause a crash if turning encoders whilst
  simultaneously switching pages in HueShift [bug 18781]

* Disabled the cache size warning popup when timeline caching is set
  to 'Disabled' [bug 21590]
  
* Fixed crash when 'try'ing a grade from the cutsview/gallery
  containing a shape strip (have to explicitly select the shape strip
  while the 'try' button held down) [bug 20435]

* flux/fl-cp now continues to copy non-image files after encountering
  a copy error [bug 21950]
  
* Fixed clipped text for Videograde "Black & White Pivots" on
  Blackboard 2 [bug 21278]

* Fixed bug where Blackboard 2 Layer Graph View would sometimes not
  update when switching between scenes [bug 21086]

* Added support for bl-export to export an empty job, and for
  bl-import to import it [bug 21974]

* Baselight no longer runs diagnostics when started with -i, -help or
  --help options [bug 21977]

* Fixed signal masking for replay [bug 21899]

* Avid MXFs are now written using Shot Keycode, taking account of its
  gearing [bug 11027]

* Fixed events showing as zero-length in some ALE files [bug 21939]

* In Stereo ALE export, fixed up the "Start/End Timecode" option
  appearing blank when it first popped up [bug 21938]

* In Stereo ALE export, fixed the "Labroll_l" and "Labroll_r" columns
  not being populated properly [bug 21938]

* Fixed a crash in ALE export with 3:2 pulldown [bug 21939]

* Fixed a bug in ALE export where, when "Retain ALE Import Metadata"
  was switched on, columns which had been explicitly disabled still
  appeared in the exported ALE, if they were present in the ALE the
  scene was conform from [bug 21938]

* Fixed failure to read some MXF files (e.g. from Sony F3) [bug 21969]

* Fixed errors with GPU rendered histogram [bug 21967]

* Added support for 'fluxstore' flag in cloud.cfg [bug 21988]

* Modified the Truelight strip user interface to provide a drop down
  list of profiles and cubes in the default folders, along with a
  browse button to access other files [bug 21776]

* Fixed crash when reading a damaged JPEG2000 DPX file [bug 21996]

* Fixed incorrect render of stacks containing cached strips when
  cropping to a mask [bug 21943]

* Fixed issue with Curve Grade when creating a discontinuous Hue curve
  and colours with zero saturation [bug 22004]

* Fixed "discontinuous timecode" warning when rendering using Record
  timecode [bug 21409]

* Fixed timecode writing to QuickTime on Mac OS X when the timecode
  rate is different from the movie frame rate [bug 21750]

* Fixed handling of negative timecodes in QuickTime movies by wrapping
  them at 24h [bug 21386]

* Fixed reading QuickTime movies with two timecode tracks on Linux
  [bug 21386]
  
* Fixed capitalisation of Shoot Date in Avid MXF export.

* Fixed crash occuring with particular resolutions (e.g. 1998x1080)
  when using strip caching [bug 18433]

* Fixed R3D timecodes for movies running at over 30fps [bug 22019]

* Fixed format editor behaviour when editing the translation of a
  reverse mapping that had non-unity scaling [bug 22028]

* Added toggle for reversing direction of Blackboard 2 Jog Shuttle
  control, to use with new redesigned hardware [bug 21953]
  
* Fixed issue where fl-diag would occasionally complain about a lack
  of valid display when connected to a Blackboard 2 ONE [bug 20916] 

* Fixed timecode range in Sequence Browser (and set as Shot Timecode)
  when using "List Timecode 2" [bug 22044]

* Changed QuickTime timecode reading on Linux to wrap at 24h to match
  behaviour of Mac OS X. This will change timecode read from some
  Canon 5D movies for example [bug 21075]

* Fixed loss of channels and/or BLG information when copying
  multichannel OpenEXR images with flux/fl-cp [bug 22057]

* Fixed error when inserting proxy-resolution sequences to a scene,
  and then adding full-resolution images [bug 22084]

* Fixed issues with GPU resource not being returned to Baselight after
  two bl-render commands are run [bug 22091]

* Updated DVI2SDI firmware addresses failure to genlock. Use the
  bl-combiner-upgrade tool to upgrade the firmware if you require this
  functionality [bug 21896]

* Fixed issue with Bars not rendering in bl-render to certain formats
  [bug 22096]

* Fixed bug which could result in incorrect renders at the start of a
  temporal degrain through a matte (could also cause a crash if
  background caching enabled) [bug 21230]

* Fixed bug which would prevent marks from being displayed for
  sequences with a frame increment of 0 [bug 22099]

* Fixed reported duration of QuickTime/MP4 files with negative
  information in stts atoms [bug 22151]

* Fixed hang when rendering with "Use Input Format" [bug 22153]

* Increased speed of copying OpenEXR files [bug 21966]

* Fixed crash in renderer with Feathered Shapes and invalid render
  string [bug 22024]
  
* Fixed memory leak in matte tool menu building [bug 22186]

* Fixed memory leak in video grade menu building [bug 22188]

* Fixed crash when switching to Y'CbCr in CDL mode [bug 21968]

* Fixed conform failure when using media accessed via a Baselight
  Kompressor [bug 22137]

* Fixed crash in colour match [bug 22181]

* Fixed Edge Crop CPU rendering misbehaving using Temporal Degrain and
  DSpot in the same stack [bug 22217]

* Fixed issue with memory usage growing over time when selecting and
  unselecting Matte Tool strips [bug 22192]
  
* Fixed issue where "Keyboard" button on Blackboard 2 desks could
  obscure characters of the soft keyboard when enabled [bug 22175]
  
* Underscore key is now always displayed on Blackboard 2 Soft Keyboard
  [bug 21557]
  
* Added a diagnostic to flag if USB connection to a Blackboard 2 ONE
  running at a slower speed than required [bug 21575]
  
* Fixed functionality of Delete All Marks and Split/Join Strips on
  Toggle Mark button on Blackboard 2 [bug 22235]

* Enabled Sharpen operators in the Input strip in Truelight Player and
  Baselight TRANSFER [bug 22235]

* Fixed crash caused by reading a damaged DNG file [bug 22344]

--------------------------------------------------------------------------

Baselight Release 4.3.5617 (2012-09-24)

New Features Since Baselight 4.3.5546
=====================================

* Added 48fps and 48@24fps timecode options.

* Added additional metadata support (including timecode) when reading
  CinemaDNG files.

* Sony SStP MXF files can now be read and written on older Baselight
  hardware which used AMD CPUs.

* Added ability to write Sony MXF using SStP/L2 SR HQ 4:4:4 at 10- and
  12-bit, and for writing 2048x1080 in SStP/L2 SR SQ 4:4:4 at 12-bit.

* Significant improvements to DNG decoding quality, speed and user
  controls. Existing strips can be updated using the "Update Sequence
  behaviour" button (next to the Sequence File Name).

* QuickTime and MP4 movies can now be optimised for "fast start"
  (streaming) playback. This will increase rendering time,
  particularly when rendering long movies.

* Added support for reading Indiecam RAW data stored in QuickTime
  movies. Because the movie contains nothing that distinguishes it
  from a "v210" uncompressed 4:2:2 movie, a new Indiecam Decode
  operator is added in Baselight to allow you to choose the encoding
  and camera model.

  PLEASE NOTE This should be considered "beta" functionality until
  advised otherwise. Support for white balance, tone curve, sharpening
  etc may be added in a later release. If you encounter issues please
  report them to baselight-support@filmlight.ltd.uk

* The de-mosaic algorithm has been improved. The algorithm preserves
  the original mosaic values, but the interpolations look sharper and
  have fewer coloured artefacts. The cross-coupling filter has the
  same effect with the same threshold values; but turning the filter
  up may now undo our new sharpness, so we recommend only turning up
  the cross-coupling filter for the images that need it. Chromatic
  aberration in the camera can still give some patterns, but the
  effects are now more subtle.

* The ARRIRAW default crosstalk setting has been changed from 0.0 to
  0.3. This is enough to remove the maze patterns seen in pinks and
  some other colours in the worst cases we have met. Increasing the
  crosstalk filter setting further will lose some high-frequency
  information. If your images have fine detail, and no flat patches of
  saturated colour, then you may want to reduce the crosstalk setting.

* Inserting ARRIRAW files now adds a Sharpen operator to the Input
  Layer. This should give a similar sense of sharpness to ARRI's ARC
  tool. If you remove the Sharpen then the image will contain the
  original mosaic pixel values.

Bug Fixes Since Baselight 4.3.5546
==================================

* Fixed crash in video grade when set to CDL mode and hitting reset on
  the Blackboard [bug 21533]

* Fixed edge errors from Pan&Scan of ARRIRAW material [bug 21556]

* Fixed errors after deleting and then recreating a job [bug 21606]

* Fixed job deletion after unlocking scenes [bug 21615]

* Improved robustness of shader cache [bug 21618]

* Fixed issue when using scopes with a viewing mask on multi-node
  systems [bug 21485]

* Fixed increasing memory usage when reading movies on multi-node
  systems [bug 21715]

* Fixed hang after an error rendering to QuickTime via a Baselight
  Kompressor [bug 21728]

* Fixed black stripes on clusters when interactively editting above a
  cached strip [bug 21729]

* Fixed crash when using %c substitution in Shots View [bug 21732]

* Fixed regression in VectorScope rendering [bug 21733]

* Disabled background caching when mouse/pen in motion on image
  display [bug 20635]

* Fixed crash on startup when running bl-render on Mac OS X 10.5
  Leopard [bug 21467]

* Fixed render failures in scenes using temporal strips (Temporal
  Degrain, DSpot etc) under explicitly cached strips [bug 20871]

* Fixed crash in flux/fl-cp when converting movies without a "." in
  their filename [bug 21736]

* Fixed reading Avid MJPEG 2:1p MXF files.

* Fixed bug which could cause a scene to be un-openable after applying
  a stack from another scene containing strips with marks [bug 21806]

* Added 0203 Keycode prefix.

--------------------------------------------------------------------------

Baselight Release 4.3.5546 (2012-08-21)

New Features Since Baselight 4.3.5530
=====================================

* Added support for using %P for clip name when editing Name and Tape
  fields in Shots View.

* Added support for utilising RED Rocket cards in several machines;
  typically one in each node of a Baselight FOUR or EIGHT. To
  configure this, edit /usr/fl/etc/cloud.cfg and add the 'redrocket'
  flag against each machine containing a RED Rocket.

  It is also possible to configure other Baselight systems to make use
  of multiple machines containing RED Rockets by adding multiple
  hostnames to an 'option redrocket' line in /usr/fl/etc/cloud.cfg.

* Added support for reading Canon C500 RAW data in RMF and DPX files.

  PLEASE NOTE this should be considered "beta" functionality until
  advised otherwise. If you encounter issues please report them to
  baselight-support@filmlight.ltd.uk

Bug Fixes Since Baselight 4.3.5530
==================================

* Layer Manager now shows "T" when current layer is a Tracker strip
  [bug 21306]

* Fixed issue with Blackboard 2 buttons not updating in rare
  circumstances [bug 21528]

* Fixed memory leak on multi-node systems

* Fixed keyframe movement using Ctrl+[ and Ctrl+] not ending properly,
  causing subsequent arrow key presses to continue moving keyframes
  until a different operator was selected [bug 21561]

--------------------------------------------------------------------------

Baselight Release 4.3.5530 (2012-08-08)

Bug Fixes Since Baselight 4.3.5524
==================================

* Fixed bug with audio timecode calculation that could cause
  repeated audio timecodes [bug 21465]

--------------------------------------------------------------------------

Baselight Release 4.3.5524 (2012-08-03)

New Features Since Baselight 4.3.5416
=====================================

* This release has required a database version increment. This will
  prevent scenes saved from this version of Baselight from being
  opened in previous versions of Baselight.

Area Tracker
------------

* It is now possible to rotate the tracking rectangles on keyframes.
  This can be done by either dragging the tracking box pivot overlay
  or by using the middle trackball ring.

* The 'new AT' button on the shape strip can now create a rotated
  rectangle to best fit the original shape.

* The 'Trackers' and 'Area Trackers' tabs in the tracker strip are now
  highlighted in purple when they contain trackers.

* You can now link a tracker to an existing shape or a transform using
  by:
   - Selecting the tracker you want to copy.
   - Tapping 'Copy' on the Blackboard (or Ctrl+Shift+C on the
     keyboard).
   - Selecting the shape/transform you want to apply the tracker to.
   - Tapping 'Paste' on the Blackboard (or Ctrl+V on the keyboard).

Sander
------

* Added new Sander operator. It is accessible either from the 'Insert'
  menu or the Matte Tool.

  Sander allows to remove speckles (white regions inside a black one)
  and holes (black regions inside a white one) without modifying the
  geometry of the matte. It uses the following parameters:

   - Search Size: Distance in pixels from the central pixel, defining
     region to consider. The search size varies from 0 to 4, with 0
     doing nothing. Increasing the size tends to remove bigger holes
     and speckles. The maximum radius can be increased to 10 using
     'Extended Ranges'.

   - DSpeckle: Threshold allowing to select the speckles in the matte
     for removal. Increasing this value will remove more speckles.

   - DHole: Threshold allowing to select the holes in the matte for
     removal. Increasing this value will remove more holes.

   - Colour Difference: Threshold allowing to control the amount of
     work produced by the two previous thresholds. Increasing the
     Colour Difference increase the amoung of work done by the
     previous threshold.

Scopes Improvements
-------------------

* Pan/Zoom: The scopes can reflect the visible portion of the image
  when panned & zoomed in the display. This is user selectable by
  selecting the Pan/Zoom option on any of the scopes right-click
  context menus.

* Truelight/Combiner: The scopes can reflect either the raw image,
  with the cursor's Truelight profile applied, or both Truelight and
  combiner settings.

* Luma/Chroma waveform: The Luma Waveform has an optional Luma/Chroma
  mode, which displays the chroma components overlaid on the luma.
  (This can't be used at the same time as the Y'CbCr Parade though and
  that view will display an error cross).

* Vectorscope rotation: The Vectorscope can be rotated +/- 180
  degrees. To match the default trackball orientation, apply a
  rotation of -13 degrees.

* Chromaticity scope: Variant of the Vectorscope, selectable from the
  Vectorscope context menu. This maps colours within the selected
  gamut, either Rec709, EBU, SMPTE-C, or P3 (either RGB or XYZ) mapped
  onto a CIE xy plot.

* Video Legal Overlay: The waveform overlays can be set to display
  either video legal or full range markings.

Performance Improvements
------------------------

* Improved perfomance of reading movies that are stored on the PFS
  (parallel file system) of a Baselight FOUR/EIGHT. A fast-access
  read-only view of /vol/images is now available under /pfs/images for
  this purpose. (This functionality requires FLOS 2.1 or later.)

* Increased speed of browsing scenes using Job Manager and
  bl-lsscenes, particularly when accessing jobs stored on remote
  database servers and/or calculating scene sizes.

* Improved performance of intermediate caching on Baselight FOUR/EIGHT
  systems.

Image Decode Improvements
-------------------------

* Improved smoothness of ARRIRAW ALEXA tone curve

  The previous LUT-based tone curve has been replaced by a function.
  This is very similar to the earlier tone curve but smoother.

* Added Nyquist Filter 'Coloured pixels' option

  De-mosaiced images can show coloured features on bright highlights
  and sharp edges. Here, the brightness changes over a pixel or two,
  and there is not enough data to reliably guess the missing colour
  values. You can also get strange colour values when de-mosaicing
  images with chromatic aberration, as the colour channels are not
  correlated accurately.

  The new filter is like a median filter on the chroma channels. It
  will make a pixel neutral if it has a neutral neighbour. This
  removes much of the strange coloured fringes. This will remove real
  image detail too, so if you use it, check the effect on the rest of
  your image.

* Improved Colour Crosstalk Reduction filter

  Most digital cameras have alternate lines of red and green pixels,
  and green and blue pixels. If there is some A/D conversion
  difference between odd and even lines, this can give 'maze' patterns
  on the de-mosaiced image.

  The de-mosaic crosstalk filter will average the values if the green
  values are some threshold outside the range of the green values of
  the neighbouring lines. Turn up the filter threshold and the 'maze'
  patterns should go away. This can remove some real image detail too,
  so if you use it, check the effect on the rest of your image.

* Improved SIV support

  SIV files now apply the default Silicon Imaging colour transform to
  bring the colour primaries to Rec.709.

  Log-format SIV files are now converted to linear when read into
  Baselight in order to be able to correctly apply the white balance
  and colour transform.

* Improved de-mosaic algorithm

  The de-mosaic algorithm (used on RAW images such as ARRIRAW, Phantom
  Cine, SIV etc) has been modified slightly to give better results for
  sharply-varying features very close to highlights.

* Improved CR2 support

  Some previously unreadable "RAW" still files (e.g. Canon sRAW/mRAW)
  are now supported. (These files contain lossless Y'CbCr subsampled
  data rather than raw sensor data.)

* Added CinemaDNG support

  Baselight can now read CinemaDNG MXF files.

* Improved DNG support

  DNG (Adobe Digital Negative) files are now decoded using the Adobe
  reference SDK. A new DNG Decode operator allows control of exposure,
  shadow clipping and colour temperature.

  PLEASE NOTE this may change the appearance of existing scenes that
  use DNG files. You may wish to finish work on these scenes using
  your previous Baselight version rather than update them.

* Correction to F65 RAW tone curves

  The exposure of Sony F65 RAW material decoded to Linear and Log
  (previously called ACES Log) tone curves has been corrected to make
  them slightly darker.

  PLEASE NOTE this will change the appearance of existing scenes that
  use F65 RAW material with Linear or ACES Log tone curves. You may
  wish to finish work on these scenes using your previous Baselight
  version rather than update them.

Miscellaneous
-------------

* Directory and filename templates in Render View and bl-render can
  now use %{ISODate} to insert the current date. Several existing %
  substitutions now have %{...} alternatives which can be used for
  clarity, as shown in bl-render command-line help, or the help panel
  on the Render View.

* Added ability to set Reference strip's default input mode to
  "Previous Layer's Output" and "Previous Layer's Input Image" from
  the preferences ("Plugins" page).

* Added bookmarks menu to Job Browser.

* When run on the command line, fl-diag now shows module identifiers.

* Added support for reading high frame-rate (HFR) Sony F65 MXFs.

* Added support for DCI 2048x1080 48p and HD 1920x1080 48p display
  modes.

* Added initial support for writing Sony SStP MXF files.

  PLEASE NOTE due to restrictions in the Sony libraries used by
  Baselight, this functionality currently only works on machines with
  Intel CPUs, which means it will not currently work on older
  Baselight hardware which used AMD CPUs. This restriction also
  applies to SStP MXF decoding.

  PLEASE NOTE SStP writing should be considered "beta" functionality
  until advised otherwise. If you encounter issues please report them
  to baselight-support@filmlight.ltd.uk

* Added ctrl+0 shortcut for Gang Cursors (previously available in
  Truelight Player but not in Baselight).

* The preference "In-memory image cache size" which specifies the
  amount of memory used for caching images has been changed from an
  absolute value to a percentage of available memory. This change
  allows better default memory usage across a range of hardware.

* When conforming from ALE, Scene and Take metadata are now set in
  Shots View.

* Shots View can now be sorted by Clip.

* After long deliberation and due to popular demand, drag-and-drop
  shot movement in the Cuts View is now disabled by default. It can
  be re-enabled by switching on "Allow Drag-and-Drop Shot Movement"
  in the "Cuts View" section of the preferences.

* Added support for Nvidia GTX 680 GPUs.

* Added MP4 to the "Sequence types cached in input strips" preference.

Bug Fixes Since Baselight 4.3.5416
==================================

* Multi-Insert now turns "Use Timecode 2" on if the browser was set to
  "List Timecode 2" [bug 20930]

* Uptime now correctly reported in bl-nodemon [bug 20717]

* Fixed bug which would cause strips with explicit caching enabled to
  be cached during playback when Timeline Caching set to "Disabled"
  [bug 20964]

* Diagnostic network tests are now bidirectional [bug 20795]

* Fixed problem exporting LUTs from the Shots view when image
  sequences had Orientation set to Flip or Flop [bug 21019]

* Fixed conform issue when using 'Tape Name in Header' and remote
  conform was in use [bug 20803]

* Fixed Mattetool so it now uses the trackballs [bug 21105]

* Fixed crashes caused by invalid filename templates in a Sequence
  [bug 21110]

* Fixed rendering of Dissolve through matte when one source image is
  empty [bug 20868]

* Fixed crash in MatteTool when added without a Blackboard attached
  [bug 21123]

* Fixed errors when reading SIV files over 4GB in length.

* Removed the Burnin settings from the tl-player Cursor View as the
  Player licence does not support burnins [bug 21136]

* Fixed crash in shapes which occured after creating a tracker from a
  large shape [bug 20279]

* Fixed crash with changing multiple stages in the Mattetool while
  changing the gang [bugs 20290, 20384]

* Fixed issue where bl-config-xorg could fail to identify when a
  Blackboard 2 desk was connected [bug 21060]

* Worked around write hang in StorNext 4.2.2 SAN driver [bug 21034]

* Fix for Flow Degrain with a matte and bypassed [bug 21212]

* Fixed incorrect pulldown renders when using explicitly cached strips
  [bug 21204]

* Fixed issues with VTRE using DDR decks [bug 17426]

* Fixed "Raw Image Alpha Channel" in Reference strip when it is used
  as a matte input to a strip at the bottom of the stack, or as an
  input to a Dissolve [bug 18107]
  
* Fixed several issues using bl-proxygen on compressed OpenEXR files
  [bug 21238]

* Fixed failure to show a folder containing a single folder when
  browsing for a folder (e.g. EDL search directory) [bug 21154]

* Fixed tone curve shift caused in a Matte Tool using a Matte Curve
  before a Blur [bug 21245]

* Fixed occasional render out hangs when rendering to many short
  movies [bug 21256]

* Fixed bug in playback cache icon when toggling input strip caching
  on/off with Timeline Caching disabled [bug 21272]

* Fixed bug which could result in unrecoverable scenes if Blackboard
  toggle keyframe button pressed while creating a second shape in a
  Shape strip [bug 21280]

* Fixed loss of alpha channel when copying 8- or 10-bit RGBA DPX files
  using flux or fl-cp.

* Stereo Geometry Fix - fixed additional X/Y-translate not working for
  very small translations without having a prior fix [bug 21337]

--------------------------------------------------------------------------

Baselight Release 4.3.5416 (2012-06-25)

Bug Fixes Since Baselight 4.3.5401
==================================

* Fixed issue with retrace errors causing Baselight audio playback to
  drift out of sync [bug 20938]

* Fixed issue with audio not staying in sync when jumping between
  shots in timeline then pressing play [bug 20969]

* Fixed occasional stall in rendering to movies [bug 21041]
  
--------------------------------------------------------------------------

Baselight Release 4.3.5401 (2012-06-18)

Bug Fixes Since Baselight 4.3.5387
==================================

* Fixed memory leak using "Cache Strips only" on a Baselight FOUR or
  EIGHT [bug 20978]

* Fixed hang when rendering file to cache [bug 20983]

* Fixed incorrect caching indicators (green line) [bug 20984]

* Fixed strip caching when used with varying output formats for
  Pan&Scan [bug 20982]

--------------------------------------------------------------------------

Baselight Release 4.3.5387 (2012-06-07)

Bug Fixes Since Baselight 4.3.5380
==================================

* Fixed reading timecode from some QuickTime movies with non-standard
  structure [bug 20934]

* Fixed UI/Image button functionality on Blackboard 1 desks
  [bug 20943]

--------------------------------------------------------------------------

Baselight Release 4.3.5380 (2012-06-07)

New Features Since Baselight 4.3.5378
=====================================

* Added button to Sequence parameters to update sequence and layer
  operators after the type of input file is changed (using the Change
  button, or through use of bl-shots). All selected sequences are
  updated if Grouped Grading is enabled. This is particularly useful
  if you change from an image sequence to a movie or vice versa.

* Moved 'Blur', 'Copy', and 'Paste' buttons on Blackboard 2 to bottom
  row of button group. Allows easier access by operators by touch.

* Moved 'Cache' button on Blackboard 2 / ONE to top right button
  panel.

* Added 'Layer 0' button for Blackboard 2 / ONE.

* Added 'Previous Frame' & 'Next Frame' buttons to bottom right 
  transport button panel on Blackboard 2 / ONE.

* Added Up/Down buttons to keypad area of soft keypad on Blackboard 2
  to allow bumping of numerical values in edit boxes. Also only keypad
  area of soft keyboard now appears when a numeric edit box has focus.

* Added 'Cursor 1..9' buttons on Blackboard 2 / ONE to allow fast 
  access to cursors with left hand.

* Added 'UI 1/2' and 'Image' buttons on Blackboard 2 / ONE to allow
  fast switching between display image and UI screens.

* Added -tapenames, -clipnames and -comments options to bl-shots,
  allowing the user to extract more metadata from a scene using the
  command line.

Bug Fixes Since Baselight 4.3.5378
==================================

* Fixed crash when exiting Machine Control on Blackboard 1 [bug 20872]

* Fixed display of Machine Control buttons on Blackboard 2.

* Fixed divide-by-zero crash when using "Apply Transform" in FCP XML
  conform [bug 20706]

* Field information (interlaced/progressive) is now correctly written
  to QuickTime movies on Linux.

* Fixed crash when accessing the matte curve in MatteTool without a
  Blackboard attached [bug 20902]

* Fixed Modify AAF/XML not functioning [bug 20913]

--------------------------------------------------------------------------

Baselight Release 4.3.5378 (2012-05-31)

Bug Fixes Since Baselight 4.3.5371
==================================

* Fixed crash on undo of Autohandles [bug 20185]

* Fixed occasional crash reading audio from QuickTime movies on Linux
  [bug 20870]

* Fixed 'flix: too many open files' error when copying multiple
  sequences with flux or fl-cp [bug 20319]

* Fixed inability to move Text far to the right in a scene with a
  working format wider than 4096 pixels [bug 20884]

* Improved reliability of flint interrupt diagnostic [bug 19189]

* Fixed frame rate of synthetic movie timecode based upon .THM sidecar
  [bug 20894]

* Fixed crash on undo of Autohandles [bug 20185]

--------------------------------------------------------------------------

Baselight Release 4.3.5371 (2012-05-28)

New Features Since Baselight 4.3.5343
=====================================

* Baselight now remembers the selected visible audio channels in the
  Audio Waveform view.

* Baselight now remembers the selected Audio Timecode Sync FPS on a
  per-job basis, and will use the last selection when creating new
  scenes within a job.

* It is now possible to perform clap detect on an audio sequence from
  the Audio Sequence operator in the Input node.

* There are now 3 timeline caching modes (available from the scene
  settings panel & preferences editor). These replace the "Timeline
  Caching" Enabled/Disabled toggle in previous versions. The new modes
  are:

  "Disabled"            - Timeline disk caching is disabled.
  "Cache Strips Only"   - Only strips with caching explicity turned
                          on are cached.
  "Full"                - Stack bottoms and strips with caching
                          explicity turned on are cached (equivalant
                          to enabling timeline caching in previous
                          versions).

  "Cache Strips Only" is a new mode, with different cache bar colour
  coding in the timeline: Areas with no explicitly cached strips are
  drawn in dark grey. Areas with explicitly cached strips that have
  not been fully cached are drawn in light grey. Areas with explicitly
  cached strips that have been cached are drawn in blue.

* You can now switch between displaying the audio offset in Frames or
  Seconds in the Audio Sequence operator, Audio Waveform view and
  Scene Settings view.

* REDCINE luma, red, green and blue curves are now read and applied
  from RMD files into the R3D Decode operator. Note that the curves
  are not displayed and cannot be edited in Baselight.

Bug Fixes Since Baselight 4.3.5343
==================================

* Six Vector now displays Layer matte correctly [bug 20719]

* QuickTime movies with multiple mono audio tracks are now read
  correctly [bug 17772]

* Stacks containing cached strips now display Layer Matte and
  Selection Output render modes correctly [bug 20455]

* Matte Merge now correctly passes metadata from its uppermost input
  strip [bug 20736]

* Fixed unordered stack when inserting external mattes first, then
  adding a layer and pressing Use Matte [bug 20465]

* The file panel no longer automatically descends into directories
  when browsing for a directory [bug 18494]

* When an error is encountered during Scene Detect, the cursor is now
  moved to the location of the error.

* Fixed bug which could cause a category-related crash on scene open
  [bug 20375]

* Fixed issue with dragging the playhead in the Audio Waveform view
  leading to an open delta that cannot be closed [bug 20530]

* Fixed issue with changing audio position & offset from the Audio
  Waveform view when using scene audio [bug 20710]

* Fixed issue with scrolling audio waveform view when dragging the
  playhead past the start or end of the current visible audio region.

* You can now set correctly negative audio offsets in frames/seconds
  in the Audio Sequence operator, Scene Settings view and Audio
  Waveform view [bug 15697]

* fl-cp and flux sync options now consider file sizes to help solve
  problems caused by failed previous copies, or bad filesystems.
  Movies and files will be re-copied when their timestamps match if
  their sizes differ [bug 19997]

* Sub-second timings are no longer read from JPEG files and THM
  sidecar files accompanying QuickTime movies, to match Canon plugin
  behaviour. This will change File Timecode but not Shot Timecode in
  existing scenes that use such files [bug 15963]

* Fixed bug which could cause a crash if trackballs are moved while
  closing a scene with the save/discard dialog visible [bug 20773]

* Categories selected in the "Shots Containing Categories" list on
  Render View now remain selected the next time the list is opened
  [bug 20698]

* Disable background caching while rendering from inside Baselight
  [bug 20699]

* Fixed bug which would cause re-valdiation of timeline cache status
  bar on a render panel setting change [bug 20713]

* Fixed bug which could cause crash if scene quickly closed after
  opening with 'Initial verification pass on scene load' Background
  Caching preference enabled [bug 20763]

* Fixed bug where udev would complain about 'unknown keys' when
  applying rules for Blackboard 2 / ONE [bug 20768]

* Fixed bug where Baselight would complain about ftdi driver on
  shutdown when Blackboard 2 / ONE is selected in prefs [bug 20768]

* Fixed flux progress text when copying multiple files [bug 19624]

* Optimised Blackboard 2 display rendering. Screens are now rendered
  using single-buffering to reduce texture memory consumption and to
  allow partial redrawing of the surface [bug 20376]

* Enabled audio levels display during playback on Blackboard 2

* Fixed issue with Spirit HD/2K/4K control not working [bug 19549]

* Fixed crash when opening Spirit view for a scene that uses a Spirit
  Preset that has been deleted. The Spirit View will keep the current
  settings, but resetting any parameters will reset them back to the
  values from the "Default" Spirit Preset [bug 15022]

* Fixed ranges of Spirit Lift, Gamma and Gain controls in Spirit View
  and Spirit Primary operator in timeline. It is now possible to reach
  the maximum extents of the correction for each parameter. For
  example, pushing the colour wheel to the maximum extents along the
  Red vector will create a correction of (1.0, -1.0, 1.0), yielding
  negative values for the green and blue channels [bug 19100]

* Fixed crash when using nudge buttons in Audio Waveform button to
  change Audio Offset in Scene Settings [bug 20832]

* Fixed inconsistent stickiness of Blackboard 2 'UI Views' button. A
  long hold when the button is latched now disengages the mode. Same
  change also made for 'Keyboard' button [bug 20812]

* Fixed rendering scenes not being shown in top-right scene list on
  menu bar [bug 20842]

* Fixed RME Hammerfall HDSPe AIO card settings file not being copied
  over when new Baselight versions are installed [bug 19684]

* Fixed colour shift on older ALEXA ARRIRAW files. Existing scenes are
  unaffected; re-insert or re-conform the .ari files to change the
  colours.

* Fixed reset in ganged parameters not returning to zero correctly in 
  the mattetool [bug 20853]

* Fixed error message when nudging audio offset left/right when audio
  is embedded in movie file [bug 20832]

* Fixed behaviour of Ctrl + Top Left Trackball button on Blackboard
  desks to reset state of current parameter strip [bug 20849]

--------------------------------------------------------------------------

Baselight Release 4.3.5343 (2012-05-11)

New Features Since Baselight 4.3.5327
=====================================

* Added support for Blackboard 2 One desk on Baselight ONE systems.
  The desk is driven entirely over USB and uses a fixed mapping of
  buttons similar to the original Blackboard.

  To enable support for the Blackboard 2 One on a Baselight ONE
  system, enable "USB" for the "Blackboard 2 / One" option in the
  System preferences tab.

* "UI Views" button added for Blackboard 2 desks. Allows fast
  switching of Workspace views (Standard, Simple, Scopes, etc) and
  toggling of view windows (Job Manager, Shots, Scene Settings, etc)

* "Cycle Cursors" button added for Blackboard 2 & Blackboard 2 One
  desks. Allows quick switching of active cursor with left hand.

* "Delete Strips" button added for Blackboard 2 & Blackboard 2 One
  desks. Removes need to flip up keyboard, or use soft keyboard to
  delete currently selected strips.

* Added the ability to enable/disable drag-and-drop shot movement in
  the Cut and Gallery views. In the Cut View preferences, the "Allow
  Drag-and-Drop Shot Movement" setting is a simple toggle button. In
  the Gallery View preferences, on the other hand, the user is able to
  disable shot movement completely, allow it only for true gallery
  scenes, or allow it always.

* Added a "Cancel" button to the "Create New Gallery" dialog, which
  allows the user to elect not to create a gallery.

* Updated the Truelight library to include the internal HD Rec1886
  display calibration: Rec709 primaries, 2.4 gamma tone curve, as
  described in ITU document R-REC-BT.1886-0-201103-I.PDF-E.pdf

* Added ability to Multi-Paste by "Record Frame Number" or "Record
  Timecode", which is useful when one wishes to paste grades between
  scenes where the cut points are the same but the source media or
  metadata has changed in some way between two cuts. Note that since
  "Copy Grades" in the EDL Import via uses Multi-Paste internally, the
  "Record Frame Number" and "Record Timecode" options are also
  available there.

* Added support for reading Sony F65 RAW Lite MXF files.

* Added support for reading SStP/L2 4:4:4 MXF files.

* "Cursor" mode on Blackboard 2 key pad now highlights current cursor
  and shows active cursor slots.

* "Cache" button on Blackboard 2 and Blackboard 2 One allows quick
  toggling of per-strip caching.

Bug Fixes Since Baselight 4.3.5327
==================================

* Fixed problem with the Temporal Degrain, where if the threshold was
  set to zero and had a matte, the plugin was not bypassed correctly
  [bug 17227]

* Fixed crash toggling hide Overlay when the cursor view was hidden
  [bug 20374]

* Fixed double grab to gallery from Blackboard 1 [bug 20401]

* Fixed colour shift on older ALEXA ARRIRAW files. Existing scenes are
  unaffected; re-insert or re-conform the .ari files to change the
  colours.

* Fixed problem with old scenes containing Hue Angles, by disabling
  the new colour space UI [bug 17395]

* Fixed scenes becoming unloadable after using strip category names
  containing the " character [bug 20618]

* Fixed crash when using an MC Color or MC Transport panel alongside a
  remote device [bug 20619]

* The Baselight hotfix script will disable PostgreSQL logging to
  syslog, as we have found it can slow down the server under heavy log
  load [bug 15484]

* Removed acceleration from Blackboard 2 / One jog wheel [bug 20416]

* Fixed invalid state change in GPU renderer [bug 20394]

* Fixed occasional crash when re-ordering shots in the Cut View/
  Gallery using drag-and-drop [bug 20624]

* Fixed error using strip caching above temporal strips [bug 20636]

* Fixed crash in Gallery View which would occur when an autoloaded
  gallery could not be created [bug 20418]

* Fixed bug in Cut/Gallery Views which could cause the incorrect
  thumbnail to be selected if the metadata display was switched on and
  the view was zoomed out a substational amount [bug 20340]

* Fixed occasional assertion in Cut View/Gallery [bug 19950]

* Fixed crash using an invalid render filename template (e.g. %-10W)
  [bug 20654]

* Fixed MatteTool always pasting keyframes [bug 20558]

* Fixed thumbnails when using Make Matte: Alpha [bug 20514]

* Fixed problem with large audio latency on systems with Hammerfall
  HDSPe AIO audio cards [bug 20653]

* Fixed crash when modifying parameters in the Spirit view [bug 20633]

* Fixed preservation of alpha channel in proxy images [bug 10162]

* Fixed the Timeline Alignment view causing re-evaluation of the
  timeline cache state (the green line in the Timeline), even though
  an alignment can't change the actual image produced by a given
  frame [bug 18983]

* Fixed opening scenes using unavailable OFX plugins.

* Fixed bug which could cause a crash if the trackballs were knocked
  while moving strips in a scene [bug 20647]

* An invalid line in volume.cfg no longer crashes Baselight startup
  [bug 20393]

* Fixed problem with Unset/Set keyframes crash [bug 20671]

* Fixed DCI 4K 23.976p display mode when used with NVIDIA 8800, 9800,
  GTX285 and GTX580 GPUs [bug 20346]

* R3D sequences with the "Do Not Use RED Rocket" option no longer
  cause the decode to happen on the CPU of the machine containing the
  RED Rocket [bug 20676]

* Fixed adjusting the MatteCurve and switching scenes [bug 20671]

* Fixed bug which could cause an edit to remain open when switching
  scenes whilst adjusting an encoder [bug 20684]

* Fixed bug which could cause crash on set/unset keyframe when using
  a Hue Shift [bug 20693]

* Categories selected in the "Shots Containing Categories" list on
  Render View now remain selected the next time the list is opened
  [bug 20698]

* Disable background caching while rendering from inside Baselight
  [bug 20699]

--------------------------------------------------------------------------

Baselight Release 4.3.5327 (2012-04-23)

New Features Since Baselight 4.3.5314
=====================================

* The Baselight About panel now shows the default Baselight Kompressor
  and RED Rocket machines that will be used.

Bug Fixes Since Baselight 4.3.5314
==================================

* Removed 'Apply To Strips' option from the timeline context menu when
  using grouped grading to set categories of multiple strips (changes
  are now applied immediately) [bug 20506]

* Toggling a default strip category now works with grouped grading
  [bug 20506]

* Fixed reset indicator of Inside/Outside and Blackboard stack manager
  during a selective layer paste [bug 19682]

* Fixed reading MXF files written by Flame [bug 20554]

* Fixed bug which could cause occasional crash on undo/redo of 
  timeline strip modifcations [bug 20553]

* Fixed render error "Insufficient tiles to complete this render"
  [bug 20412]

--------------------------------------------------------------------------

Baselight Release 4.3.5314 (2012-04-13)

New Features Since Baselight 4.3.5245
=====================================

* Added support for reading and writing MXF files encoded using DNx444
  (4:4:4 DNxHD).

* Added gain control to right-click context menu on scope views.

* The Sony F65 Decode "Exposure Index" control is now a slider rather
  than a popup menu with fixed values.

* Cursor View can now be floated.

* SMPTE timecode stored in Phantom cine files is now read by
  Baselight.

* Fixed DNxHD on Mac OS X 10.5.

* Added fl-diag test to verify permissions on /dev/shm.

Bug Fixes Since Baselight 4.3.5245
==================================

* Video grade now saves the currently selected page as the default
  for new grades when the (customize) menu option 'Save Config To
  User Preferences' is selected [bug 20329]

* Fixed potential crash when adjusting shape feathering with very
  small values while grouped grading & switching scenes [bug 20356]

* The list of Truelight profiles and LUTs in the Render View is now
  updated when 'Reload' is selected in Cursor View and when a scene
  using a file from a non-standard directory is selected [bug 20357]

* Reinstated option to render to 64bit RIFF64 WAV files (required for
  long multi-channel audio files) [bug 20367]

* Fix for AAF conform timing with speed events [bug 18187]

* Fixed bug which could cause crash when tracking with 290 series
  nvidia drivers [bug 20280]

* Reinstated option to render to 64bit RIFF64 WAV files (required for
  long multi-channel audio files) [bug 20367]

* Fixed bug which could cause a scene containing a sequence with 'OFX'
  in the filename to crash Baselight (only on systems with a
  Blackboard connected) [bug 20363]

* Fixed reading large MXF files on Mac [bug 20432]

* Fixed incorrect cache resize warnings when background caching a
  scene containing explicitly cached strips [bug 20450]

* Fixed issue with AAF reading crashing [bug 19953]

* Removed StereoGrade from the inside/outside layer0 list [bug 20494]

* Fixed double speed playback [bug 20251]

* Fixed performance drop after extended periods of grading [bug 20461]

* Fixed rendering of video luts & intermediate caching [bug 20502]

* Fixed crashes reading JPEG2000-encoded DPX files [bug 20254]

* Fixed thumbnail caching of RAW files [bug 20511]

* Fixed slow conform, by making it optional to scan for movie files
  with missing or no extension (i.e. filenames not ending in .mov,
  .mxf etc). To enable scanning for these files, turn on the
  preference (under Timeline->Conform) [bug 20462]

--------------------------------------------------------------------------

Baselight Release 4.3.5245 (2012-03-23)

New Features Since Baselight 4.3.5238
=====================================

* Importing scene and job archives now restores folder structure from
  the saved scenes.

* Added support for reading movie files where the image data is split
  over several MXF files (e.g. Canon XF305).

Bug Fixes Since Baselight 4.3.5238
==================================

* Fixed failure to load scene containing missing formats [bug 19713]

* Upgraded scenes are now saved immediately after upgrade. This
  prevents the scene from becoming unrecoverable if Baselight crashes
  before the scene is next saved.

* Video grades created in new scenes will now remember their last 
  selected tab page [bug 20329]

* Fixed XML conform issue with old v4 FCP XML files [bug 19592]

--------------------------------------------------------------------------

Baselight Release 4.3.5238 (2012-03-21)

New Features Since Baselight 4.2
================================

Caching Improvements
--------------------

* Caching is no longer controlled on a per-cursor basis; it has been
  replaced by a toggle button on the scene settings panel: 'Timeline
  Caching'. When this option is enabled, stacks (excluding those
  containing a single, raw sequence input strip) will be written to
  the cache during playback and in the background during idle time.

  The default caching state for newly created scenes can be set from
  the 'System' page of the preferences editor (using the 'Enable
  timeline caching for new scenes' control). There is a separate
  preference in the 'Player' page, for scenes created in the
  Truelight Player where the default behaviour is not to cache.

* When adjusting a strip in a stack, the inputs to that strip are
  automatically cached in memory. This can result in dramatically
  improved interactive grading performance, as the entire stack does
  not have to be rendered every time a grade parameter is changed.

* Explicit Strip Caching

  The output of every strip can now optionally be cached locally to
  disk. This is controlled using the 'C' icon button (located at the
  top right of the Parameters View). Once enabled, a 'C' indicator
  will be drawn on the corresponding strip in the timeline.

  Strip caching is useful in a couple of scenarios:

  - The stack you are working on has grown to a point where grading/
    playback performance at the bottom of the stack has started to
    degrade noticeably. In this scenario, turning on strip caching
    at/near the bottom of the stack will, in effect, reset performance
    at that point (because any strips below will be working from a
    cached sequence on local storage).

  - You are working with input strips containing sequences which
    cannot be read/decoded acceptably fast enough to work with
    natively. In this scenario, turning on strip caching for those
    problematic input strips will ensure you're working from decoded
    images on local storage.

    Input strips can be configured to have strip caching enabled
    automatically based on their sequence type from the preferences
    editor ('System' page, 'Cache' section).

  Strips with explicit caching enabled will be cached (written to
  disk) when the stack in which they reside is either played through,
  or processed by the background caching.

  Modifying a strip above an explicitly cached strip will result in
  that strip's cache being invalidated (requiring a new version to be
  written to disk next time the stack is played or background cached).

* Background Caching

  During idle time, Baslight will now attempt to cache (the bottom of)
  the current cursor's scene. It will first cache the stack/shot the
  cursor is parked in, before moving on to the rest of the scene.

  The current status of the scene caching is indicated by colour
  coding the horizontal separator bar between the strip and timecode
  display areas of the timeline. Regions of the bar can be one of 4
  colours:

  Grey   : The region of the timeline has not yet been processed by
           the background caching.
  Green  : The region of the timeline has been processed and the result
           is stored in the timeline cache.
  Purple : The region of the timeline contains a single raw sequence
           input strip and has not been cached because this is not
           usually required for playing raw sequences. However smooth
           playback cannot be guaranteed due to potential variations
           in sequence decode performance, file location etc. If
           caching is required for a raw sequence, explicit strip
           caching should be enabled for its input strip (see above).
  Red    : Baselight has attempted to cache a region, but the rendering
           has failed.

  While the background caching is in operation a green spinner is
  drawn on either the left or right of the timeline (to indicate where
  the background caching is currently taking place relative to the
  timeline window).

  The green line & spinner displays on the timeline can be turned off
  from the 'System' page of the preferences editor (or from the right
  click context menu of the timeline itself). When disabled, these
  indicators are replaced by a small icon on the application menu bar
  (which changes depending on the background caching status).

  Background caching can be disabled altogether from 'System' page of
  the preferences editor.

Gallery & Cut View
------------------

* A second Gallery view has been added to Baselight - to see it,
  simply insert it into your current workspace in the usual
  manner:(right-click on a Splitter), Windows+right click (Ctrl+
  right-click on Mac) and select "Gallery 2".

* The open scenes in the Gallery are now shown as tabs above the
  scrolling thumbnail areas, making it possible to switch between
  gallery scenes without needing to use the right-click context menu.
  It's also possible to close a gallery scene by clicking the "X"
  control on the right-hand side of each tab.

* The way Baselight Galleries load scenes has been substantially
  improved. The behaviour is controlled from the "Gallery Autoloads"
  and "Gallery 2 Autoloads" sections on the "Cuts View, Gallery &
  Scratchpad" page of the preferences. Each Gallery has three
  autoloading slots, allowing it to automatically load three different
  types of galleries at once. For example, by default, the first
  Gallery View will automatically load a gallery for the current user
  and a per-job gallery as a new job is encountered when a scene is
  loaded into the Timeline View. Gallery 2 is set up to have no
  autoloads by default, but if you wanted your per-job gallery to live
  in Gallery 2, you can simply select a per-job option in one of
  Gallery 2's autoload slots and switch off the per-job obtain in the
  first gallery. The arcane substitution-based gallery scene naming
  scheme is largely hidden now, but is still available by selecting
  "Custom" from an autoload slot's dropdown. An edit box then appears,
  allowing you to type in a specific template.

* It's now possible to have either/both of the galleries contain a tab
  which maps to the current cursor, essentially giving you a second
  Cut View (without the ability to scroll lock, however). This gallery
  will share DBS location and "red square" selection state with the
  Cut View. To set up such a tab, simply set on of Gallery/Gallery 2's
  autoloading slots to "Current Cursor".

* The Gallery Views now contain a '+' menu to the right of the gallery
  tabs. It contains the following options:
   - "Load Missing Autoload Galleries": If you've closed autoloaded
     Galleries, or had autoloading disabled for a while, you can get
     them back by selecting this option. It simply evaluates the
     current autoload preferences for the Gallery and loads anything
     which isn't already present.
   - "Disable Autoloading": Disables autoloading. Useful if you want
     to quickly load a scene into the timeline and don't want a
     per-job gallery autoload to slow you down.
   - "Current Cursor": Adds a tab which reflects the state of the
     current cursor, in effect making the Gallery a Cut View when
     that tab is selected.
   - "Open Scene..": Bring up a Job Manager to load an explict scene
     into the Gallery. Any type of scene can be loaded, including
     scenes which currently have timeline cursors associated with
     then.
   - A list of the last 5 scenes which have been opened in either
     Gallery.

* The host and job which store gallery scenes is now specified in
  the "Gallery Job" preference in the "Gallery" section.

* If a gallery scene has failed to load (perhaps due to being locked
  by another user), a "Retry" button now appears below the error text.
  This allows the user to resolve the problem and then load the scene
  without needing to restart Baselight.

* In previous versions of Baselight, locking the DBS to the current
  cursor would update the DBS location as the current shot changed and
  also cause the Cut View to scroll to keep the current cursor
  location centred. These two behaviours have now been split into
  separate locks: "DBS Lock" and "Scroll Lock". This allows the user
  to position the DBS on a desired shot and leave it there, whilst
  still having the Cut View scroll along with the current cursor
  position.

* By default, the Cuts View will now switch on "DBS Lock" and "Scroll
  Lock" as soon as playback begins. Either/both of these behaviours
  can be switched off using the preferences located in the "Cuts View"
  section of the "Cuts View, Gallery & Scratchpad" page.

* The DBS left/right/up/down buttons are now active when the "View"
  button is held down, allowing the DBS to be moved whilst viewing.
  This functionality was previously only available on the trackballs.

* The DBS left/right/up/down buttons and the trackball can now be used
  whilst the "Try" button is down, allowing the user to try a large
  number of grades on the current shot simply by holding down "Try"
  and moving the DBS position.

* When the "Goto DBS", "View" or "Try" buttons are down, any of the
  trackball rings can be used to scrub within the shot, replicating
  functionality which was previously only available on the jog wheel.

* It's now possible to select multiple shots in the Gallery using
  exactly the same mechanism as used in the Cut View. This allows the
  users to remove multiple shots in the gallery at once.

* Cuts and Gallery views now report rendering errors (eg missing
  files) to the standard Baselight message log, making it much easier
  to work out why a given thumbnail is displaying an "X".

* It's now possible to change the width of the borders around
  thumbnails used to represent the DBS and selected shots. The
  relevent preference is in the "General" section of the "Cuts View,
  Gallery & Scratchpad" page. In addition, the default value has been
  reduced from 7 pixels to 5.

* The Cuts and Gallery Views now support inertial scrolling, giving a
  feel of inertia when scrolling, allowing more rapid navigation of
  large scenes. The specific feel of the inertial scrolling can be
  controlled by adjusting the sliders in the "Inertial Scrolling"
  section of the "Cuts View, Gallery & Scratchpad" page.

* It is now possible to re-order shots in the Cuts and Gallery views
  simply by dragging and dropping into the space between thumbnails in
  the same view: a green "dumbbell" will appear showing the insertion
  point. Multiple shots can be moved by dragging a selected thumbnail
  (red square).

* Drag and Drop can be used to quickly grab multiple shots to a
  Gallery. Simply red-select multiple thumbnails in the Cut View and
  drag and drop into a gallery. Again, a green "dumbbell" will appear,
  allowing you to specify where the newly grabbed thumbs will appear.

* Drag and Drop can also be used to apply the grade from one thumbnail
  to another, simply by dropping directly on top of another shot (from
  either Cut View or Gallery). The Drag and Drop apply obeys all of
  the current Paste/Apply settings. A grade can be applied to multiple
  shots simply by red-selecting them, switching on group grading and
  then dragging onto one of them.

* Pressing the 'Esc' key during any of the above drag-and-drop
  operations cancels the drag.

* Since there can now be three possible owners of the DBS (Cut View,
  Gallery & Gallery 2), the "Cut View/Gallery" button on the
  Blackboard now has "Alt+Tab"-style behaviour in that pressing that
  button slowly simply toggles between the last two DBS owners. Only
  if pressed rapidly will it cycle through all the possible owners.

* The Cuts and Gallery view are now capable of displaying various
  pieces of metadata beneath each thumbnail. To enable this metadata
  display, simply right-click on a thumbnail and tick the desired
  pieces of metadata in the "Metadata Display" sub-menu. The Cuts
  View, Gallery and Gallery 2 all have separate metadata display
  preferences, so each can be configured to display separate metadata.
  Most of the metadata types are read-only, the only exception being
  "Comment (Editable)". This is especially useful in the Galleries, as
  it's a convenient way to add a label to a gallery thumbnail.

* Cut/Gallery Views who don't currently own the DBS now have a "ghost"
  (semi-transparent) DBS drawn, showing where the DBS would be if they
  were to receive DBS focus.

* The three separate "Select", "Deselect" and "Invert" sub-menus in
  the Cut View's right-click context menu have been all been
  consolidated into a single "Select Multiple" menu.

* The Cut View now displays the position of all cursors within the
  current scene. Each cursor is drawn with a numeric label making the
  cursor position much easier to see.

User Interface Improvements
---------------------------

* Baselight can now support up to 3 UI monitors. Workspaces can be
  configured to dock any view on any of the 3 monitors.

  This functionality is only supported on Baselight TWO, FOUR and
  EIGHT systems, and requires a UI host with an NVIDIA Quadro NVS 450
  GPU. On the Quadro NVS 450, the UI monitors must be plugged into
  ports 1-3, and the Blackboard plugged into port 4.

  The tablet on a Blackboard only maps to one UI monitor at a time.
  To cycle the tablet between UI monitors, use "Tablet Mon" on a Blackboard
  2, double-tap "UI Image" on a Blackboard 1, or use Ctrl-Shift-Esc on
  the keyboard.

* Added inertial panning to all controls which pan across a larger
  area. These controls can now be panned using a middle mouse button
  drag anyway within the panning area, obviating the need to use the
  scroll bar in most situations. However, if a control embedded within
  a panner also responds to the middle mouse button (e.g. graphs
  within CurveGrade), the embedded control will win and panning will
  not occur.

* Improved mouse wheel support throughout Baselight, making it work in
  places it previously didn't and utilising inertial scrolling,
  allowing more subtle scrolling. The "feel" of inertial scrolling can
  be adjusted in the "Inertial Scrolling" section of the "UI" tab of
  the Baselight preferences.

* The CtrlLock+pen drag panning metaphor used in Timeline View has now
  been extended generally throughout Baselight, including the Cuts and
  Gallery views.

Scopes and Histogram Improvements
---------------------------------

* Baselight now has several new views available when using the GPU
    Vectorscope - a vectorscope plotting Rec 709 chroma (Cb, Cr) as
    (x, y), with reticules showing the targets for Rec 709/SMPTE
    colour bars.

    Luma Waveform - a Rec 709 luma waveform.

    RGB Parade - three waveforms of the red, green and blue components
    of the image.

    Y'CbCr Parade - three waveforms of a Rec 709 Y'CbCr conversion of
    the image.

  These can be displayed in monochrome or colour mode, by
  right-clicking on the scope (excluding the Luma Waveform).

  Additionally, a high-resolution histogram is now generated on the
  GPU. This has a number of additional features, which can be selected
  by right clicking on the Histogram view:

    The orientation of the histogram can be made horizontal or
    vertical by changing the aspect ratio of the histogram view. The
    orientation can be locked in place so the orientation doesn't
    change when the view is resized.

    The histogram has three different filtering modes, none, low and
    high. As the resolution is higher, you may see high frequency
    peaks and troughs when working with limited bit-depth input
    imagery (10-bits or less). Increasing the filtering will make the
    histogram easier to read in these cases.

    An option to fill the space below the histogram curve.

  When picking colour values on the image, corresponding points will
  be displayed on the vectorscope/waveforms and histogram.

  The scopes and histogram match the output setting from the combiner,
  i.e. no-conversion, full-to-legal, clip, soft-clip.

Timeline Alignment View
-----------------------

* It is now possible to clean up the vertical alignment of all the
  shots in a Baselight scene. In the "Views" menu, simply select
  "Timeline Alignment" - a new view will pop up containing the
  following options:
    - Align: Specifies how to align within each track:
      "Stack": Either the tops or bottoms of the stacks within
        each track will be aligned.
      "Selected Strips Within Each Stack": The selected strips
        within each stack will be aligned. Any stacks without
	selected strips will be moved out of the way either
	"Upwards" or "Downwards".

    - Derive Tracks: Alignment occurs by putting all the shots
      in the timeline into a track and then aligning within each
      track. This setting specifies how shots are matched
      to tracks:
	"By Flattening": Shots are placed in the lowest possible
	  track which isn't already occupied by a shot below
	  them.
	"From Original Conform Tracks": Shots are placed in the
	  same track as they were in when the scene was conformed.
	  If the scene was conformed prior to Baselight 4.3, the
	  behaviour will be the same as "By Flattening".
	"By Row Snapping": Shots are placed in tracks alongside
	  other shots lying at a similar height in the timeline.

    - Empty Rows: The number of empty rows which are desired below
      and/or above each track.

    - Gap Above Lower Eye: The number of empty rows between lower and
      upper eyes in stereo scenes. This option won't appear in
      non-stereo scenes.

    - Remove Unreferenced Strips: "Yes" or "No". Whether or not to
      remove strips (or parts thereof) which don't contribute to the
      final image (ie, the semi-transparent strips in the Baselight
      Timeline View). It's a useful setting for simplifying a complex
      multi-track timeline.

  Once the alignment options have been set, simply press "Align" to
  vertically align the strips. Via the "Customise" menu, it's possible
  to store common alignment settings in tabs for quick retrieval.

* The current Timeline Alignment settings can quickly applied by
  pressing the ';' (semicolon) button. The Timeline Alignment view
  can be popped up/popped down using the Win+';' accelerator
  (Ctrl+';' on Mac).

* For "Rendering Avid Media and Updating AAF" and "Rendering Quicktime
  Media and Updating FCP XML" workflows, Timeline Sort now ensures
  that the original conform ranges of all shots are all present
  post-sort. This means that the user is free to simplify complex
  multi-format timelines for grading by removing unreferenced strips
  (in the new Timeline Alignment view) without fear of it causing
  Modify AAF or Modify XML problems later.

Strip Categories
----------------

* Strips can now be tagged with one or more categories defined on the
  'Timeline' page of the preferences editor. Strip categories can be
  set/unset from either the UI or the Blackboard:

  From the UI:  Right clicking on a strip brings up a context menu for
                that strip. The 'Set Strip Categories' menu option
                allows you to choose which categories are associated
                with the strip.

                The strip context menu can also be used to set
                categories for multiple strips in one go. To do this,
                select all the strips you wish to categorise, enable
                grouped grading and right click on any of the
                selections (this method also works for selections made
                in the Cutview).

                You can also toggle a default strip category using
                the keyboard shortcut 'J' or the Mark/Strips menu
                'Toggle Strip Catergory' option. The default strip
                category settings are also configured from this menu.

  Blackboard:   On a Blackboard 1 the 'Mark/Strips' menu contains an
                option for switching the behaviour of the panel's 'I'
                button between toggling a default mark and toggling a
                default strip category.

                On a Blackboard 2 there is a dedicated button for
                toggling a default strip category (below the toggle
                mark 'I' button). This button dynamically changes its
                appearance depending on the (default) category status
                of the shot/grade strip at the current cursor
                position.

* The 'Bypass All' toggle behaviour can be set to not bypass strips
  tagged with particular categories. This is useful, for example, when
  your stacks contain transform strips (to re-rack your shots) which
  you do not want to disable when viewing your stacks bypassed/without
  their grades.

  To specify which strips are not bypassed, select the 'Timeline' page
  in the Preferences editor. On that page there is a 'Category Groups'
  section which contains a set of categories called 'Don't bypass
  strips of category'. This set can also be overridden on a per-scene
  basis from the 'Category Groups' tab of the scene settings panel.

* Rendering shots only containing strips of a particular category is
  now supported. To select these shots for rendering from the render
  panel, use the 'Select Frames' dropdown menu and select the
  categories from the 'Shots Containing Categories' sub-menu.

  For command line rendering, categories can be specified using the
  '-render scats:A,B,C' option (run 'bl-render --help' for more).

* Shots View allows the displayed shots to be filtered by the category
  of the Input Layer.

Thumbnail Generation
--------------------

* Thumbnail generation is now completely automatic for both images and
  movies; Baselight no longer writes thumbnail images to disk.

  For speed, thumbnail images are cached in a separate cache directory
  (/vol/images/.baselight-tn-cache by default) and will regenerate as
  required if the source material changes. This directory is created
  automatically by the installer and administered in the same manner
  as the render cache via preferences and bl-reset-cache -thumb

  Proxy generation from the Job Manager and bl-proxygen no longer
  creates thumbnail images.

Area Tracker
------------

* Baselight now includes a new type of tracker designed to simplify
  tracking areas of an image sequence. 'Area Tracks' can be created
  from within shape and transform strips using the 'New Area Track' UI
  button (or 'New AT' Blackboard key). They can also be created from
  an existing tracker strip (on the 'Area Tracks' page) for use later
  (by using 'Copy Name To Clipboard' and then pasting that name into a
  shape/transform 'Current Track' text box).

  Once an area track has been created, the rectangular track region
  can be refined by dragging the centre cross or one of the corner
  hotspots on the image. On the Blackboard the middle trackball is
  used to adjust position. The right trackball can be used to adjust
  the overall size and the ring to modify the X/Y size independently if
  required. When a keyframe is set up, the left trackball can be used
  either for changing the position of the result rectangle, or when
  holding down the ctrl key for the scale. The ring allows the rotation
  modification.

  The area tracker supports the same tools for refining a track as the
  previous point tracker. For example, if a track is lost part way
  through a shot (because the target object becomes occluded) it is
  possible to continue that track by using 'New Reference' to pick up
  a (still visible) part of the same object. Also, if the target goes
  offscreen existing track results can be extrapolated to approximate
  new results.

Y'CbCr Video Grade
------------------

* The Video grade now has a new page: Y'CbCr. This page contains new
  controls to change Lift, Gamma and Gain in Y'CbCr space. On the RGB
  page there is also a new control "Y' Lift, Gamma, Gain" which allows
  editing of the luma channel while controlling the RGB values with
  the trackballs. The Black and White points have been combined into a
  single control to allow space for the new Y' control. On switching
  to the Y'CbCr page the RGB graph changes to Y' correct graph. All
  Y'CbCr corrections are affected by the selected mode (CDL, Graphs or
  FilmLight).

Stereo Geometry Fix
-------------------

* The Stereo Geometry Fix strip now supports a new 'Automatic'
  alignment mode (as well as the previous semi-automatic mode).

  To align the left/right images of a stereo pair in automatic mode,
  simply press the 'Analyze frame' button. This will align the images
  based on the default transform type. However, once the frame has
  been analyzed (and the images aligned) the transform type can be
  changed (from the dropdown) to one of the following:

  None                  : Disable image alignment.

  Translate             : Align the current eye image to the other
                          using only a best fit vertical translation.

  Translate,Rotate,     : Align the images using a transform that includes
  Scale                   vertical translation, 2D Rotation and XY-Scaling.

  Perspective           : Use a perspective transform to align the images.

  Translate, Rotate,    : Align the images in 2 passes. The first pass uses
  Scale + Perspective     a best fit translate, rotate & scale transform. A
                          second pass performs an addition perspective pass
                          to further refine the alignment.

  Translate, Rotate     : As above but without the scaling on the first pass.
  + Perspective

  Note: The last 2 options use 2 passes to minimize potential distortion
  introduced by a single perspective transform.

  The 'Display alignment features' can be used to display all the
  matched features computed during analysis. When enabled, this mode
  can also be used to delete matched features. Usually this is not
  necessary unless there are very few features (where a single bad match
  might skew the results). A feature can be deleted by clicking on it
  in the image display with the shift key held down.

  Grayed out crosses indicate features that the transform fitting
  algorithm thought are too far out to correspond with the best chosen
  transform. This does not necessarily indicate they are wrong (but
  could be an indication they might be).

  Automatic alignment mode also supports grouped grading for aligning
  multiple shots at the same time. To use this, select all the shots
  you wish to align (in one eye), enable grouped grading (so all the
  shots flash) and press 'Analyze frame'. A progress bar will be
  displayed while the alignment of all the shots progresses.

EDL Import and Timeline Sort
----------------------------

* When Transforms are added by the EDL Import View, they are now
  embedded in an Inside/Outside layer, thus allowing a layer number
  to be assigned to the Transform. The default layer number is 99,
  but this may be changed to any desired number via the edit field
  in the "Apply Image Transforms" row. Higher layer numbers are useful
  if you want to keep the transform at the bottom of the grading
  stack, as grading layers inserted via layer number will be
  inserted between the top strip and the transform.

* Transform strips inserted by the EDL Import View may now be
  tagged with a strip category. By default the "Editorial" category
  will be used, but it's possible use any category, simply toggling
  categories on/off in the "Category" menu in the "Apply Image
  Transforms" row of the EDL Import settings.

* Timeline Sort now has a new setting allowing the user to 
  remove strips tagged with a given strip category. By default,
  strips tagged with "Editorial" will be removed, however any
  category can be used simply by toggling the categories displayed
  in the "Marked by Category" dropdown in the "Remove Strips" row of
  the Timeline Sort settings.

  When rendering movies for the Avid AAF or FCP XML workflows, it
  is important the transforms generated by the EDL Import View are
  removed. Failing to so will mean that the Transforms are burnt
  into the rendered media, giving the appearance of the transform
  being applied twice once back in Avid/FCP.

StereoGrade
-----------

* Baselight now includes a new strip called StereoGrade that includes
  common stereoscopic workflow tools for making convergence adjustments
  and adding floating windows.

  As well as using sliders or dragging overlays to make adjustments,
  Stereograde supports making changes from the Blackboard trackballs
  using the following mappings:

  Left trackball        : Controls the left floating window edge.
  Left trackball ring   : Controls the tilt of the floating window edge.
  Middle trackball      : Changes the stereo convergence.
  Right trackball       : Controls the right floating edge window.
  Right trackball ring  : Controls the tilt of the floating window edge.

  Stereograde includes 2 custom picking modes for measuring or adjusting
  convergence by clicking on the image directly. These modes are:

  "Zero convergence plan" : Moves the zero disparity plane to the
                            selected point clicked on the image.
  "Display convergence"   : Displays a numerical value of the computed
                            disparity (in pixels) at the point clicked on
                            on the image. This value will be displayed
                            in one of three colours; Green if the disparity
                            is positive, yellow if the disparity is negative
                            and red if the system is unconfident of the
                            calculated value (this might happen, for example,
                            if the selected point is either occluded in the
                            other eye image, the vertical disparity between
                            the feature in both images is too large etc.).

  When an adjustment is made, Stereograde will automatically add an
  equivalent strip to the other eye.

  Convergence changes will automatically adjust the floating window
  positions so there is no need to correct them afterwards

Matte Tool
----------

* A collection of matte operators have been placed together in a
  single operator. This operator, Matte Tool, is used in place of the
  Blur operator. It can be configured to contain Blur, Threshold,
  Erode/Dilate, Median and the new Matte Curve. These can be placed in
  any order and as many times as is required within the Matte Tool.
  The Blackboard is configured to contain all the effects on available
  panels so each operator can be edited at the same time.

* The Matte Curve is a simplified curve grade, which is intended to
  only work on mattes. It is restricted to 2 control points, or a
  simple auto handles mode. It is intended to allow the user to have
  more control over the S-curve like drop-off.

* The In/Out Blur is a new blur operator which only blurs inwards or
  outwards from the matte. It is intended to allow the user more
  control over the shape of the matte during bluring.

* The Blur functionality on the Blackboard has been taken over by the
  Matte Tool. So when the blur button is hit, a Matte Tool plugin with
  only the Blur tab enabled will be inserted. This only works when the
  blur button is hit inside a matte. For Layers the blur functionality
  remains the same.

LUT export from Shots View
--------------------------

* Added LUT export format to the Export from Shots View. This provides
  options to generate LUT files equivalent to grades in the current
  scene. Grades within the scene can be replaced with Truelight strips
  using the newly generated LUT files.

Miscellaneous
-------------

* Added Nyquist Filter strip. This can be used to reduce various forms
  of high-frequency noise in images. This strip was previously
  available as part of the Baselight Restoration option.

* Added ability to use Transform as an operator in Layers
  (inside/outside strips).

* Improved startup speed on machines running 260.x or greater video
  driver by usage of precompiled GLSL shaders.

* Shots View now has buttons that move the selection up and down in
  the list of shots. This can be used with a category filter, for
  example, to allow stepping through shots of a particular category.

* In poster frame navigation mode ("Swap Next/Prev Cut/Poster
  Controls" ticked on Navigate menu), Shots View will move the cursor
  to the shot poster frames, rather than the first frame.

* Shots View can now be navigated using Tab and Shift+Tab, and
  vertically (when the cursor is in a text field) using the Up and
  Down keys.

* Shots View now allows textual columns to be resized.

* bl-shots and bl-containers can now provide information on older
  scenes without requiring them to be updated in Baselight.

* The Timeline View's cursor icons now match those used within the
  Cut and Gallery views.

* Added ability to modify strength of "notches" on Blackboard 2 Jog
  Shuttle to "Blackboard 2 Setup" dialog.

* The Output Format selected in a Sequence operator now causes the
  colour space conversion (from the Output Format's colour space to
  the cursor's format's colour space) to be applied after all any
  other operators in the Input Layer.

  This means, for example, that when you use OpenEXR material in a
  log-format scene and put an EXR Exposure operator in the Input
  Layer, the EXR Exposure can be made to operate in linear space by
  choosing in the Sequence an Output Format that is set to linear
  colour space.

* Added updated version of the FilmLight EDL Specification to include
  asc_sat optical. It's FL-GN-TN-0476-FLESpec.txt.

* QuickTime and AVI movies with incorrect or no file extension are now
  correctly identified.

* Select Missing Material (on Shots View) now shows a progress panel.

* Added an option to use tetrahedral interpolation when applying cubes
  or profiles in a Truelight strip. Enabling tetrahedral interpolation
  can give more accurate results for applying LUTs, and this is the
  default setting for Truelight strips inserted using the Shots View's
  Export and conversion of grades to LUTs. This form of interpolation
  is slower to process so otherwise the default setting for inserting
  Truelight strips is not to use this.

* On MC Color desks the default encoder page is now the right hand 
  page. The two encoder pages can still be switched using the "< Page"
  and "Page >" buttons.

* Added Shift+W shortcut for inserting an R3D Params strip.

* Blackboard Shift+'Mark Toggle' now removes all marks at the current
  cursor position. 'Join Stacks' has been moved to Control+Shift+'Mark
  Toggle'.

* The "Grab To Gallery" button on Blackboard 1 & 2 now grabs to the 
  gallery view with DBS focus, or the first gallery view if none
  currently have focus.

* Added support for using % variable substitutions when editing the
  Tape column in the Shots View.

* Added support for using %W variable when changing Tape, Clip or
  Name fields in the Shots View. This is substituted for the source
  filename for a shot with the extension removed.

* Added support for ARRIRAW files from ALEXA Studio cameras utilising
  a neutral density filter.

Bug Fixes Since Baselight 4.2
=============================

* Fixed paste of Layer 0 operators to a empty destination causing
  crash [bug 18804]

* Fixed bug in Baselight exit where unsaved preferences changes were
  not correctly enumerated.

* Fixed bug which could cause a crash if the trackballs were moved
  while a layer was being moved up/down the stack at the same time
  [bug 12579]

* Fixed "Layer 0 Op" removing all the layers when Paste mode was
  replace [bug 19072]

* Fixed issue with wdaemon failing to identify certain types of wacom
  tablet [bug 19071]

* Fixed bug which allowed addition of marks before start of timeline
  [bug 17805]

* Copying & pasting a single Curve Grade curve now copies across the 
  'Auto Handles' state [bug 17776]

* Layer number is now updated when a selected strip is moved up/down
  within its stack [bug 14322]

* Fixed problem where BB keypad was being left in layer mode after a 
  parameter paste [bug 11643]

* Fixed thumbnails in the Layer view when gallery material was offline
  [bug 19002]

* Fixed bug that caused the Apply button to lock the keypad into layer
  mode [bug 17336]

* Fixed bug which could result in a crash when moving/renumbering a
  layer within a (single stack) dissolve [bug 18042]

* Fixed Gallery to always show as much of the Gallery thumbnails
  as possible, especially when the Gallery View is large enough to
  show all of them.

* Fixed bug which caused two menus to pop up when a Windows+right
  click was performed on a docked Job Manager.

* Occasional sluggishness in the Baselight UI when having a large
  number of visible thumbnails in the Cut View.

* Fixed incorrect Paste/Apply behaviour when the "Replace" paste mode
  was used with Grouped Grading. The error occurred when a stack had
  separate explicit (yellow) and group grading (red) selections.

* Fixed bug where "Apply" wouldn't obey the "Paste Keyframes"
  preference.

* Fixed bug in Gallery View where the view would scroll to the top of
  the gallery if the last thumbnail in the Gallery was removed.

* Fixed occasional weird inertial scrolling in Timeline View. It
  occurred when undertaking a very rapid pan, stopping suddenly and
  then delaying before releasing the mouse button.

* Fixed in Cut View/Gallery where the thumbnail image wasn't being
  correctly restored to the poster frame at the end of a scrub.

* A Gallery autoload will no longer create or load a per-job/
  per-scene gallery for any scene lying within the gallery job.

* Increased the width of the Tape column in Shots View [bug 17651]

* 'Clear Undo History' now removes any references to categories no
  longer used in the scene's timeline [bug 19562]

* Fixed the default movie output filename to not include scene folder
  names [bug 19593]

* Fixed issue with installing Baselight on cluster systems with Nvidia
  290.10 driver [bug 19653]

* Fixed occasional slowdown in Baselight UI if a gallery failed to
  load [bug 18305]

* Fixed occasional crash which could occur when closing a scene when a
  gallery failed to load [bug 19619]

* Fixed issue with bl-config-xorg not generating correct xorg.conf
  file on Gen1-Gen3 Baselight ONEs [bug 19645]

* Fixed cropping of Burnin text when it extends beyond a transformed
  image [bug 19440]

* Fixed hang on startup on Baselight systems with Nvidia 290.10 driver
  [bug 19607]

* Fixed flux failure to copy files with \ characters in their
  filenames [bug 4452]

* Fixed crash on Mac when monitors added/removed from the machine
  whilst Baselight application is running [bug 19694]

* Fixed crash on Mac when running with Blackboard 2 enabled in the
  prefs [bug 19692]

* Fixed issue with bl-config-xorg not generating correct config for UI
  hosts with Nvidia Quadro NVS450 GPUs.

* Fixed issue with bl-config-video failing if it was required to
  restart X11 [bug 19738]

* Fixed issue where Matte tab would be temporarily inaccessible after
  removing current matte strip via 'undo' [bug 19796]

* Use of the soft keyboard cursor keys will not not close the keyboard 
  when in "transient" mode [bug 19591]

* "Seed" value for Camera Shake can now be modified via encoder on
  Blackboard 1 & 2 [bug 19703]

* Fixed crash with primaries Apply with no primaries in the stack
  [bug 19870]

* Added grouped grading support to image transform settings

* Fixed Layer Output mode to work with Blanks and Bars [bug 19914]

* Fixed GPU memory accounting on GEN4 Baselight ONE systems [bug 19894]

* Fixed node memory monitoring on busy systems [bug 13385]

* Truelight profile and cube directory listings no longer check any
  dotfiles in the default directories [bug 19340]

* Prevented crash on recovery of scene containing a Matte Tool
  [bug 19691]

* Changed the behaviour of Truelight Local Display Settings in Setups.
  If Local Display is set to 'from profile', or a profile with 'use
  local display' disabled is selected in the cursor, the Brightness
  and Flare values in Setups are not applied, leaving the values from
  the profile unchanged [bug 19919]

* Fixed problem with the ordering of events when removing stages from
  the Matte Tool [bug 19986]

* Fixed a crash in tl-player in no database mode, when inserting a
  movie or sequence with an unknown format [bug 19427]

* Moved MatteMerge button to below matte element buttons on Matte tab
  [bug 20029]

* Fixed crash from rendering scenes containing a Y'CbCr video grade
  from bl-render [bug 20006]

* Improved handling of spurious parallel barrier ('flint') interrupts
  in flos 2.1, to fix 'connection timed out errors' on gen2 platforms
  [bug 19485]

* Fixed a issue where when pressing "Play Backwards" on Blackboard
  or MC Transport desks while playing forwards would leave the "Play
  Forwards" button illuminated [bug 19706]

* Improved MC Color desk support for Transform operator. Common
  actions are now mapped to the CG/PG button area [bug 19705]

* Fixed issue where desk displays on MC Color desks could occasionally
  appear corrupt when using Videograde [bug 20003]

* Fixed crash in Matte Tool is all the stages are deleted [bug 20073]

* Fixed slow updates to Truelight values in Setups when there are
  large numbers of profiles and cubes in the default Truelight
  directories [bug 20080]

* Fixed MatteCurve click off setting handle to zero [bug 20089]

* Fixed problem with deleting Matte Tool then reinserting [bug 20040]

* Fixed problem with deleting the last stage then undoing [bug 20078]

* Fixed crash hitting the gallery buttons with no scene open
  [bug 20156]

* Fixed bug when applying a scratchpad slot to outgoing shot of 
  dissolve [bug 13240]

* Fixed crash while moving the encoder while switching to the
  Matte Tool [bug 20177]

* Added preset drop down to the Matte Tool Matte Curve [bug 20092]

* Fixed crash when doing a stereo sync operator when the destination
  strip does not contain an inside outside [bug 20096]

* Fixed crash when toggling Auto handles in Matte Tool matte curve
  [bug 20185]

* Fixed crash on Blackboard 2 when using "Ctrl"+"Shift"+"End" shortcut
  to switch off desk lights [bug 20211]

* Reduced amount of Blackboard 2 related chatter in log. Now only
  reports firmware revision and diverts error messages to stderr [bug
  19605]

* Fixed stereo stack sync so that stereo operators correctly invert
  parameters

* Fixed StereoGrade in an inside outside doesn't turn purble when
  convergence changed [bug 20215]

* Fix for issue with desk encoder movements sometimes being lost when
  editing control points in Matte Tool Matte Curve [bug 20140]

* Fix for rightmost screen on Blackboard 2 not being cleared when
  closing current scene [bug 20197]

* Fixed the gallery getting locked into a "Try" state if the "Gallery/
  Cut View" button was pressed whilst "Try" was down [bug 20208]

* Fixed behaviour of "Alt" keys on Blackboard 2 [bug 20243]

* Fixed StereoGrade disparity display should be in parallax/theater
  space [bug 20260]

* Fixed crash caused by very large LUTs applied to the cursor 
  [bug 19356]

* Fixed bug which could potentially cause a crash when using
  'Try'/'Apply' with 'Include Input Strip' paste option [bug 20216]

* Added test to prevent moving strips above the paste destination if
  there is enough space to fit the resultant stack [bug 20221]

* Fixed bug which could cause a crash after many (specific) grade
  'try' actions from the Cutview or Gallery [bug 9633]

* Fixed apply being applied to incorrect stack in an AB dissolve 
  [bug 20305]

* Added check on selected strip to prevent crash on apply [bug 20271]

* DFuse and Sharpen now appear correctly on Blackboard 1 & 2 when used
  in an Inside/Outside strips [bug 20293]

* Removed Grade/Matte switch from Baselight Transfer application,
  where matte operations are not available [bug 20298]

* Fixed crash in applying from an empty stack with primaries on
  [bug 20320]

* Improved error message when renders fail on Baselight FOUR/EIGHT
  systems, for example when the output disk is full [bug 18542]

* Fixed issue with audio playback not working on systems with
  RME Hammerfall HDSP PCI cards [bug 20322]

--------------------------------------------------------------------------
  
Release history prior to Baselight 4.3 has been removed to prevent
this file becoming too large. If you believe you need access to this,
please contact baselight-support@filmlight.ltd.uk.


