add_library(zlib STATIC 
    "zlib/adler32.c"
    "zlib/compress.c"
    "zlib/crc32.c"
    "zlib/deflate.c"
    "zlib/gzio.c"
    "zlib/infback.c"
    "zlib/inffast.c"
    "zlib/inflate.c"
    "zlib/inftrees.c"
    "zlib/trees.c"
    "zlib/uncompr.c"
    "zlib/zutil.c"
)

add_library(libjpeg STATIC 
    "ljpeg/jcapimin.c"
    "ljpeg/jcapistd.c"
    "ljpeg/jccoefct.c"
    "ljpeg/jccolor.c"
    "ljpeg/jcdctmgr.c"
    "ljpeg/jchuff.c"
    "ljpeg/jcinit.c"
    "ljpeg/jcmainct.c"
    "ljpeg/jcmarker.c"
    "ljpeg/jcmaster.c"
    "ljpeg/jcomapi.c"
    "ljpeg/jcparam.c"
    "ljpeg/jcphuff.c"
    "ljpeg/jcprepct.c"
    "ljpeg/jcsample.c"
    "ljpeg/jctrans.c"
    "ljpeg/jdapimin.c"
    "ljpeg/jdapistd.c"
    "ljpeg/jdatadst.c"
    "ljpeg/jdatasrc.c"
    "ljpeg/jdcoefct.c"
    "ljpeg/jdcolor.c"
    "ljpeg/jddctmgr.c"
    "ljpeg/jdhuff.c"
    "ljpeg/jdinput.c"
    "ljpeg/jdmainct.c"
    "ljpeg/jdmarker.c"
    "ljpeg/jdmaster.c"
    "ljpeg/jdmerge.c"
    "ljpeg/jdphuff.c"
    "ljpeg/jdpostct.c"
    "ljpeg/jdsample.c"
    "ljpeg/jdtrans.c"
    "ljpeg/jerror.c"
    "ljpeg/jfdctflt.c"
    "ljpeg/jfdctfst.c"
    "ljpeg/jfdctint.c"
    "ljpeg/jidctflt.c"
    "ljpeg/jidctfst.c"
    "ljpeg/jidctint.c"
    "ljpeg/jidctred.c"
    "ljpeg/jquant1.c"
    "ljpeg/jquant2.c"
    "ljpeg/jutils.c"
    "ljpeg/jmemmgr.c"
    "ljpeg/jmemnobs.c"
)

target_include_directories(libjpeg PUBLIC "ljpeg")
target_include_directories(libjpeg PUBLIC "ljpeg/extras")

add_library(libpng STATIC
    "lpng/png.c"
    "lpng/pngerror.c"
    "lpng/pnggccrd.c"
    "lpng/pngget.c"
    "lpng/pngmem.c"
    "lpng/pngpread.c"
    "lpng/pngread.c"
    "lpng/pngrio.c"
    "lpng/pngrtran.c"
    "lpng/pngrutil.c"
    "lpng/pngset.c"
    "lpng/pngtrans.c"
    "lpng/pngvcrd.c"
    "lpng/pngwio.c"
    "lpng/pngwrite.c"
    "lpng/pngwtran.c"
    "lpng/pngwutil.c"
)

target_include_directories(libpng PUBLIC "lpng")
target_include_directories(libpng PUBLIC "zlib")

add_library(lungif STATIC
    "lungif/dgif_lib.c"
    "lungif/egif_lib.c"
    "lungif/gif_err.c"
    "lungif/gifalloc.c"
)

target_include_directories(lungif PUBLIC "lungif")