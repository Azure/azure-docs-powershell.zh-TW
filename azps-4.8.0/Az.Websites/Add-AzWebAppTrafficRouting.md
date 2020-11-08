---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128392"
---
# <span data-ttu-id="da5d8-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="da5d8-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="da5d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="da5d8-103">在槽中新增路由規則。</span><span class="sxs-lookup"><span data-stu-id="da5d8-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="da5d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="da5d8-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da5d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="da5d8-105">DESCRIPTION</span></span>
<span data-ttu-id="da5d8-106">**載入 AzWebAppTrafficRouting** Cmdlet 會將路由規則新增至 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="da5d8-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="da5d8-107">示例</span><span class="sxs-lookup"><span data-stu-id="da5d8-107">EXAMPLES</span></span>

### <span data-ttu-id="da5d8-108">範例1新增路由規則，以將15% 的生產 traffice 傳送到 Stg 槽</span><span class="sxs-lookup"><span data-stu-id="da5d8-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="da5d8-109">這個命令會新增路由規則，以將15% 的生產 traffice 傳送到 Stg 槽</span><span class="sxs-lookup"><span data-stu-id="da5d8-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="da5d8-110">範例2新增路由規則，將生產 traffice 轉換成以遞增方式從50% 轉移到90% 的 Stg 槽範圍。</span><span class="sxs-lookup"><span data-stu-id="da5d8-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="da5d8-111">這個命令會新增一個路由規則，將生產 traffice 轉換成以遞增方式從50% 轉移到90% 的 Stg 槽範圍。</span><span class="sxs-lookup"><span data-stu-id="da5d8-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="da5d8-112">參數</span><span class="sxs-lookup"><span data-stu-id="da5d8-112">PARAMETERS</span></span>

### <span data-ttu-id="da5d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5d8-113">-DefaultProfile</span></span>
<span data-ttu-id="da5d8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da5d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="da5d8-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="da5d8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="da5d8-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="da5d8-117">-RoutingRule</span></span>
<span data-ttu-id="da5d8-118">Web App RoutingRule。</span><span class="sxs-lookup"><span data-stu-id="da5d8-118">Web App RoutingRule.</span></span>
<span data-ttu-id="da5d8-119">範例：-RoutingRule @ {ActionHostName = $slot。DefaultHostName ;ReroutePercentage = $ReroutePercentage;名稱 = $slotName}</span><span class="sxs-lookup"><span data-stu-id="da5d8-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="da5d8-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="da5d8-120">-WebAppName</span></span>
<span data-ttu-id="da5d8-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="da5d8-121">WebApp Name</span></span>

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

### <span data-ttu-id="da5d8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="da5d8-122">-Confirm</span></span>
<span data-ttu-id="da5d8-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da5d8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5d8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da5d8-124">-WhatIf</span></span>
<span data-ttu-id="da5d8-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da5d8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da5d8-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da5d8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5d8-127">CommonParameters</span></span>
<span data-ttu-id="da5d8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da5d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5d8-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da5d8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5d8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="da5d8-130">INPUTS</span></span>

### <span data-ttu-id="da5d8-131">所有</span><span class="sxs-lookup"><span data-stu-id="da5d8-131">None</span></span>

## <span data-ttu-id="da5d8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="da5d8-132">OUTPUTS</span></span>

### <span data-ttu-id="da5d8-133">RampUpRule 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="da5d8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="da5d8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="da5d8-134">NOTES</span></span>

## <span data-ttu-id="da5d8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="da5d8-135">RELATED LINKS</span></span>
[<span data-ttu-id="da5d8-136">更新-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="da5d8-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="da5d8-137">AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="da5d8-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="da5d8-138">移除-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="da5d8-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)