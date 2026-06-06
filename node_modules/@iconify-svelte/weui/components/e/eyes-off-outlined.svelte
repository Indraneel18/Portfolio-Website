<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/t7m9o8f6t.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="t7m9o8f6t"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:eyes-off-outlined" {...props}></Icon>
