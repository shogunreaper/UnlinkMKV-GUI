# What is it?


Provides a GUI interface for the UnlinkMKV project by Garret Noling. Aditionally, incorpoates changes from Shane Panke to run cross-platform and provide unified support over many different operating systems.

UnlinkMKV: https://github.com/gnoling/UnlinkMKV

Written with C#, runs on Mono for many different operating systems. 

# Dependencies

The following are required on every platform:

* Perl (required)
* FFmpeg (optional, encoding)
* MKVToolnix (required)
* Mono or .NET Framework

Following the below directions for getting the depedencies you might need:

## Windows

**Perl**: Strawberry Perl has been tested on Windows and works with this application. If you already have some Perl version of some sort installed, it will probably work and you can skip this. Otherwise, install Strawberry Perl from http://strawberryperl.com/ The latest version will be fine.

**MKVToolnix**: Install from here and use the installer https://www.bunkus.org/videotools/mkvtoolnix/downloads.html (or you can download the ZIP and add it to your PATH, if you prefer)

**FFmpeg**: This is optional, only required if you want to encode but you can find many guides on the internet to setting it up, such as this: http://jonhall.info/how_to/setup_and_use_ffmpeg_on_windows

**.NET**: You should already have this.


## OSX

**Perl**: This is already installed for you
**MKVToolnix**: You can install it from Homebrew. If you don't have Homebrew yet, run `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Then, you should be able to run:

`brew install -vb --with-flac mkvtoolnix`

**Fmpeg**: Run with Brew, `brew install ffmpeg --with-fdk-aac --with-ffplay --with-freetype --with-frei0r --with-libass --with-libvo-aacenc --with-libvorbis --with-libvpx --with-opencore-amr --with-openjpeg --with-opus --with-rtmpdump --with-schroedinger --with-speex --with-theora --with-tools`

**Mono**: `brew install mono` to install Mono from Brew.

**About Homebrew**: You will require the XCode Command Line Tools to use Homebrew; you can find a guide on that here: http://railsapps.github.io/xcode-command-line-tools.html

## Linux

If you're running on Linux, you will need to look up how to get the tools above from your local package repository via your package manager from your distribution of choice.

## Every Operating System

You will probably need `Log::Log4perl` for your Perl installation. You can do this step just in case if you're not sure if it's installed. 

1. Open a terminal or command prompt on your operating system
2. Type `cpan Log::Log4perl` and then press return/enter
3. The CPAN manager should install the logging module, you should be able to exit the terminal now.


# Using the application

After installing all the depedencies, just run the application. 

* Input Folder: Just select where the files you want to unlink are and they will be handled
* Output Folder: Just select where you want the files to be placed

The check boxes should be left unchecked for the most part unless you have a particular issue with a release. You can play around with them and file a bug report if a certain MKV file is not working.

# I found a bug/the application doesn't Unlink my MKV's properly. Help?

You can post the issue with a verbose log on the issue tracker. Tick the "verbose output" checkbox in the options when doing the run before posting a log on the issue tracked. If the issue is part of the UnlinkMKV core, it will be addressed there. Otherwise, it will be addressed here. 

# For developers

Pull requests are appreciated. Please feel free to submit them.