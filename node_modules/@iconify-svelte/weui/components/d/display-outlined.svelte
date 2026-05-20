<script>
import Icon from '@iconify/css-svelte';
import '../../css/j/j34g6udkl.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="j34g6udkl"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:display-outlined" {...props}></Icon>
