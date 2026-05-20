<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hoswc34or.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hoswc34or"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:volume-up-outlined" {...props}></Icon>
