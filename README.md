# JessiLiz.github.io
<script>
    (function setupNbinteract() {
        // If NbInteract hasn't loaded, wait one second and try again
        if (window.NbInteract === undefined) {
        setTimeout(setupNbinteract, 1000)
        return
        }

        var interact = new window.NbInteract({
        spec: '{GitHub_UserName}/{Gist_ID}/master',
        baseUrl: 'https://mybinder.org',
        provider: 'gh',
        })
        interact.prepare()

        window.interact = interact
    })()
</script>
