---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 08fa41232a6f473b371c0e44e22b21712f61f1b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613121"
---
# <span data-ttu-id="583f7-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-101">Start-AzVM</span></span>

## <span data-ttu-id="583f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="583f7-102">SYNOPSIS</span></span>
<span data-ttu-id="583f7-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="583f7-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="583f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="583f7-104">SYNTAX</span></span>

### <span data-ttu-id="583f7-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="583f7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583f7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="583f7-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="583f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="583f7-107">DESCRIPTION</span></span>
<span data-ttu-id="583f7-108">**AzVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="583f7-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="583f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="583f7-109">EXAMPLES</span></span>

### <span data-ttu-id="583f7-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="583f7-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="583f7-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="583f7-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="583f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="583f7-112">PARAMETERS</span></span>

### <span data-ttu-id="583f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="583f7-113">-AsJob</span></span>
<span data-ttu-id="583f7-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="583f7-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="583f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583f7-115">-DefaultProfile</span></span>
<span data-ttu-id="583f7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="583f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="583f7-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="583f7-117">-Id</span></span>
<span data-ttu-id="583f7-118">虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="583f7-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583f7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="583f7-119">-Name</span></span>
<span data-ttu-id="583f7-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="583f7-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583f7-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="583f7-121">-NoWait</span></span>
<span data-ttu-id="583f7-122">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="583f7-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="583f7-123">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="583f7-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="583f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="583f7-125">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="583f7-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583f7-126">-確認</span><span class="sxs-lookup"><span data-stu-id="583f7-126">-Confirm</span></span>
<span data-ttu-id="583f7-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="583f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583f7-128">-WhatIf</span></span>
<span data-ttu-id="583f7-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="583f7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="583f7-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="583f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583f7-131">CommonParameters</span></span>
<span data-ttu-id="583f7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="583f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583f7-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="583f7-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583f7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="583f7-134">INPUTS</span></span>

### <span data-ttu-id="583f7-135">System.object</span><span class="sxs-lookup"><span data-stu-id="583f7-135">System.String</span></span>

## <span data-ttu-id="583f7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="583f7-136">OUTPUTS</span></span>

### <span data-ttu-id="583f7-137">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="583f7-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="583f7-138">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="583f7-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="583f7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="583f7-139">NOTES</span></span>

## <span data-ttu-id="583f7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="583f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="583f7-141">AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="583f7-142">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="583f7-143">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="583f7-144">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="583f7-145">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="583f7-146">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="583f7-146">Update-AzVM</span></span>](./Update-AzVM.md)


