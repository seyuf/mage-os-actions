# magento-create-project

This is a magento installer using github action.
**This version of the installer is not using official adobe src but the open source [Mage os](https://mage-os.org/) version.**

```
    - name: 'install fresh magento repo'
      #if: ${{false}}
      uses: MAD-I-T/magento-actions@v3.20
      with:
        process: 'install-mage-os'
        magento_version: 2.4.6
```

The benefit of using Mage os is that no authentication is required. As you're not using the magento composer repo.
Nonetheless, if you're looking for the adobe version  [check here](https://github.com/seyuf/magento-create-project) file.
Also Mage os as of the time of the writing only supports magento >= 2.4.x versions


Reminder : 
Make sure you use ***actions/checkout@v2*** before the action as in the sample main.yml file.
Because a habit to follow https://12factor.net composer credentials are set through github secret option.

***Warning :*** Magento 2.3.3-p1 to 2.3.7-p2 and 2.4.0 to 2.4.3-p1 are compromised ([see bulletin](https://support.magento.com/hc/en-us/articles/4426353041293-Security-updates-available-for-Adobe-Commerce-APSB22-12-)). If you choose to install theses versions please apply the patch ([instructions here](https://gist.github.com/seyuf/0cd908a897f9b544d20de97dd2dcc25a))


<div align="center">
  <a href="https://www.youtube.com/watch?v=cqI79AKN7Gk"><img src="https://user-images.githubusercontent.com/3765910/154555377-2ab4d165-9bbb-42a4-b6cf-22586156477d.png" alt="install magento 2 using github actions"></a>
  <span>Install process in video</scan>
</div>


Ask questions here https://forum.madit.fr/t/install-magento-using-github-actions/13
