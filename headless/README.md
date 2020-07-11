# Godot Engine Standard Headless

Version: Godot Engine v3.2.2.stable.official - https://godotengine.org

Run your GDScript and unit tests.

```
# hw.gd
extends SceneTree

func _init():
    print("Hello, world!")
    quit()
```

```
docker run -it --rm -v`pwd`:/s -w /s mtmk/godot /godot -s hw.gd
```

Place an alias in your .rc file for convenience
```
alias godots='docker run -it --rm -v $(pwd):/s -w /s mtmk/godot /godot -s'

$ godots hw.gd
Godot Engine v3.2.2.stable.official - https://godotengine.org

Hello, world!
```
