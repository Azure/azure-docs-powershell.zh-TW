---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138221"
---
# <span data-ttu-id="45e00-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-101">Start-AzVM</span></span>

## <span data-ttu-id="45e00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45e00-102">SYNOPSIS</span></span>
<span data-ttu-id="45e00-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45e00-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="45e00-104">句法</span><span class="sxs-lookup"><span data-stu-id="45e00-104">SYNTAX</span></span>

### <span data-ttu-id="45e00-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="45e00-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e00-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="45e00-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45e00-107">說明</span><span class="sxs-lookup"><span data-stu-id="45e00-107">DESCRIPTION</span></span>
<span data-ttu-id="45e00-108">**AzVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45e00-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="45e00-109">示例</span><span class="sxs-lookup"><span data-stu-id="45e00-109">EXAMPLES</span></span>

### <span data-ttu-id="45e00-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="45e00-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="45e00-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45e00-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="45e00-112">參數</span><span class="sxs-lookup"><span data-stu-id="45e00-112">PARAMETERS</span></span>

### <span data-ttu-id="45e00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45e00-113">-AsJob</span></span>
<span data-ttu-id="45e00-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="45e00-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="45e00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e00-115">-DefaultProfile</span></span>
<span data-ttu-id="45e00-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45e00-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45e00-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="45e00-117">-Id</span></span>
<span data-ttu-id="45e00-118">虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="45e00-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="45e00-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="45e00-119">-Name</span></span>
<span data-ttu-id="45e00-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="45e00-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="45e00-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45e00-121">-NoWait</span></span>
<span data-ttu-id="45e00-122">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="45e00-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="45e00-123">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="45e00-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="45e00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e00-124">-ResourceGroupName</span></span>
<span data-ttu-id="45e00-125">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45e00-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="45e00-126">-確認</span><span class="sxs-lookup"><span data-stu-id="45e00-126">-Confirm</span></span>
<span data-ttu-id="45e00-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45e00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e00-128">-WhatIf</span></span>
<span data-ttu-id="45e00-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45e00-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45e00-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45e00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e00-131">CommonParameters</span></span>
<span data-ttu-id="45e00-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45e00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e00-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45e00-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e00-134">輸入</span><span class="sxs-lookup"><span data-stu-id="45e00-134">INPUTS</span></span>

### <span data-ttu-id="45e00-135">System.object</span><span class="sxs-lookup"><span data-stu-id="45e00-135">System.String</span></span>

## <span data-ttu-id="45e00-136">輸出</span><span class="sxs-lookup"><span data-stu-id="45e00-136">OUTPUTS</span></span>

### <span data-ttu-id="45e00-137">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="45e00-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="45e00-138">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="45e00-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="45e00-139">筆記</span><span class="sxs-lookup"><span data-stu-id="45e00-139">NOTES</span></span>

## <span data-ttu-id="45e00-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="45e00-140">RELATED LINKS</span></span>

[<span data-ttu-id="45e00-141">AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="45e00-142">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="45e00-143">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="45e00-144">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="45e00-145">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="45e00-146">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="45e00-146">Update-AzVM</span></span>](./Update-AzVM.md)

