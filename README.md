# Native Function Static Map

#### What is this?
- A *very* naive attempt to use `Windbg Preview`'s scripting component to generate `JSON`, which was then rendered to a table in `ReactJS`
    - The result you see is just a `PDF` of the rendered page 

#### Who wrote it?
- Justin Lucas  ([@the_bit_diddler](https://twitter.com/the_bit_diddler))

#### What problem are you trying to solve?
- A [question](https://twitter.com/0xBoku/status/1470770303714353165) posed by [Bobby Cooke](https://twitter.com/0xBoku) got me thinking of an older [`PoC`](https://gist.github.com/EspressoCake/3c7743742840992c7d7424d569ae5e02#file-naivegrabzwntcalls-js), and I figured that it could be extended/modified to suit some aspects of that request
    - Notably, ~~ab~~use of the `.logopen` and `.logclose` `Windbg` commands to dump the global `JSON` representation

#### What about a dynamic/traced version, vs. static?
- Please refer to [b33f's](https://twitter.com/FuzzySec) project utilizing Frida, [Fermion!](https://github.com/FuzzySecurity/Fermion)

#### What are the limitations?
- It isn't guaranteed that all/any of these calls will be reflected on *your specific system/build version*; verify yourself!
- The original script has its limitations, and I'm aware of it's missing of some more obvious functions/symbols (e.g. `CreateProcess(Ex)`)
    - I plan on identifying the cause of this at some point, but no promises
