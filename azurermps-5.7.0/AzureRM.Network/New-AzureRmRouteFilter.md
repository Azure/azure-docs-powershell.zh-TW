---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 9ba5f47427dc8f542e1475a8431f5d82c63c5974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625875"
---
# <span data-ttu-id="aaee0-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aaee0-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="aaee0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaee0-102">SYNOPSIS</span></span>
<span data-ttu-id="aaee0-103">建立路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="aaee0-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaee0-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaee0-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaee0-105">說明</span><span class="sxs-lookup"><span data-stu-id="aaee0-105">DESCRIPTION</span></span>
<span data-ttu-id="aaee0-106">New-AzureRmRouteFilter Cmdlet 會建立 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="aaee0-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="aaee0-107">示例</span><span class="sxs-lookup"><span data-stu-id="aaee0-107">EXAMPLES</span></span>

### <span data-ttu-id="aaee0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aaee0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="aaee0-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="aaee0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="aaee0-110">參數</span><span class="sxs-lookup"><span data-stu-id="aaee0-110">PARAMETERS</span></span>

### <span data-ttu-id="aaee0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaee0-111">-AsJob</span></span>
<span data-ttu-id="aaee0-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aaee0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aaee0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaee0-113">-DefaultProfile</span></span>
<span data-ttu-id="aaee0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aaee0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaee0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aaee0-115">-Force</span></span>
<span data-ttu-id="aaee0-116">表示此 Cmdlet 會建立路由資料表，即使已存在具有相同名稱的路由篩選器也一樣。</span><span class="sxs-lookup"><span data-stu-id="aaee0-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="aaee0-117">-位置</span><span class="sxs-lookup"><span data-stu-id="aaee0-117">-Location</span></span>
<span data-ttu-id="aaee0-118">指定此 Cmdlet 建立路由篩選器的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="aaee0-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaee0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="aaee0-119">-Name</span></span>
<span data-ttu-id="aaee0-120">指定路由篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaee0-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaee0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaee0-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaee0-122">指定此 Cmdlet 用來建立路由篩選器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaee0-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaee0-123">-規則</span><span class="sxs-lookup"><span data-stu-id="aaee0-123">-Rule</span></span>
<span data-ttu-id="aaee0-124">指定路由篩選規則物件的陣列，以與路由篩選器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="aaee0-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaee0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaee0-125">-Tag</span></span>
<span data-ttu-id="aaee0-126">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="aaee0-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aaee0-127">例如：</span><span class="sxs-lookup"><span data-stu-id="aaee0-127">For example:</span></span>

<span data-ttu-id="aaee0-128">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="aaee0-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaee0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="aaee0-129">-Confirm</span></span>
<span data-ttu-id="aaee0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aaee0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaee0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaee0-131">-WhatIf</span></span>
<span data-ttu-id="aaee0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aaee0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaee0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aaee0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaee0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaee0-134">CommonParameters</span></span>
<span data-ttu-id="aaee0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaee0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaee0-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aaee0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaee0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="aaee0-137">INPUTS</span></span>

### <span data-ttu-id="aaee0-138">所有</span><span class="sxs-lookup"><span data-stu-id="aaee0-138">None</span></span>
<span data-ttu-id="aaee0-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="aaee0-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aaee0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="aaee0-140">OUTPUTS</span></span>

### <span data-ttu-id="aaee0-141">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aaee0-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="aaee0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="aaee0-142">NOTES</span></span>
<span data-ttu-id="aaee0-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="aaee0-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="aaee0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaee0-144">RELATED LINKS</span></span>

[<span data-ttu-id="aaee0-145">AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aaee0-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="aaee0-146">新-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaee0-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="aaee0-147">移除-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aaee0-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="aaee0-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aaee0-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
