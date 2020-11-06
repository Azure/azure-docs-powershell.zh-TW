---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449402"
---
# <span data-ttu-id="bb66e-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bb66e-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="bb66e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb66e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb66e-103">停用 IaaS 虛擬機器上的加密。</span><span class="sxs-lookup"><span data-stu-id="bb66e-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb66e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb66e-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb66e-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb66e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb66e-106">**Disable AzureRmVMDiskEncryption** Cmdlet 會將基礎結構上的加密停成服務 (IaaS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bb66e-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="bb66e-107">這個 Cmdlet 只在 Windows 虛擬電腦（而不是 Linux 虛擬機器）上受到支援。</span><span class="sxs-lookup"><span data-stu-id="bb66e-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="bb66e-108">這個 Cmdlet 會在虛擬機器上安裝擴充功能，以停用加密。</span><span class="sxs-lookup"><span data-stu-id="bb66e-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="bb66e-109">如果未指定 *Name* 參數，則會建立預設名稱為「AzureDiskEncryption For Windows vm」的副檔名。</span><span class="sxs-lookup"><span data-stu-id="bb66e-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="bb66e-110">注意：此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bb66e-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="bb66e-111">示例</span><span class="sxs-lookup"><span data-stu-id="bb66e-111">EXAMPLES</span></span>

### <span data-ttu-id="bb66e-112">範例1：針對 Windows 虛擬機器上的所有磁片停用加密</span><span class="sxs-lookup"><span data-stu-id="bb66e-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="bb66e-113">這個命令會針對屬於名為 Group001 之資源群組的名稱為 VM002 的虛擬機器，停用對 all 類型的磁片加密。</span><span class="sxs-lookup"><span data-stu-id="bb66e-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="bb66e-114">由於未指定 *VolumeType* 參數，因此 Cmdlet 會將值設定為 All。</span><span class="sxs-lookup"><span data-stu-id="bb66e-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="bb66e-115">範例2：停用 Windows 虛擬機器上的資料量加密</span><span class="sxs-lookup"><span data-stu-id="bb66e-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="bb66e-116">這個命令會針對名為「Group002」資源群組的名為 VM004 的虛擬機器，停用針對類型資料的加密量。</span><span class="sxs-lookup"><span data-stu-id="bb66e-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="bb66e-117">參數</span><span class="sxs-lookup"><span data-stu-id="bb66e-117">PARAMETERS</span></span>

### <span data-ttu-id="bb66e-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bb66e-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bb66e-119">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="bb66e-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb66e-120">-Force</span></span>
<span data-ttu-id="bb66e-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bb66e-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb66e-122">-Name</span></span>
<span data-ttu-id="bb66e-123">Specifes 代表副檔名的 Azure 資源管理器 (ARM) 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66e-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="bb66e-124">如果未指定此參數，此 Cmdlet 預設為「Windows Vm 的 AzureDiskEncryption」。</span><span class="sxs-lookup"><span data-stu-id="bb66e-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb66e-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb66e-126">指定虛擬機器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66e-126">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bb66e-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="bb66e-128">指定加密延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="bb66e-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="bb66e-129">如果您沒有指定此參數的值，就會使用最新版本的延伸。</span><span class="sxs-lookup"><span data-stu-id="bb66e-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="bb66e-130">-VMName</span></span>
<span data-ttu-id="bb66e-131">指定此 Cmdlet 停用加密的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66e-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-132">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="bb66e-132">-VolumeType</span></span>
<span data-ttu-id="bb66e-133">指定要執行加密操作的虛擬機器體積類型。</span><span class="sxs-lookup"><span data-stu-id="bb66e-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="bb66e-134">針對 Windows 虛擬機器，有效值為：</span><span class="sxs-lookup"><span data-stu-id="bb66e-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="bb66e-135">同時</span><span class="sxs-lookup"><span data-stu-id="bb66e-135">All</span></span>
- <span data-ttu-id="bb66e-136">OS</span><span class="sxs-lookup"><span data-stu-id="bb66e-136">OS</span></span>
- <span data-ttu-id="bb66e-137">資料.</span><span class="sxs-lookup"><span data-stu-id="bb66e-137">Data.</span></span>
<span data-ttu-id="bb66e-138">如果您沒有指定此參數的值，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="bb66e-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="bb66e-139">Linux 目前不支援 [停用加密]。</span><span class="sxs-lookup"><span data-stu-id="bb66e-139">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-140">-確認</span><span class="sxs-lookup"><span data-stu-id="bb66e-140">-Confirm</span></span>
<span data-ttu-id="bb66e-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb66e-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb66e-142">-WhatIf</span></span>
<span data-ttu-id="bb66e-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb66e-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bb66e-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb66e-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb66e-145">CommonParameters</span></span>
<span data-ttu-id="bb66e-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb66e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb66e-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb66e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb66e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="bb66e-148">INPUTS</span></span>

### <span data-ttu-id="bb66e-149">所有</span><span class="sxs-lookup"><span data-stu-id="bb66e-149">None</span></span>
<span data-ttu-id="bb66e-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bb66e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb66e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="bb66e-151">OUTPUTS</span></span>

### <span data-ttu-id="bb66e-152">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bb66e-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bb66e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="bb66e-153">NOTES</span></span>

## <span data-ttu-id="bb66e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb66e-154">RELATED LINKS</span></span>

[<span data-ttu-id="bb66e-155">AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="bb66e-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="bb66e-156">移除-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bb66e-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="bb66e-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bb66e-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


