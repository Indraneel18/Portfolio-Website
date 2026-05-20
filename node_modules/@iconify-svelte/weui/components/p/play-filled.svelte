<script>
import Icon from '@iconify/css-svelte';
import '../../css/v/v9fas1ukt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="v9fas1ukt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:play-filled" {...props}></Icon>
