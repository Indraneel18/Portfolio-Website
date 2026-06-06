<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/empx9xa-x.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="empx9xa-x"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add-filled" {...props}></Icon>
