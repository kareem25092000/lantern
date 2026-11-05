]633;E;{ echo "# Evidence: B"\x3b sec E1 "E1"\x3b sec E3 "E3"\x3b sec E4 "E4"\x3b sec E5b "E5 (b)"\x3b sec E6 "E6"\x3b } > evidence/B.md;d8020bfc-2c72-4e95-80af-2e71d9b2d928]633;C# Evidence: B

## E1
```
$ git remote -v
origin	git@github.com:Kareem25092000/lantern.git (fetch)
origin	git@github.com:Kareem25092000/lantern.git (push)

```

## E3
```
def balancedSums(arr):
    # Write your code here
    if len(arr) == 1:
        return "YES"
    right_sum = 0
    sum_arr =[arr[0]]
    for i in range(1,len(arr)):
        sum_arr.append(sum_arr[i-1]+arr[i])
    for j in range(len(arr)-1,0,-1):
        right_sum += arr[j]
        if right_sum == sum_arr[j-2]:
            return "YES"
        if right_sum == 0 and (j-1)== 0:
            return "YES"
    return "NO"
```

## E4
```
$ git log --oneline --graph --decorate -10
*   4a194f6 (HEAD -> main) fixed merge conflict
|\  
| * c6d5d7e feat(storage): write JSON with indent of 2  with a body
* | 916d7da feat(tasks): add done flag to new tasks
|/  
*   e584633 (origin/main, origin/HEAD) Merge branch 'main' of https://github.com/kareem25092000/lantern
|\  
| *   98bb394 Merge branch 'main' of github.com:Kareem25092000/lantern
| |\  
| * | 18d2e83 chore(scratch): remove placeholder
| * | ccf9c56 chore(scratch): add placeholder
| * | 8ec7eba refactor(storage): name the tasks file constant
| * | 102f873 docs(usage): describe add and list commands
| * | 3b2ea17 feat(storage): add load and save helpers

```

## E5 (b)
```
$ git reflog -8
256e707 HEAD@{0}: reset: moving to origin/main
27b7703 HEAD@{1}: commit: docs(usage): add usage heading
256e707 HEAD@{2}: pull: Fast-forward
449f535 HEAD@{3}: commit (merge): Merge branch 'main' of github.com:Kareem25092000/lantern
d031f59 HEAD@{4}: commit: fix(build): untrack generated files
5a0d697 HEAD@{5}: commit: chore(build): add logs and cache
4a194f6 HEAD@{6}: commit (merge): fixed merge conflict
916d7da HEAD@{7}: merge fix/stable-key-order: Fast-forward

```

## E6
```
$ git stash list
stash@{0}: On feature/list-sort: wip: list --sort option
stash@{1}: On feature/list-sort: wip: list --sort option

```
