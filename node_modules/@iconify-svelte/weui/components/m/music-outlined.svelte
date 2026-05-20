<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/anzoiqb_t.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="anzoiqb_t"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:music-outlined" {...props}></Icon>
