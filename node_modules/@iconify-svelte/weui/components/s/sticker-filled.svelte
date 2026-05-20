<script>
import Icon from '@iconify/css-svelte';
import '../../css/w/wte99mb7f.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="wte99mb7f"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:sticker-filled" {...props}></Icon>
