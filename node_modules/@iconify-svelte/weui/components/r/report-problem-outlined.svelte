<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hvn9s80eo.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hvn9s80eo"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:report-problem-outlined" {...props}></Icon>
