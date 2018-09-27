###############################################################################
# Project infos

project('epsilon-updater',
  'cpp',
  version: '0.1',
  meson_version: '>=0.45.0',
)

i18n = import('i18n')

config = configuration_data()

gettext_package = meson.project_name()
config.set('GETTEXT_PACKAGE', gettext_package)

###############################################################################
# Dependencies

gtk3    = dependency('gtk+-3.0', version: '>=3.0')
libusb  = dependency('libusb-1.0')

###############################################################################

configure_file(
  output: 'config.h',
  configuration: config,
)
rootInclude = include_directories('.')

subdir('po')
subdir('src')
