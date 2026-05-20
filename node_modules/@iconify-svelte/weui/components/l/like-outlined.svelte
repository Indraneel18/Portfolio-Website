<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/teped2blx.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="teped2blx"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:like-outlined" {...props}></Icon>
