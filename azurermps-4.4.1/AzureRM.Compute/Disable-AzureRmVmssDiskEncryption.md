---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456847"
---
# <span data-ttu-id="e3d0f-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e3d0f-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="e3d0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d0f-103">在 VM 比例集上停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3d0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3d0f-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d0f-106">在 VM 比例集上停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="e3d0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d0f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3d0f-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e3d0f-109">在屬於名為 Group001 之資源群組的 VM 規模集上，停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e3d0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="e3d0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d0f-111">-DefaultProfile</span></span>
<span data-ttu-id="e3d0f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d0f-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e3d0f-113">-ExtensionName</span></span>
<span data-ttu-id="e3d0f-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-114">The extension name.</span></span>
<span data-ttu-id="e3d0f-115">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d0f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e3d0f-116">-Force</span></span>
<span data-ttu-id="e3d0f-117">強制從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="e3d0f-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="e3d0f-118">-ForceUpdate</span></span>
<span data-ttu-id="e3d0f-119">產生 [強制更新] 的標記。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-119">Generate a tag for force update.</span></span>  <span data-ttu-id="e3d0f-120">這應該是為了在同一個 VM 上執行重複的加密作業。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="e3d0f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d0f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3d0f-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-122">The resource group name.</span></span>

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

### <span data-ttu-id="e3d0f-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e3d0f-123">-VMScaleSetName</span></span>
<span data-ttu-id="e3d0f-124">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="e3d0f-125">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="e3d0f-125">-VolumeType</span></span>
<span data-ttu-id="e3d0f-126">要執行加密作業 (OS 或資料) 的音量類型</span><span class="sxs-lookup"><span data-stu-id="e3d0f-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="e3d0f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e3d0f-127">-Confirm</span></span>
<span data-ttu-id="e3d0f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d0f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d0f-129">-WhatIf</span></span>
<span data-ttu-id="e3d0f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d0f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d0f-132">CommonParameters</span></span>
<span data-ttu-id="e3d0f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d0f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d0f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e3d0f-135">INPUTS</span></span>

### <span data-ttu-id="e3d0f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e3d0f-136">System.String</span></span>

## <span data-ttu-id="e3d0f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e3d0f-137">OUTPUTS</span></span>

### <span data-ttu-id="e3d0f-138">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e3d0f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e3d0f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e3d0f-139">NOTES</span></span>

## <span data-ttu-id="e3d0f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3d0f-140">RELATED LINKS</span></span>

