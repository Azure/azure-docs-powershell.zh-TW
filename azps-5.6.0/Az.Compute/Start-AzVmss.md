---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 2ff37cec23499afb0a0bb14069dc4e694f4440f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906781"
---
# <span data-ttu-id="832d0-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="832d0-101">Start-AzVmss</span></span>

## <span data-ttu-id="832d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="832d0-102">SYNOPSIS</span></span>
<span data-ttu-id="832d0-103">啟動 VMSS 或 VMSS 內的一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="832d0-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="832d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="832d0-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="832d0-105">描述</span><span class="sxs-lookup"><span data-stu-id="832d0-105">DESCRIPTION</span></span>
<span data-ttu-id="832d0-106">**Start-Az Vmss** Cmdlet 會啟動虛擬機器縮放集 (VMSS) 或一組虛擬機器內的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="832d0-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="832d0-107">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="832d0-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="832d0-108">例子</span><span class="sxs-lookup"><span data-stu-id="832d0-108">EXAMPLES</span></span>

### <span data-ttu-id="832d0-109">範例 1：在 VMSS 中啟動一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="832d0-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="832d0-110">此命令會啟動一組由實例識別碼字串陣列所指定的特定虛擬機器，該陣列屬於名為 Contoso VMSS 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="832d0-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="832d0-111">範例 2：啟動 VMSS 內的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="832d0-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="832d0-112">此命令會啟動所有屬於名為 Contoso VMSS 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="832d0-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="832d0-113">參數</span><span class="sxs-lookup"><span data-stu-id="832d0-113">PARAMETERS</span></span>

### <span data-ttu-id="832d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="832d0-114">-AsJob</span></span>
<span data-ttu-id="832d0-115">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="832d0-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="832d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="832d0-116">-DefaultProfile</span></span>
<span data-ttu-id="832d0-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="832d0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="832d0-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="832d0-118">-InstanceId</span></span>
<span data-ttu-id="832d0-119">指定 Cmdlet 啟動實例的識別碼或識別碼，做為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="832d0-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="832d0-120">例如： `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="832d0-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="832d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="832d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="832d0-122">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="832d0-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="832d0-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="832d0-123">-VMScaleSetName</span></span>
<span data-ttu-id="832d0-124">指定此 Cmdlet 啟動虛擬機器的 VMSS 名稱。</span><span class="sxs-lookup"><span data-stu-id="832d0-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="832d0-125">-確認</span><span class="sxs-lookup"><span data-stu-id="832d0-125">-Confirm</span></span>
<span data-ttu-id="832d0-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="832d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="832d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="832d0-127">-WhatIf</span></span>
<span data-ttu-id="832d0-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="832d0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="832d0-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="832d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="832d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="832d0-130">CommonParameters</span></span>
<span data-ttu-id="832d0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="832d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="832d0-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="832d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="832d0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="832d0-133">INPUTS</span></span>

### <span data-ttu-id="832d0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="832d0-134">System.String</span></span>

### <span data-ttu-id="832d0-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="832d0-135">System.String[]</span></span>

## <span data-ttu-id="832d0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="832d0-136">OUTPUTS</span></span>

### <span data-ttu-id="832d0-137">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="832d0-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="832d0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="832d0-138">NOTES</span></span>

## <span data-ttu-id="832d0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="832d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="832d0-140">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="832d0-141">New-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="832d0-142">Remove-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="832d0-143">Restart-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="832d0-144">Set-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="832d0-145">Stop-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="832d0-146">Update-AzEvss</span><span class="sxs-lookup"><span data-stu-id="832d0-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


