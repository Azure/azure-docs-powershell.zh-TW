---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622661"
---
# <span data-ttu-id="bdbd2-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-101">Start-AzVM</span></span>

## <span data-ttu-id="bdbd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbd2-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="bdbd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdbd2-104">SYNTAX</span></span>

### <span data-ttu-id="bdbd2-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="bdbd2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bdbd2-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbd2-107">說明</span><span class="sxs-lookup"><span data-stu-id="bdbd2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdbd2-108">**AzVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="bdbd2-109">示例</span><span class="sxs-lookup"><span data-stu-id="bdbd2-109">EXAMPLES</span></span>

### <span data-ttu-id="bdbd2-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bdbd2-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="bdbd2-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="bdbd2-112">參數</span><span class="sxs-lookup"><span data-stu-id="bdbd2-112">PARAMETERS</span></span>

### <span data-ttu-id="bdbd2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdbd2-113">-AsJob</span></span>
<span data-ttu-id="bdbd2-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bdbd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd2-115">-DefaultProfile</span></span>
<span data-ttu-id="bdbd2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdbd2-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="bdbd2-117">-Id</span></span>
<span data-ttu-id="bdbd2-118">虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bdbd2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdbd2-119">-Name</span></span>
<span data-ttu-id="bdbd2-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-120">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdbd2-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bdbd2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bdbd2-123">-Confirm</span></span>
<span data-ttu-id="bdbd2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbd2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbd2-125">-WhatIf</span></span>
<span data-ttu-id="bdbd2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdbd2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbd2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbd2-128">CommonParameters</span></span>
<span data-ttu-id="bdbd2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbd2-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbd2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bdbd2-131">INPUTS</span></span>

### <span data-ttu-id="bdbd2-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bdbd2-132">System.String</span></span>

## <span data-ttu-id="bdbd2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="bdbd2-133">OUTPUTS</span></span>

### <span data-ttu-id="bdbd2-134">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="bdbd2-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="bdbd2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="bdbd2-135">NOTES</span></span>

## <span data-ttu-id="bdbd2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdbd2-136">RELATED LINKS</span></span>

[<span data-ttu-id="bdbd2-137">AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bdbd2-138">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="bdbd2-139">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="bdbd2-140">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="bdbd2-141">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="bdbd2-142">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd2-142">Update-AzVM</span></span>](./Update-AzVM.md)


