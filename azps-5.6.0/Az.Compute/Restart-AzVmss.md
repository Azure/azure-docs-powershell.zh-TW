---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: a29e21bba3d04ca301d5f2bf3d2b5f9050fe9765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912902"
---
# <span data-ttu-id="55b2b-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="55b2b-101">Restart-AzVmss</span></span>

## <span data-ttu-id="55b2b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="55b2b-103">重新開機 VMSS 或 VMSS 內的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55b2b-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="55b2b-104">語法</span><span class="sxs-lookup"><span data-stu-id="55b2b-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b2b-105">描述</span><span class="sxs-lookup"><span data-stu-id="55b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="55b2b-106">**Restart-Az Vms Cmdlet** 會重新開機 VMSS (的虛擬機器縮放) 。</span><span class="sxs-lookup"><span data-stu-id="55b2b-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="55b2b-107">此 Cmdlet 也可以用來使用 *InstanceId* 參數在 VMSS 內重新開機特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55b2b-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="55b2b-108">例子</span><span class="sxs-lookup"><span data-stu-id="55b2b-108">EXAMPLES</span></span>

### <span data-ttu-id="55b2b-109">範例 1：重新開機 VMSS</span><span class="sxs-lookup"><span data-stu-id="55b2b-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="55b2b-110">此命令會重新開機名為 VMSS001 的 VMSS，該 VMSS 屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="55b2b-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="55b2b-111">範例 2：重新開機 VMSS 內的特定虛擬機器</span><span class="sxs-lookup"><span data-stu-id="55b2b-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="55b2b-112">此命令會重新開機虛擬機器，該虛擬機器在 VMSS 名為 VMSS001 的 VMSS 中，其實例識別碼為 1，該虛擬機器屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="55b2b-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="55b2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="55b2b-113">PARAMETERS</span></span>

### <span data-ttu-id="55b2b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b2b-114">-AsJob</span></span>
<span data-ttu-id="55b2b-115">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="55b2b-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="55b2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b2b-116">-DefaultProfile</span></span>
<span data-ttu-id="55b2b-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55b2b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b2b-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="55b2b-118">-InstanceId</span></span>
<span data-ttu-id="55b2b-119">指定需要重新開機之實例的識別碼做為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="55b2b-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b2b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b2b-120">-ResourceGroupName</span></span>
<span data-ttu-id="55b2b-121">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55b2b-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="55b2b-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="55b2b-122">-VMScaleSetName</span></span>
<span data-ttu-id="55b2b-123">此 Cmdlet 重新開機的 VMSS 名稱。</span><span class="sxs-lookup"><span data-stu-id="55b2b-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="55b2b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="55b2b-124">-Confirm</span></span>
<span data-ttu-id="55b2b-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55b2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b2b-126">-WhatIf</span></span>
<span data-ttu-id="55b2b-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55b2b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55b2b-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55b2b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b2b-129">CommonParameters</span></span>
<span data-ttu-id="55b2b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55b2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b2b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b2b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b2b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="55b2b-132">INPUTS</span></span>

### <span data-ttu-id="55b2b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="55b2b-133">System.String</span></span>

### <span data-ttu-id="55b2b-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="55b2b-134">System.String[]</span></span>

## <span data-ttu-id="55b2b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="55b2b-135">OUTPUTS</span></span>

### <span data-ttu-id="55b2b-136">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="55b2b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="55b2b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="55b2b-137">NOTES</span></span>

## <span data-ttu-id="55b2b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="55b2b-138">RELATED LINKS</span></span>

[<span data-ttu-id="55b2b-139">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="55b2b-140">New-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="55b2b-141">Remove-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="55b2b-142">Set-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="55b2b-143">Start-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="55b2b-144">Stop-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="55b2b-145">Update-AzEvss</span><span class="sxs-lookup"><span data-stu-id="55b2b-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


