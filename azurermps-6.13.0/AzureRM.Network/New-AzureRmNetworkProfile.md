---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449024"
---
# <span data-ttu-id="e6359-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e6359-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="e6359-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6359-102">SYNOPSIS</span></span>
<span data-ttu-id="e6359-103">建立新的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="e6359-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6359-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6359-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6359-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6359-105">DESCRIPTION</span></span>
<span data-ttu-id="e6359-106">**新的-AzureRmNetworkProfile** Cmdlet 會建立新的網路設定檔頂層資源。</span><span class="sxs-lookup"><span data-stu-id="e6359-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="e6359-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6359-107">EXAMPLES</span></span>

### <span data-ttu-id="e6359-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e6359-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="e6359-109">這會建立新的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="e6359-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="e6359-110">參數</span><span class="sxs-lookup"><span data-stu-id="e6359-110">PARAMETERS</span></span>

### <span data-ttu-id="e6359-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6359-111">-AsJob</span></span>
<span data-ttu-id="e6359-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e6359-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6359-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e6359-113">-ContainerNicConfig</span></span>
<span data-ttu-id="e6359-114">要新增至此網路設定檔的容器網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="e6359-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6359-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6359-115">-DefaultProfile</span></span>
<span data-ttu-id="e6359-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6359-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6359-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6359-117">-Force</span></span>
<span data-ttu-id="e6359-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="e6359-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e6359-119">-位置</span><span class="sxs-lookup"><span data-stu-id="e6359-119">-Location</span></span>
<span data-ttu-id="e6359-120">位置。</span><span class="sxs-lookup"><span data-stu-id="e6359-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6359-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6359-121">-Name</span></span>
<span data-ttu-id="e6359-122">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6359-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6359-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6359-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6359-124">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e6359-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6359-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6359-125">-Tag</span></span>
<span data-ttu-id="e6359-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="e6359-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e6359-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e6359-127">-Confirm</span></span>
<span data-ttu-id="e6359-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6359-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6359-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6359-129">-WhatIf</span></span>
<span data-ttu-id="e6359-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6359-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6359-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6359-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6359-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6359-132">CommonParameters</span></span>
<span data-ttu-id="e6359-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6359-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6359-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6359-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6359-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e6359-135">INPUTS</span></span>

### <span data-ttu-id="e6359-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e6359-136">System.String</span></span>

### <span data-ttu-id="e6359-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6359-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6359-138">[System.object]. 清單 ' 1 [PSContainerNetworkInterface，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="e6359-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e6359-139">[System.object]. 清單 ' 1 [PSContainerNetworkInterfaceConfiguration，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="e6359-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6359-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e6359-140">OUTPUTS</span></span>

### <span data-ttu-id="e6359-141">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6359-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="e6359-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e6359-142">NOTES</span></span>

## <span data-ttu-id="e6359-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6359-143">RELATED LINKS</span></span>
