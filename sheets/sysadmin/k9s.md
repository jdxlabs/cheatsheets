# k9s cheatsheet

## Installation

```bash
brew install derailed/k9s/k9s
```

## Shortcuts

| Action                                      | Command           |
| ------------------------------------------- | ----------------- |
| Open a new session                          | k9s               |
| Switch contexts                             | :ctx              |
| Switch namespaces                           | :ns               |
| Display a list of shortcuts                 | ?                 |
| Display a list of resources                 | :alias, CTRL+a    |
| Jump directly to a specific resource        | :<my-resource>    |
| Quit                                        | :q, ctrl-c        |
| Show resource details                       | d                 |
| Edit resource                               | e                 |
| Kill a resource (with prompt)               | CTRL+k            |
| Show logs                                   | l                 |
| Open an interactive shell session           | s                 |
| Search (in the current view)                | /                 |
| Switch between preset views                 | 0-9               |
| Show infos about k9s config                 | k9s info          |

## Usefull links

* [k9scli - Commands](https://k9scli.io/topics/commands/)
* [k9s cheat sheet - Chai Biscuit](https://chaibiscuit.rajivy.me/devops/containerization/k8s/k9s_cheat_sheet)
* [K9s : gestion efficace de Kubernetes sans CLI](https://blog.stephane-robert.info/docs/conteneurs/orchestrateurs/outils/k9s/)
