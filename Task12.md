# Task 12 - Handling Variations in User Input in our Custom AIML file


## Variations in User Input
Just like we did in the last Task, we can create different responses according to different variations in user input:

```
<?xml version="1.0" encoding="UTF-8"?>
<aiml>
    <category>
        <pattern>Does UBC have 2 campuses</pattern>
        <template>Yes that is right</template>
    </category>
    <category>
        <pattern>Does UBC have more than 2 campuses</pattern>
        <template> No, UBC only has two campuses</template>
    </category>
</aiml>

```

## Random Responses to a Pattern
We also have the option to randomly generate a response from a list of responses.

```
<?xml version="1.0" encoding="UTF-8"?>
<aiml>
    <category>
        <pattern>Give a synonym for good</pattern>
        <template>
            <random>    
                <li>fine</li>
                <li>quality</li>
                <li>acceptable</li>
                <li>adequate</li>
                <li>up to the mark</li>
                <li>satisfactory</li>
            </random>
        </template>
    </category>
</aiml>

```

## Onto Task-13 -->
