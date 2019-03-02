# Titanium Android BottomSheet module

Use the native Android `BottomSheet` view in Appcelerator Titanium. 

Credits go to the native [`michael-rapp/AndroidBottomSheet`](https://github.com/michael-rapp/AndroidBottomSheet) library 
and [@chrystoffer](https://github.com/chrystoffer) for the initial Hyperloop based example. Thanks guys! 🤘

<img src="./screenshot.png" width="300" alt="Example Screenshot" />

## Requirements
- [x] Titanium SDK 7.0.0+

## Download
- [x] [Stable release](https://github.com/hansemannn/titanium-android-bottom-sheet/releases)

## API's

### `createOptionDialog`

#### Arguments

| Name | Type |
| - | - |
| `title` | String |
| `options` | Array<String> |
| `cancelable` | Boolean |
| `destructive`* | Number |

> `*` The `destructive` option is there to mimic the native iOS behavior by tinting the title
red. Different to iOS, the title will be red if the index is > -1 and is not applied to a single
option but the title.

#### Events

##### `click`

| Name | Type |
| - | - |
| `index` | Number |
| `cancel` | Boolean |

## Examples

```js
import TiBottomSheet from 'ti.bottomsheet';

const options = TiBottomSheet.createOptionDialog({
  title: 'Titanium rocks!',
  options: [ 'Option A', 'Option B' ],
  cancelable: true
});

options.addEventListener('click', event => {
  alert(event);
});

options.show();
```

## Build
```js
cd android
ti build -p android --build-only
```

## Legal

Copyright (c) 2019-present by Hans Knöchel. All Rights Reserved.
