---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613122"
---
# <span data-ttu-id="39e45-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="39e45-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="39e45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39e45-102">SYNOPSIS</span></span>
<span data-ttu-id="39e45-103">修改 VMSS 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="39e45-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="39e45-104">句法</span><span class="sxs-lookup"><span data-stu-id="39e45-104">SYNTAX</span></span>

### <span data-ttu-id="39e45-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="39e45-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e45-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="39e45-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e45-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="39e45-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e45-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="39e45-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39e45-109">說明</span><span class="sxs-lookup"><span data-stu-id="39e45-109">DESCRIPTION</span></span>
<span data-ttu-id="39e45-110">**AzVmssVM** Cmdlet 會修改虛擬機器縮放集 (VMSS) 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="39e45-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="39e45-111">示例</span><span class="sxs-lookup"><span data-stu-id="39e45-111">EXAMPLES</span></span>

## <span data-ttu-id="39e45-112">參數</span><span class="sxs-lookup"><span data-stu-id="39e45-112">PARAMETERS</span></span>

### <span data-ttu-id="39e45-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39e45-113">-AsJob</span></span>
<span data-ttu-id="39e45-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="39e45-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e45-115">-DefaultProfile</span></span>
<span data-ttu-id="39e45-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39e45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e45-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="39e45-117">-InstanceId</span></span>
<span data-ttu-id="39e45-118">指定此 Cmdlet 修改狀態的 VMSS 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="39e45-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e45-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="39e45-119">-PerformMaintenance</span></span>
<span data-ttu-id="39e45-120">表示此 Cmdlet 會在 VMSS 中的虛擬機器上執行維護。</span><span class="sxs-lookup"><span data-stu-id="39e45-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e45-121">-重新部署</span><span class="sxs-lookup"><span data-stu-id="39e45-121">-Redeploy</span></span>
<span data-ttu-id="39e45-122">表示此 Cmdlet redeploys VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39e45-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e45-123">-重新映射</span><span class="sxs-lookup"><span data-stu-id="39e45-123">-Reimage</span></span>
<span data-ttu-id="39e45-124">表示此 Cmdlet reimages VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="39e45-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e45-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="39e45-125">-ReimageAll</span></span>
<span data-ttu-id="39e45-126">表示 Cmdlet reimages VMSS 實例中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="39e45-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e45-127">-ResourceGroupName</span></span>
<span data-ttu-id="39e45-128">指定包含 VMSS 實例之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39e45-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="39e45-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="39e45-129">-VMScaleSetName</span></span>
<span data-ttu-id="39e45-130">指定此 Cmdlet 所修改之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="39e45-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="39e45-131">-確認</span><span class="sxs-lookup"><span data-stu-id="39e45-131">-Confirm</span></span>
<span data-ttu-id="39e45-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39e45-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e45-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e45-133">-WhatIf</span></span>
<span data-ttu-id="39e45-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39e45-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39e45-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39e45-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e45-136">CommonParameters</span></span>
<span data-ttu-id="39e45-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39e45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e45-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39e45-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e45-139">輸入</span><span class="sxs-lookup"><span data-stu-id="39e45-139">INPUTS</span></span>

### <span data-ttu-id="39e45-140">System.object</span><span class="sxs-lookup"><span data-stu-id="39e45-140">System.String</span></span>

## <span data-ttu-id="39e45-141">輸出</span><span class="sxs-lookup"><span data-stu-id="39e45-141">OUTPUTS</span></span>

### <span data-ttu-id="39e45-142">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="39e45-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="39e45-143">筆記</span><span class="sxs-lookup"><span data-stu-id="39e45-143">NOTES</span></span>

## <span data-ttu-id="39e45-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="39e45-144">RELATED LINKS</span></span>

[<span data-ttu-id="39e45-145">AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="39e45-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
