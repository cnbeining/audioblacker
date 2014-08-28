audioblacker
============

Yet another video patch tool to bypass Letvcloud's encode.

This cheat would not add video time, which is better than VFR(https://github.com/cnbeining/FlvPatcher  ). Also quicker and use less space.

Requirement
-------

- Python 2.7
- ffmpeg
- ffprobe
- Enough spare space: the size of the original video plus 2 (3 if use safe mode with auto-cleaning failed) times of the audio stream.

Usage
------

    Usage:
    
    python audioblacker.py (-h) (-i input.mp4) (-o output.mp4) (-b 1900000) (-a 110000) (-s 1)
    
    -h: Default: None
        Help.
    
    -i: Default: Blank
        Input file.
        If the file and audioblacker are not under the same path,
        it is suggested to use absolute path to avoid possible failure.
    
    -o Default: input-filename.black.mp4
       Output file.
       Would be in the same folder with the original file if not specified.
       
    -b: Default: 1900000
        Target bitrate.
    
    -a: Default: 110000
        Target audio bitrate.
        
    audioblacker would calculate both of the required black time,
    and choose the larger one to make sure your convert is successful.
    
    Please notice that if your original video/audio bitrate is too small,
    audioblacker would throw you an ERROR and quit.
    
    -s: Default: 1
        Use safe mode.
        audioblacker would check whether the file's audio is AAC.
        Disabling would save you some space and time,
        if you know what you are doing.


Author
-----

Beining, http://www.cnbeining.com/

License
-----

GNUv2 license.

Misc
-----

- You are not supposed to refer/mention/promote this software at any service within Chinese Mainland.

- This method is enlightened by @七音弦樱 and @LYF.

History
----

0.21: Fix if some metadata included the programme would failed

0.2: Fix accuracy; Fix safemode failed; Fix codec; Fix if filename contain '.' the auto filename would failed; Change default 

0.1: The very beginning
