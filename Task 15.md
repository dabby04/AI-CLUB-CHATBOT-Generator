# Task 15 - Pattern Re-Use using &lt;srai&gt; Tag in AIML

In this Task we will be using the &lt;srai&gt; tag to define different targets for the same template.Example:

 The &lt;srai&gt; is a multipurpose tag. Some of the commonly used areas are:
```
1)Symbolic Reduction
2)Divide and Conquer 
3)Synonyms Resolution
4)Keywords Detection
```

## Symbolic Reduction
This technique is used to simplify patterns. It helps to reduce complex grammatical patterns with simple pattern(s)
For Example consider the following conversation:
```
Human: Who was Albert Einstein?
Bot: Albert Einstein was a German physicist.
Human: Who was Isaac Newton?
Bot: Isaac Newton was a English physicist and mathematician.
```


Now what if the converstation was like this:
```
Human: DO YOU KNOW WHO Albert Einstein IS?
Human: DO YOU KNOW WHO Isaac Newton IS?

```
 Here the &lt;srai&gt; tag works. It can take pattern of the user as a template.
 Example :
```
 <category>
   <pattern>WHO IS ALBERT EINSTEIN?</pattern>
   <template>Albert Einstein was a German physicist.</template>
</category>

<category>
   <pattern> WHO IS Isaac NEWTON? </pattern>
   <template>Isaac Newton was a English physicist and mathematician.</template>
</category>
```
Converting this using &lt;srai&gt; tag
```
<category>
      <pattern> WHO IS ALBERT EINSTEIN </pattern>
      <template>Albert Einstein was a German physicist.</template>
</category>
   
<category>
    <pattern> WHO IS Isaac NEWTON </pattern>
    <template>Isaac Newton was a English physicist and mathematician.</template>
</category>
   
<category>
    <pattern>DO YOU KNOW WHO * IS</pattern>
    <template>
        <srai>WHO IS <star/></srai>
    </template>
</category>

```

To know more about the other commonly used areas of &lt;srai&gt; visit this website: [Click Here](https://www.tutorialspoint.com/aiml/aiml_srai_tag.htm)

