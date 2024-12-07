python_sources()

python_tests(
    name="tests",
)


# This target allows us to build a `.whl` bdist and a `.tar.gz` sdist by auto-generating
#  `setup.py`. See https://www.pantsbuild.org/docs/python-distributions.
#
# Because this target has no source code, Pants cannot infer dependencies. We depend on `:lib`,
#  which means we'll include all the non-test Python files in this directory, and any of
#  their dependencies.
python_distribution(
    name="dist",
    dependencies=[],
    wheel=True,
    sdist=True,
    provides=setup_py(
        name="otrace",
        version="0.0.1",
        description="Application profiler",
    ),
)
