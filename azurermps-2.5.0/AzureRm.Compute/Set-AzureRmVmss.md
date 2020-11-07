---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801018"
---
# <span data-ttu-id="ff34f-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="ff34f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff34f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff34f-103">在指定的 VMSS 上設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="ff34f-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff34f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff34f-104">SYNTAX</span></span>

### <span data-ttu-id="ff34f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ff34f-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff34f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ff34f-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff34f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff34f-107">DESCRIPTION</span></span>
<span data-ttu-id="ff34f-108">**AzureRmVmss** Cmdlet 會在虛擬機器縮放集 (VMSS) 設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="ff34f-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ff34f-109">這個 Cmdlet 支援的唯一動作是重新鏡像。</span><span class="sxs-lookup"><span data-stu-id="ff34f-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="ff34f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ff34f-110">EXAMPLES</span></span>

### <span data-ttu-id="ff34f-111">範例1：重新鏡像 VMSS</span><span class="sxs-lookup"><span data-stu-id="ff34f-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ff34f-112">這個命令會 reimages 名為 ContosoGroup 之資源群組的 VMSS 命名 ContosoVMSS。</span><span class="sxs-lookup"><span data-stu-id="ff34f-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ff34f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ff34f-113">PARAMETERS</span></span>

### <span data-ttu-id="ff34f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff34f-114">-AsJob</span></span>
<span data-ttu-id="ff34f-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ff34f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ff34f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff34f-116">-DefaultProfile</span></span>
<span data-ttu-id="ff34f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff34f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff34f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ff34f-118">-InstanceId</span></span>
<span data-ttu-id="ff34f-119">虛擬機器的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff34f-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ff34f-120">-重新映射</span><span class="sxs-lookup"><span data-stu-id="ff34f-120">-Reimage</span></span>
<span data-ttu-id="ff34f-121">表示 Cmdlet reimages VMSS。</span><span class="sxs-lookup"><span data-stu-id="ff34f-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff34f-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="ff34f-122">-ReimageAll</span></span>
<span data-ttu-id="ff34f-123">表示 Cmdlet reimages VMSS 中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="ff34f-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff34f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff34f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff34f-125">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff34f-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ff34f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ff34f-126">-VMScaleSetName</span></span>
<span data-ttu-id="ff34f-127">Species 此 Cmdlet 針對其設定動作的 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff34f-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="ff34f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ff34f-128">-Confirm</span></span>
<span data-ttu-id="ff34f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff34f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff34f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff34f-130">-WhatIf</span></span>
<span data-ttu-id="ff34f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff34f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff34f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff34f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff34f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff34f-133">CommonParameters</span></span>
<span data-ttu-id="ff34f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff34f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff34f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff34f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff34f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ff34f-136">INPUTS</span></span>

### <span data-ttu-id="ff34f-137">所有</span><span class="sxs-lookup"><span data-stu-id="ff34f-137">None</span></span>
<span data-ttu-id="ff34f-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ff34f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff34f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ff34f-139">OUTPUTS</span></span>

### <span data-ttu-id="ff34f-140">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ff34f-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ff34f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ff34f-141">NOTES</span></span>

## <span data-ttu-id="ff34f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff34f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff34f-143">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ff34f-144">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ff34f-145">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ff34f-146">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ff34f-147">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ff34f-148">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ff34f-149">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff34f-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


