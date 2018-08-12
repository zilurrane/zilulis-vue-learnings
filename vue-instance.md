
## Vue Instance

### 1. Creating New Vue Instance
```JS
    var vm = new Vue({
    // options
    })
```

### 2. Data
```JS
    // Our data object
    var data = { a: 1 }

    // The object is added to a Vue instance
    var vm = new Vue({
    data: data
    })

    // Getting the property on the instance
    // returns the one from the original data
    vm.a == data.a // => true

    // Setting the property on the instance
    // also affects the original data
    vm.a = 2
    data.a // => 2

    // ... and vice-versa
    data.a = 3
    vm.a // => 3
```

### 3. Instance Properties and Methods
```JS
    var data = { a: 1 }
    var vm = new Vue({
    el: '#example',
    data: data
    })

    vm.$data === data // => true
    vm.$el === document.getElementById('example') // => true

    // $watch is an instance method
    vm.$watch('a', function (newValue, oldValue) {
    // This callback will be called when `vm.a` changes
    })
```

### 4. Instance Lifecycle Hooks
```JS
    new Vue({
    data: {
        a: 1
    },
    created: function () {
        // `this` points to the vm instance
        console.log('a is: ' + this.a)
    }
    })
    // => "a is: 1"
```
![Instance Lifecycle Diagram](https://vuejs.org/images/lifecycle.png)
