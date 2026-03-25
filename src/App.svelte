<script>
	import Headline from './Headline.svelte';

	function headline(title, links) {
		return { title, links };
	}

	const headlines = [
		headline("Windows 11 Update KB5063878 Reportedly Causing SSD Failures", [
			"https://www.ubergizmo.com/2025/08/windows-11-update-ssd-failures/"
		]),
		headline("Microsoft confirms Windows 11 October 2025 Update breaks WinRE (Recovery) input", [
			"https://www.windowslatest.com/2025/10/18/microsoft-confirms-windows-11-october-2025-update-breaks-winre-recovery-input/",
		]),
		headline("Windows 11 update breaks localhost, prompting mass uninstall workaround", [
			"https://www.theregister.com/2025/10/16/windows_11_update_localhost/",
		]),
		headline("Microsoft confirms Windows 11 media creation tool is broken for Windows 10 users", [
			"https://betanews.com/article/oops-microsoft-confirms-windows-11-media-creation-tool-is-broken-for-windows-10-users/",
			"https://www.techworm.net/2025/10/windows-11-media-creation-tool-not-working-on-windows-10-pcs.html",
		]),
		headline("Windows 11 24H2 and 25H2 Updates Break IIS Websites After Patch Tuesday", [
			"https://windowsreport.com/windows-11-24h2-and-25h2-updates-break-iis-websites-after-patch-tuesday/",
		]),
		headline("Microsoft Security Update Causes Active Directory Sync Failures on Windows Server 2025", [
			"https://cybersecuritynews.com/microsoft-update-active-directory-sync/",
		]),
		headline("A bizarre Windows 11 bug duplicates Task Manager instead of closing it", [
			"https://www.theverge.com/news/811233/microsoft-windows-11-task-manager-duplicate-bug",
		]),
		headline("Microsoft warns Windows 11 25H2, 24H2 October update triggers BitLocker recovery on PCs for businesses", [
			"https://www.windowslatest.com/2025/11/05/microsoft-warns-windows-11-25h2-24h2-october-update-triggers-bitlocker-recovery-on-pcs-for-businesses/",
		]),
		headline("False \"End of Support\" Warning Appears in Windows 10 Despite Extended Support", [
			"https://www.techpowerup.com/342612/false-end-of-support-warning-appears-in-windows-10-despite-extended-support",
		]),
		headline("Microsoft WSUS Remote Code Execution (CVE-2025-59287) Actively Exploited in the Wild", [
			"https://unit42.paloaltonetworks.com/microsoft-cve-2025-59287/",
		]),
		headline("Windows 11 KB5068861 won't install, File Explorer SMB search not working on network shares, and other issues", [
			"https://www.windowslatest.com/2025/11/17/windows-11-kb5068861-issues-update-wont-install-file-explorer-smb-search-not-working-on-network-shares-handheld-performance/",
		]),
		headline("Microsoft: Windows 11 bug crashes Explorer and Start Menu", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-11-24h2-bug-crashes-key-system-components/",
		]),
		headline("Microsoft Will Preload Windows 11 File Explorer to Fix Bad Performance", [
			"https://www.techpowerup.com/343149/microsoft-will-preload-windows-11-file-explorer-to-fix-bad-performance",
		]),
		headline("Microsoft: Windows updates make password login option invisible", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-updates-hide-password-icon-on-lock-screen/",
		]),
		headline("Microsoft Breaks File Explorer Dark Mode With Latest Non-Security Update", [
			"https://www.techpowerup.com/343551/microsoft-breaks-file-explorer-dark-mode-with-latest-non-security-update",
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-kb5070311-triggers-file-explorer-bright-white-flashes-in-dark-mode/"
		]),
		headline("Recent Windows 11 updates may break the Start menu, taskbar, and other components", [
			"https://winaero.com/recent-windows-11-updates-may-break-the-start-menu-taskbar-and-other-components/",
		]),
		headline("Microsoft confirms Windows 11's taskbar/explorer crashes and stuttering in games during launch, rolls out fixes", [
			"https://www.windowslatest.com/2025/12/03/microsoft-confirms-windows-11s-taskbar-explorer-crashes-and-stuttering-in-games-during-launch-rolls-out-fixes/",
		]),
		headline("Microsoft Confirms Windows Security Update Breaks VPN Connections", [
			"https://www.forbes.com/sites/daveywinder/2025/12/19/microsoft-confirms-windows-11-security-update-breaks-vpn-access/",
		]),
		headline("Microsoft Confirms Recent Windows 11 24H2/25H2 and Server 2025 Update Breaks RemoteApp Connections", [
			"https://cybersecuritynews.com/windows-11-and-server-2025-update-remoteapp/",
		]),
		headline("'Fail To Shut Down' - Microsoft Issues Windows Update Warning", [
			"https://www.forbes.com/sites/zakdoffman/2026/01/16/fail-to-shut-down-microsoft-issues-windows-update-warning/",
			"https://www.theregister.com/2026/01/19/windows_11_shutdown_bug/",
			"https://www.bleepingcomputer.com/news/security/microsoft-some-windows-pcs-fail-to-shut-down-after-january-update/"
		]),
		headline("Microsoft Windows 11 January 2026 Update Causes Outlook Crashes, Microsoft Issues Fix", [
			"https://www.thedailyjagran.com/technology/microsoft-windows-11-january-2026-update-causes-outlook-crashes-microsoft-issues-fix-10294936",
			"https://www.techpowerup.com/345341/windows-11-january-2026-update-triggers-black-screens-outlook-failures-and-emergency-patches"
		]),
		headline("Windows 11 KB5074109 breaks Azure Virtual Desktop", [
			"https://www.windowslatest.com/2026/01/17/windows-11-kb5074109-issues-black-screen-freezes-outlook-pop-breaks-azure-virtual-desktop-localizedresourcename-desktop-ini/",
		]),
		headline("January Windows security updates are breaking audio on PCs using external DACs", [
			"https://www.tomshardware.com/software/windows/january-windows-security-updates-are-breaking-audio-on-pcs-using-external-dacs",
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-january-windows-security-updates-break-audio-playback/"
		]),
		headline("Windows BitLocker bug triggers warnings on devices with TPMs", [
			"https://www.neowin.net/news/microsoft-windows-1110-tpm-pcs-with-bitlocker-encryption-facing-an-admin-related-bug/",
			"https://www.bleepingcomputer.com/news/microsoft/windows-bitlocker-bug-triggers-warnings-on-devices-with-tpms/",
			"https://www.windowslatest.com/2025/01/16/microsoft-confirms-windows-11-bitlocker-bug-causes-settings-are-managed-by-administrator-error/"
		]),
		headline("Windows security update triggers BitLocker recovery in some systems - bug mostly impacts Intel PCs with Modern Standby support", [
			"https://www.tomshardware.com/software/windows/windows-security-update-triggers-bitlocker-recovery-in-some-systems-bug-mostly-impacts-intel-pcs-with-modern-standby-support",
		]),
		headline("Microsoft Rushes Emergency Fix After Latest Windows Update Leaves Bluetooth, Audio, and Webcams Useless", [
			"https://www.headphonesty.com/2025/01/microsoft-emergency-fix-windows-january-update/",
			"https://www.techradar.com/computing/windows/im-absolutely-sick-of-microsofts-windows-11-24h2-update-as-its-now-causing-bluetooth-and-webcam-issues",
			"https://www.pcworld.com/article/2589290/windows-11-24h2-patch-breaks-audio-bluetooth-webcams-and-more.html",
			"https://itdaily.com/news/software/windows-update-headphones-webcams-broken/",
		]),
		headline("Microsoft: Classic Outlook bug prevents opening encrypted emails", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-classic-outlook-bug-prevents-opening-encrypted-emails/",
			"https://www.techradar.com/pro/security/use-classic-outlook-this-microsoft-bug-might-stop-you-from-opening-encrypted-emails"
		]),
		headline("Windows 11 KB5053598 issues, install fails, RDP disconnects, BSODs Windows 11 24H2", [
			"https://www.windowslatest.com/2025/03/13/windows-11-kb5053598-issues-install-fails-rdp-disconnects-bsods-windows-11-24h2/",
		]),
		headline("Microsoft says new Outlook can't open some Excel attachments", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-says-new-outlook-cant-open-some-excel-attachments/",
		]),
		headline("Windows 11 April Update Triggers BSOD, Breaks Windows Hello", [
			"https://www.techpowerup.com/335601/windows-11-april-update-triggers-bsod-breaks-windows-hello",
			"https://www.windowslatest.com/2025/04/14/windows-11-kb5055523-install-fails-windows-hello-not-working-april-2025-update-issues/"
		]),
		headline("Microsoft: Windows bug blocks Microsoft 365 desktop app installs", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-bug-blocks-microsoft-365-desktop-app-installs/",
		]),
		headline("Play Call of Duty: Black Ops 6? Windows 11's latest patch reportedly has a game-breaking bug", [
			"https://www.tweaktown.com/news/103642/play-call-of-duty-black-ops-6-windows-11s-latest-patch-reportedly-has-game-breaking-bug/index.html",
		]),
		headline("Windows 11 KB5050094 has major issues, including spinning cursor on Windows 11 24H2", [
			"https://www.pcworld.com/article/2600499/more-windows-11-patch-woes-this-time-with-mouse-pointers-acting-up.html",
			"https://www.windowslatest.com/2025/02/05/windows-11-kb5050094-has-major-issues-including-spinning-cursor-on-windows-11-24h2/"
		]),
		headline("Windows 11 update breaks Adobe Premiere Pro's ability to move or drag clips on the timeline", [
			"https://www.windowslatest.com/2025/02/07/windows-11-update-breaks-adobe-premiere-pros-ability-to-move-or-drag-clips-on-the-timeline/"
		]),
		headline("Microsoft pulls Windows 11 KB5039302 update causing reboot loops", [
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-pulls-june-windows-11-kb5039302-update-causing-repeated-restarts/",
			"https://www.windowslatest.com/2024/06/27/windows-11-kb5039302-breaks-some-pcs-microsoft-pulls-the-update/"
		]),
		headline("Windows 11 KB5052093 install fails, gets pulled, then re-released", [
			"https://www.windowslatest.com/2025/03/02/windows-11-kb5052093-install-fails-gets-pulled-then-re-released/",
		]),
		headline("Microsoft: Windows 10 KB5068781 ESU update may fail with 0x800f0922 errors", [
			"https://www.forbes.com/sites/daveywinder/2025/11/16/bad-news-for-microsoft-windows-10-users---another-security-update-fail/",
			"https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-10-kb5068781-esu-update-may-fail-with-0x800f0922-errors/"
		]),
		headline("Windows 11 25H2 Build 26200.7623 breaks sleep mode (S3), Citrix Director, and other problems (January 2026 Update)", [
			"https://www.techradar.com/computing/windows/windows-11-update-is-breaking-sleep-mode-on-some-pcs-but-theres-one-trick-that-might-help",
			"https://www.windowslatest.com/2026/01/21/2026s-first-windows-11-update-is-causing-more-problems-now-as-microsoft-enters-damage-control-mode/"
		]),
		headline("Microsoft says uninstall Windows 11 KB5074109 to fix Outlook POP, PST hang, as 2026's first update causes havoc", [
			"https://www.windowslatest.com/2026/01/22/microsoft-says-uninstall-windows-11-kb5074109-to-fix-outlook-pop-pst-hang-as-2026s-first-update-causes-havoc/",
		]),
		headline("Windows 11 24H2 September Patch Breaks HDCP/DRM Video Playback", [
			"https://www.techpowerup.com/341206/windows-11-24h2-september-patch-breaks-hdcp-drm-video-playback",
			"https://www.neowin.net/news/microsoft-confirms-windows-11-kb5065426-kb5064081-break-drmhdcp-video-playback/"
		]),
		headline("Nvidia confirms Windows 11 25H2, 24H2 update is hurting gaming performance, releases a new driver", [
			"https://www.windowslatest.com/2025/11/20/nvidia-confirms-windows-11-25h2-24h2-update-is-hurting-gaming-performance-releases-a-new-driver/",
		]),
		headline("'We Apologize' - Microsoft Confirms Windows Update Mistake", [
			"https://www.forbes.com/sites/zakdoffman/2025/07/20/we-apologize-microsoft-confirms-windows-update-mistake/",
			"https://www.windowslatest.com/2025/07/16/windows-11-july-2025-update-issues-confirmed-microsoft-says-it-falsely-claimed-fixes/"
		]),
		headline("Microsoft explains how a key Windows feature can lead to theft of your entire encrypted data", [
			"https://www.neowin.net/news/microsoft-explains-how-a-key-windows-feature-can-lead-to-theft-of-your-entire-encrypted-data/",
		]),
		headline("Microsoft admits it accidentally crashed apps like Notepad, Paint, Snipping Tool on Windows 11, rolls out a fix", [
			"https://www.windowslatest.com/2026/01/24/microsoft-admits-it-accidentially-crashed-apps-like-notepad-paint-snipping-tool-on-windows-11-rolls-out-a-fix/",
			"https://www.neowin.net/news/notepad-snipping-tool-other-apps-broken-by-new-bug-in-windows-11/",
			"https://www.techradar.com/computing/windows/windows-11s-2026-goes-from-bad-to-worse-as-two-new-bugs-cause-havoc-crashing-apps-but-there-are-possible-fixes"
		]),
		headline("Microsoft admits it broke “Reset this PC” in Windows 11 23H2 KB5063875, Windows 10 KB5063709", [
			"https://www.windowslatest.com/2025/08/19/microsoft-admits-it-broke-reset-this-pc-in-windows-11-23h2-kb5063875-windows-10-kb5063709/",
			"https://tech.yahoo.com/computing/articles/microsoft-admits-broke-vital-pc-113147097.html"
		]),
		headline("Microsoft acknowledges Windows issue: apps crash when saving to OneDrive or Dropbox", [
			"https://itdaily.com/news/software/microsoft-apps-crash-saving-onedrive-dropbox/",
			"https://tech.yahoo.com/computing/articles/saving-files-currently-broken-windows-170929966.html"
		]),
		headline("Microsoft confirms Windows 11 24H2 stability issues, affecting games, tests performance fixes", [
			"https://www.windowslatest.com/2025/07/28/microsoft-confirms-windows-11-24h2-stability-issues-affecting-games-tests-performance-fixes/",
		]),
		headline("Troubled Windows 11 January Patch Now Preventing Some PCs From Booting Up", [
			"https://www.pcmag.com/news/windows-11-january-patch-now-stops-some-pcs-from-booting-altogether",
		]),
		headline("Microsoft accidentally wipes out Copilot in latest Windows 11 update", [
			"https://www.pcmag.com/news/oops-update-accidentally-removes-copilot-from-windows",
			"https://www.theverge.com/news/631053/microsoft-windows-11-update-uninstall-copilot"
		]),
		headline("Microsoft finally admits almost all major Windows 11 core features are broken", [
			"https://www.neowin.net/news/microsoft-finally-admits-almost-all-major-windows-11-core-features-are-broken/",
		]),
		headline("Microsoft confirms Windows 11 bug crippling PCs and making drive C inaccessible", [
			"https://www.neowin.net/news/microsoft-confirms-windows-11-bug-crippling-pcs-and-making-drive-c-inaccessible/",
		]),
		headline("Update KB5079473 breaks sign-ins on Teams and OneDrive", [
			"https://www.bleepingcomputer.com/news/microsoft/new-kb5085516-emergency-update-fixes-microsoft-account-sign-in/",
		]),
	];
</script>

<div id="main">
	<div id="header">
		<img src="./images/meme.webp" alt="meme">
	</div>
	<div id="contents">
		{#each headlines as headline}
			<Headline {...headline}/>
		{/each}
	</div>
</div>

<style>
	#contents {
		width: min(max(800px, 55vw), 100vw);
		margin: auto;
	}

	#header {
		text-align: center;
		background-color: rgb(0, 0, 0);
	}

	#header img {
		height: 50%;
	}
</style>
