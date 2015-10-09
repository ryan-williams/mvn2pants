# squarepants/src/test/python/squarepants_test/plugins/BUILD
# HANDWRITTEN

# Default target. Provided as a convenience to run all test targets in this directory

target(name='plugins',
  dependencies = [
    ':run_compile_prep',
    ':sake_wire_codegen',
    ':square_depmap',
    ':staging_build',
  ]
)

python_requirements('requirements.txt')

target(name='common',
  dependencies = [
    'squarepants/src/test/python/squarepants_test:common',
  ],
)

python_tests(name='sake_wire_codegen',
  sources = [ 'test_sake_wire_codegen.py' ],
  dependencies = [
    ':common',
    'squarepants/src/main/python/squarepants/plugins/sake_wire_codegen',
    ':pantsbuild.pants.testinfra',
  ],
)

python_tests(name='run_compile_prep',
  sources = [ 'test_run_compile_prep.py' ],
  dependencies = [
    ':common',
    'squarepants/src/main/python/squarepants/plugins/compile_prep_command',
    ':pantsbuild.pants.testinfra',
  ],
)

python_tests(name='square_depmap',
  sources = [ 'test_square_depmap.py' ],
  dependencies = [
    ':common',
    'squarepants/src/main/python/squarepants/plugins/square_depmap',
  ],
)

python_tests(name='staging_build',
  sources = [ 'test_staging_build.py' ],
  dependencies = [
    ':common',
    'squarepants/src/main/python/squarepants/plugins/staging_build',
   ':pantsbuild.pants.testinfra',
  ],
)
