from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

# add hdc15 src files.
if GetDepend('PKG_USING_HDC15'):
    src += Glob('src/hdc15.c')

if GetDepend('PKG_USING_HDC15_SAMPLE'):
    src += Glob('samples/hdc15_sample.c')

# add hdc15 include path.
path  = [cwd + '/inc']

# add src and include to group.
group = DefineGroup('hdc15', src, depend = ['PKG_USING_HDC15'], CPPPATH = path)

Return('group')
