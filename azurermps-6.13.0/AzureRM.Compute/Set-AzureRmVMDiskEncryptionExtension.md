---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3eb2c1c175f52f980ecd451bb7a9474984543f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449235"
---
# <span data-ttu-id="947e2-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="947e2-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="947e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="947e2-102">SYNOPSIS</span></span>
<span data-ttu-id="947e2-103">在 Azure 中的執行 IaaS 虛擬機器上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="947e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="947e2-104">SYNTAX</span></span>

### <span data-ttu-id="947e2-105">SinglePassParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="947e2-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e2-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e2-106">AADClientSecretParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e2-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e2-107">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="947e2-108">DESCRIPTION</span></span>
<span data-ttu-id="947e2-109">**AzureRmVMDiskEncryptionExtension** Cmdlet 可在執行中的基礎結構上加密，成為 Azure 中的服務 (IaaS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="947e2-109">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="947e2-110">這個 Cmdlet 可在虛擬機器上安裝磁片加密延伸來啟用加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="947e2-111">如果未指定 *Name* 參數，則會安裝針對執行 Windows 作業系統或 AzureDiskEncryptionForLinux for Linux 虛擬機器的虛擬機器使用預設名稱 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="947e2-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="947e2-112">這個 Cmdlet 需要使用者確認，因為啟用加密的其中一個步驟需要重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="947e2-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="947e2-113">建議您在執行此 Cmdlet 前，先將工作儲存在虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="947e2-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="947e2-114">示例</span><span class="sxs-lookup"><span data-stu-id="947e2-114">EXAMPLES</span></span>

### <span data-ttu-id="947e2-115">範例1：啟用加密</span><span class="sxs-lookup"><span data-stu-id="947e2-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="947e2-116">這個範例示範如何啟用加密，而不指定廣告認證。</span><span class="sxs-lookup"><span data-stu-id="947e2-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="947e2-117">範例2：使用流水線輸入啟用加密</span><span class="sxs-lookup"><span data-stu-id="947e2-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzureRmVmDiskEncryptionExtension
```

<span data-ttu-id="947e2-118">這個範例示範如何使用流水線輸入傳送參數，以在不指定廣告認證的情況下啟用加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="947e2-119">範例3：使用 Azure AD 用戶端識別碼和用戶端密碼啟用加密</span><span class="sxs-lookup"><span data-stu-id="947e2-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="947e2-120">這個範例啟用使用 Azure AD 用戶端識別碼和用戶端密碼的加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="947e2-121">範例4：使用 Azure AD 用戶端識別碼和用戶端認證指紋啟用加密</span><span class="sxs-lookup"><span data-stu-id="947e2-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    {
        "data" : "$filecontentencoded",
        "dataType" : "pfx",
        "password" : "$CertPassword"
    }
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="947e2-122">這個範例啟用使用 Azure AD 用戶端識別碼與用戶端認證指紋的加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="947e2-123">範例5：使用金鑰加密金鑰啟用使用 Azure AD 用戶端識別碼、用戶端密碼及自動換行磁片加密金鑰的加密功能</span><span class="sxs-lookup"><span data-stu-id="947e2-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="947e2-124">這個範例使用金鑰加密金鑰來啟用使用 Azure AD 用戶端識別碼、用戶端密碼及自動換行的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="947e2-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="947e2-125">範例6：使用 Azure AD 用戶端識別碼、用戶端憑證指紋，以及使用金鑰加密金鑰來包裝磁片 encryption.encryptionkey 來啟用加密</span><span class="sxs-lookup"><span data-stu-id="947e2-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    {
        "data" : "$filecontentencoded",
        "dataType" : "pfx",
        "password" : "$CertPassword"
    }
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="947e2-126">這個範例使用金鑰加密金鑰來啟用使用 Azure AD 用戶端識別碼、用戶端憑證指紋及自動換行磁片加密金鑰的加密。</span><span class="sxs-lookup"><span data-stu-id="947e2-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="947e2-127">參數</span><span class="sxs-lookup"><span data-stu-id="947e2-127">PARAMETERS</span></span>

### <span data-ttu-id="947e2-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="947e2-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="947e2-129">指定 AzureActive 目錄的指紋， (的 Azure AD) 應用程式用戶端憑證，且具有將機密寫入 **KeyVault** 的許可權。</span><span class="sxs-lookup"><span data-stu-id="947e2-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="947e2-130">就必要而言，Azure AD 用戶端憑證必須先部署到虛擬機器的 [本機電腦] `my` 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="947e2-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="947e2-131">Add-AzureRmVMSecret Cmdlet 可以用來將憑證部署到 Azure 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="947e2-131">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="947e2-132">如需詳細資訊，請參閱 **Add AzureRmVMSecret** Cmdlet 說明。</span><span class="sxs-lookup"><span data-stu-id="947e2-132">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="947e2-133">證書必須先部署到 [虛擬機器本機電腦] 的 [我的證書] 存放區。</span><span class="sxs-lookup"><span data-stu-id="947e2-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="947e2-134">-AadClientID</span></span>
<span data-ttu-id="947e2-135">指定擁有將機密寫入 **KeyVault** 之許可權的 Azure AD 應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="947e2-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="947e2-136">-AadClientSecret</span></span>
<span data-ttu-id="947e2-137">指定擁有將機密寫入 **KeyVault** 之許可權的 Azure AD 應用程式的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="947e2-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947e2-138">-DefaultProfile</span></span>
<span data-ttu-id="947e2-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="947e2-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="947e2-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="947e2-141">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="947e2-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="947e2-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="947e2-143">指定要上傳虛擬機器加密金鑰之 **KeyVault** 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="947e2-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="947e2-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="947e2-145">指定要將虛擬機器加密金鑰上傳到哪個 **KeyVault** URL。</span><span class="sxs-lookup"><span data-stu-id="947e2-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="947e2-146">-EncryptFormatAll</span></span>
<span data-ttu-id="947e2-147">Encrypt-Format 尚未加密的所有資料磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="947e2-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="947e2-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="947e2-149">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="947e2-149">The extension publisher name.</span></span> <span data-ttu-id="947e2-150">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="947e2-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="947e2-151">-ExtensionType</span></span>
<span data-ttu-id="947e2-152">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="947e2-152">The extension type.</span></span> <span data-ttu-id="947e2-153">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="947e2-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-154">-Force</span><span class="sxs-lookup"><span data-stu-id="947e2-154">-Force</span></span>
<span data-ttu-id="947e2-155">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="947e2-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="947e2-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="947e2-157">指定用來包裝及解出虛擬機器金鑰加密金鑰的演算法。</span><span class="sxs-lookup"><span data-stu-id="947e2-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="947e2-158">預設值為 RSA-OAEP。</span><span class="sxs-lookup"><span data-stu-id="947e2-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="947e2-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="947e2-160">指定金鑰加密金鑰的 URL，該金鑰是用來包裝及解包虛擬機器加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="947e2-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="947e2-161">這必須是完整的版本控制 URL。</span><span class="sxs-lookup"><span data-stu-id="947e2-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="947e2-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="947e2-163">指定包含金鑰加密金鑰的 **KeyVault** 的資源識別碼，該金鑰是用來包裝及解包虛擬機器加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="947e2-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="947e2-164">這必須是完整版本的 URL。</span><span class="sxs-lookup"><span data-stu-id="947e2-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="947e2-165">-Name</span></span>
<span data-ttu-id="947e2-166">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="947e2-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="947e2-167">針對執行 Windows 作業系統的虛擬機器或 Linux 虛擬機器的 AzureDiskEncryptionForLinux，預設值是 AzureDiskEncryption。</span><span class="sxs-lookup"><span data-stu-id="947e2-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-168">-密碼</span><span class="sxs-lookup"><span data-stu-id="947e2-168">-Passphrase</span></span>
<span data-ttu-id="947e2-169">指定僅用於加密 Linux 虛擬機器的密碼。</span><span class="sxs-lookup"><span data-stu-id="947e2-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="947e2-170">此參數不適用於執行 Windows 作業系統的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="947e2-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947e2-171">-ResourceGroupName</span></span>
<span data-ttu-id="947e2-172">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="947e2-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="947e2-173">-SequenceVersion</span></span>
<span data-ttu-id="947e2-174">指定虛擬機器加密作業的序列值。</span><span class="sxs-lookup"><span data-stu-id="947e2-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="947e2-175">每個在同一個虛擬機器上執行的加密作業都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="947e2-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="947e2-176">Get-AzureRmVMExtension Cmdlet 可用來檢索以前使用的序列值。</span><span class="sxs-lookup"><span data-stu-id="947e2-176">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="947e2-177">-SkipVmBackup</span></span>
<span data-ttu-id="947e2-178">略過 Linux Vm 的備份建立</span><span class="sxs-lookup"><span data-stu-id="947e2-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="947e2-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="947e2-180">指定加密延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="947e2-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="947e2-181">-VMName</span></span>
<span data-ttu-id="947e2-182">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="947e2-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-183">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="947e2-183">-VolumeType</span></span>
<span data-ttu-id="947e2-184">指定要執行加密操作的虛擬機器體積類型。</span><span class="sxs-lookup"><span data-stu-id="947e2-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="947e2-185">執行 Windows 作業系統的虛擬機器允許的值如下： [全部]、[作業系統] 和 [資料]。</span><span class="sxs-lookup"><span data-stu-id="947e2-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="947e2-186">Linux 虛擬機器的允許值如下所示： [全部]、[作業系統] 和 [Linux] 發佈所支援的資料。</span><span class="sxs-lookup"><span data-stu-id="947e2-186">The allowed values for Linux virtual machines are as follows: All, OS, and Data when supported by the Linux distribution.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-187">-確認</span><span class="sxs-lookup"><span data-stu-id="947e2-187">-Confirm</span></span>
<span data-ttu-id="947e2-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="947e2-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947e2-189">-WhatIf</span></span>
<span data-ttu-id="947e2-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="947e2-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="947e2-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="947e2-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947e2-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947e2-192">CommonParameters</span></span>
<span data-ttu-id="947e2-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="947e2-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947e2-194">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="947e2-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947e2-195">輸入</span><span class="sxs-lookup"><span data-stu-id="947e2-195">INPUTS</span></span>

### <span data-ttu-id="947e2-196">System.object</span><span class="sxs-lookup"><span data-stu-id="947e2-196">System.String</span></span>

### <span data-ttu-id="947e2-197">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="947e2-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="947e2-198">輸出</span><span class="sxs-lookup"><span data-stu-id="947e2-198">OUTPUTS</span></span>

### <span data-ttu-id="947e2-199">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="947e2-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="947e2-200">筆記</span><span class="sxs-lookup"><span data-stu-id="947e2-200">NOTES</span></span>

## <span data-ttu-id="947e2-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="947e2-201">RELATED LINKS</span></span>

[<span data-ttu-id="947e2-202">附加 AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="947e2-202">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="947e2-203">AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="947e2-203">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="947e2-204">移除-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="947e2-204">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

