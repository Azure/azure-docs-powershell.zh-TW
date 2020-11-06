---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447329"
---
# <span data-ttu-id="1142f-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1142f-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="1142f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1142f-102">SYNOPSIS</span></span>
<span data-ttu-id="1142f-103">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="1142f-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1142f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1142f-104">SYNTAX</span></span>

### <span data-ttu-id="1142f-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="1142f-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1142f-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="1142f-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1142f-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="1142f-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1142f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1142f-108">DESCRIPTION</span></span>
<span data-ttu-id="1142f-109">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="1142f-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="1142f-110">示例</span><span class="sxs-lookup"><span data-stu-id="1142f-110">EXAMPLES</span></span>

### <span data-ttu-id="1142f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1142f-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="1142f-112">上述將會在 [West 美國] 地區建立資源群組 "testRG"，並在 Azure 中的該資源群組中建立 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="1142f-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="1142f-113">VirtualWan 已更新為新的屬性。</span><span class="sxs-lookup"><span data-stu-id="1142f-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="1142f-114">參數</span><span class="sxs-lookup"><span data-stu-id="1142f-114">PARAMETERS</span></span>

### <span data-ttu-id="1142f-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="1142f-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1142f-116">允許分支分支機搆 VirtualWan 的流量。</span><span class="sxs-lookup"><span data-stu-id="1142f-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="1142f-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="1142f-118">允許 vnet 至 vnet 流量以進行 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="1142f-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1142f-119">-AsJob</span></span>
<span data-ttu-id="1142f-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1142f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1142f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1142f-121">-DefaultProfile</span></span>
<span data-ttu-id="1142f-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1142f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1142f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1142f-123">-Force</span></span>
<span data-ttu-id="1142f-124">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1142f-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1142f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1142f-125">-InputObject</span></span>
<span data-ttu-id="1142f-126">要修改的虛擬 wan 物件</span><span class="sxs-lookup"><span data-stu-id="1142f-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1142f-127">-Name</span></span>
<span data-ttu-id="1142f-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1142f-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1142f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1142f-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1142f-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1142f-131">-ResourceId</span></span>
<span data-ttu-id="1142f-132">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1142f-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1142f-133">-Tag</span></span>
<span data-ttu-id="1142f-134">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="1142f-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1142f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="1142f-135">-Confirm</span></span>
<span data-ttu-id="1142f-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1142f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1142f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1142f-137">-WhatIf</span></span>
<span data-ttu-id="1142f-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1142f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1142f-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1142f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1142f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1142f-140">CommonParameters</span></span>
<span data-ttu-id="1142f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1142f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1142f-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1142f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1142f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1142f-143">INPUTS</span></span>

### <span data-ttu-id="1142f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1142f-144">System.String</span></span>

### <span data-ttu-id="1142f-145">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1142f-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="1142f-146">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1142f-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1142f-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1142f-147">OUTPUTS</span></span>

### <span data-ttu-id="1142f-148">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1142f-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="1142f-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1142f-149">NOTES</span></span>

## <span data-ttu-id="1142f-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1142f-150">RELATED LINKS</span></span>
