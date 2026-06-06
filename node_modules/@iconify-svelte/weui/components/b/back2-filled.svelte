<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/h1p_6uu5p.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="h1p_6uu5p"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:back2-filled" {...props}></Icon>
