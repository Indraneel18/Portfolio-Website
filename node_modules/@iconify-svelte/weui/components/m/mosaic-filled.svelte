<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/u1-52n4_l.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="u1-52n4_l"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:mosaic-filled" {...props}></Icon>
