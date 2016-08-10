task :default do
  sh "rm -f riverl_usa.shp"
  sh "cat riverl_usa.shp.aa riverl_usa.shp.ab riverl_usa.shp.ac > riverl_usa.shp"
  sh "rm -f riverl_usa.dbf"
  sh "cat riverl_usa.dbf.aa riverl_usa.dbf.ab > riverl_usa.dbf"
end
task :split do
  %w{riverl_usa.shp riverl_usa.dbf}.each {|path|
    sh "split -b 85m #{path} #{path}."
  }
end
