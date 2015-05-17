# heightmaps

Ready to use heightmaps from SRTM

SRTM data are distributed in two levels: SRTM1 (for the U.S. and its territories and possessions) with data sampled at one arc-second intervals in latitude and longitude, and SRTM3 (for the world) sampled at three arc-seconds.

Data are divided into one by one degree latitude and longitude tiles in "geographic" projection, which is to say a raster presentation with equal intervals of latitude and longitude in no projection at all but easy to manipulate and mosaic.

File names refer to the latitude and longitude of the lower left corner of the tile - e.g. N37W105 has its lower left corner at 37 degrees north latitude and 105 degrees west longitude. To be more exact, these coordinates refer to the geometric center of the lower left pixel, which in the case of SRTM3 data will be about 90 meters in extent.

Height files have the extension .HGT and are signed two byte integers. The bytes are in Motorola "big-endian" order with the most significant byte first, directly readable by systems such as Sun SPARC, Silicon Graphics and Macintosh computers using Power PC processors. DEC Alpha, most PCs and Macintosh computers built after 2006 use Intel ("little-endian") order so some byte-swapping may be necessary. Heights are in meters referenced to the WGS84/EGM96 geoid. Data voids are assigned the value -32768.

