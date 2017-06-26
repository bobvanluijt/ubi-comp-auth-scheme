# Ubiquotes Computing and Internet of Things simple identification scheme.

The following scheme is a simple authentication tree scheme used for authenticating devices, objects, etcetera. It is created to understand relations between objects inside Ubiquitous Computing and Internet of Things platforms.

# Why this scheme?
The goal is to make communication as simple as possible. You can have multiple use-cases based on this scheme. For example: a branch of keys can represent location, time, individuals, etcetera.

# Definition
1. There is one root key.
2. With every key, a child key can be generated.
3. A child key can have write, read, delete, and execution rights.
4. A parent has access to a child, a child its children, etcetera.
5. A child has no access to a parent.
6. A child can have an expiration timestamp which, when expired, all children expire too.
7. A child can inherit all values from a parent except for the actual key.

# Miscellaneous
- An object can have multiple keys.
- If you want to have a parent that can't write, read, delete or execute on a child. You can set these values to `false` and within the child to `true`.
- This is _not_ and authentication but identification scheme.

# Comments or suggestions
If you see opportunity to improve this scheme, please create an issue in this repo.
