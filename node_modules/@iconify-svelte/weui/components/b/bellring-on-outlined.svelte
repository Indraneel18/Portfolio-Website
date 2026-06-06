<script>
import Icon from '@iconify/css-svelte';
import '../../css/i/ig8js3b9f.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ig8js3b9f"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:bellring-on-outlined" {...props}></Icon>
