---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625647"
---
# <span data-ttu-id="1595c-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1595c-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1595c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1595c-102">SYNOPSIS</span></span>
<span data-ttu-id="1595c-103">更新儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="1595c-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1595c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1595c-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1595c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1595c-105">DESCRIPTION</span></span>
<span data-ttu-id="1595c-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet 會更新儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="1595c-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="1595c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1595c-107">EXAMPLES</span></span>

### <span data-ttu-id="1595c-108">範例1：使用 JSON 更新 NetworkRule 的所有屬性、輸入規則</span><span class="sxs-lookup"><span data-stu-id="1595c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="1595c-109">這個命令會以 JSON 更新 NetworkRule、輸入規則的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="1595c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="1595c-110">範例2： NetworkRule 的更新旁路屬性</span><span class="sxs-lookup"><span data-stu-id="1595c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="1595c-111">此命令會更新 NetworkRule 的旁路屬性 (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="1595c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="1595c-112">範例3：清除儲存空間帳戶 NetworkRule 的規則</span><span class="sxs-lookup"><span data-stu-id="1595c-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="1595c-113">這個命令會清理 NetworkRule 儲存帳戶的規則， (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="1595c-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="1595c-114">參數</span><span class="sxs-lookup"><span data-stu-id="1595c-114">PARAMETERS</span></span>

### <span data-ttu-id="1595c-115">-略過</span><span class="sxs-lookup"><span data-stu-id="1595c-115">-Bypass</span></span>
<span data-ttu-id="1595c-116">要更新至儲存空間帳戶之 NetworkRule 屬性的旁路值。</span><span class="sxs-lookup"><span data-stu-id="1595c-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="1595c-117">[允許] 值為 [無] 或 [任何] 的組合： [存儲記錄]-[存儲] 資料 Azureservices</span><span class="sxs-lookup"><span data-stu-id="1595c-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1595c-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1595c-118">-DefaultAction</span></span>
<span data-ttu-id="1595c-119">要更新至儲存空間帳戶之 NetworkRule 屬性的 DefaultAction 值。</span><span class="sxs-lookup"><span data-stu-id="1595c-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="1595c-120">允許的選項：-[存儲] 允許-[存儲拒絕]</span><span class="sxs-lookup"><span data-stu-id="1595c-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1595c-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1595c-121">-IPRule</span></span>
<span data-ttu-id="1595c-122">要更新至儲存空間帳戶之 NetworkRule 屬性的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="1595c-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1595c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1595c-123">-Name</span></span>
<span data-ttu-id="1595c-124">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1595c-124">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1595c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1595c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1595c-126">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1595c-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1595c-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1595c-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="1595c-128">要更新至儲存空間帳戶之 NetworkRule 屬性的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="1595c-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1595c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1595c-129">-Confirm</span></span>
<span data-ttu-id="1595c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1595c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1595c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1595c-131">-WhatIf</span></span>
<span data-ttu-id="1595c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1595c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1595c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1595c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1595c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1595c-134">-DefaultProfile</span></span>
<span data-ttu-id="1595c-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1595c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1595c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1595c-136">CommonParameters</span></span>
<span data-ttu-id="1595c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1595c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1595c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1595c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1595c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1595c-139">INPUTS</span></span>

### <span data-ttu-id="1595c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1595c-140">System.String</span></span>
<span data-ttu-id="1595c-141">PSIpRule [] PSVirtualNetworkRule [].. [] 的 [] （[]）</span><span class="sxs-lookup"><span data-stu-id="1595c-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1595c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1595c-142">OUTPUTS</span></span>

### <span data-ttu-id="1595c-143">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="1595c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1595c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1595c-144">NOTES</span></span>

## <span data-ttu-id="1595c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1595c-145">RELATED LINKS</span></span>

