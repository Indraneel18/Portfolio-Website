<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/u2a3ezblb.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="u2a3ezblb"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:done-outlined" {...props}></Icon>
