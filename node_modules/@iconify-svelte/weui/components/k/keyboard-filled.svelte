<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hxovt7blt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hxovt7blt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:keyboard-filled" {...props}></Icon>
