---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 8851f7e2820e1c9a0a63b475544c49fe5c0c8ee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452975"
---
# <span data-ttu-id="d4e05-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4e05-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d4e05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4e05-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e05-103">更新儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d4e05-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e05-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4e05-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e05-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4e05-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e05-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet 會更新儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d4e05-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d4e05-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4e05-107">EXAMPLES</span></span>

### <span data-ttu-id="d4e05-108">範例1：使用 JSON 更新 NetworkRule 的所有屬性、輸入規則</span><span class="sxs-lookup"><span data-stu-id="d4e05-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="d4e05-109">這個命令會以 JSON 更新 NetworkRule、輸入規則的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="d4e05-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="d4e05-110">範例2： NetworkRule 的更新旁路屬性</span><span class="sxs-lookup"><span data-stu-id="d4e05-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="d4e05-111">此命令會更新 NetworkRule 的旁路屬性 (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="d4e05-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="d4e05-112">範例3：清除儲存空間帳戶 NetworkRule 的規則</span><span class="sxs-lookup"><span data-stu-id="d4e05-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="d4e05-113">這個命令會清理 NetworkRule 儲存帳戶的規則， (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="d4e05-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="d4e05-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4e05-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e05-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4e05-115">-AsJob</span></span>
<span data-ttu-id="d4e05-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d4e05-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4e05-117">-略過</span><span class="sxs-lookup"><span data-stu-id="d4e05-117">-Bypass</span></span>
<span data-ttu-id="d4e05-118">要更新至儲存空間帳戶之 NetworkRule 屬性的旁路值。</span><span class="sxs-lookup"><span data-stu-id="d4e05-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="d4e05-119">允許的值為 [無] 或 [任何] 的組合：•記錄•度量• Azureservices</span><span class="sxs-lookup"><span data-stu-id="d4e05-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="d4e05-120">-DefaultAction</span></span>
<span data-ttu-id="d4e05-121">要更新至儲存空間帳戶之 NetworkRule 屬性的 DefaultAction 值。</span><span class="sxs-lookup"><span data-stu-id="d4e05-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="d4e05-122">允許的選項：•允許•拒絕</span><span class="sxs-lookup"><span data-stu-id="d4e05-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e05-123">-DefaultProfile</span></span>
<span data-ttu-id="d4e05-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4e05-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e05-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d4e05-125">-IPRule</span></span>
<span data-ttu-id="d4e05-126">要更新至儲存空間帳戶之 NetworkRule 屬性的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="d4e05-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4e05-127">-Name</span></span>
<span data-ttu-id="d4e05-128">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e05-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e05-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4e05-130">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e05-130">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4e05-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="d4e05-132">要更新至儲存空間帳戶之 NetworkRule 屬性的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="d4e05-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e05-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d4e05-133">-Confirm</span></span>
<span data-ttu-id="d4e05-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4e05-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e05-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e05-135">-WhatIf</span></span>
<span data-ttu-id="d4e05-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4e05-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e05-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4e05-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e05-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e05-138">CommonParameters</span></span>
<span data-ttu-id="d4e05-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4e05-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e05-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4e05-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e05-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d4e05-141">INPUTS</span></span>

### <span data-ttu-id="d4e05-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d4e05-142">System.String</span></span>
<span data-ttu-id="d4e05-143">PSIpRule [] PSVirtualNetworkRule [].. [] 的 [] （[]）</span><span class="sxs-lookup"><span data-stu-id="d4e05-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d4e05-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d4e05-144">OUTPUTS</span></span>

### <span data-ttu-id="d4e05-145">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d4e05-145">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d4e05-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d4e05-146">NOTES</span></span>

## <span data-ttu-id="d4e05-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4e05-147">RELATED LINKS</span></span>
