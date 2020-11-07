---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802098"
---
# <span data-ttu-id="d71db-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="d71db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d71db-102">SYNOPSIS</span></span>
<span data-ttu-id="d71db-103">重新開機 VMSS 或 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d71db-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d71db-104">句法</span><span class="sxs-lookup"><span data-stu-id="d71db-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d71db-105">說明</span><span class="sxs-lookup"><span data-stu-id="d71db-105">DESCRIPTION</span></span>
<span data-ttu-id="d71db-106">**Restart AzureRmVmss** Cmdlet 會重新開機虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="d71db-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d71db-107">這個 Cmdlet 也可以用來在 VMSS 內使用 *InstanceId* 參數重新開機特定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d71db-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="d71db-108">示例</span><span class="sxs-lookup"><span data-stu-id="d71db-108">EXAMPLES</span></span>

### <span data-ttu-id="d71db-109">範例1：重新開機 VMSS</span><span class="sxs-lookup"><span data-stu-id="d71db-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="d71db-110">這個命令會重新開機屬於名為 Group001 之資源群組的名為 VMSS001 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d71db-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="d71db-111">範例2：在 VMSS 中重新開機特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="d71db-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="d71db-112">這個命令會在屬於名為 Group001 之資源群組的名稱為 VMSS 的 VMSS001 中，重新開機實例識別碼為1的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d71db-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="d71db-113">參數</span><span class="sxs-lookup"><span data-stu-id="d71db-113">PARAMETERS</span></span>

### <span data-ttu-id="d71db-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d71db-114">-AsJob</span></span>
<span data-ttu-id="d71db-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d71db-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d71db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71db-116">-DefaultProfile</span></span>
<span data-ttu-id="d71db-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d71db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d71db-118">-InstanceId</span></span>
<span data-ttu-id="d71db-119">指定為字串陣列（需要重新開機的實例識別碼）。</span><span class="sxs-lookup"><span data-stu-id="d71db-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d71db-120">-ResourceGroupName</span></span>
<span data-ttu-id="d71db-121">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d71db-121">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d71db-122">-VMScaleSetName</span></span>
<span data-ttu-id="d71db-123">Species 此 Cmdlet 重新開機之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d71db-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d71db-124">-Confirm</span></span>
<span data-ttu-id="d71db-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d71db-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d71db-126">-WhatIf</span></span>
<span data-ttu-id="d71db-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d71db-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d71db-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d71db-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71db-129">CommonParameters</span></span>
<span data-ttu-id="d71db-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d71db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71db-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d71db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71db-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d71db-132">INPUTS</span></span>

### <span data-ttu-id="d71db-133">所有</span><span class="sxs-lookup"><span data-stu-id="d71db-133">None</span></span>
<span data-ttu-id="d71db-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d71db-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d71db-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d71db-135">OUTPUTS</span></span>

###  
<span data-ttu-id="d71db-136">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d71db-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d71db-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d71db-137">NOTES</span></span>

## <span data-ttu-id="d71db-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d71db-138">RELATED LINKS</span></span>

[<span data-ttu-id="d71db-139">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d71db-140">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d71db-141">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d71db-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d71db-143">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d71db-144">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="d71db-145">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d71db-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


