<script>
import Icon from '@iconify/css-svelte';
import '../../css/k/k926z6j4f.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="k926z6j4f"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:done2-outlined" {...props}></Icon>
