---
category: Components
type: Feedback
title: Modal
---

Use to show important information for the system, and ask for user feedback. eg: When deleting an important content, pop up a Modal for secondary confirmation.

### Rules
- Use as few as possible. Modal will interrupt user operation, only use it at important situation.
- Title should be concise, do not exceed 1 line; description should be concise and complete, generally no more than 2 lines.
- Operation buttons are up to 3(vertical), generally 1-2(horizontal); [ActionSheet](/components/action-sheet) is preferred when there are more than 3 actions.
- Generally put the most likely clicked button on the right side. In addition, the cancel button should always be on the left.

## API

### Modal ( Support Platform：WEB、React-Native )

| Property             | Description                    | Type     | Default        |
|------------------|-----------------------|----------|---------------|
| prefixCls (web only)      | Class name prefix of elements |    String   | `am-modal`      |
| visible      | Determine whether a modal dialog is visible or not | Boolean          | false           |
| onClose      | Callback for clicking close icon x or mask        | (): void   | - |
| title (only transparent)       | title           | React.Element    | -           |
| closable    | Determine whether a close (x) button is visible or not | Boolean    | `false`       |
| maskClosable (only transparent) | Determine whether to close the modal dialog when clicked mask of it | Boolean   | true       |
| footer  (only not transparent)     | footer content       |  Array [{text, onPress}]    | [] |
| transparent | transparent mode or full screen mode       | Boolean   |  false |
| animationType (`rn only`) | Options: 'slide-down/up'(only transparent) / 'fade' / 'slide'(only not tranparent) | String |   fade |
| style (`web only`) |  style    | Object | transparent: {width: '286px', height: 'auto'}, <br />not transparent:  {width: '100%', height: '100%'} (web)|

### Modal.alert(title, message, actions?) ( Support Platform：WEB、React-Native )

| Property             | Description                                         | Type     | Default        |
|------------------|----------------------------------------------|----------|---------------|
| title        | title                      | String or React.Element   | -            |
| message      | message                  | String or React.Element    | -    |
| actions         | button group, [{text, onPress, style}]       | Array | -            |

### Modal.prompt(title, message, callbackOrActions, type?, defaultValue?) ( Support Platform：WEB )

| Property             | Description                                         | Type     | Default        |
|------------------|----------------------------------------------|----------|---------------|
| title        | title                      | String or React.Element   | -            |
| message      | message                  | String or React.Element                    | -    |
| callbackOrActions  | button group [{text, onPress}] or callback      | Array or Function | -            |
| type       | prompt style   | String (`default`, `secure-text`, `login-password`)|  `default`  |
| defaultValue       | Default(input whick type is password is not supported)   | String |   -  |

### Modal.operation(actions?) ( Support Platform：WEB、React-Native )

| Property             | Description                                         | Type     | Default        |
|------------------|----------------------------------------------|----------|---------------|
| actions         | button group, [{text, onPress, style}]       | Array | -            |
