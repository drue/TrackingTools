TrackingTools
-------------

This is a small set of scripts I wrote for processing concerts to upload to and downloaded from etree.org.

### copytags

Copies tags from FLAC files to FLAC files or MP3 files.
Copying to MP3 requires the command line tool `id3tag` but I don't know
which or where it came from.  It needs to be converted to mutagen like the others.


### cuecutter

Cuecutter reads a cuesheet and uses it too cut up a flac file.  You
specify the output filenames like this "aShow2012t%s.flac" and it puts
the track number where you want it.  You can also have it drop the
first and/or last track.

### flac2mp3

Converts flac files to mp3 using shntool and lame.

### reshow

Copy to the band / date / venue / location in standard etree format to
the pasteboard then run this script, giving it a list of FLAC or MP3 files,
and it set the artist, album, and track number tags for you.  This
only works on Mac OSX because it uses the pbpaste command.  It assumes
the ordering is band, date, venue, then location and it assumes the
date format.

The format looks like this:

    Holiday Jam
    2012-12-24
    Fillmore East
    New York City, NY

In which case the album tag will be `2012-12-24 Fillmore East, New York City NY`

### retitle

Copy the setlist to the pasteboard and run this script on a set of
FLACs or MP3s.  It will parse the setlist and set the title and track
number for you.  It's a little smart, skipping things like "Set 1" and
making sure the number of tracks it parsed matches the number of files
you supply, but it's not very smart.

### rsplits

Renames flac files in a directory.  Give it a new name like
`myshow2012-00-00s1t%s.flac` and it will put the track number in for
you.

