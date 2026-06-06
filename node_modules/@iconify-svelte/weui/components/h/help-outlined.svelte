<script>
import Icon from '@iconify/css-svelte';
import '../../css/w/wd93nu3lx.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="wd93nu3lx"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:help-outlined" {...props}></Icon>
