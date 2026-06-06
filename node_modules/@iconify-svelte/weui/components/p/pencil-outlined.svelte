<script>
import Icon from '@iconify/css-svelte';
import '../../css/f/f9m8hylsc.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="f9m8hylsc"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:pencil-outlined" {...props}></Icon>
