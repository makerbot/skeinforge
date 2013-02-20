# vim:ai:et:ff=unix:fileencoding=utf-8:sw=4:syntax=python:ts=4:

import os

env = Environment(ENV = os.environ)

env.Tool('mb_install', toolpath=[Dir('submodule/mw-scons-tools')])
env.MBInstallResources('documentation', 'skeinforge')
env.MBInstallResources('fabmetheus_utilities', 'skeinforge')
env.MBInstallResources('skeinforge_application', 'skeinforge')

# seriously, skeinforge?
env.Command('winding', [], [Mkdir('winding')])
env.MBInstallResources('winding', os.path.join('skeinforge', 'skeinforge_application', 'profiles'))

env.MBCreateInstallTarget()