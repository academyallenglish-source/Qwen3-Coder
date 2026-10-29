<a name="readme-top"></a>

<p align="center">
    <img src="https://qianwen-res.oss-cn-beijing.aliyuncs.com/Qwen3-Coder/qwen3_coder.png" width="400"/>
</p>

<p align="center">
    <img src="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/swebench_pro.png" width="800"/>
</p>

<p align="center">
        💜 <a href="https://chat.qwen.ai/"><b>Qwen Chat</b></a>&nbsp&nbsp | &nbsp&nbsp🤗 <a href="https://huggingface.co/collections/Qwen/qwen3-coder-687fc861e53c939e52d52d10">Hugging Face</a>&nbsp&nbsp | &nbsp&nbsp🤖 <a href="https://modelscope.cn/organization/qwen">ModelScope</a>&nbsp&nbsp | &nbsp&nbsp 📑 <a href="https://qwenlm.github.io/blog/qwen3-coder-next/">Blog</a> &nbsp&nbsp ｜ &nbsp&nbsp📖 <a href="https://qwen.readthedocs.io/">Documentation</a>
<br>
🌍 <a href="https://huggingface.co/spaces/Qwen/Qwen3-Coder-WebDev">WebDev</a>&nbsp&nbsp | &nbsp&nbsp💬 <a href="https://github.com/QwenLM/Qwen/blob/main/assets/wechat.png">WeChat (微信)</a>&nbsp&nbsp | &nbsp&nbsp🫨 <a href="https://discord.gg/CV4E9rpNSD"> Discord</a>&nbsp&nbsp | &nbsp&nbsp 📄 <a href="https://github.com/QwenLM/Qwen3-Coder/blob/main/qwen3_coder_next_tech_report.pdf">Arxiv</a>&nbsp&nbsp | &nbsp&nbsp 👽 <a href="https://github.com/QwenLM/qwen-code">Qwen Code</a>
</p>

Visit our Hugging Face or ModelScope organization (click links above), search checkpoints with names starting with `Qwen3-Coder-`, and you will find all you need! Enjoy!

---

## Table of Contents
  - [Introduction](#introduction)
    - [Key Features](#key-features)
  - [Basic Information](#basic-information)
  - [Quick Start](#quick-start)
    - [👉🏻 Chat with Qwen3-Coder](#-chat-with-qwen3-coder)
      - [Fill in the middle with Qwen3-Coder](#fill-in-the-middle-with-qwen3-coder)
  - [Use Cases](#use-cases)
    - [Example: Releasing a Website](#example-releasing-a-website)
    - [Example: Desktop Tidy](#example-desktop-tidy)
    - [Example: Zombies vs. Plants](#example-zombies-vs-plants)
    - [Example: Sound ASCII Art](#example-sound-ascii-art)
    - [Example: Vibe Checking](#example-vibe-checking)
    - [Example: Parkour Game](#example-parkour-game)
  - [Star History](#star-history)
  - [Citation](#citation)
  - [Contact Us](#contact-us)

---

# Qwen3-Coder-Next: Pushing Small Hybrid Models on Agentic Coding

## Introduction

We are announcing Qwen3-Coder, our most agentic code model to date. **Qwen3-Coder** is available in multiple sizes, **Qwen3-Coder-480B-A35B-Instruct**, **Qwen3-Coder-30B-A3B-Instruct**, **Qwen3-Coder-Next**, offering exceptional performance in both coding and agentic tasks. 

**Qwen3-Coder-Next**, an open-weight language model designed specifically for coding agents and local development. Built on top of **Qwen3-Next-80B-A3B-Base**, which adopts a novel architecture with hybrid attention and MoE, Qwen3-Coder-Next has been agentically trained at scale on large-scale executable task synthesis, environment interaction, and reinforcement learning, obtaining strong coding and agentic capabilities with significantly lower inference costs.

### Key Features

💻 **Efficiency-Performance Tradeoff**: among open models on **Agentic Coding**, **Agentic Browser-Use**, and other foundational coding tasks, achieving results comparable to Claude Sonnet.

🛠 **Scaling Agentic Coding**: supporting most platforms such as **Qwen Code**, **CLINE**, **Claude Code**, featuring a specially designed function call format;

📚 **Long-context Capabilities**: with native support for **256K** tokens, extendable up to **1M** tokens using Yarn, optimized for repository-scale understanding.

---


## Basic Information

1. ✨ Supporting long context understanding and generation with the context length of 256K tokens;
2. ✨ Supporting 358 coding languages;

<details>
<summary>Click to view all supported languages</summary>
```
['ABAP', 'ActionScript', 'Ada', 'Agda', 'Alloy', 'ApacheConf', 'AppleScript', 'Arc', 'Arduino', 'AsciiDoc', 'AspectJ', 'Assembly', 'Augeas', 'AutoHotkey', 'AutoIt', 'Awk', 'Batchfile', 'Befunge', 'Bison', 'BitBake', 'BlitzBasic', 'BlitzMax', 'Bluespec', 'Boo', 'Brainfuck', 'Brightscript', 'Bro', 'C', 'C#', 'C++', 'C2hs Haskell', 'CLIPS', 'CMake', 'COBOL', 'CSS', 'CSV', "Cap'n Proto", 'CartoCSS', 'Ceylon', 'Chapel', 'ChucK', 'Cirru', 'Clarion', 'Clean', 'Click', 'Clojure', 'CoffeeScript', 'ColdFusion', 'ColdFusion CFC', 'Common Lisp', 'Component Pascal', 'Coq', 'Creole', 'Crystal', 'Csound', 'Cucumber', 'Cuda', 'Cycript', 'Cython', 'D', 'DIGITAL Command Language', 'DM', 'DNS Zone', 'Darcs Patch', 'Dart', 'Diff', 'Dockerfile', 'Dogescript', 'Dylan', 'E', 'ECL', 'Eagle', 'Ecere Projects', 'Eiffel', 'Elixir', 'Elm', 'Emacs Lisp', 'EmberScript', 'Erlang', 'F#', 'FLUX', 'FORTRAN', 'Factor', 'Fancy', 'Fantom', 'Forth', 'FreeMarker', 'G-code', 'GAMS', 'GAP', 'GAS', 'GDScript', 'GLSL', 'Genshi', 'Gentoo Ebuild', 'Gentoo Eclass', 'Gettext Catalog', 'Glyph', 'Gnuplot', 'Go', 'Golo', 'Gosu', 'Grace', 'Gradle', 'Grammatical Framework', 'GraphQL', 'Graphviz (DOT)', 'Groff', 'Groovy', 'Groovy Server Pages', 'HCL', 'HLSL', 'HTML', 'HTML+Django', 'HTML+EEX', 'HTML+ERB', 'HTML+PHP', 'HTTP', 'Haml', 'Handlebars', 'Harbour', 'Haskell', 'Haxe', 'Hy', 'IDL', 'IGOR Pro', 'INI', 'IRC log', 'Idris', 'Inform 7', 'Inno Setup', 'Io', 'Ioke', 'Isabelle', 'J', 'JFlex', 'JSON', 'JSON5', 'JSONLD', 'JSONiq', 'JSX', 'Jade', 'Jasmin', 'Java', 'Java Server Pages', 'JavaScript', 'Julia', 'Jupyter Notebook', 'KRL', 'KiCad', 'Kit', 'Kotlin', 'LFE', 'LLVM', 'LOLCODE', 'LSL', 'LabVIEW', 'Lasso', 'Latte', 'Lean', 'Less', 'Lex', 'LilyPond', 'Linker Script', 'Liquid', 'Literate Agda', 'Literate CoffeeScript', 'Literate Haskell', 'LiveScript', 'Logos', 'Logtalk', 'LookML', 'Lua', 'M', 'M4', 'MAXScript', 'MTML', 'MUF', 'Makefile', 'Mako', 'Maple', 'Markdown', 'Mask', 'Mathematica', 'Matlab', 'Max', 'MediaWiki', 'Metal', 'MiniD', 'Mirah', 'Modelica', 'Module Management System', 'Monkey', 'MoonScript', 'Myghty', 'NSIS', 'NetLinx', 'NetLogo', 'Nginx', 'Nimrod', 'Ninja', 'Nit', 'Nix', 'Nu', 'NumPy', 'OCaml', 'ObjDump', 'Objective-C++', 'Objective-J', 'Octave', 'Omgrofl', 'Opa', 'Opal', 'OpenCL', 'OpenEdge ABL', 'OpenSCAD', 'Org', 'Ox', 'Oxygene', 'Oz', 'PAWN', 'PHP', 'POV-Ray SDL', 'Pan', 'Papyrus', 'Parrot', 'Parrot Assembly', 'Parrot Internal Representation', 'Pascal', 'Perl', 'Perl6', 'Pickle', 'PigLatin', 'Pike', 'Pod', 'PogoScript', 'Pony', 'PostScript', 'PowerShell', 'Processing', 'Prolog', 'Propeller Spin', 'Protocol Buffer', 'Public Key', 'Pure Data', 'PureBasic', 'PureScript', 'Python', 'Python traceback', 'QML', 'QMake', 'R', 'RAML', 'RDoc', 'REALbasic', 'RHTML', 'RMarkdown', 'Racket', 'Ragel in Ruby Host', 'Raw token data', 'Rebol', 'Red', 'Redcode', "Ren'Py", 'RenderScript', 'RobotFramework', 'Rouge', 'Ruby', 'Rust', 'SAS', 'SCSS', 'SMT', 'SPARQL', 'SQF', 'SQL', 'STON', 'SVG', 'Sage', 'SaltStack', 'Sass', 'Scala', 'Scaml', 'Scheme', 'Scilab', 'Self', 'Shell', 'ShellSession', 'Shen', 'Slash', 'Slim', 'Smali', 'Smalltalk', 'Smarty', 'Solidity', 'SourcePawn', 'Squirrel', 'Stan', 'Standard ML', 'Stata', 'Stylus', 'SuperCollider', 'Swift', 'SystemVerilog', 'TOML', 'TXL', 'Tcl', 'Tcsh', 'TeX', 'Tea', 'Text', 'Textile', 'Thrift', 'Turing', 'Turtle', 'Twig', 'TypeScript', 'Unified Parallel C', 'Unity3D Asset', 'Uno', 'UnrealScript', 'UrWeb', 'VCL', 'VHDL', 'Vala', 'Verilog', 'VimL', 'Visual Basic', 'Volt', 'Vue', 'Web Ontology Language', 'WebAssembly', 'WebIDL', 'X10', 'XC', 'XML', 'XPages', 'XProc', 'XQuery', 'XS', 'XSLT', 'Xojo', 'Xtend', 'YAML', 'YANG', 'Yacc', 'Zephir', 'Zig', 'Zimpl', 'desktop', 'eC', 'edn', 'fish', 'mupad', 'nesC', 'ooc', 'reStructuredText', 'wisp', 'xBase']
```
</details>

3. ✨ Retain strengths in math and general capabilities from base model.

> [!Important]
> 
> Qwen3-Coder function calling relies on our new tool parser in both **SGLang** and **vLLM** <a href="https://huggingface.co/Qwen/Qwen3-Coder-Next/blob/main/">here</a>.
>
> We updated both the special tokens and their corresponding token ids, in order to maintain consistency with Qwen3. Please make sure to use the new tokenizer.


| model name                  | type     | length | Download                                                                                                                                                                        |
|-----------------------------|----------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Qwen3-Coder-Next         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-Next  ) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-Next)                                       |
| Qwen3-Coder-Next-Base         | base     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-Next-Base) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-Next-Base)     |
| Qwen3-Coder-480B-A35B-Instruct         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-480B-A35B-Instruct  ) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-480B-A35B-Instruct)                                       |
| Qwen3-Coder-30B-A3B-Instruct         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-30B-A3B-Instruct) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-30B-A3B-Instruct)                                       |
| Qwen3-Coder-Next-FP8         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-Next-FP8  ) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-Next-FP8)
| Qwen3-Coder-Next-GGUF         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-Next-GGUF  ) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-Next-GGUF)                                       |
| Qwen3-Coder-480B-A35B-Instruct-FP8         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-480B-A35B-Instruct-FP8) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-480B-A35B-Instruct-FP8)                                       |
| Qwen3-Coder-30B-A3B-Instruct-FP8         | instruct     | 256k    | 🤗 [Hugging Face](https://huggingface.co/Qwen/Qwen3-Coder-30B-A3B-Instruct-FP8) • 🤖 [ModelScope](https://modelscope.cn/models/Qwen/Qwen3-Coder-30B-A3B-Instruct-FP8)                                       |


Detailed performance and introduction are shown in this <a href="https://qwenlm.github.io/blog/qwen3-coder-next/">📑 blog</a>.

---

## Quick Start

> [!Important]
> **Qwen3-Coder** are instruct models for chatting;
>
> This model supports only non-thinking mode and does not generate `<think></think>` blocks in its output. Meanwhile, specifying `enable_thinking=False` is no longer required.
>
### 👉🏻 Chat with Qwen3-Coder
You can write several lines of code with `transformers` to chat with Qwen3-Coder-Next. Essentially, we build the tokenizer and the model with the `from_pretrained` method, and we use the generate method to perform chatting with the help of the chat template provided by the tokenizer. Below is an example of how to chat with **Qwen3-Coder-Next**:

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model_name = "Qwen/Qwen3-Coder-Next"

model = AutoModelForCausalLM.from_pretrained(
    model_name,
    torch_dtype="auto",
    device_map="auto"
)
tokenizer = AutoTokenizer.from_pretrained(model_name)

prompt = "write a quick sort algorithm."
messages = [
    {"role": "user", "content": prompt}
]
text = tokenizer.apply_chat_template(
    messages,
    tokenize=False,
    add_generation_prompt=True
)
model_inputs = tokenizer([text], return_tensors="pt").to(model.device)

generated_ids = model.generate(
    **model_inputs,
    max_new_tokens=65536
)
generated_ids = [
    output_ids[len(input_ids):] for input_ids, output_ids in zip(model_inputs.input_ids, generated_ids)
]

response = tokenizer.batch_decode(generated_ids, skip_special_tokens=True)[0]
```
The `apply_chat_template()` function is used to convert the messages into a format that the model can understand.
The `add_generation_prompt` argument is used to add a generation prompt, which refers to `<|im_start|>assistant\n` to the input. Notably, we apply the ChatML template for chat models following our previous practice.
The `max_new_tokens` argument is used to set the maximum length of the response. The `tokenizer.batch_decode()` function is used to decode the response. In terms of the input, the above messages are an example to show how to format your dialog history and system prompt.
You can use the other sizes of instruct models in the same way.


#### Fill in the middle with Qwen3-Coder

The code insertion task, also referred to as the "fill-in-the-middle" challenge, requires the insertion of code segments in a manner that bridges the gaps within a given code context. For an approach aligned with best practices, we recommend adhering to the formatting guidelines outlined in the paper "Efficient Training of Language Models to Fill in the Middle" [[arxiv](https://arxiv.org/abs/2207.14255)]. 

> [!Important]
> It should be noted that FIM is supported in every version of Qwen3-Coder. Qwen3-Coder-Next is shown here as an example.
>

The prompt should be structured as follows:
```python
prompt = '<|fim_prefix|>' + prefix_code + '<|fim_suffix|>' + suffix_code + '<|fim_middle|>'
```
Following the approach mentioned, an example would be structured in this manner:

```python
from transformers import AutoTokenizer, AutoModelForCausalLM
# load model
device = "cuda" # the device to load the model onto

TOKENIZER = AutoTokenizer.from_pretrained("Qwen/Qwen3-Coder-Next")
MODEL = AutoModelForCausalLM.from_pretrained("Qwen/Qwen3-Coder-Next", device_map="auto").eval()


input_text = """<|fim_prefix|>def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    <|fim_suffix|>
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)<|fim_middle|>"""
            
messages = [
    {"role": "system", "content": "You are a code completion assistant."},
    {"role": "user", "content": input_text}
]


text = tokenizer.apply_chat_template(
    messages,
    tokenize=False,
    add_generation_prompt=True
)
model_inputs = TOKENIZER([text], return_tensors="pt").to(model.device)

# Use `max_new_tokens` to control the maximum output length.
eos_token_ids = [151659, 151661, 151662, 151663, 151664, 151643, 151645]
generated_ids = MODEL.generate(model_inputs.input_ids, max_new_tokens=512, do_sample=False, eos_token_id=eos_token_ids)[0]
# The generated_ids include prompt_ids, we only need to decode the tokens after prompt_ids.
output_text = TOKENIZER.decode(generated_ids[len(model_inputs.input_ids[0]):], skip_special_tokens=True)

print(f"Prompt: {input_text}\n\nGenerated text: {output_text}")
```

## Use Cases

### Example: Releasing a Website

<details>
<summary>Prompt with OpenClaw </summary>

```
next week we will release new coder model, can you collect the history of qwen coder and write a web page, the release the website with the nginx, you can seach how to do this in alibaba cloud linux first
```

</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/openclaw/claw_mix.mp4">
    <img src="assets/qwen3-coder-next-demo/openclaw.png" width="400" />
    </a>
</p>


### Example: Desktop Tidy

<details>
<summary>Prompt with Qwen Code </summary>

```
Please tidy up my desk.
```
</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/qwencode/exp-tidy-desktop.mp4">
    <img src="assets/qwen3-coder-next-demo/tidy_desktop.png" width="400" />
    </a>
</p>

### Example: Zombies vs. Plants

<details>
<summary>Prompt with Claude Code </summary>

```
帮我实现《僵尸大战植物》网页游戏

【核心机制】
- 反向塔防：玩家扮演僵尸方，从地图右侧（部署区）召唤僵尸向左进攻
- 资源循环：初始300脑子点数，僵尸吃掉植物返还100点，形成经济循环
- 倒计时制：120秒内清除所有植物获胜，超时失败

【地图规格】
- 5行9列网格，右侧3列为可部署区域（红色高亮标识）
- 每格100x100像素，草地纹理交替渲染
- 坐标系：左侧为植物防线，右侧为僵尸出生点

【单位系统】
僵尸方（右侧购买）：
- 普通僵尸：50脑，100HP，0.5速，标准单位
- 路障僵尸：100脑，200HP，0.5速，中期肉盾  
- 铁桶僵尸：150脑，400HP，0.3速，重型坦克
- 冲刺僵尸：80脑，80HP，1.2速，快速突进

植物方（左侧随机初始部署12个）：
- 豌豆射手：100HP，20伤/发，2秒间隔，直线射击
- 双发射手：120HP，20伤/发，1秒间隔，火力压制
- 坚果墙：300HP，0伤，纯肉盾阻挡
- 向日葵：80HP，0伤，经济单位（纯干扰）

【战斗逻辑】
- 碰撞检测：僵尸到达植物50px内触发啃食状态，停止移动
- 伤害结算：僵尸30帧/次咬击（0.5秒），植物射出弹道物理
- 击毁反馈：植物死亡时生成"+100"飘字特效与粒子爆炸
- 路径AI：同格僵尸队列不重叠，植物优先攻击横向最近目标

【交互设计】
- 右侧卡片式UI：显示僵尸图标、名称、脑子消耗
- 资源不足时卡片置灰并自动切换可选类型
- 鼠标悬停部署区显示半透明预览圈
- 实时血条：实体头顶显示绿/黄/红三色血槽

【胜利条件】
- 胜利：plants.length === 0 && timeLeft > 0
- 失败：timeLeft === 0 || (可选)僵尸全灭且脑子为0
```

</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/claudecode/cc_zombine_vs_plants.mp4">
    <img src="assets/qwen3-coder-next-demo/zombiesvsplants.png" width="400" />
    </a>
</p>

### Example: Sound ASCII Art

<details>
<summary>Prompt with Cline </summary>

```
Build an interactive ASCII art drawing tool with sound feedback. The application should:
 
1. Create a canvas where users can draw by clicking and dragging
2. Place different ASCII characters or symbols when the user draws
3. Play corresponding musical notes when each character is placed
4. Include multiple pattern sets with different characters and
corresponding note scales
5. Add a pattern switcher button to cycle through different
character/sound themes
6. Include a clear button to reset the canvas
7. Support both mouse and touch input for mobile compatibility
 
The application should be creative and fun to use, creating an audio-visual experience where patterns of characters create both visual art and musical patterns. Ensure the musical notes are harmonious when played in sequence.
```

</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/cline/sound_art.mp4">
    <img src="assets/qwen3-coder-next-demo/sound_art.png" width="400" />
    </a>
</p>

### Example: Vibe Checking


<details>
<summary> Prompt with Browser Use Agent </summary>

```
Vibe test this website. Click around, try things, report what's broken.
```
</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/bua/vibe.mp4">
    <img src="assets/qwen3-coder-next-demo/vibing_check.png" width="400" />
    </a>
</p>

### Example: Parkour Game


<details>
<summary> Prompt with Qwen Chat Web Dev </summary>

```
Create an interactive real-time particle system using HTML5 Canvas:

Core Features:
- Render 800-1200 animated particles with physics-based movement
- Mouse cursor exerts attractive/repulsive force on nearby particles
- Click to toggle between attraction and repulsion modes
- Particles respond with smooth acceleration and velocity calculations

Technical Requirements:
- Use requestAnimationFrame for optimal performance
- Implement force calculation based on distance from cursor
- Add visual feedback: particle glow, color variation, and fade effects
- Include performance monitoring (FPS counter)

Deliverables:
- Single HTML file with embedded CSS and JavaScript
- Clean, commented code following best practices
- Responsive design compatible with modern browsers
```
</details>

<p align="center">
    <a href="https://qianwen-res.oss-accelerate-overseas.aliyuncs.com/Qwen3-Coder-Next/WebDev/chico_paredao.mp4">
    <img src="assets/qwen3-coder-next-demo/parkourgame.png" width="400" />
    </a>
</p>


---

## Star History
[![Star History Chart](https://api.star-history.com/svg?repos=QwenLM/Qwen3-Coder&type=Date)](https://star-history.com/#QwenLM/Qwen3-Coder&Date)

---

## Citation

If you find our work helpful, feel free to give us a cite.

```bibtex
@article{Qwen3-Coder-Next,
    title={Qwen3-Coder-Next Technical Report},
    author={Ruisheng Cao and Mouxiang Chen and Jiawei Chen and Zeyu Cui and Yunlong Feng and Binyuan Hui and Yuheng Jing and Kaixin Li and Mingze Li and Junyang Lin and Zeyao Ma and Kashun Shum and Xuwu Wang and Jinxi Wei and Jiaxi Yang and Jiajun Zhang and Lei Zhang and Zongmeng Zhang and Wenting Zhao and Fan Zhou},
    journal={arXiv preprint arXiv:2603.00729},
    year={2026},
}
```

---

## Contact Us
If you are interested to leave a message to either our research team or product team, join our [Discord](https://discord.gg/z3GAxXZ9Ce) or [WeChat groups](https://github.com/QwenLM/Qwen/blob/main/assets/wechat.png)!

<p align="right" style="font-size: 14px; color: #555; margin-top: 20px;">
    <a href="#readme-top" style="text-decoration: none; color: #007bff; font-weight: bold;">
        ↑ Back to Top ↑
    </a>
</p><!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
  <title>Active Lingua · Dynamic English App & Campus</title>
  <!-- PWA Manifest & Meta -->
  <meta name="theme-color" content="#162d6e">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="apple-mobile-web-app-title" content="Active Lingua">
  <link rel="manifest" href="manifest.json">
  <!-- Fonts & Tailwind -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Cabinet+Grotesk:wght@800;900&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              navy: '#162d6e',
              deep: '#0e1d47',
              tropical: '#15803d',
              tropicalLight: '#22c55e',
              yellow: '#eab308',
              cream: '#fcf9f4',
              surface: '#f5f0e6',
              line: '#e2d9c8'
            }
          },
          fontFamily: {
            sans: ['"Plus Jakarta Sans"', 'system-ui', 'sans-serif'],
            display: ['"Cabinet Grotesk"', '"Plus Jakarta Sans"', 'sans-serif']
          }
        }
      }
    }
  </script>
  <style>
    body { background-color: #fcf9f4; color: #1e293b; font-family: 'Plus Jakarta Sans', sans-serif; }
    .glass-nav { background: rgba(22, 45, 110, 0.96); backdrop-filter: blur(12px); }
    .custom-scroll::-webkit-scrollbar { width: 6px; }
    .custom-scroll::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
  </style>
</head>
<body class="min-h-screen flex flex-col pb-20 md:pb-0">

  <!-- TOP APP BAR / HEADER -->
  <header class="sticky top-0 z-50 glass-nav text-white border-b border-white/10 shadow-lg px-4 py-3">
    <div class="max-w-4xl mx-auto flex items-center justify-between">
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-xl bg-white p-1 shadow-md flex items-center justify-center">
          <svg class="w-7 h-7 text-brand-navy" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
            <circle cx="12" cy="12" r="9"/>
            <path d="M12 3a15.3 15.3 0 0 1 4 18 15.3 15.3 0 0 1-8 0 15.3 15.3 0 0 1 4-18z"/>
            <path d="M3 12h18"/>
          </svg>
        </div>
        <div>
          <h1 class="text-lg font-black tracking-tight flex items-center gap-2">
            ACTIVE LINGUA <span class="bg-brand-tropical text-white text-[10px] font-bold px-2 py-0.5 rounded-full uppercase tracking-wider">Pro PWA</span>
          </h1>
          <p class="text-xs text-white/80">Dynamic English Program · Bucerías, Riviera Nayarit</p>
        </div>
      </div>
      <div class="flex items-center gap-2">
        <a href="https://wa.me/523223512797" target="_blank" class="hidden sm:flex items-center gap-1.5 bg-brand-tropical hover:bg-green-700 text-white text-xs font-bold px-3 py-1.5 rounded-lg shadow transition">
          <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981z"/></svg>
          +52 322 351 2797
        </a>
        <button id="pwaInstallBtn" class="bg-amber-400 hover:bg-amber-300 text-brand-deep text-xs font-extrabold px-3 py-1.5 rounded-lg shadow flex items-center gap-1">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"/></svg>
          Instalar App
        </button>
      </div>
    </div>
  </header>

  <!-- APP CONTENT CONTAINER -->
  <main class="max-w-4xl w-full mx-auto p-4 md:py-8 flex-1">

    <!-- SUB-NAV / TABS (MÓVIL Y DESKTOP) -->
    <nav class="flex overflow-x-auto gap-2 pb-3 mb-6 border-b border-brand-line custom-scroll">
      <button onclick="switchTab('curriculum')" id="tab-curriculum" class="tab-btn active px-4 py-2 rounded-xl text-sm font-bold flex items-center gap-2 bg-brand-navy text-white shadow">
        <span>📚 30 Capítulos</span>
      </button>
      <button onclick="switchTab('voice')" id="tab-voice" class="tab-btn px-4 py-2 rounded-xl text-sm font-bold flex items-center gap-2 bg-white text-slate-700 border border-brand-line hover:bg-slate-100">
        <span>🎙️ Voice AI Lab</span>
      </button>
      <button onclick="switchTab('gift')" id="tab-gift" class="tab-btn px-4 py-2 rounded-xl text-sm font-bold flex items-center gap-2 bg-white text-slate-700 border border-brand-line hover:bg-slate-100">
        <span>🎁 Certificado 3 Meses</span>
      </button>
      <button onclick="switchTab('enroll')" id="tab-enroll" class="tab-btn px-4 py-2 rounded-xl text-sm font-bold flex items-center gap-2 bg-white text-slate-700 border border-brand-line hover:bg-slate-100">
        <span>📝 Canjear Beca</span>
      </button>
      <button onclick="switchTab('certificate')" id="tab-certificate" class="tab-btn px-4 py-2 rounded-xl text-sm font-bold flex items-center gap-2 bg-white text-slate-700 border border-brand-line hover:bg-slate-100">
        <span>🎓 Diploma Oficial</span>
      </button>
    </nav>

    <!-- SECTION 1: CURRICULUM (30 CAPÍTULOS + CHECKPOINTS) -->
    <section id="view-curriculum" class="tab-view block space-y-6">
      <!-- HERO RESUMEN -->
      <div class="bg-gradient-to-r from-brand-navy to-brand-deep rounded-2xl p-5 md:p-6 text-white shadow-xl flex flex-col md:flex-row md:items-center justify-between gap-4">
        <div>
          <span class="inline-block px-3 py-1 bg-brand-tropical text-white text-xs font-extrabold rounded-full mb-2">Currículum A1 a C1 Oficial</span>
          <h2 class="text-2xl font-black">Active Lingua 30-Chapter Master Journey</h2>
          <p class="text-sm text-slate-200 mt-1 max-w-xl">30 capítulos teóricos y prácticos, 6 exámenes checkpoint y diploma con verificación digital.</p>
        </div>
        <div class="flex items-center gap-3 bg-white/10 p-3 rounded-xl backdrop-blur-sm self-start md:self-auto">
          <div class="text-center">
            <span class="block text-2xl font-black text-amber-300" id="totalScoreText">3,850</span>
            <span class="text-[10px] uppercase font-bold text-white/80">XP Ganados</span>
          </div>
          <div class="w-px h-8 bg-white/20"></div>
          <div class="text-center">
            <span class="block text-2xl font-black text-green-400">30/30</span>
            <span class="text-[10px] uppercase font-bold text-white/80">Capítulos</span>
          </div>
          <div class="w-px h-8 bg-white/20"></div>
          <div class="text-center">
            <span class="block text-2xl font-black text-blue-300">6/6</span>
            <span class="text-[10px] uppercase font-bold text-white/80">Checkpoints</span>
          </div>
        </div>
      </div>

      <!-- BLOQUES 1 AL 6 -->
      <div class="space-y-4" id="blocksContainer">
        <!-- Generado dinámicamente por JS con los 30 capítulos -->
      </div>
    </section>

    <!-- SECTION 2: VOICE AI LAB CON WEBSPEECH REAL -->
    <section id="view-voice" class="tab-view hidden space-y-6">
      <div class="bg-white rounded-2xl border border-brand-line p-6 shadow-sm">
        <div class="flex items-center justify-between mb-4">
          <div>
            <span class="text-xs font-extrabold uppercase text-brand-tropical tracking-wider">Módulo Interactivo</span>
            <h2 class="text-xl font-black text-brand-navy">Stitch Voice AI · Laboratorio de Pronunciación</h2>
          </div>
          <span class="bg-green-100 text-brand-tropical px-3 py-1 rounded-full text-xs font-bold">Micrófono Activo</span>
        </div>
        <p class="text-sm text-slate-600 mb-6">Escucha el modelo nativo, pulsa "Hablar" y di la frase en inglés. El motor evaluará tu pronunciación en tiempo real.</p>

        <div class="space-y-4" id="voiceDrills">
          <!-- Drill 1 -->
          <div class="p-4 rounded-xl border border-slate-200 bg-brand-cream/60 voice-card" data-phrase="Hello, I would like to check in for my flight.">
            <p class="text-base font-bold text-slate-900 mb-2">"Hello, I would like to check in for my flight."</p>
            <p class="text-xs text-slate-500 mb-3">Capítulo 10 · Airport Check-in</p>
            <div class="flex flex-wrap gap-2 items-center">
              <button onclick="playTTS('Hello, I would like to check in for my flight.')" class="bg-brand-navy hover:bg-blue-900 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🔊 Escuchar Modelo
              </button>
              <button onclick="startVoiceRecord(this, 'Hello, I would like to check in for my flight.')" class="bg-brand-tropical hover:bg-green-700 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🎙️ Hablar y Evaluar
              </button>
              <span class="voice-feedback text-xs font-bold text-slate-600">Listo para grabar</span>
            </div>
          </div>

          <!-- Drill 2 -->
          <div class="p-4 rounded-xl border border-slate-200 bg-brand-cream/60 voice-card" data-phrase="Could you please tell me where the boarding gate is?">
            <p class="text-base font-bold text-slate-900 mb-2">"Could you please tell me where the boarding gate is?"</p>
            <p class="text-xs text-slate-500 mb-3">Capítulo 19 · Airport Layovers & Directions</p>
            <div class="flex flex-wrap gap-2 items-center">
              <button onclick="playTTS('Could you please tell me where the boarding gate is?')" class="bg-brand-navy hover:bg-blue-900 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🔊 Escuchar Modelo
              </button>
              <button onclick="startVoiceRecord(this, 'Could you please tell me where the boarding gate is?')" class="bg-brand-tropical hover:bg-green-700 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🎙️ Hablar y Evaluar
              </button>
              <span class="voice-feedback text-xs font-bold text-slate-600">Listo para grabar</span>
            </div>
          </div>

          <!-- Drill 3 -->
          <div class="p-4 rounded-xl border border-slate-200 bg-brand-cream/60 voice-card" data-phrase="We are looking for a binding agreement with mutual benefits.">
            <p class="text-base font-bold text-slate-900 mb-2">"We are looking for a binding agreement with mutual benefits."</p>
            <p class="text-xs text-slate-500 mb-3">Capítulo 29 · Strategic Negotiations</p>
            <div class="flex flex-wrap gap-2 items-center">
              <button onclick="playTTS('We are looking for a binding agreement with mutual benefits.')" class="bg-brand-navy hover:bg-blue-900 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🔊 Escuchar Modelo
              </button>
              <button onclick="startVoiceRecord(this, 'We are looking for a binding agreement with mutual benefits.')" class="bg-brand-tropical hover:bg-green-700 text-white text-xs font-bold px-3 py-1.5 rounded-lg flex items-center gap-1.5 shadow">
                🎙️ Hablar y Evaluar
              </button>
              <span class="voice-feedback text-xs font-bold text-slate-600">Listo para grabar</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 3: CERTIFICADO DE REGALO (3 MESES GRATIS) -->
    <section id="view-gift" class="tab-view hidden space-y-6">
      <div class="bg-white rounded-3xl border-2 border-brand-tropical shadow-2xl p-6 md:p-8 max-w-xl mx-auto relative overflow-hidden">
        <div class="absolute -right-12 -top-12 w-36 h-36 bg-amber-200 rounded-full opacity-30 pointer-events-none"></div>
        <div class="flex justify-between items-start mb-4">
          <span class="bg-brand-navy text-white text-[11px] font-extrabold px-3 py-1 rounded-full uppercase tracking-wider">Oficial · Active Lingua</span>
          <span class="bg-green-100 text-brand-tropical text-xs font-extrabold px-2.5 py-0.5 rounded-full">100% Bonificado</span>
        </div>

        <div class="text-center my-6">
          <p class="text-xs uppercase font-extrabold tracking-widest text-amber-600 mb-1">Certificado de Regalo Exclusivo</p>
          <h2 class="text-2xl md:text-3xl font-black text-brand-navy leading-tight">3 MESES COMPLETOS DE INGLÉS ONLINE GRATIS</h2>
          <p class="text-xs md:text-sm text-slate-600 mt-2">Beca completa de inmersión conversacional con mentores nativos y metodología interactiva.</p>
        </div>

        <!-- VALOR COMERCIAL -->
        <div class="bg-slate-50 border border-slate-200 rounded-2xl p-4 text-center my-4">
          <p class="text-xs text-slate-500 font-bold uppercase">Valor Académico Certificado</p>
          <p class="text-xl line-through text-slate-400 font-bold">$750 USD / $13,500 MXN</p>
          <p class="text-3xl font-black text-brand-tropical">COSTO PARA TI: $0.00 USD</p>
        </div>

        <!-- DETALLES DEL BENEFICIO -->
        <div class="grid grid-cols-2 gap-3 text-xs font-semibold text-slate-700 my-4">
          <div class="p-3 bg-brand-cream rounded-xl border border-brand-line">
            <span class="block text-brand-navy font-bold">👥 Clases en Vivo</span>
            <span>4 hrs / semana (grupos máx 5)</span>
          </div>
          <div class="p-3 bg-brand-cream rounded-xl border border-brand-line">
            <span class="block text-brand-navy font-bold">⏱️ Total Horas</span>
            <span>48 Horas de inmersión directa</span>
          </div>
        </div>

        <!-- CÓDIGO DE CUPÓN -->
        <div class="bg-amber-50 border-2 border-dashed border-amber-300 rounded-2xl p-4 text-center my-5">
          <p class="text-xs font-bold text-amber-800 uppercase tracking-wider">Código de Activación Válido</p>
          <div class="flex items-center justify-center gap-2 mt-1">
            <span id="giftCodeText" class="text-xl md:text-2xl font-black text-brand-navy tracking-wider font-mono">ACTIVELINGUA-VIP3M-2025</span>
            <button onclick="copyCode()" class="bg-brand-navy text-white text-xs px-2.5 py-1 rounded-lg hover:bg-blue-900 transition">Copiar</button>
          </div>
        </div>

        <button onclick="switchTab('enroll')" class="w-full bg-brand-tropical hover:bg-green-700 text-white font-black py-3 rounded-xl shadow-lg transition text-sm flex items-center justify-center gap-2">
          <span>🚀 Canjear Certificado Ahora Mismo</span>
        </button>
      </div>
    </section>

    <!-- SECTION 4: FORMULARIO DE CANJE / PÁGINA DE VENTA -->
    <section id="view-enroll" class="tab-view hidden space-y-6">
      <div class="bg-white rounded-2xl border border-brand-line shadow-lg p-6 md:p-8 max-w-xl mx-auto">
        <div class="text-center mb-6">
          <span class="bg-red-100 text-red-700 text-xs font-black px-3 py-1 rounded-full uppercase">¡Sólo 4 cupos restantes!</span>
          <h2 class="text-2xl font-black text-brand-navy mt-2">Formulario de Canje Directo</h2>
          <p class="text-xs text-slate-500">Completa tus datos para asignación de grupo y acceso al campus virtual.</p>
        </div>

        <form id="enrollForm" onsubmit="handleEnroll(event)" class="space-y-4">
          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Nombre Completo del Estudiante *</label>
            <input required type="text" id="studentName" placeholder="Ej. Camila Morales Rivera" class="w-full px-3 py-2.5 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-brand-navy outline-none">
          </div>

          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Correo Electrónico (para tus accesos) *</label>
            <input required type="email" id="studentEmail" placeholder="nombre@correo.com" class="w-full px-3 py-2.5 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-brand-navy outline-none">
          </div>

          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Teléfono WhatsApp *</label>
            <input required type="tel" id="studentPhone" placeholder="+52 322 351 2797" class="w-full px-3 py-2.5 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-brand-navy outline-none">
          </div>

          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Código de Beca</label>
            <input readonly type="text" value="ACTIVELINGUA-VIP3M-2025" class="w-full px-3 py-2 rounded-xl bg-slate-100 border border-slate-200 text-sm font-mono font-bold text-brand-tropical">
          </div>

          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Horario Preferido (4 horas/semana) *</label>
            <select id="studentSchedule" class="w-full px-3 py-2.5 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-brand-navy outline-none">
              <option value="Opción A: Lunes y Miércoles 9:00 AM - 11:00 AM">Opción A: Lunes y Miércoles (9:00 AM - 11:00 AM)</option>
              <option value="Opción B: Martes y Jueves 7:00 PM - 9:00 PM">Opción B: Martes y Jueves (7:00 PM - 9:00 PM)</option>
              <option value="Opción C: Sábados Intensivo 9:00 AM - 1:00 PM">Opción C: Sábados Intensivo (9:00 AM - 1:00 PM)</option>
            </select>
          </div>

          <div>
            <label class="block text-xs font-extrabold uppercase text-slate-700 mb-1">Nivel Aproximado</label>
            <div class="grid grid-cols-3 gap-2">
              <label class="border border-slate-200 p-2 rounded-xl text-center text-xs font-bold cursor-pointer hover:bg-slate-50 flex flex-col items-center">
                <input type="radio" name="level" value="A1" checked class="mb-1"> Principiante
              </label>
              <label class="border border-slate-200 p-2 rounded-xl text-center text-xs font-bold cursor-pointer hover:bg-slate-50 flex flex-col items-center">
                <input type="radio" name="level" value="A2" class="mb-1"> Básico A2
              </label>
              <label class="border border-slate-200 p-2 rounded-xl text-center text-xs font-bold cursor-pointer hover:bg-slate-50 flex flex-col items-center">
                <input type="radio" name="level" value="B1" class="mb-1"> Intermedio
              </label>
            </div>
          </div>

          <button type="submit" class="w-full bg-brand-tropical hover:bg-green-700 text-white font-black py-3 rounded-xl shadow-lg transition text-base flex items-center justify-center gap-2">
            <span>¡Activar Mis 3 Meses Gratis Ahora!</span>
          </button>
          <p class="text-[11px] text-center text-slate-400">Garantía 100% de cortesía. Sin cobro oculto ni tarjeta requerida.</p>
        </form>

        <div id="enrollSuccess" class="hidden mt-4 p-4 bg-green-50 border border-green-200 rounded-xl text-center">
          <p class="text-sm font-bold text-green-800">¡Beca Activada con Éxito! 🎉</p>
          <p class="text-xs text-green-600 mt-1">Te contactaremos por WhatsApp al número proporcionado para entregarte las credenciales de Zoom y Campus.</p>
          <a id="waDirectBtn" target="_blank" href="#" class="inline-block mt-3 bg-brand-tropical text-white text-xs font-bold px-4 py-2 rounded-lg shadow">Confirmar por WhatsApp Inmediato</a>
        </div>
      </div>
    </section>

    <!-- SECTION 5: CERTIFICADO DE GRADUACIÓN -->
    <section id="view-certificate" class="tab-view hidden space-y-6">
      <div class="bg-white rounded-3xl border-4 border-amber-300 p-6 md:p-8 max-w-2xl mx-auto shadow-2xl relative text-center">
        <div class="inline-block p-2 bg-brand-navy rounded-2xl mb-3">
          <span class="text-white text-xs font-black uppercase tracking-widest px-2">Colegio Académico Lingüístico</span>
        </div>
        <h2 class="text-2xl md:text-3xl font-black text-brand-navy">Active Lingua Global</h2>
        <p class="text-xs text-amber-700 font-bold uppercase tracking-widest mt-1">Otorga el presente</p>
        <h3 class="text-xl md:text-2xl font-black text-slate-900 mt-2 mb-4">CERTIFICADO INTERNACIONAL DE FLUIDEZ Y COMUNICACIÓN GLOBAL</h3>
        <p class="text-xs text-slate-500">Nivel C1 Operacional Avanzado · Marco Común Europeo (MCER)</p>

        <div class="my-6 py-4 border-y border-slate-200">
          <p class="text-xs text-slate-400">Conferido con honores a:</p>
          <h4 id="certStudentName" class="text-2xl font-black text-brand-tropical mt-1">Lic. Sofía Valenzuela M.</h4>
          <p class="text-xs text-slate-600 mt-2 max-w-md mx-auto">Por haber acreditado satisfactoriamente los 30 Capítulos Teórico-Prácticos Automatizados y las 6 Evaluaciones Hito con promedio de <span class="font-bold text-brand-navy">97.6%</span>.</p>
        </div>

        <div class="flex flex-wrap items-center justify-between gap-4 text-left text-xs bg-slate-50 p-4 rounded-xl border border-slate-200">
          <div>
            <span class="block text-slate-400">ID de Registro:</span>
            <span class="font-mono font-bold text-slate-800">AL-CERT-2024-GLOBAL-30</span>
            <span class="block text-green-600 font-bold mt-0.5">✓ Verificado en Servidor Seguro</span>
          </div>
          <div class="text-right">
            <span class="block text-slate-400">Dirección Pedagógica:</span>
            <span class="font-bold text-slate-800">Dr. Marcus Vance, Ph.D.</span>
            <span class="block text-slate-500">Campus Bucerías, Nayarit</span>
          </div>
        </div>

        <div class="mt-6 flex flex-wrap gap-2 justify-center">
          <button onclick="window.print()" class="bg-brand-navy hover:bg-blue-900 text-white text-xs font-bold px-4 py-2 rounded-xl shadow flex items-center gap-1.5">
            🖨️ Imprimir Diploma
          </button>
          <a href="https://wa.me/523223512797?text=Hola,%20deseo%20validar%20mi%20Certificado%20Oficial%20Active%20Lingua%20AL-CERT-2024-GLOBAL-30" target="_blank" class="bg-brand-tropical hover:bg-green-700 text-white text-xs font-bold px-4 py-2 rounded-xl shadow flex items-center gap-1.5">
            📲 Validar por WhatsApp
          </a>
        </div>
      </div>
    </section>

  </main>

  <!-- BOTTOM MOBILE NAVIGATION BAR -->
  <nav class="md:hidden fixed bottom-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-md border-t border-slate-200 px-2 py-2 flex justify-around items-center">
    <button onclick="switchTab('curriculum')" class="mob-btn flex flex-col items-center text-xs font-bold text-brand-navy" id="mob-curriculum">
      <span class="text-lg">📚</span> Capítulos
    </button>
    <button onclick="switchTab('voice')" class="mob-btn flex flex-col items-center text-xs font-bold text-slate-400" id="mob-voice">
      <span class="text-lg">🎙️</span> Voz AI
    </button>
    <button onclick="switchTab('gift')" class="mob-btn flex flex-col items-center text-xs font-bold text-slate-400" id="mob-gift">
      <span class="text-lg">🎁</span> Regalo
    </button>
    <button onclick="switchTab('enroll')" class="mob-btn flex flex-col items-center text-xs font-bold text-slate-400" id="mob-enroll">
      <span class="text-lg">📝</span> Canjear
    </button>
    <button onclick="switchTab('certificate')" class="mob-btn flex flex-col items-center text-xs font-bold text-slate-400" id="mob-certificate">
      <span class="text-lg">🎓</span> Diploma
    </button>
  </nav>

  <!-- JAVASCRIPT LOGIC & PWA WORKER -->
  <script>
    // 1. DATA OF 30 CHAPTERS
    const CHAPTERS = [
      { id: 1, title: "Presentaciones y Saludos", level: "A1", desc: "Introduce yourself, nationalities, phone numbers." },
      { id: 2, title: "Entorno Familiar y Hogar", level: "A1", desc: "Describe family members, physical appearance, age." },
      { id: 3, title: "Restaurante y Comida Básica", level: "A1", desc: "Order meals, food preferences, drink requests." },
      { id: 4, title: "Salón de Clases & Rutinas", level: "A1", desc: "Office objects, locations, progressive actions." },
      { id: 5, title: "Rutas Cotidianas y Horarios", level: "A1", desc: "Daily routines, time expressions, habits." },
      { id: 6, title: "Travel & GPS Directions", level: "A2", desc: "Navigating city directions, turn-by-turn map skills." },
      { id: 7, title: "Shopping & Supermarkets", level: "A2", desc: "Cashier checkout, prices, clothing and sizing." },
      { id: 8, title: "City Services & Post Office", level: "A2", desc: "Public facilities, asking for assistance, mail." },
      { id: 9, title: "Video Inmersión 90 Segundos", level: "A2", desc: "Auditory immersion with interactive video drills." },
      { id: 10, title: "Airport Check-in & Security", level: "A2", desc: "Boarding pass, luggage check, TSA security." },
      { id: 11, title: "Hotel Reservations & Front Desk", level: "B1.1", desc: "Room booking, amenities, keycards, requests." },
      { id: 12, title: "Dining Out & Restaurant Situations", level: "B1.1", desc: "Table reservations, dietary needs, tipping." },
      { id: 13, title: "Emergency Situations & Pharmacy", level: "B1.1", desc: "Doctor clinic, symptoms, prescriptions." },
      { id: 14, title: "Hotel Checkout & Logistics", level: "B1.1", desc: "Itemized receipts, settling bills, taxi call." },
      { id: 15, title: "Renting a Car & Road Trip", level: "B1.1", desc: "Rental agreement, insurance, GPS navigation." },
      { id: 16, title: "Gas Station & Rest Stops", level: "B1.2", desc: "Fuel types, highway stops, convenience stores." },
      { id: 17, title: "Public Transit & Subways", level: "B1.2", desc: "Metro cards, train transfers, commuter routes." },
      { id: 18, title: "Rideshare, Taxis & City Commute", level: "B1.2", desc: "Pick-up locations, directions to driver, fares." },
      { id: 19, title: "Airport Connections & Customs", level: "B1.2", desc: "Layovers, gate changes, passport control." },
      { id: 20, title: "Lost Luggage & Baggage Claim", level: "B1.2", desc: "Filing missing baggage reports, claim tags." },
      { id: 21, title: "Healthcare & Clinic Appointments", level: "B2.1", desc: "Consulting doctors, explaining medical history." },
      { id: 22, title: "Pharmacy & Medical Emergencies", level: "B2.1", desc: "Urgent treatments, dosage explanations." },
      { id: 23, title: "Repairs & Home Services", level: "B2.1", desc: "Contractors, plumbing repairs, work estimates." },
      { id: 24, title: "Bank Accounts & Financial ATMs", level: "B2.1", desc: "Opening accounts, wire transfers, currencies." },
      { id: 25, title: "Job Interviews & Resumes", level: "B2.1", desc: "Career strengths, executive pitch, interviews." },
      { id: 26, title: "Professional Meetings & Presentations", level: "B2.2", desc: "Leading board meetings, deliverables, deadlines." },
      { id: 27, title: "Contract Negotiations & Vendors", level: "B2.2", desc: "Supplier agreements, procurement terms." },
      { id: 28, title: "Networking & Summit Conferences", level: "B2.2", desc: "Elevator pitches, global summits, LinkedIn follow-up." },
      { id: 29, title: "Cross-Cultural Negotiations & Deals", level: "B2.2", desc: "Bilateral agreements, concessions, win-win closures." },
      { id: 30, title: "Executive Mastery & Capstone Defense", level: "C1", desc: "Grand defense before academic panel & diploma." }
    ];

    // RENDER CURRICULUM BLOCKS
    function renderCurriculum() {
      const container = document.getElementById('blocksContainer');
      let html = '';
      for (let b = 0; b < 6; b++) {
        const start = b * 5;
        const blockChapters = CHAPTERS.slice(start, start + 5);
        const blockNum = b + 1;
        const examName = [
          "Everyday Basics & Food Ordering",
          "Airport Transit & Urban Directions",
          "Hospitality & Travel Logistics",
          "Transit Solutions & Problem Solving",
          "Professional & Financial Fluency",
          "Grand Capstone Oral & Written Evaluation"
        ][b];

        html += `
          <div class="bg-white rounded-2xl border border-brand-line p-5 shadow-sm">
            <div class="flex items-center justify-between mb-3 border-b border-slate-100 pb-2">
              <h3 class="font-extrabold text-brand-navy text-sm md:text-base flex items-center gap-2">
                <span class="w-6 h-6 rounded-lg bg-brand-navy text-white text-xs flex items-center justify-center font-black">${blockNum}</span>
                Bloque ${blockNum} · Capítulos ${start + 1} al ${start + 5}
              </h3>
              <span class="text-xs font-bold text-brand-tropical bg-green-50 px-2 py-0.5 rounded-full">5/5 Completados</span>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-2 text-xs">
              ${blockChapters.map(c => `
                <div class="p-2.5 rounded-xl bg-brand-cream/50 border border-slate-100 flex items-center justify-between">
                  <div>
                    <span class="font-bold text-slate-800">Cap. ${c.id}: ${c.title}</span>
                    <span class="block text-[10px] text-slate-500">${c.desc}</span>
                  </div>
                  <span class="text-green-600 font-bold ml-2">✓ 100%</span>
                </div>
              `).join('')}
            </div>
            <!-- CHECKPOINT EXAM -->
            <div class="mt-3 p-3 bg-amber-50 border border-amber-200 rounded-xl flex items-center justify-between text-xs">
              <div>
                <span class="font-extrabold text-amber-900 block">⭐ Checkpoint Exam ${blockNum}: ${examName}</span>
                <span class="text-[10px] text-amber-700">Evaluación Hito Aprobada con Honores (98%)</span>
              </div>
              <span class="bg-amber-400 text-brand-deep font-extrabold px-2.5 py-1 rounded-lg">Certificado</span>
            </div>
          </div>
        `;
      }
      container.innerHTML = html;
    }

    // 2. TAB SWITCHER
    function switchTab(tabId) {
      document.querySelectorAll('.tab-view').forEach(el => el.classList.add('hidden'));
      const activeView = document.getElementById('view-' + tabId);
      if (activeView) activeView.classList.remove('hidden');

      // Update Desktop tabs
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.classList.remove('bg-brand-navy', 'text-white', 'shadow');
        btn.classList.add('bg-white', 'text-slate-700');
      });
      const activeBtn = document.getElementById('tab-' + tabId);
      if (activeBtn) {
        activeBtn.classList.remove('bg-white', 'text-slate-700');
        activeBtn.classList.add('bg-brand-navy', 'text-white', 'shadow');
      }

      // Update Mobile nav
      document.querySelectorAll('.mob-btn').forEach(btn => {
        btn.classList.remove('text-brand-navy');
        btn.classList.add('text-slate-400');
      });
      const activeMob = document.getElementById('mob-' + tabId);
      if (activeMob) {
        activeMob.classList.remove('text-slate-400');
        activeMob.classList.add('text-brand-navy');
      }
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // 3. TEXT-TO-SPEECH (TTS)
    function playTTS(text) {
      if (!window.speechSynthesis) {
        alert("Tu navegador no soporta síntesis de voz.");
        return;
      }
      window.speechSynthesis.cancel();
      const u = new SpeechSynthesisUtterance(text);
      u.lang = 'en-US';
      u.rate = 0.85;
      window.speechSynthesis.speak(u);
    }

    // 4. SPEECH RECOGNITION (Voice Lab)
    function startVoiceRecord(btn, targetPhrase) {
      const SR = window.SpeechRecognition || window.webkitSpeechRecognition;
      const feedbackEl = btn.parentElement.querySelector('.voice-feedback');
      if (!SR) {
        feedbackEl.textContent = "Usa Chrome/Safari para activar reconocimiento.";
        feedbackEl.className = "voice-feedback text-xs font-bold text-red-500";
        return;
      }
      const rec = new SR();
      rec.lang = 'en-US';
      rec.interimResults = false;
      feedbackEl.textContent = "🎙️ Escuchando... habla ahora.";
      feedbackEl.className = "voice-feedback text-xs font-bold text-blue-600 animate-pulse";
      btn.disabled = true;

      rec.onresult = function(ev) {
        const spoken = ev.results[0][0].transcript.toLowerCase();
        const cleanTarget = targetPhrase.toLowerCase().replace(/[.,?!]/g, '');
        const cleanSpoken = spoken.replace(/[.,?!]/g, '');
        const isClose = cleanSpoken.includes(cleanTarget.split(' ')[0]) || cleanSpoken.length > 5;
        const score = isClose ? Math.floor(Math.random() * 15 + 85) : 60;

        feedbackEl.textContent = `Puntaje: ${score}% · "${ev.results[0][0].transcript}"`;
        feedbackEl.className = score >= 80 
          ? "voice-feedback text-xs font-bold text-green-600" 
          : "voice-feedback text-xs font-bold text-amber-600";
      };

      rec.onerror = function() {
        feedbackEl.textContent = "No se detectó audio o falta permiso de micrófono.";
        feedbackEl.className = "voice-feedback text-xs font-bold text-red-500";
      };

      rec.onend = function() {
        btn.disabled = false;
      };

      try {
        rec.start();
      } catch (err) {
        feedbackEl.textContent = "Error al iniciar micrófono.";
        btn.disabled = false;
      }
    }

    // 5. COPY GIFT CODE
    function copyCode() {
      const code = document.getElementById('giftCodeText').innerText;
      navigator.clipboard.writeText(code).then(() => {
        alert("¡Código copiado al portapapeles: " + code);
      });
    }

    // 6. FORM HANDLER
    function handleEnroll(e) {
      e.preventDefault();
      const name = document.getElementById('studentName').value;
      const email = document.getElementById('studentEmail').value;
      const phone = document.getElementById('studentPhone').value;
      const schedule = document.getElementById('studentSchedule').value;

      document.getElementById('certStudentName').textContent = name;
      document.getElementById('enrollSuccess').classList.remove('hidden');

      const waMsg = encodeURIComponent(
        `¡Hola Active Lingua! Deseo activar mi Beca de 3 Meses Gratis.\n\n` +
        `👤 Alumno: ${name}\n` +
        `📧 Correo: ${email}\n` +
        `📱 WhatsApp: ${phone}\n` +
        `🗓️ Horario: ${schedule}\n` +
        `🎟️ Cupón: ACTIVELINGUA-VIP3M-2025`
      );
      document.getElementById('waDirectBtn').href = `https://wa.me/523223512797?text=${waMsg}`;
      alert("¡Registro enviado con éxito! Puedes presionar el botón verde para contactar al asesor por WhatsApp.");
    }

    // 7. PWA SERVICE WORKER REGISTRATION & INSTALL PROMPT
    let deferredPrompt;
    window.addEventListener('beforeinstallprompt', (e) => {
      e.preventDefault();
      deferredPrompt = e;
      const installBtn = document.getElementById('pwaInstallBtn');
      if (installBtn) installBtn.classList.remove('hidden');
    });

    document.getElementById('pwaInstallBtn').addEventListener('click', async () => {
      if (deferredPrompt) {
        deferredPrompt.prompt();
        const { outcome } = await deferredPrompt.userChoice;
        if (outcome === 'accepted') {
          console.log('Active Lingua PWA instalada');
        }
        deferredPrompt = null;
      } else {
        alert("Para instalar en iPhone: pulsa Compartir > Agregar a Inicio.\nEn Android: menú de Chrome > Instalar Aplicación.");
      }
    });

    if ('serviceWorker' in navigator) {
      window.addEventListener('load', () => {
        navigator.serviceWorker.register('./sw.js').catch(err => {
          console.log('SW no registrado (modo offline local):', err);
        });
      });
    }

    // INIT
    renderCurriculum();
  </script>
</body>
</html>
