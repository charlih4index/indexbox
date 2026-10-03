{% assign vowels = "ㄚ,ㄛ,ㄜ,ㄝ,ㄞ,ㄟ,ㄠ,ㄡ,ㄢ,ㄣ,ㄤ,ㄥ,ㄦ" | split: "," %}
{% assign consonants = "␢,ㄅ,ㄆ,ㄇ,ㄈ,ㄉ,ㄊ,ㄋ,ㄌ,ㄍ,ㄎ,ㄏ,ㄐ,ㄑ,ㄒ,ㄓ,ㄔ,ㄕ,ㄖ,ㄗ,ㄘ,ㄙ" | split: "," %}

<table>
  <caption>Zhuyin Table (Auto‑Generated with Jekyll)</caption>

  <thead>
    <tr>
      <th>Vowel</th>
      <th>Index</th>
      {% for c in consonants %}
        <th>{{ c }}</th>
      {% endfor %}
    </tr>
  </thead>

  <tbody>
    {% for v in vowels %}
      <tr>
        <td>{{ v }}</td>
        <td>{{ forloop.index }}</td>

        {% for c in consonants %}
          <td>{{ c }}{{ v }}</td>
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>

{% assign vowels = "ㄚ,ㄛ,ㄜ,ㄝ,ㄞ,ㄟ,ㄠ,ㄡ,ㄢ,ㄣ,ㄤ,ㄥ,ㄦ" | split: "," %}
{% assign consonants = "␢,ㄅ,ㄆ,ㄇ,ㄈ,ㄉ,ㄊ,ㄋ,ㄌ,ㄍ,ㄎ,ㄏ,ㄐ,ㄑ,ㄒ,ㄓ,ㄔ,ㄕ,ㄖ,ㄗ,ㄘ,ㄙ" | split: "," %}
{% assign tones = "1,2,3,4,5" | split: "," %}

<table>
  <caption>Zhuyin Table with Tones</caption>

  <thead>
    <tr>
      <th>Vowel</th>
      <th>Index</th>
      {% for c in consonants %}
        <th>{{ c }}</th>
      {% endfor %}
      {% for t in tones %}
        <th>Tone {{ t }}</th>
      {% endfor %}
    </tr>
  </thead>

  <tbody>
    {% for v in vowels %}
      <tr>
        <td>{{ v }}</td>
        <td>{{ forloop.index }}</td>

        {% for c in consonants %}
          <td>{{ c }}{{ v }}</td>
        {% endfor %}

        {% for t in tones %}
          <td>{{ v }}{{ t }}</td>
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>
