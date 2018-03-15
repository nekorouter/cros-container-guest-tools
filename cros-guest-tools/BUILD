load("@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar", "pkg_deb")

pkg_tar(
    name = "debian-data",
)

pkg_deb(
    name = "cros-guest-tools-deb",
    architecture = "all",
    data = ":debian-data",
    description_file = "deb-description",
    homepage = "https://chromium.org",
    maintainer = "The Chromium OS Authors <chromium-os-dev@chromium.org>",
    package = "cros-guest-tools",
    version = "0.4",
    section = "misc",
    depends = ["cros-garcon"],
    recommends = ["bash-completion",
                  "cros-apt-config",
                  "cros-sudo-config",
                  "cros-ui-config",
                  "cros-wayland",
                  "cros-xwl-config",
                  "xwl"],
)