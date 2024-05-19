# OsuExec
OsuExec is a modding software directed towards the game osu!. It allows you to execute Lua scripts to do various things to the osu! game client, such as create a simple relax for standard.

## Disclaimer
This software should be used offline to reduce the chance of your account getting restricted. osu! strictly prehibits the use of modifications (esp ones **that give you an unfair advantage**).

## Notable Features
### Completely External
OsuExec is completely external, meaning you will probably not get banned by the anticheat. Still be aware of the risks of setting scores that are cheated, since if you get too much performance points too fast, your account is basically gone.

### Custom Lua Env
We use a custom lua env, allowing for the use of variables that Lua wouldn't have normally, such as audio time or current hitobject positions.

### Unrestricted Scripting
OUr software is designed to allow users to create any scripts they would like, ranging from relax hacks to aim assist. More functionality to make more scripts will be added eventually.

## Lua Env Documentation
### As stated above, our lua env comes with custom values, variables, and functions to be used. They can be found below.

/ / OSU VALUES / /

(INTEGER) audio_time - The osu! beatmap audio time

/ / HITOBJECT VALUES / /

(INTEGER) current_hitobject_x - X position component of the current hitobject

(INTEGER) current_hitobject_y - Y position component of the current hitobject

(STRING) current_hitobject_type - Returns the type of hitobject (Circle, Slider, Spinner)

(INTEGER) current_hitobject_starttime - Returns the position in the audio where the note starts

(INTEGER) current_hitobject_endtime - Returns the position in the audio where the note ends

/ / EVENT FUNCTIONS / /

(FUNCTION) note_event(int x, int y, string type, int start_time, int end_time) - A function that is called for every note

(FUNCTION) state_event(string state) - A function that is called every time the osu! client state changes (ex: switching from menu to beatmap selection)

/ / INPUT FUNCTIONS / /

(FUNCTION) move_mouse_relatively(int deltaX, int deltaY) - Moves the mouse using deltas

(FUNCTION) press_key(int keycode) - Presses a key down

(FUNCTION) release_key(int keycode) - Stops pressing a key

## WIP
