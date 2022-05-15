# Introduction

A picker component implemented fully using javascript. It is highly customizable and flexible. It can be used with expo projects and non expo. However, it has been tested only with expo projects

# Installation

```js
npm i @manatsa/simple-react-native-picker --save
```


# Usage

```js 
import Picker from "@manatsa/simple-react-native-picker" 
```

# Props
 - **_value_** \* - the selected value.
 - **_onValueChange_** \* - the function/method to execute when user selects a value.
 - **_items_** \* - the items to populate picker options. The items should be an array of objects with label and value keys eg. `{label:'Option 1', value:'Value 1'}`.
 - **_prompt_** \* - the placeholder to show before selection is done.
 - **_icon_** - icon name to show to the left of the picker boundary (_optional_). The component uses MaterialCommunityIcons from `react-native-vector-icons` package.
 - **_defaultColor_** - default selected option color and icons color (_optional_).
 - **_optionsBoldText_** - the boolean instructing the component to show options as bold text (_optional_)
 - **_optionsTextSize_** - options text size as a number (_optional_)
 - **_optionsHeaderBackgroundColor_** - string color as header background (_optional_)
 - **_optionsHeaderTextColor_** - options header text color as string (_optional_)
 - **_width_** - width of the options container as `string | number` (_optional_)
 - **_callback_** - a callback method to retrieve picker value for other uses eg. show/hide other components.

 # Example

 ```js
    import Picker from "@manatsa/simple-react-native-picker" 
    import ...

    const Example=()=>{

        const [choice, setChoice] = React.useState("")
        const [value, setValue]=React.useState('O')
        const genderPickerOptions=[
            {label:'Female', value:'F'},
            {label:'Male', value:'M'},
            {label:'Other', value:'O'}
        ]

        return (
            <>
                <Picker 
                    value={value}
                    items={genderPickerOptions}
                    onValueChange={val=>console.log(val)}
                    callback={setChoice}
                />
                { choice==='M' && <Text>{'No more males allowed!'}</Text>

                }
            </>
        )

    }
 ```

 # License

 MIT License

 # Author

 <a href="mailto:manatsachinyeruse@gmail.com">Manatsa Chinyeruse</a>


