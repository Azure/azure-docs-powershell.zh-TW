---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447404"
---
# <span data-ttu-id="a3d0a-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="a3d0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d0a-103">在指定的 VMSS 上設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3d0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3d0a-104">SYNTAX</span></span>

### <span data-ttu-id="a3d0a-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="a3d0a-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d0a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a3d0a-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d0a-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="a3d0a-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d0a-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="a3d0a-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3d0a-109">說明</span><span class="sxs-lookup"><span data-stu-id="a3d0a-109">DESCRIPTION</span></span>
<span data-ttu-id="a3d0a-110">**AzureRmVmss** Cmdlet 會在虛擬機器縮放集 (VMSS) 設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a3d0a-111">這個 Cmdlet 支援的唯一動作是重新鏡像。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="a3d0a-112">示例</span><span class="sxs-lookup"><span data-stu-id="a3d0a-112">EXAMPLES</span></span>

### <span data-ttu-id="a3d0a-113">範例1：重新鏡像 VMSS</span><span class="sxs-lookup"><span data-stu-id="a3d0a-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a3d0a-114">這個命令會 reimages 名為 ContosoGroup 之資源群組的 VMSS 命名 ContosoVMSS。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="a3d0a-115">參數</span><span class="sxs-lookup"><span data-stu-id="a3d0a-115">PARAMETERS</span></span>

### <span data-ttu-id="a3d0a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3d0a-116">-AsJob</span></span>
<span data-ttu-id="a3d0a-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a3d0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d0a-118">-DefaultProfile</span></span>
<span data-ttu-id="a3d0a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d0a-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a3d0a-120">-InstanceId</span></span>
<span data-ttu-id="a3d0a-121">虛擬機器的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d0a-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="a3d0a-122">-PerformMaintenance</span></span>
<span data-ttu-id="a3d0a-123">表示此 Cmdlet 會在 VMSS 中執行一或多個虛擬機器的維護作業。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="a3d0a-124">-重新部署</span><span class="sxs-lookup"><span data-stu-id="a3d0a-124">-Redeploy</span></span>
<span data-ttu-id="a3d0a-125">表示 Cmdlet redeploys VMSS 中的一或多個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="a3d0a-126">-重新映射</span><span class="sxs-lookup"><span data-stu-id="a3d0a-126">-Reimage</span></span>
<span data-ttu-id="a3d0a-127">表示 Cmdlet reimages VMSS。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="a3d0a-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="a3d0a-128">-ReimageAll</span></span>
<span data-ttu-id="a3d0a-129">表示 Cmdlet reimages VMSS 中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="a3d0a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d0a-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3d0a-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d0a-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a3d0a-132">-VMScaleSetName</span></span>
<span data-ttu-id="a3d0a-133">Species 此 Cmdlet 針對其設定動作的 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d0a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a3d0a-134">-Confirm</span></span>
<span data-ttu-id="a3d0a-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d0a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d0a-136">-WhatIf</span></span>
<span data-ttu-id="a3d0a-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3d0a-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d0a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d0a-139">CommonParameters</span></span>
<span data-ttu-id="a3d0a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d0a-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d0a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a3d0a-142">INPUTS</span></span>

### <span data-ttu-id="a3d0a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a3d0a-143">System.String</span></span>

### <span data-ttu-id="a3d0a-144">System.object []</span><span class="sxs-lookup"><span data-stu-id="a3d0a-144">System.String[]</span></span>

## <span data-ttu-id="a3d0a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a3d0a-145">OUTPUTS</span></span>

### <span data-ttu-id="a3d0a-146">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a3d0a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a3d0a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a3d0a-147">NOTES</span></span>

## <span data-ttu-id="a3d0a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3d0a-148">RELATED LINKS</span></span>

[<span data-ttu-id="a3d0a-149">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-150">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-151">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-152">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-153">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-154">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a3d0a-155">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3d0a-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


