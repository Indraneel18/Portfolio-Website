<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/ug4xqib1d.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ug4xqib1d"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:more2-outlined" {...props}></Icon>
