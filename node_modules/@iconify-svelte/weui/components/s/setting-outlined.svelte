<script>
import Icon from '@iconify/css-svelte';
import '../../css/r/rjt5249cl.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="rjt5249cl"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:setting-outlined" {...props}></Icon>
