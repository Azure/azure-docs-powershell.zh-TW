---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 90dd1854db30ff20cd864dc04b3235cc4e34c4d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613135"
---
# <span data-ttu-id="d4e8f-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d4e8f-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="d4e8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e8f-103">在 VM 比例集上啟用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="d4e8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4e8f-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4e8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e8f-106">**AzVmssDiskEncryptionExtension** Cmdlet 可在 VM 規模集中進行加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="d4e8f-107">這個 Cmdlet 可在 VM 規模集上安裝磁片加密延伸來啟用加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="d4e8f-108">針對 Linux 虛擬電腦， *VolumeType* 參數必須存在，而且必須設定為 "Data"</span><span class="sxs-lookup"><span data-stu-id="d4e8f-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="d4e8f-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e8f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d4e8f-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="d4e8f-111">這個命令會在 VM 規模集中的所有 Windows Vm 磁片上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="d4e8f-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d4e8f-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="d4e8f-113">這個命令會在 VM 規模集中的所有 Linux Vm 的資料磁片上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="d4e8f-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4e8f-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e8f-115">-DefaultProfile</span></span>
<span data-ttu-id="d4e8f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d4e8f-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d4e8f-118">停用次要版本的自動升級</span><span class="sxs-lookup"><span data-stu-id="d4e8f-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d4e8f-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="d4e8f-120">要放置產生的加密金鑰之 KeyVault 的 ResourceID</span><span class="sxs-lookup"><span data-stu-id="d4e8f-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="d4e8f-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="d4e8f-122">要放置產生的加密金鑰之 KeyVault 的 URL</span><span class="sxs-lookup"><span data-stu-id="d4e8f-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d4e8f-123">-ExtensionName</span></span>
<span data-ttu-id="d4e8f-124">副檔名。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-124">The extension name.</span></span>
<span data-ttu-id="d4e8f-125">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="d4e8f-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="d4e8f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d4e8f-126">-Force</span></span>
<span data-ttu-id="d4e8f-127">在虛擬機器規模集上強制啟用加密。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d4e8f-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="d4e8f-128">-ForceUpdate</span></span>
<span data-ttu-id="d4e8f-129">產生 [強制更新] 的標記。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-129">Generate a tag for force update.</span></span>  <span data-ttu-id="d4e8f-130">這應該是為了在同一個 VM 上執行重複的加密作業。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d4e8f-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="d4e8f-132">用來加密大量加密金鑰的 KeyEncryption 演算法</span><span class="sxs-lookup"><span data-stu-id="d4e8f-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="d4e8f-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="d4e8f-134">用來加密磁片加密金鑰之 KeyEncryptionKey 的版本控制 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="d4e8f-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="d4e8f-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d4e8f-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="d4e8f-136">包含用來加密磁片加密金鑰之 KeyEncryptionKey 的 KeyVault ResourceID</span><span class="sxs-lookup"><span data-stu-id="d4e8f-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="d4e8f-137">-密碼</span><span class="sxs-lookup"><span data-stu-id="d4e8f-137">-Passphrase</span></span>
<span data-ttu-id="d4e8f-138">[參數] 中指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="d4e8f-139">這個參數只適用于 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="d4e8f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e8f-140">-ResourceGroupName</span></span>
<span data-ttu-id="d4e8f-141">VM 比例集所屬的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d4e8f-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="d4e8f-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d4e8f-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="d4e8f-143">類型處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4e8f-144">-VMScaleSetName</span></span>
<span data-ttu-id="d4e8f-145">虛擬機器規模集的名稱</span><span class="sxs-lookup"><span data-stu-id="d4e8f-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="d4e8f-146">-VolumeType</span></span>
<span data-ttu-id="d4e8f-147">指定要執行加密作業的虛擬機器體積類型：作業系統、資料或全部。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="d4e8f-148">Linux： **VolumeType** 參數必須存在，且必須設定為 Data。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="d4e8f-149">Windows： **VolumeType** 參數（如果有的話）必須設定為 ALL 或 OS。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="d4e8f-150">如果省略 **VolumeType** 參數，則預設為 "All"。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-151">-確認</span><span class="sxs-lookup"><span data-stu-id="d4e8f-151">-Confirm</span></span>
<span data-ttu-id="d4e8f-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e8f-153">-WhatIf</span></span>
<span data-ttu-id="d4e8f-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e8f-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e8f-156">CommonParameters</span></span>
<span data-ttu-id="d4e8f-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e8f-158">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4e8f-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e8f-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d4e8f-159">INPUTS</span></span>

### <span data-ttu-id="d4e8f-160">System.object</span><span class="sxs-lookup"><span data-stu-id="d4e8f-160">System.String</span></span>

### <span data-ttu-id="d4e8f-161">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d4e8f-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4e8f-162">輸出</span><span class="sxs-lookup"><span data-stu-id="d4e8f-162">OUTPUTS</span></span>

### <span data-ttu-id="d4e8f-163">PSVirtualMachineScaleSetExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d4e8f-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="d4e8f-164">筆記</span><span class="sxs-lookup"><span data-stu-id="d4e8f-164">NOTES</span></span>

## <span data-ttu-id="d4e8f-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4e8f-165">RELATED LINKS</span></span>
