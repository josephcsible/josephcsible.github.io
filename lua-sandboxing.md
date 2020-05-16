<!-- left off just before library.c -->

# Functions

| Name | MediaWiki LuaSandbox |
| - | - |
| getmetatable | Restricted<sup>4</sup> |
| pcall | Restricted<sup>1</sup> |
| setmetatable | Unrestricted |
| xpcall | Restricted<sup>1</sup> |

# Resources
| Name | MediaWiki LuaSandbox |
| - | - |
| CPU time | Limited<sup>2</sup> |
| Memory | Limited<sup>3</sup> |

# Other
| Name | MediaWiki LuaSandbox |
| - | - |
| Passing tables to PHP | Restricted<sup>5</sup> |

# Footnotes

* <sup>1</sup> Some errors have a "fatal" marker object, which `pcall` and `xpcall` are wrapped to be unable to catch
* <sup>2</sup> TODO
* <sup>3</sup> Uses a custom `lua_Alloc` function to deny allocations past a configurable limit
* <sup>4</sup> `getmetatable` is wrapped to only operate on tables, the way `setmetatable` already works
* <sup>5</sup> The depth of nested tables that will be traversed is limited, circular references are disallowed, and only strings and numbers are allowed as keys
