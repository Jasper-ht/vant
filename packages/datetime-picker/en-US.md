## DatetimePicker

### Install
``` javascript
import { DatetimePicker } from 'vant';

Vue.use(DatetimePicker);
```

### Usage

#### Choose DateTime

```html
<van-datetime-picker
  v-model="currentDate"
  type="datetime"
  :min-date="minDate"
  :max-date="maxDate"
/>
```

```javascript
export default {
  data() {
    return {
      minHour: 10,
      maxHour: 20,
      minDate: new Date(),
      maxDate: new Date(2019, 10, 1),
      currentDate: new Date()
    };
  }
};
```

#### Choose Date

```html
<van-datetime-picker
  v-model="currentDate"
  type="date"
  :min-date="minDate"
/>
```

```js
export default {
  data() {
    return {
      currentDate: new Date()
    };
  }
}
```

#### Choose Year-Month

```html
<van-datetime-picker
  v-model="currentDate"
  type="year-month"
  :min-date="minDate"
/>
```

```js
export default {
  data() {
    return {
      currentDate: new Date()
    };
  }
}
```

#### Choose Time

```html
<van-datetime-picker
  v-model="currentDate"
  type="time"
  :min-hour="minHour"
  :max-hour="maxHour"
/>
```

```js
export default {
  data() {
    return {
      currentDate: '12:00'
    };
  }
}
```

### API

| Attribute | Description | Type | Default |
|-----------|-----------|-----------|-------------|-------------|
| type | Can be set to `date` `time` `year-month` | `String` | `datetime` |
| min-date | Min date | `Date` | Ten years ago on January 1 |
| max-date | Max date | `Date` | Ten years later on December 31 |
| min-hour | Min hour | `Number` | `0` |
| max-hour | Max hour | `Number` | `23` |
| title | Toolbar title | `String` | `''` |
| loading | Whether to show loading prompt | `Boolean` | `false` |
| item-height | Option height | `Number` | `44` |
| confirm-button-text | Text of confirm button | `String` | `Confirm` |
| cancel-button-text | Text of cancel button | `String` | `Cancel` |
| visible-item-count | Count of visible columns | `Number` | `5` |

### Event

| Event | Description | Arguments |
|-----------|-----------|-----------|
| change | Triggered when value changed | picker: picker instance |
| confirm | Triggered when click confirm button | value: current value |
| cancel | Triggered when click cancel button | - |
