# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    An example of a visial heirarch that could be modelded with components is a movie review application. The initial component could be different genres that the user can choose between. The next component, after deciding on a genre, would be a list of movie titles. The next component after the user has selected a movie could be each user's review. Each piece would be its own component because each piece must be individually reachable and editable within the hierarchy, even though they all relate to the same application. Each piece might be its own component because they each represent a view state that will undergo its own specific changes.

    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    The resulting files that are created are a component file for what ever component was generated (using `my-map` from the last question, a `my-map` component file) and a `my-map` template file.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{#each model as |contact|}}
      {{my-contact contacts=contacts}}
    {{/each}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each model.phones as |phone|}}
      {{my-phone phone=phone}}
    {{/each}}
    ```
