<script>
import Icon from '@iconify/css-svelte';
import '../../css/m/ma3conxig.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ma3conxig"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:transfer2-outlined" {...props}></Icon>
