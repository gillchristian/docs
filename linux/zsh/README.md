# zsh

- [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh).
- [antigen](http://antigen.sharats.me/). zsh plugin manager.
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting).
- [LS_COLORS](https://github.com/trapd00r/LS_COLORS).
- [z](https://github.com/rupa/z). `cd` with ML powers!

---

## Troubleshooting

### `ga` outcomplete not working

```shell
_git-add: Function definition file not found
```

It's an issue with `zcompdump` files that need to be removed ([reference](https://github.com/robbyrussell/oh-my-zsh/issues/3996#issuecomment-356049501)).
