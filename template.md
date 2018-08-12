## Template
### 1. Interpolation

```html

    <span>Message: {{ msg }}</span> <!--Text-->

    <span v-once>This will never change: {{ msg }}</span> <!--Only once-->
    
    <p>Using v-html directive: <span v-html="rawHtml"></span></p> <!--Raw HTML-->
    
    <div v-bind:id="dynamicId"></div> <!--Attributes-->

    <p v-if="seen">Now you see me</p> <!--Directives-->

    <form v-on:submit.prevent="onSubmit"> ... </form> <!--.prevent modifier tells the v-on directive to call event.preventDefault()-->
```

### 2. Shorthands

```html
    <!-- full syntax -->
    <a v-bind:href="url"> ... </a>

    <!-- shorthand -->
    <a :href="url"> ... </a>

    <!-- full syntax -->
    <a v-on:click="doSomething"> ... </a>

    <!-- shorthand -->
    <a @click="doSomething"> ... </a>
```