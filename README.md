# zemojify

## Emoji on the command line :scream: - The ZSH Version

This is a ZSH version of the excellent [emojify] by [Justyna Rachowicz]. Thanks
Justyna!

I came across [this issue] on the original repository and, even though a port to
ZSH wasn't needed, I thought "why not? :man_shrugging:"

## Installation

Just add `zemojify` to your `$PATH` and you're good to go.

### Zplug

If you use Zplug, you can add `zemojify` with the following:

```zsh
zplug filipekiss/zemojify, as:"command"
```

If you wanna replace `emojify`

```zsh
zplug filipekiss/zemojify, as:"command", rename-to:emojify
```

## Usage

If you use `emojify`, `zemojify` is a drop-in replacement. (In fact, you can
even name it `emojify` and it will work as expected.)

##### Replace in string

`zemojify "Welcome to Narnia! :lion_face:`

Output: Welcome to Narnia! :lion_face:

##### Pipe-in

`git log --color | zemojify | less`

##### Using in all pagers

Add this to your .zshrc

`(( $+commands[zemojify]] )) && export PAGER="zemojify | ${PAGER}"`

## Related

*   [emojify] - The original bash script
*   [pyemojify](https://github.com/lord63/pyemojify) - python port

## License

MIT

[emojify]: https://github.com/mrowa44/emojify
[justyna rachowicz]: https://github.com/mrowa44
[this issue]: https://github.com/mrowa44/emojify/issues/32