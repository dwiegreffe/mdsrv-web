#Bla

<iframe>
        <div id="app"></div>
        <script type="text/javascript" src="./molstar.js"></script>
        <script type="text/javascript">
            molstar.Viewer.create('app', {
                layoutIsExpanded: true,
                layoutShowControls: true,
                layoutShowRemoteState: false,
                layoutShowSequence: true,
                layoutShowLog: false,    
                layoutShowLeftPanel: true,

                viewportShowExpand: true,  
                viewportShowSelectionMode: false,
                viewportShowAnimation: true,

                pdbProvider: 'rcsb', 
                emdbProvider: 'rcsb',
            }).then(viewer => {

             function getParam(name, regex) {
                var r = new RegExp(name + '=' + '(' + regex + ')[&]?', 'i');
                return decodeURIComponent(((window.location.search || '').match(r) || [])[1] || '');
            }
                var sessionUrl = getParam('session-url', '[^&]+').trim();
                viewer.loadSessionFromUrl(sessionUrl);
                //viewer.loadEmdb('EMD-30210', { detail: 6 });
                // viewer.loadAllModelsOrAssemblyFromUrl('https://cs.litemol.org/5ire/full', 'mmcif', false, { representationParams: { theme: { globalName: 'operator-name' } } })
            });
        </script>
</iframe>








