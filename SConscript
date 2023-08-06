from building import *

cwd = GetCurrentDir()

src = []
CPPPATH = []

if GetDepend('PKG_USING_CMSIS_DSP'):
    CPPPATH += [cwd + '/Include']
    CPPPATH += [cwd + '/Include/dsp']
    CPPPATH += [cwd + '/PrivateInclude']
    CPPPATH += [cwd + 'ComputeLibrary/Include']

    if GetDepend('PKG_CMSIS_DSP_BASIC_MATH'):
        src += [cwd + '/Source/BasicMathFunctions/BasicMathFunctions.c']
        src += [cwd + '/Source/BasicMathFunctions/BasicMathFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_BAYES'):
        src += [cwd + '/Source/BayesFunctions/BayesFunctions.c']
        src += [cwd + '/Source/BayesFunctions/BayesFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_COMMON_TABLES'):
        src += [cwd + '/Source/CommonTables/CommonTables.c']
        src += [cwd + '/Source/CommonTables/CommonTablesF16.c']

    if GetDepend('PKG_CMSIS_DSP_COMPLEX_MATH'):
        src += [cwd + '/Source/ComplexMathFunctions/ComplexMathFunctions.c']
        src += [cwd + '/Source/ComplexMathFunctions/ComplexMathFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_CONTROLLER'):
        src += [cwd + '/Source/ControllerFunctions/ControllerFunctions.c']

    if GetDepend('PKG_CMSIS_DSP_DISTANCE'):
        src += [cwd + '/Source/DistanceFunctions/DistanceFunctions.c']
        src += [cwd + '/Source/DistanceFunctions/DistanceFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_FAST_MATH'):
        src += [cwd + '/Source/FastMathFunctions/FastMathFunctions.c']
        src += [cwd + '/Source/FastMathFunctions/FastMathFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_FILTERING'):
        src += [cwd + '/Source/FilteringFunctions/FilteringFunctions.c']
        src += [cwd + '/Source/FilteringFunctions/FilteringFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_INTERPOLATION'):
        src += [cwd + '/Source/InterpolationFunctions/InterpolationFunctions.c']
        src += [cwd + '/Source/InterpolationFunctions/InterpolationFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_MATRIX'):
        src += [cwd + '/Source/MatrixFunctions/MatrixFunctions.c']
        src += [cwd + '/Source/MatrixFunctions/MatrixFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_QUATERNION_MATH'):
        src += [cwd + '/Source/QuaternionMathFunctions/QuaternionMathFunctions.c']

    if GetDepend('PKG_CMSIS_DSP_STATISTICS'):
        src += [cwd + '/Source/StatisticsFunctions/StatisticsFunctions.c']
        src += [cwd + '/Source/StatisticsFunctions/StatisticsFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_SUPPORT'):
        src += [cwd + '/Source/SupportFunctions/SupportFunctions.c']
        src += [cwd + '/Source/SupportFunctions/SupportFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_SVM'):
        src += [cwd + '/Source/SVMFunctions/SVMFunctions.c']
        src += [cwd + '/Source/SVMFunctions/SVMFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_TRANSFORM'):
        src += [cwd + '/Source/TransformFunctions/TransformFunctions.c']
        src += [cwd + '/Source/TransformFunctions/TransformFunctionsF16.c']

    if GetDepend('PKG_CMSIS_DSP_WINDOW'):
        src += [cwd + '/Source/WindowFunctions/WindowFunctions.c']

    if GetDepend('PKG_CMSIS_DSP_COMPUTE_LIBRARY'):
        src += [cwd + '/ComputeLibrary/Source/*.c']

group = DefineGroup('CMSIS_DSP', src, depend = ['PKG_USING_CMSIS_DSP'], CPPPATH = CPPPATH)

Return('group')
