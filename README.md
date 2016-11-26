# Speech-to-Text_via_Max
Implementing communication with IBM Watson's Bluemix STT engine with Cycling 74 Max

Max is a tool developed by &copy;Cycling '74, "Max connects objects with virtual patch cords to create interactive sounds, graphics, and custom effects". Basically, users create nodes with functioning objects and then connect them together to work.

This implementation utilizes Max's built-in curl tool, Maxurl to realize communication with IBM Bluemix STT engine via curl commands, which is direct and easy.

__Note__: Languange preference for STT conversion in the socket: English (default).

####Instructions
    1.(For first time users)Install Max, a registration and trial activation is needed to actually save Max projects users created(save functionality otherwise nulled by default)
    2.Open Speech-to-Text.maxpat in Max, by default the lock icon on the bottom left corner is locked, which means the patch is "turned on", keep it locked
Double click the upmost box that says "dict @embed 1", which pops out the Dictionary Editor window.
    3.In the Dictionary Editor window, replace the value for "http_auth", i.e. "username:password", with your credentials generated from Bluemix console's STT instance(if you don't have one already, you'll need to register for a free account on Bluemix and create one yourself, and IBM assigns its Bluemix users with certain amounts of free monthly usage of Bluemix services)
    4.Replace the value for "filename_in" with the actual path for the speech clip you want to turn into text.
__NOTE__ that the format for file path displayed by default is the pattern for macOS, if you're running the patch on Windows, format for file paths would be something like "[volume]:\\Project\\voiceinput.wav"
    5.Close the window for Dictionary Editor directly.
    6.There are two buttons (square boxes with grey cirles inside) in the patch, click the upper one first, then click the second one
    7.The converted text should appear in the message box on the bottom right corner.
