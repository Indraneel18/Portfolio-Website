<script>
import Icon from '@iconify/css-svelte';
import '../../css/o/o7s0spbog.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="o7s0spbog"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:previous2-filled" {...props}></Icon>
