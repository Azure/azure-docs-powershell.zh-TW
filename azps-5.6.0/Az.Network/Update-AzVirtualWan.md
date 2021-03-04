---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901790"
---
# <span data-ttu-id="d722c-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="d722c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d722c-102">SYNOPSIS</span></span>
<span data-ttu-id="d722c-103">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="d722c-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="d722c-104">語法</span><span class="sxs-lookup"><span data-stu-id="d722c-104">SYNTAX</span></span>

### <span data-ttu-id="d722c-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="d722c-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d722c-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d722c-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d722c-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d722c-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d722c-108">描述</span><span class="sxs-lookup"><span data-stu-id="d722c-108">DESCRIPTION</span></span>
<span data-ttu-id="d722c-109">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="d722c-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="d722c-110">例子</span><span class="sxs-lookup"><span data-stu-id="d722c-110">EXAMPLES</span></span>

### <span data-ttu-id="d722c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d722c-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="d722c-112">上述步驟將在「美國西部」地區建立資源群組「testRG」，以及 Azure 中該資源群組中的 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="d722c-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="d722c-113">VirtualWan 會以新的屬性更新。</span><span class="sxs-lookup"><span data-stu-id="d722c-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="d722c-114">參數</span><span class="sxs-lookup"><span data-stu-id="d722c-114">PARAMETERS</span></span>

### <span data-ttu-id="d722c-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="d722c-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="d722c-116">允許分支到 VirtualWan 的分支流量。</span><span class="sxs-lookup"><span data-stu-id="d722c-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="d722c-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="d722c-118">允許 vnet 到 VirtualWan 的 vnet 流量。</span><span class="sxs-lookup"><span data-stu-id="d722c-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d722c-119">-AsJob</span></span>
<span data-ttu-id="d722c-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d722c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d722c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d722c-121">-DefaultProfile</span></span>
<span data-ttu-id="d722c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d722c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-123">-強制</span><span class="sxs-lookup"><span data-stu-id="d722c-123">-Force</span></span>
<span data-ttu-id="d722c-124">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="d722c-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d722c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d722c-125">-InputObject</span></span>
<span data-ttu-id="d722c-126">要修改的虛擬 wan 物件</span><span class="sxs-lookup"><span data-stu-id="d722c-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="d722c-127">-Name</span></span>
<span data-ttu-id="d722c-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d722c-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d722c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d722c-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d722c-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d722c-131">-ResourceId</span></span>
<span data-ttu-id="d722c-132">虛擬 Wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d722c-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-133">-標記</span><span class="sxs-lookup"><span data-stu-id="d722c-133">-Tag</span></span>
<span data-ttu-id="d722c-134">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d722c-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d722c-135">-VirtualWANType</span></span>
<span data-ttu-id="d722c-136">虛擬 Wan 的類型。</span><span class="sxs-lookup"><span data-stu-id="d722c-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d722c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="d722c-137">-Confirm</span></span>
<span data-ttu-id="d722c-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d722c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d722c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d722c-139">-WhatIf</span></span>
<span data-ttu-id="d722c-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d722c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d722c-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d722c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d722c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d722c-142">CommonParameters</span></span>
<span data-ttu-id="d722c-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d722c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d722c-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d722c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d722c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d722c-145">INPUTS</span></span>

### <span data-ttu-id="d722c-146">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="d722c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d722c-147">System.String</span></span>

## <span data-ttu-id="d722c-148">輸出</span><span class="sxs-lookup"><span data-stu-id="d722c-148">OUTPUTS</span></span>

### <span data-ttu-id="d722c-149">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="d722c-150">筆記</span><span class="sxs-lookup"><span data-stu-id="d722c-150">NOTES</span></span>

## <span data-ttu-id="d722c-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d722c-151">RELATED LINKS</span></span>

[<span data-ttu-id="d722c-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="d722c-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="d722c-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d722c-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
