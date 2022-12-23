# LUA

## 变量

```lua
num = 100
local num = 100
```

## 方法

```lua
function SayHello()
    print("Hello")
end

SayHello()
```

## 循环

```lua
for i = 1, 10, 1 do
    print(i)
end
```

## 表

```lua
local config = {}
config.words = "Hello"
config.num = 100
config["name"]= "Xiao Wang"

print(config.name)
print(config.num)
print(config.words)

-- 表的遍历
for index, value in pairs(config) do
    print(index, value)
end
```

## 数组

```lua
local arr = {1, 2, 3, 4, 5}

for index, value in ipairs(arr) do
    print(index, value)
end
```

## 类

```lua
function People(name)
    local self = {}
    local function init()
        self.name = name
    end

    self.sayHi = function ()
        print("Hello" .. self.name)
    end
    init()
    return self
end

local p = People("ZhangSan")
p:sayHi()
```
