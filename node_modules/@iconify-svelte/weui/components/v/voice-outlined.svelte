<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/sat40obmj.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="sat40obmj"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:voice-outlined" {...props}></Icon>
