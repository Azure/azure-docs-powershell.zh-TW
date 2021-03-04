---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916796"
---
# <span data-ttu-id="72693-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="72693-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="72693-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72693-102">SYNOPSIS</span></span>
<span data-ttu-id="72693-103">將路由規則更新至 Slot。</span><span class="sxs-lookup"><span data-stu-id="72693-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="72693-104">語法</span><span class="sxs-lookup"><span data-stu-id="72693-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72693-105">描述</span><span class="sxs-lookup"><span data-stu-id="72693-105">DESCRIPTION</span></span>
<span data-ttu-id="72693-106">**Update-AzWebAppTrafficRoudlet** 會更新 Azure Web App Slot 的路由規則組式。</span><span class="sxs-lookup"><span data-stu-id="72693-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="72693-107">例子</span><span class="sxs-lookup"><span data-stu-id="72693-107">EXAMPLES</span></span>

### <span data-ttu-id="72693-108">範例 1 更新路由規則，將 15% 生產流量轉移到 Stg slot</span><span class="sxs-lookup"><span data-stu-id="72693-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="72693-109">此命令會更新路由規則，將 15% 生產流量轉移到 Stg slot。</span><span class="sxs-lookup"><span data-stu-id="72693-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="72693-110">範例 2 更新路由規則，以增量方式將生產流量轉移到 Stg slot 範圍從 50% 到 90%。</span><span class="sxs-lookup"><span data-stu-id="72693-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="72693-111">此命令會更新路由規則，以增量方式將生產流量傳輸至 Stg 插槽的範圍從 50% 到 90%。</span><span class="sxs-lookup"><span data-stu-id="72693-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="72693-112">參數</span><span class="sxs-lookup"><span data-stu-id="72693-112">PARAMETERS</span></span>

### <span data-ttu-id="72693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72693-113">-DefaultProfile</span></span>
<span data-ttu-id="72693-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72693-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72693-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72693-115">-ResourceGroupName</span></span>
<span data-ttu-id="72693-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72693-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72693-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="72693-117">-RoutingRule</span></span>
<span data-ttu-id="72693-118">Web App 路由規則。</span><span class="sxs-lookup"><span data-stu-id="72693-118">Web App RoutingRule.</span></span>
<span data-ttu-id="72693-119">範例：-RoutingRule @{ActionHostName=$slot。DefaultHostName ;ReroutePercentage=$ReroutePercentage ;Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="72693-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72693-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="72693-120">-WebAppName</span></span>
<span data-ttu-id="72693-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="72693-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72693-122">-確認</span><span class="sxs-lookup"><span data-stu-id="72693-122">-Confirm</span></span>
<span data-ttu-id="72693-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="72693-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72693-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72693-124">-WhatIf</span></span>
<span data-ttu-id="72693-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72693-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72693-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72693-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72693-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72693-127">CommonParameters</span></span>
<span data-ttu-id="72693-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72693-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72693-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72693-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72693-130">輸入</span><span class="sxs-lookup"><span data-stu-id="72693-130">INPUTS</span></span>

### <span data-ttu-id="72693-131">沒有</span><span class="sxs-lookup"><span data-stu-id="72693-131">None</span></span>

## <span data-ttu-id="72693-132">輸出</span><span class="sxs-lookup"><span data-stu-id="72693-132">OUTPUTS</span></span>

### <span data-ttu-id="72693-133">Microsoft.Azure.management.Websites.models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="72693-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="72693-134">筆記</span><span class="sxs-lookup"><span data-stu-id="72693-134">NOTES</span></span>

## <span data-ttu-id="72693-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="72693-135">RELATED LINKS</span></span>

[<span data-ttu-id="72693-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="72693-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="72693-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="72693-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="72693-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="72693-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)