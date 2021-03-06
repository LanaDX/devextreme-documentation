DevExtreme editors support the <a href="https://v3.vuejs.org/guide/forms.html" target="_blank">`v-model`</a> directive that creates two-way binding on the editor's value.

    <!-- tab: App.vue -->
    <template>
        <DxTextBox v-model="bindingProperty" />
    </template>

    <script>
    import DxTextBox from 'devextreme-vue/text-box';

    export default {
        components: {
            DxTextBox
        },
        data() {
            return {
                bindingProperty: 'Some value'
            }
        }
    }
    </script>

Alternatively, you can [use the `sync` modifier](/concepts/55%20Vue%20Components/20%20Component%20Configuration%20Syntax/33%20Two-Way%20Property%20Binding.md '/Documentation/Guide/Vue_Components/Component_Configuration_Syntax/#Two-Way_Property_Binding').