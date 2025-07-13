project(
    'ne',
    'c',
    meson_version: '>= 1.3.0',
    version: '0.1',
    default_options: ['warning_level=3', 'c_std=c99'],
)

dependencies = [dependency('curses')]

add_project_arguments(
    '-D_GNU_SOURCE',
    '-DSTDC_HEADERS',
    '-DDNOWCHAR',
    '-DHAVE_SNPRINTF',
    '-fno-strict-aliasing',
    '-D_REGEX_LARGE_OFFSETS',
    '-Wp,-D_FORTIFY_SOURCE=2',
    '-Wno-error=implicit-function-declaration',
    '-DGLOBALDIR="/usr/local/share/ne"',
    language: 'c',
)

subdir('src')
exe = executable(
    'ne',
    [sources],
    dependencies: [dependency('ncurses')],
    install: true,
)
