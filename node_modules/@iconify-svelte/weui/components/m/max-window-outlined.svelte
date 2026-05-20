<script>
import Icon from '@iconify/css-svelte';
import '../../css/y/yjhmhrwgm.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="yjhmhrwgm"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:max-window-outlined" {...props}></Icon>
