https://wiiubrew.org/wiki/Cafe_OS#SysCalls


## 0x1700, FindClosestSymbol
### Finds the symbol at address or the next lowest symbol
#### Registers
| register | in | out
| - | - | - |
| r3 | address to check | 0 upon success |
| r4 | address to store nearest symbol address  | - |
| r5 | address to store symbol name text | - |
| r6 | symbol name max length | - |
| r7 | address to store info text | - |
| r8 | info text max length | - |

#### Errors
| error value | error condition |
| - | - |
| 0 | success |
| 0xbad200a | text ptr is 0 and text length is not 0
|

```cpp
uint32_t FindClosestSymbol(void* address, uint32_t* outOffsetFromSymbol, char* symbolNameBuffer, uint32_t symbolNameMaxLength, char* infoBuffer, uint32_t infoLen);
```