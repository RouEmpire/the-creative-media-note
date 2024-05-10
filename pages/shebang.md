type:: [[Programming Features]] 
Language:: All Shelll Languages, in cluding [BASH](BASH - soon_class)

- Shebang start at the first line of the file
- She bang always start with `#!`
- example `#!/bin/bash` or `#!/bin/fish
- Every Single thing in shebang has meaning
	- `#` means *This is shebang* we type this to start shebang
	- `!` means _root directory_ this is like we are in a root, the `/` need to be present after this
	- `/` means _sub-directory_, the next word after `/` is a deeper directory name
- generally, when the `#` start, the rest of the line will be treat as a [[comment]]. Except when it's in the first line, it will become a shebang