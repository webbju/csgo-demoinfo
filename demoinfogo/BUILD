
proto_library(
  name = "netmessages_proto",
  srcs = ["netmessages_public.proto"],
)

proto_library(
  name = "cstrike15_usermessages_proto",
  srcs = ["cstrike15_usermessages_public.proto"],
  deps = [":netmessages_proto"],
)

cc_proto_library(
  name = "netmessages_cc_proto",
  deps = [":netmessages_proto"],
)

cc_proto_library(
  name = "cstrike15_usermessages_cc_proto",
  deps = [":cstrike15_usermessages_proto"],
)

cc_binary(
  name = "demoinfogo",
  srcs = [
    "demofile.cpp",
    "demofile.h",
    "demofilebitbuf.cpp",
    "demofilebitbuf.h",
    "demofiledump.cpp",
    "demofiledump.h",
    "demofilepropdecode.cpp",
    "demofilepropdecode.h",
    "demoinfogo.cpp"
  ],
  deps = [
    ":netmessages_cc_proto",
    ":cstrike15_usermessages_cc_proto",
  ],
)
