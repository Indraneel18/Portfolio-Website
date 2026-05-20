<script>
import Icon from '@iconify/css-svelte';
import '../../css/g/g4l3s8_di.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="g4l3s8_di"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:text-outlined" {...props}></Icon>
