---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909905"
---
# <span data-ttu-id="166a9-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="166a9-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="166a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="166a9-102">SYNOPSIS</span></span>
<span data-ttu-id="166a9-103">新增路由規則至插槽。</span><span class="sxs-lookup"><span data-stu-id="166a9-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="166a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="166a9-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166a9-105">描述</span><span class="sxs-lookup"><span data-stu-id="166a9-105">DESCRIPTION</span></span>
<span data-ttu-id="166a9-106">**Add-AzWebAppTrafficRoudlet** 會新增路由規則至 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="166a9-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="166a9-107">例子</span><span class="sxs-lookup"><span data-stu-id="166a9-107">EXAMPLES</span></span>

### <span data-ttu-id="166a9-108">範例 1 新增路由規則以將 15% 生產流量轉移到 Stg slot</span><span class="sxs-lookup"><span data-stu-id="166a9-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="166a9-109">此命令會新增路由規則，將 15% 生產流量轉移到 Stg slot</span><span class="sxs-lookup"><span data-stu-id="166a9-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="166a9-110">範例 2 新增路由規則，以增量方式將生產流量轉移到 Stg slot 範圍從 50% 到 90%。</span><span class="sxs-lookup"><span data-stu-id="166a9-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="166a9-111">此命令會新增路由規則，以增量方式將生產流量傳輸至 Stg slot 範圍從 50% 到 90%。</span><span class="sxs-lookup"><span data-stu-id="166a9-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="166a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="166a9-112">PARAMETERS</span></span>

### <span data-ttu-id="166a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166a9-113">-DefaultProfile</span></span>
<span data-ttu-id="166a9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="166a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="166a9-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="166a9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="166a9-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="166a9-117">-RoutingRule</span></span>
<span data-ttu-id="166a9-118">Web App 路由規則。</span><span class="sxs-lookup"><span data-stu-id="166a9-118">Web App RoutingRule.</span></span>
<span data-ttu-id="166a9-119">範例：-RoutingRule @{ActionHostName=$slot。DefaultHostName ;ReroutePercentage=$ReroutePercentage ;Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="166a9-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="166a9-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="166a9-120">-WebAppName</span></span>
<span data-ttu-id="166a9-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="166a9-121">WebApp Name</span></span>

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

### <span data-ttu-id="166a9-122">-確認</span><span class="sxs-lookup"><span data-stu-id="166a9-122">-Confirm</span></span>
<span data-ttu-id="166a9-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="166a9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166a9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166a9-124">-WhatIf</span></span>
<span data-ttu-id="166a9-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="166a9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="166a9-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="166a9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="166a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166a9-127">CommonParameters</span></span>
<span data-ttu-id="166a9-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="166a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166a9-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="166a9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166a9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="166a9-130">INPUTS</span></span>

### <span data-ttu-id="166a9-131">沒有</span><span class="sxs-lookup"><span data-stu-id="166a9-131">None</span></span>

## <span data-ttu-id="166a9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="166a9-132">OUTPUTS</span></span>

### <span data-ttu-id="166a9-133">Microsoft.Azure.management.Websites.models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="166a9-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="166a9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="166a9-134">NOTES</span></span>

## <span data-ttu-id="166a9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="166a9-135">RELATED LINKS</span></span>
[<span data-ttu-id="166a9-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="166a9-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="166a9-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="166a9-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="166a9-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="166a9-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
