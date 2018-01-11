### Dust JS Get Started 

```
<ul>
{#friends}
  <li>{name}, {age}{~n}</li>
{:else}
  <p>You have no friends!</p>
{/friends}
</ul>

```

JSON

```
  {
   friends: [
      { name: "Moe", age: 37 },
      { name: "Larry", age: 39 },
      { name: "Curly", age: 35 }
    ]
   }
```

HTML Rendered 

```
 <ul>
  <li>Moe, 37</li>
  <li>Larry, 39</li>
  <li>Curly, 35</li>
 </ul>
```

If empty JSON then {else} will excuted


