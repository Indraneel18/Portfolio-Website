<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hwvtwsb5r.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hwvtwsb5r"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:pad-outlined" {...props}></Icon>
