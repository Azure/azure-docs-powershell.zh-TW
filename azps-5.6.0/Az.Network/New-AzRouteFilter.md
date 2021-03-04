---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 9a262bd5680a9d5cd89d5ec32e3a57edbdaf60f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909506"
---
# <span data-ttu-id="84c8d-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="84c8d-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="84c8d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="84c8d-103">建立路由篩選。</span><span class="sxs-lookup"><span data-stu-id="84c8d-103">Creates a route filter.</span></span>

## <span data-ttu-id="84c8d-104">語法</span><span class="sxs-lookup"><span data-stu-id="84c8d-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84c8d-105">描述</span><span class="sxs-lookup"><span data-stu-id="84c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="84c8d-106">Cmdlet New-AzRouteFilter建立 Azure 路由篩選。</span><span class="sxs-lookup"><span data-stu-id="84c8d-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="84c8d-107">例子</span><span class="sxs-lookup"><span data-stu-id="84c8d-107">EXAMPLES</span></span>

### <span data-ttu-id="84c8d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="84c8d-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="84c8d-109">該命令會建立新的路由篩選。</span><span class="sxs-lookup"><span data-stu-id="84c8d-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="84c8d-110">參數</span><span class="sxs-lookup"><span data-stu-id="84c8d-110">PARAMETERS</span></span>

### <span data-ttu-id="84c8d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84c8d-111">-AsJob</span></span>
<span data-ttu-id="84c8d-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="84c8d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84c8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c8d-113">-DefaultProfile</span></span>
<span data-ttu-id="84c8d-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84c8d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c8d-115">-強制</span><span class="sxs-lookup"><span data-stu-id="84c8d-115">-Force</span></span>
<span data-ttu-id="84c8d-116">表示此 Cmdlet 會建立路由資料表，即使已存在相同名稱的路由篩選。</span><span class="sxs-lookup"><span data-stu-id="84c8d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="84c8d-117">-位置</span><span class="sxs-lookup"><span data-stu-id="84c8d-117">-Location</span></span>
<span data-ttu-id="84c8d-118">指定此 Cmdlet 建立路由篩選的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="84c8d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="84c8d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="84c8d-119">-Name</span></span>
<span data-ttu-id="84c8d-120">指定路由篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="84c8d-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="84c8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="84c8d-122">指定此 Cmdlet 建立路由篩選的資源組名。</span><span class="sxs-lookup"><span data-stu-id="84c8d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="84c8d-123">-規則</span><span class="sxs-lookup"><span data-stu-id="84c8d-123">-Rule</span></span>
<span data-ttu-id="84c8d-124">指定要與路由篩選建立關聯的路由篩選規則物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="84c8d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c8d-125">-標記</span><span class="sxs-lookup"><span data-stu-id="84c8d-125">-Tag</span></span>
<span data-ttu-id="84c8d-126">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="84c8d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84c8d-127">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="84c8d-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84c8d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="84c8d-128">-Confirm</span></span>
<span data-ttu-id="84c8d-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84c8d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c8d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c8d-130">-WhatIf</span></span>
<span data-ttu-id="84c8d-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84c8d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84c8d-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84c8d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c8d-133">CommonParameters</span></span>
<span data-ttu-id="84c8d-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84c8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c8d-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="84c8d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c8d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="84c8d-136">INPUTS</span></span>

### <span data-ttu-id="84c8d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="84c8d-137">System.String</span></span>

### <span data-ttu-id="84c8d-138">Microsoft.Azure.Commands.Network.models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="84c8d-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="84c8d-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="84c8d-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84c8d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="84c8d-140">OUTPUTS</span></span>

### <span data-ttu-id="84c8d-141">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="84c8d-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="84c8d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="84c8d-142">NOTES</span></span>
<span data-ttu-id="84c8d-143">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="84c8d-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="84c8d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="84c8d-144">RELATED LINKS</span></span>

[<span data-ttu-id="84c8d-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="84c8d-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="84c8d-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="84c8d-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="84c8d-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="84c8d-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="84c8d-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c8d-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="84c8d-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c8d-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="84c8d-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c8d-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="84c8d-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c8d-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="84c8d-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c8d-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
