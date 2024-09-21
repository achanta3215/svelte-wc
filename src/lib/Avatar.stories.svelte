<script context="module">
  import Avatar from './Avatar.svelte';

  export const meta = {
    title: 'Components/Avatar',
    component: Avatar,
    argTypes: {
      name: { control: 'text' },
      url: { control: 'text' },
    },
  };
</script>

<script>
  import { Story, Template } from '@storybook/addon-svelte-csf';
</script>

<Template let:args>
  <sv-avatar {...args}></sv-avatar>
</Template>

<Story name="Default" args={{ name: 'John Doe', url: 'https://example.com/johndoe.jpg' }} />

<Story name="WithoutImage" args={{ name: 'Jane Smith' }} />

<Story name="Empty" args={{ name: '', url: '' }} />

<!-- Dynamic snippet should be disabled for this story -->
<Story name="Avatar No Args">
  <sv-avatar></sv-avatar>
</Story>