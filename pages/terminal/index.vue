<template>
    <DocComponent title="Vue Terminal Component" header="Terminal" description="Terminal is a text based user interface." :componentDocs="docs" :apiDocs="['Terminal', 'TerminalService']" :ptTabComponent="ptComponent" :themingDocs="themingDoc" />
</template>

<script>
import ThemingDoc from '@/doc/Terminal/theming/index.vue';
import AccessibilityDoc from '@/doc/terminal/AccessibilityDoc';
import BasicDoc from '@/doc/terminal/BasicDoc';
import ImportDoc from '@/doc/terminal/ImportDoc';
import PTComponent from '@/doc/terminal/pt/index.vue';

export default {
    data() {
        return {
            docs: [
                {
                    id: 'import',
                    label: 'Import',
                    component: ImportDoc
                },
                {
                    id: 'basic',
                    label: 'Basic',
                    component: BasicDoc
                },
                {
                    id: 'accessibility',
                    label: 'Accessibility',
                    component: AccessibilityDoc
                }
            ],
            ptComponent: PTComponent,
            themingDoc: ThemingDoc
        };
    }
};
</script>
