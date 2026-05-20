<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/a6_4-sbgx.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="a6_4-sbgx"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:photo-wall-outlined" {...props}></Icon>
