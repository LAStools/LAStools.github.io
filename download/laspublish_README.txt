****************************************************************

  laspublish:

  Creates a LiDAR portal for 3D visualization (and optionally also
  for downloading) of LAS and LAZ files in any modern Web browser
  using the WebGL Potree from Markus Schuetz.

  For updates check the website or join the LAStools mailing list.

  http://rapidlasso.com/laspublish/
  http://rapidlasso.com/LAStools/
  http://groups.google.com/group/LAStools/
  http://twitter.com/LAStools/
  http://facebook.com/LAStools/
  http://linkedin.com/groups/4408378

  Martin @LAStools

****************************************************************

example usage:

>> laspublish -i lidar.laz -odir portal_dir -o portal.html -olaz

creates a directory called "./portal_dir" containing an HTML file
called "portal.html" that allows exploring the LiDAR points from
the file "lidar.laz" once the directory is moved into Web space.

>> laspublish -i tiles_final/*.laz -odir portal_dir -o portal.html -olaz

same as above for an entire folder of input files.

>> laspublish -i tiles_final/*.laz -copy_source_files -odir portal_dir -o portal.html -olaz

same as above but also copies the original LAZ files into the portal
subdirectory ./portal_dir/pointclouds/portal/source where they need
to reside in order for the download map to link to them properly 

>> laspublish -i tiles_final/*.laz -only_3D -odir portal_dir -o portal.html -olaz

same as above but only the 3D online viewer (without the map)

>> laspublish -i tiles_final/*.laz -only_2D -odir portal_dir -o portal.html -olaz

same as above but only the 2D map

>> laspublish -i tiles_final/*.laz -only_2D -copy_source_files -odir portal_dir -o portal.html -olaz

same as above but also copies the original LAZ files into the portal
subdirectory ./portal_dir/pointclouds/portal/source where they need
to reside in order for the download map to link to them properly 

Instead of using '-copy_source_files' or '-move_source_files' it is
also possible to copy or move the LAZ files manually to the correct
subfolder in the portal. For this example command line here

>> laspublish -i tiles/*.laz -odir aaaaa -o bbbbb.html -olaz

this subfolder needs to be located in this exact location

./aaaaa/pointclouds/bbbbb/source

so that all links from the download map will correctly link to the
original LAZ files

---------------

if you find bugs let me (martin.isenburg@rapidlasso.com) know.