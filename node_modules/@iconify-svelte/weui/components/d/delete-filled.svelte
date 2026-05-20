<script>
import Icon from '@iconify/css-svelte';
import '../../css/m/m5rkeab4b.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="m5rkeab4b"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:delete-filled" {...props}></Icon>
