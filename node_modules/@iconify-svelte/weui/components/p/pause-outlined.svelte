<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/u51kufbla.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="u51kufbla"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:pause-outlined" {...props}></Icon>
