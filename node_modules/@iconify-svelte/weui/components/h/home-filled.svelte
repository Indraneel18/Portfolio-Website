<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/sg0g_ibbe.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="sg0g_ibbe"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:home-filled" {...props}></Icon>
