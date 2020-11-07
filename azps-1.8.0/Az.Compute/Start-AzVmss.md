---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 93c70344b2a5ce9f03e4b0c1088fa785989912da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788277"
---
# <span data-ttu-id="6b736-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-101">Start-AzVmss</span></span>

## <span data-ttu-id="6b736-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b736-102">SYNOPSIS</span></span>
<span data-ttu-id="6b736-103">在 VMSS 中啟動 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6b736-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="6b736-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b736-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b736-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b736-105">DESCRIPTION</span></span>
<span data-ttu-id="6b736-106">**AzVmss** Cmdlet 會啟動虛擬機器縮放集 (VMSS) 或一組虛擬機器中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6b736-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="6b736-107">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6b736-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="6b736-108">示例</span><span class="sxs-lookup"><span data-stu-id="6b736-108">EXAMPLES</span></span>

### <span data-ttu-id="6b736-109">範例1：在 VMSS 中啟動一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6b736-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="6b736-110">這個命令會啟動由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6b736-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="6b736-111">範例2：啟動 VMSS 中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6b736-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="6b736-112">這個命令會啟動屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6b736-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6b736-113">參數</span><span class="sxs-lookup"><span data-stu-id="6b736-113">PARAMETERS</span></span>

### <span data-ttu-id="6b736-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b736-114">-AsJob</span></span>
<span data-ttu-id="6b736-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="6b736-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6b736-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b736-116">-DefaultProfile</span></span>
<span data-ttu-id="6b736-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b736-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b736-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6b736-118">-InstanceId</span></span>
<span data-ttu-id="6b736-119">指定為字串陣列，即 Cmdlet 啟動之實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="6b736-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="6b736-120">例如： `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="6b736-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="6b736-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b736-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b736-122">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b736-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6b736-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6b736-123">-VMScaleSetName</span></span>
<span data-ttu-id="6b736-124">指定此 Cmdlet 啟動虛擬機器的 VMSS 名稱。</span><span class="sxs-lookup"><span data-stu-id="6b736-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="6b736-125">-確認</span><span class="sxs-lookup"><span data-stu-id="6b736-125">-Confirm</span></span>
<span data-ttu-id="6b736-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b736-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b736-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b736-127">-WhatIf</span></span>
<span data-ttu-id="6b736-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b736-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b736-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b736-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b736-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b736-130">CommonParameters</span></span>
<span data-ttu-id="6b736-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b736-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b736-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b736-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b736-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6b736-133">INPUTS</span></span>

### <span data-ttu-id="6b736-134">System.object</span><span class="sxs-lookup"><span data-stu-id="6b736-134">System.String</span></span>

### <span data-ttu-id="6b736-135">System.object []</span><span class="sxs-lookup"><span data-stu-id="6b736-135">System.String[]</span></span>

## <span data-ttu-id="6b736-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6b736-136">OUTPUTS</span></span>

### <span data-ttu-id="6b736-137">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6b736-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6b736-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6b736-138">NOTES</span></span>

## <span data-ttu-id="6b736-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b736-139">RELATED LINKS</span></span>

[<span data-ttu-id="6b736-140">AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6b736-141">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6b736-142">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6b736-143">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6b736-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6b736-145">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6b736-146">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b736-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


