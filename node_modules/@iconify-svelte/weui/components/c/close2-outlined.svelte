<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/ek-30ob9y.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ek-30ob9y"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:close2-outlined" {...props}></Icon>
