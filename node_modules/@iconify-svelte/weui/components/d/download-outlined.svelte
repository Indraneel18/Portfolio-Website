<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hodiracmn.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hodiracmn"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:download-outlined" {...props}></Icon>
