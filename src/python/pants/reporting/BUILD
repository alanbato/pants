# Copyright 2014 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

python_library(
  sources=globs('*.py', exclude=[['report.py']]),
  dependencies=[
    '3rdparty/python:future',
    '3rdparty/python:ansicolors',
    '3rdparty/python:pystache',
    '3rdparty/python:six',
    ':report',
    ':reporting_resources',
    'src/python/pants/base:build_environment',
    'src/python/pants/base:build_file',
    'src/python/pants/base:mustache',
    'src/python/pants/base:project_tree',
    'src/python/pants/base:run_info',
    'src/python/pants/base:workunit',
    'src/python/pants/build_graph',
    'src/python/pants/option',
    'src/python/pants/pantsd:process_manager',
    'src/python/pants/stats',
    'src/python/pants/subsystem',
    'src/python/pants/util:dirutil',
    'src/python/pants/util:memo',
  ]
)

resources(
  name='reporting_resources',
  sources=rglobs('assets/*', 'templates/*.mustache')
)

python_library(
  name='report',
  sources=['report.py'],
  dependencies=[
    '3rdparty/python:future',
  ],
)
