# Chocolatey
<p>Document the software automation process with Chocolatey.</p>

<h2>Installation</h2>
<p>Open the Windows PowerShell as administrator and then install Chocolatey using the following commands:</p>

<code>
Set-ExecutionPolicy Unrestricted -Force -Scope Process;
  
iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex 
</code>

<h2>Upgrade</h2>
<p>To upgrading Chocolatey to the latest stable release you can use the following command:</p>

<code>
choco upgrade chocolatey
</code>

<h2>Run install script</h2>
<p>To run the <a href="/install-script.ps1">install-script.ps1</a> launch the Windows PowerShell, navigate to the directory where the script lives and execute the script:</p>

<code>
.\install-script.ps1 
</code>

<h2>Create Desktop Shortcuts</h2>
<p>If desktop shortcuts should be automatically created the helper module <a href="https://chocolatey.org/docs/helpers-install-chocolatey-shortcut">Install-ChocolateyShortcut</a> could be used in a Windows PowerShell script followed by the command(s) to create the shortcut(s):</p>

<code>
Import-Module "$env:ChocolateyInstall\helpers\chocolateyInstaller.psm1" -Force

Install-ChocolateyShortcut -ShortcutFilePath "C:\Users\max\Desktop\FileZilla.lnk" -TargetPath "C:\Program Files\FileZilla FTP Client\filezilla.exe"  
</code>

<h2>Frequent Commands</h2>

<ul>
<li><code>choco list -l</code></li>
<li><code>choco install &lt;pkg&gt;</code></li>
<li><code>choco uninstall &lt;pkg&gt;</code></li>
<li><code>choco upgrade &lt;pkg&gt; -y</code></li>
<li><code>choco upgrade all -y</code></li>
<li><code>choco feature list</code></li>
<li><code>choco feature disable -n=bob</code></li>
<li><code>choco feature enable -n=bob</code></li>
</ul>

<h2>Links</h2>
<ul>
<li><a href="https://chocolatey.org/" rel="nofollow">Chocolatey</a></li>
<li><a href="https://chocolatey.org/packages">Chocolatey Packages</a></li>
</ul>


