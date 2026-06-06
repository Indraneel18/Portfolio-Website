<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/e394lrbqt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="e394lrbqt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:voice-filled" {...props}></Icon>
