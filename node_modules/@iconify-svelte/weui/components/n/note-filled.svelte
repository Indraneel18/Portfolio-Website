<script>
import Icon from '@iconify/css-svelte';
import '../../css/y/ydxeveb1u.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ydxeveb1u"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:note-filled" {...props}></Icon>
