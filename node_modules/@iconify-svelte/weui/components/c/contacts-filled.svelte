<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/esbz12vtr.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="esbz12vtr"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:contacts-filled" {...props}></Icon>
