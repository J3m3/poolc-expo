---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

```
            *     ,MMM8&&&&.            *
                 .MMMM88&&&&&.    .
     *           MMM88&&&&&&&&
                 'MMM88&&&&&&'
                   'MMM8&&&'      *
          |\___/|     /\___/\
          )     (     )    ~( .             '
         =\     /=   =\~    /=
           )===(       ) ~ (
          /     \     /     \
          |     |     ) ~   (
         /       \   /     ~ \
         \       /   \~     ~/
  _/\_/\_/\__  _/_/\_/\__~__/_/\_/\_/\_/\_/\_
  |  |  |  |( (  |  |  | ))  |  |  |  |  |  |
  |  |  |  | ) ) |  |  |//|  |  |  |  |  |  |
  |  |  |  |(_(  |  |  (( |  |  |  |  |  |  |
  |  |  |  |  |  |  |  |\)|  |  |  |  |  |  |
```

```python
>>> print("Hello, PoolC!")
>>> print("문제를 보시려면 아래 버튼을 클릭해주세요!")
```

<div style="display: flex; justify-content: center; gap: 1em">
<button id="non-major-problem-btn" style="width: 50%">비전공자용 문제</button>
<button id="major-problem-btn" style="width: 50%">전공자용 문제</button>
</div>

<script type="text/javascript">
  var majorProblemUrls = [
    {% for problem in site.major %}
      "{{ site.baseurl }}{{ problem.url }}"{% if forloop.last == false %},{% endif %}
    {% endfor %}
  ];

  var nonMajorProblemUrls = [
    {% for problem in site.non_major %}
      "{{ site.baseurl }}{{ problem.url }}"{% if forloop.last == false %},{% endif %}
    {% endfor %}
  ];

  document.getElementById("major-problem-btn").onclick = function() {
    var randomIndex = Math.floor(Math.random() * majorProblemUrls.length);
    var randomUrl = majorProblemUrls[randomIndex];
    window.location.href = randomUrl;
  };

  document.getElementById("non-major-problem-btn").onclick = function() {
    var randomIndex = Math.floor(Math.random() * nonMajorProblemUrls.length);
    var randomUrl = nonMajorProblemUrls[randomIndex];
    window.location.href = randomUrl;
  };
</script>

<style>
button {
  background-color: #444;
  color: #fff;
  border: 2px solid #888;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  font-family: Arial, sans-serif;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s ease, color 0.3s ease;
}

button:hover {
  background-color: #555;
  color: #ddd;
  border-color: #aaa;
}

button:active {
  background-color: #333;
  border-color: #777;
}
</style>
