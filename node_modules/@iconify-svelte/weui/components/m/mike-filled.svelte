<script>
import Icon from '@iconify/css-svelte';
import '../../css/p/peeizybjw.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="peeizybjw"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:mike-filled" {...props}></Icon>
