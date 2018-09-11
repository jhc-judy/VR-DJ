# VR DJ
Game Application --> demo.exe

A modification version of [Virtual-Reality-DJ-Unity](https://github.com/khoslaventures/Virtual-Reality-DJ-Unity/blob/master/README.md)

**meant to be play with HTC Vive MGE or later HMD with built-in microphone

Using STT engine to control Unity game content. Currently in its initial phase that allows the user to control volume and EQ simply with voice commands.

The game content is a virtual reality music visualizer. The scene has 8 panels in total (3 bars in each panel -> 24 bars), each panel represents different frequency (30Hz, 90Hz, 250Hz, 600Hz, 1400Hz, 4500Hz, 12000Hz, 20000Hz).
The highlighted (yellow-greenish) panel is the one the user is gazing at. To tune the gain of a certain frequency, the user is required to speak the keywords “higher” and “lower”. Once the STT engine catches a voice from the microphone built in HMD, it’ll transcribe the audio and pass the result back, the words will be shown in the middle of the screen. All we need to do is to check whether the result string contains our keywords. If it does, for example, has an “higher” word in it, the highlighted frequency gain will be added. If the frequency gain is added (> 1), the bars will appear in the color red; on the contrary, if the frequency gain is reduced (< 1), the bars will appear in the color blue. There will also be an effect to notify the user that the gain had been tuned.

List of commands:
    EQ: "higher" & "lower"
    volume: "volume up" or "louder"
            "volume down" or "quieter"
    extra commands: "mute" & "unmute"
