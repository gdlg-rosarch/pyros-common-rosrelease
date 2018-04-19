# Script generated with Bloom
pkgdesc="ROS - Common interfaces packages for Pyros framework"


pkgname='ros-kinetic-pyros-common'
pkgver='0.4.2_2'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-kinetic-catkin-pip>=0.2.0'
'ros-kinetic-catkin>=0.6.18'
'ros-kinetic-pyros-config>=0.1.5'
'ros-kinetic-pyzmp>=0.0.14'
)

depends=('ros-kinetic-pyros-config>=0.1.5'
'ros-kinetic-pyzmp>=0.0.14'
)

conflicts=()
replaces=()

_dir=pyros_common
source=()
md5sums=()

prepare() {
    cp -R $startdir/pyros_common $srcdir/pyros_common
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

