<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/dg9j3pb4h.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="dg9j3pb4h"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:eyes-on-outlined" {...props}></Icon>
