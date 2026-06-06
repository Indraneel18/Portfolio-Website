<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/doceul2pl.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="doceul2pl"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:home-outlined" {...props}></Icon>
