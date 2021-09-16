# oh-my-zsh-emoji-theme
- oh-my-zsh随机emoji主题
- 枯燥的coding生活添一些乐趣
- 每一次回车，随机出不同的emoji，哈哈哈。。。

- 只需要把`${emoji_arr[$[${RANDOM}%${len_arr}]]}`添加到自己使用主题里的PROMPT变量中，就可以使用了
```shell
emoji_arr=(😀 😁 😂 😃 😄 😅 😆 😉 😊 😋 😎 😍 😘 😗 😙 😚 😇 😐 😑 😶 😏 😣 😥 😮 😯 😪 😫 😴 😌 😛 😜 😝 😒 😓 😔 😕 😲 😷 😖 😞 😟 😤 😢 😭 😦 😧 😨 😬 😰 😱 😳 😵 😡 😠 😈 👿 👹 👺 💀 👻 👽 👦 👧 👨 👩 👴 👵 👶 👱 👮 👲 👳 👷 👸 💂 🎅 👰 👼 💆 💇 🙍 🙎 🙅 🙆 💁 🙋 🙇 🙌 🙏 👤 👥 🚶 🏃 👯 💃 👫 👬 👭 💏 💑 👪 💪 👈 👉 ☝ 👆 👇 ✌ ✋ 👌 👍 👎 ✊ 👊 👋 👏 👐 ✍ 👣 👀 👂 👃 👅 👄 💋 👓 👔 👕 👖 👗 👘 👙 👚 👛 👜 👝 🎒 💼 👞 👟 👠 👡 👢 👑 👒 🎩 🎓 💄 💅 💍 🌂  🙈 🙉 🙊 🐵 🐒 🐶 🐕 🐩 🐺 🐱 😺 😸 😹 😻 😼 😽 🙀 😿 😾 🐈 🐯 🐅 🐆 🐴 🐎 🐮 🐂 🐃 🐄 🐷 🐖 🐗 🐽 🐏 🐑 🐐 🐪 🐫 🐘 🐭 🐁 🐀 🐹 🐰 🐇 🐻 🐨 🐼 🐾 🐔 🐓 🐣 🐤 🐥 🐦 🐧 🐸 🐊 🐢 🐍 🐲 🐉 🐳 🐋 🐬 🐟 🐠 🐡 🐙 🐚 🐌 🐛 🐜 🐝 🐞 🦋  💐 🌸 💮 🌹 🌺 🌻 🌼 🌷 🌱 🌲 🌳 🌴 🌵 🌾 🌿 ☘ 🍀 🍁 🍂 🍃)
len_arr=${#emoji_arr[*]}

PROMPT='xxxxx ${emoji_arr[$[${RANDOM}%${len_arr}]]} xxxxx'
```

- 如果不想每次回车都改变，而是打开终端才随机，需要把单引号改成双引号，为了不影响原主题效果，可以这么写

```shell
# 原PROMPT
PROMPT='%{$fg[green]%}%n@%m: %{$fg_bold[blue]%}%2~ $(git_prompt_info)%{$reset_color%}%(!.#.$) '

# 修改之后
PROMPT='%{$fg[green]%}%n@%m:'
PROMPT+="${emoji_arr[$[${RANDOM}%${len_arr}]]}"
PROMPT+='%{$fg_bold[blue]%}%2~ $(git_prompt_info)%{$reset_color%}%(!.#.$) '
```
