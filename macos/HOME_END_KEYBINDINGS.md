If you set HOME and END to hexcode `0x01` and `0x05` in iTerm2 key mapping, the keys would work at the prompt
But will stop working in VIM.

If you don't set HOME and END as above, the keys will work in VIM.

To fix this:
- Remove any mappings in iTerm2 key mappings
- Add this to `~/.zshrc`
  * `bindkey "^[[H" beginning-of-line`
  * `bindkey "^[[F" end-of-line`
- source ~/.zshrc

Ref: https://apple.stackexchange.com/a/420407/429035
