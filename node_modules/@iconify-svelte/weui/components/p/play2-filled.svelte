<script>
import Icon from '@iconify/css-svelte';
import '../../css/p/pmbf_2bij.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="pmbf_2bij"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:play2-filled" {...props}></Icon>
