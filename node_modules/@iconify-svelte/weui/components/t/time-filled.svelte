<script>
import Icon from '@iconify/css-svelte';
import '../../css/v/vmb0t7bxz.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="vmb0t7bxz"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:time-filled" {...props}></Icon>
