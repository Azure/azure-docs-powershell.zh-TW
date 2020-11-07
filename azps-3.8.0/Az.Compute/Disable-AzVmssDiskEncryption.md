---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 14f29bb7097f584c89fa1bf92bf816cf4ca3d511
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966098"
---
# <span data-ttu-id="bdfc2-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bdfc2-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="bdfc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfc2-103">在 VM 比例集上停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="bdfc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdfc2-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdfc2-105">說明</span><span class="sxs-lookup"><span data-stu-id="bdfc2-105">DESCRIPTION</span></span>
<span data-ttu-id="bdfc2-106">在 VM 比例集上停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="bdfc2-107">示例</span><span class="sxs-lookup"><span data-stu-id="bdfc2-107">EXAMPLES</span></span>

### <span data-ttu-id="bdfc2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bdfc2-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="bdfc2-109">在屬於名為 Group001 之資源群組的 VM 規模集上，停用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="bdfc2-110">參數</span><span class="sxs-lookup"><span data-stu-id="bdfc2-110">PARAMETERS</span></span>

### <span data-ttu-id="bdfc2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdfc2-111">-AsJob</span></span>
<span data-ttu-id="bdfc2-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bdfc2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdfc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfc2-113">-DefaultProfile</span></span>
<span data-ttu-id="bdfc2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdfc2-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="bdfc2-115">-ExtensionName</span></span>
<span data-ttu-id="bdfc2-116">副檔名。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-116">The extension name.</span></span>
<span data-ttu-id="bdfc2-117">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="bdfc2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bdfc2-118">-Force</span></span>
<span data-ttu-id="bdfc2-119">強制從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="bdfc2-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="bdfc2-120">-ForceUpdate</span></span>
<span data-ttu-id="bdfc2-121">產生 [強制更新] 的標記。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-121">Generate a tag for force update.</span></span>  <span data-ttu-id="bdfc2-122">這應該是為了在同一個 VM 上執行重複的加密作業。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="bdfc2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdfc2-123">-ResourceGroupName</span></span>
<span data-ttu-id="bdfc2-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-124">The resource group name.</span></span>

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

### <span data-ttu-id="bdfc2-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bdfc2-125">-VMScaleSetName</span></span>
<span data-ttu-id="bdfc2-126">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="bdfc2-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="bdfc2-127">-VolumeType</span></span>
<span data-ttu-id="bdfc2-128">要執行加密作業 (OS 或資料) 的音量類型</span><span class="sxs-lookup"><span data-stu-id="bdfc2-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="bdfc2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="bdfc2-129">-Confirm</span></span>
<span data-ttu-id="bdfc2-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdfc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdfc2-131">-WhatIf</span></span>
<span data-ttu-id="bdfc2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdfc2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdfc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfc2-134">CommonParameters</span></span>
<span data-ttu-id="bdfc2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfc2-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfc2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bdfc2-137">INPUTS</span></span>

### <span data-ttu-id="bdfc2-138">System.object</span><span class="sxs-lookup"><span data-stu-id="bdfc2-138">System.String</span></span>

### <span data-ttu-id="bdfc2-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="bdfc2-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bdfc2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bdfc2-140">OUTPUTS</span></span>

### <span data-ttu-id="bdfc2-141">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="bdfc2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bdfc2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bdfc2-142">NOTES</span></span>

## <span data-ttu-id="bdfc2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdfc2-143">RELATED LINKS</span></span>
