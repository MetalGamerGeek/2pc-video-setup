# 2 PC setup without extra hardware (captpure card)

### Video capture

Install Sunshine on Gaming PC - https://app.lizardbyte.dev/Sunshine/?lng=en-US - This will act in tandem with Moonlight as your capture card and send your gameplay video / audio to clients on your network

    1. Set up admin account
    2. Input tab - Uncheck everything as this is just going to be used to send video / audio over to the Streaming PC. Leaving these checked will make it so when you move the mouse/use the keyboard on the Streaming PC, it will mirror onto the host machine (Gaming PC)
    3. Advanced tab - At the bottom, I selected to force the Nvidia NVENC encoder
 
Install Moonlight on Streaming PC - https://moonlight-stream.org/ - This will receive the video/audio from Sunshine. Moonlight will detect any PC's that have Sunshine installed on it and give you the option to stream the Desktop or in Big Picture Mode on the Gaming machine. 

#### BEFORE YOU DO ANYTHING - Open the settings on Moonlight

**Basic Settings**

    1. Resolution and FPS - Set it to at least 1080p x 60fps and whatever bitrate your network can handle or else your Gaming machine will get all wonky. If your machine can handle it, go higher
    2. Display Mode - Borderless Windowed, unless you have an additional monitor you can dedicate to it for fullscreen mode
        
**Audio Settings**
    
    1. Make sure that the following are not checked 
        a. Mute host PC speakers while streaming
        b. Mute audio stream when Moonlight is not the active window
        
**Advanced Settings**

    1. Video decoder
        a. Force hardware decoding
        b. Video codec - If you've got a newer 40XX series, go for AV1. Otherwise go for HEVC
        
Now you can run either Desktop Capture or Big Picture Mode and in Moonlight and it will capture with basically no latency

### OBS

    1. Add a Game Capture source
        a. Choose the window for Moonlight
        b. Make sure you select Capture Audio

