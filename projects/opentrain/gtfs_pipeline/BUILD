# gtfs_pipeline definition

genrule(
    name = "data_analysis_part1",
    srcs = ["@gtfs_data//:agency.txt",
            "@gtfs_data//:calendar.txt",
            "@gtfs_data//:fare_attributes.txt",
            "@gtfs_data//:fare_rules.txt",
            "@gtfs_data//:routes.txt",
            "@gtfs_data//:shapes.txt",
            "@gtfs_data//:stop_times.txt",
            "@gtfs_data//:stops.txt",
            "@gtfs_data//:translations.txt",
            "@gtfs_data//:trips.txt"
            ],
    cmd = "$(location //projects/opentrain/gtfs_pipeline/data_handler:data_handler) $(location @gtfs_data//:agency.txt) $(location @gtfs_data//:calendar.txt) $(location @gtfs_data//:fare_attributes.txt) $(location @gtfs_data//:fare_rules.txt) $(location @gtfs_data//:routes.txt) $(location @gtfs_data//:shapes.txt) $(location @gtfs_data//:stop_times.txt) $(location @gtfs_data//:stops.txt) $(location @gtfs_data//:translations.txt) $(location @gtfs_data//:trips.txt) $@",
    outs = ["files_content"],
    tools = ["//projects/opentrain/gtfs_pipeline/data_handler:data_handler"],
)