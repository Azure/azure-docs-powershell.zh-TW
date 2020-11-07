---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796054"
---
# <span data-ttu-id="2fdf2-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-101">Remove-AzVM</span></span>

## <span data-ttu-id="2fdf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdf2-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="2fdf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fdf2-104">SYNTAX</span></span>

### <span data-ttu-id="2fdf2-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="2fdf2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdf2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2fdf2-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdf2-107">說明</span><span class="sxs-lookup"><span data-stu-id="2fdf2-107">DESCRIPTION</span></span>
<span data-ttu-id="2fdf2-108">**AzVM** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="2fdf2-109">示例</span><span class="sxs-lookup"><span data-stu-id="2fdf2-109">EXAMPLES</span></span>

### <span data-ttu-id="2fdf2-110">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2fdf2-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2fdf2-111">這個命令會從 [資源群組 ResourceGroup11] 中移除名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2fdf2-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fdf2-112">PARAMETERS</span></span>

### <span data-ttu-id="2fdf2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fdf2-113">-AsJob</span></span>
<span data-ttu-id="2fdf2-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2fdf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdf2-115">-DefaultProfile</span></span>
<span data-ttu-id="2fdf2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fdf2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2fdf2-117">-Force</span></span>
<span data-ttu-id="2fdf2-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fdf2-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2fdf2-119">-Id</span></span>
<span data-ttu-id="2fdf2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-120">The resource group name.</span></span>

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

### <span data-ttu-id="2fdf2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fdf2-121">-Name</span></span>
<span data-ttu-id="2fdf2-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-122">The resource name.</span></span>

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

### <span data-ttu-id="2fdf2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdf2-123">-ResourceGroupName</span></span>
<span data-ttu-id="2fdf2-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2fdf2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2fdf2-125">-Confirm</span></span>
<span data-ttu-id="2fdf2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdf2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdf2-127">-WhatIf</span></span>
<span data-ttu-id="2fdf2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2fdf2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdf2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdf2-130">CommonParameters</span></span>
<span data-ttu-id="2fdf2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdf2-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdf2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2fdf2-133">INPUTS</span></span>

### <span data-ttu-id="2fdf2-134">所有</span><span class="sxs-lookup"><span data-stu-id="2fdf2-134">None</span></span>
<span data-ttu-id="2fdf2-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2fdf2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fdf2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2fdf2-136">OUTPUTS</span></span>

### <span data-ttu-id="2fdf2-137">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2fdf2-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2fdf2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2fdf2-138">NOTES</span></span>

## <span data-ttu-id="2fdf2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fdf2-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fdf2-140">AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2fdf2-141">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2fdf2-142">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2fdf2-143">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2fdf2-144">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="2fdf2-145">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fdf2-145">Update-AzVM</span></span>](./Update-AzVM.md)


