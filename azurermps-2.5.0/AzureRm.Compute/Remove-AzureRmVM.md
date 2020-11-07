---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800538"
---
# <span data-ttu-id="95e65-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="95e65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95e65-102">SYNOPSIS</span></span>
<span data-ttu-id="95e65-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95e65-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95e65-104">句法</span><span class="sxs-lookup"><span data-stu-id="95e65-104">SYNTAX</span></span>

### <span data-ttu-id="95e65-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="95e65-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e65-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="95e65-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e65-107">說明</span><span class="sxs-lookup"><span data-stu-id="95e65-107">DESCRIPTION</span></span>
<span data-ttu-id="95e65-108">**AzureRmVM** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95e65-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="95e65-109">示例</span><span class="sxs-lookup"><span data-stu-id="95e65-109">EXAMPLES</span></span>

### <span data-ttu-id="95e65-110">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="95e65-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="95e65-111">這個命令會從 [資源群組 ResourceGroup11] 中移除名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95e65-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="95e65-112">參數</span><span class="sxs-lookup"><span data-stu-id="95e65-112">PARAMETERS</span></span>

### <span data-ttu-id="95e65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95e65-113">-AsJob</span></span>
<span data-ttu-id="95e65-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="95e65-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95e65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e65-115">-DefaultProfile</span></span>
<span data-ttu-id="95e65-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95e65-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95e65-117">-Force</span><span class="sxs-lookup"><span data-stu-id="95e65-117">-Force</span></span>
<span data-ttu-id="95e65-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="95e65-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e65-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="95e65-119">-Id</span></span>
<span data-ttu-id="95e65-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e65-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e65-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="95e65-121">-Name</span></span>
<span data-ttu-id="95e65-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="95e65-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e65-123">-ResourceGroupName</span></span>
<span data-ttu-id="95e65-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e65-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e65-125">-確認</span><span class="sxs-lookup"><span data-stu-id="95e65-125">-Confirm</span></span>
<span data-ttu-id="95e65-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95e65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e65-127">-WhatIf</span></span>
<span data-ttu-id="95e65-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95e65-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="95e65-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e65-130">CommonParameters</span></span>
<span data-ttu-id="95e65-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95e65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e65-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95e65-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e65-133">輸入</span><span class="sxs-lookup"><span data-stu-id="95e65-133">INPUTS</span></span>

### <span data-ttu-id="95e65-134">所有</span><span class="sxs-lookup"><span data-stu-id="95e65-134">None</span></span>
<span data-ttu-id="95e65-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="95e65-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95e65-136">輸出</span><span class="sxs-lookup"><span data-stu-id="95e65-136">OUTPUTS</span></span>

### <span data-ttu-id="95e65-137">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="95e65-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="95e65-138">筆記</span><span class="sxs-lookup"><span data-stu-id="95e65-138">NOTES</span></span>

## <span data-ttu-id="95e65-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="95e65-139">RELATED LINKS</span></span>

[<span data-ttu-id="95e65-140">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="95e65-141">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="95e65-142">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="95e65-143">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="95e65-144">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="95e65-145">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95e65-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


