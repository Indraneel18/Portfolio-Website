<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/ub3lhrgwm.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ub3lhrgwm"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:album-outlined" {...props}></Icon>
