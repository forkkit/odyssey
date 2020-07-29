---
template: component
name: Button
lead: An Odyssey button appears as a rounded rectangle that is wider than it is tall, with a descriptive caption in its center. Users press the button by clicking it with a pointer controlled by a mouse, keystrokes can also be used to execute the command of a button.
links:
  - icon: github
    label: View source
    href: https://github.com/okta/odyssey/blob/master/packages/odyssey/src/scss/components/_button.scss
  - icon: figma
    label: View designs
    href: https://www.figma.com/file/pULYhG6KIhBsnQTFjkpTFv/Buttons?node-id=2660%3A365
---

::: slot overview
## Button types
In Odyssey there are 5 different button types; Primary, Secondary, Danger, Clear, and Overlay.

#### Primary
Our default button is used for primary action on a page or view. For example, “Save”. Use this button sparingly to provide a clear target for users to get to. 

It’s best to use this button on a white background.

<Example/>

<figure>
  <button class="ods-button">Primary</button>
  <button class="ods-button is-ods-button-hover">Hover</button>
  <button class="ods-button is-ods-button-focus">Focus</button>
  <button disabled="disabled" class="ods-button">Disabled</button>
</figure>

#### Secondary
Ideal for a secondary actions to compliment the Primary button. Similar to the Primary button, use this button sparingly to provide focus to the user. 

It’s best to use this button on a white background.

<figure>
  <button class="ods-button is-ods-button-secondary">Secondary</button>
  <button class="ods-button is-ods-button-secondary is-ods-button-hover">Hover</button>
  <button class="ods-button is-ods-button-secondary is-ods-button-focus">Focus</button>
  <button disabled="disabled" class="ods-button is-ods-button-secondary">Disabled</button>
</figure>

#### Danger
Use this button for scenarios where a user may be deleting information or completing a task that could not be reversed. 

It’s best to use this button on a white background.

<figure>
  <button class="ods-button is-ods-button-danger">Danger</button>
  <button class="ods-button is-ods-button-danger is-ods-button-hover">Hover</button>
  <button class="ods-button is-ods-button-danger is-ods-button-focus">Focus</button>
  <button disabled="disabled" class="ods-button is-ods-button-danger">Disabled</button>
</figure>

#### Clear
These are used for in-page interactions that modify the visible UI but do not modify data or an ongoing process. For example, hiding or showing a password field. 

They pair well with Primary and Secondary buttons. 

It’s best to use this button on a white background.

<figure>
  <button class="ods-button is-ods-button-clear">Secondary</button>
  <button class="ods-button is-ods-button-clear is-ods-button-hover">Hover</button>
  <button class="ods-button is-ods-button-clear is-ods-button-focus">Focus</button>
  <button disabled="disabled" class="ods-button is-ods-button-clear">Disabled</button>
</figure>

#### Overlay
These buttons may only be used on top of a “Base Color” such as Purple 500 or on top of a colored background, photo, or illustration. They should only be used in the scenario where Primary, Secondary, and regular text links cannot be used.

Lastly, they only exist at the large size.

<figure>
  <button class="ods-button is-ods-button-overlay">Overlay</button>
  <button class="ods-button is-ods-button-overlay is-ods-button-hover">Hover</button>
  <button class="ods-button is-ods-button-overlay is-ods-button-focus">Focus</button>
  <button disabled="disabled" class="ods-button is-ods-button-overlay">Disabled</button>
</figure>

<hr />

:::

::: slot scss

##### Primary

<figure class="ods--example">
  <div class="ods--rendered">
    <button class="ods-button">Primary</button>
    <button class="ods-button is-ods-button-hover">Hover</button>
    <button class="ods-button is-ods-button-focus">Focus</button>
    <button class="ods-button" disabled>Disabled</button>
  </div>

  ```html
  <button class="ods-button">Primary</button>
  <button class="ods-button" disabled>Primary</button>
  ```
</figure>

##### Secondary

<figure class="ods--example">
  <div class="ods--rendered">
    <button class="ods-button is-ods-button-secondary">Secondary</button>
    <button class="ods-button is-ods-button-secondary is-ods-button-hover">Hover</button>
    <button class="ods-button is-ods-button-secondary is-ods-button-focus">Focus</button>
    <button class="ods-button is-ods-button-secondary" disabled>Disabled</button>
  </div>

  ```html
  <button class="ods-button is-ods-button-secondary">Secondary</button>
  <button class="ods-button is-ods-button-secondary" disabled>Secondary</button>
  ```
</figure>

##### Danger

<figure class="ods--example">
  <div class="ods--rendered">
    <button class="ods-button is-ods-button-danger">Danger</button>
    <button class="ods-button is-ods-button-danger is-ods-button-hover">Hover</button>
    <button class="ods-button is-ods-button-danger is-ods-button-focus">Focus</button>
    <button class="ods-button is-ods-button-danger" disabled>Disabled</button>
  </div>

  ```html
  <button class="ods-button is-ods-button-danger">Danger</button>
  <button class="ods-button is-ods-button-danger" disabled>Danger</button>
  ```
</figure>

##### Overlay

<figure class="ods--example">
  <div class="ods--rendered is-rendered-success">
    <button class="ods-button is-ods-button-overlay">Overlay</button>
    <button class="ods-button is-ods-button-overlay is-ods-button-hover">Hover</button>
    <button class="ods-button is-ods-button-overlay is-ods-button-focus">Focus</button>
    <button class="ods-button is-ods-button-overlay" disabled>Disabled</button>
  </div>

  ```html
  <button class="ods-button is-ods-button-overlay">Overlay</button>
  <button class="ods-button is-ods-button-overlay" disabled>Overlay</button>
  ```
</figure>

##### Clear

<figure class="ods--example">
  <div class="ods--rendered">
    <button class="ods-button is-ods-button-clear">Clear</button>
    <button class="ods-button is-ods-button-clear is-ods-button-hover">Hover</button>
    <button class="ods-button is-ods-button-clear is-ods-button-focus">Focus</button>
    <button class="ods-button is-ods-button-clear" disabled>Disabled</button>
  </div>

  ```html
  <button class="ods-button is-ods-button-clear">Clear</button>
  <button class="ods-button is-ods-button-clear" disabled>Clear</button>
  ```
</figure>

---

## Implementation

### SCSS

Styles related to buttons can be found in `/components/_button.scss`.

Semantic states can be combined to produce Secondary Danger styles.

<figure class="ods-table--figure">
  <table class="ods-table">
    <thead>
      <tr>
        <th scope="column">
          Selector
        </th>
        <th scope="column">
          Purpose
        </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <code>.ods-button</code>
        </td>
        <td>
          Applies primary & general button styles
        </td>
      </tr>
      <tr>
        <td>
          <code>.is-ods-button-secondary</code>
        </td>
        <td>
          Applies Secondary button styles
        </td>
      </tr>
      <tr>
        <td>
          <code>.is-ods-button-danger</code>
        </td>
        <td>
          Applies Danger button styles
        </td>
      </tr>
    </tbody>
  </table>
</figure>
:::
