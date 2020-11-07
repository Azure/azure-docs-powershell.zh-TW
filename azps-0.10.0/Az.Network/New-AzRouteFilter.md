---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794243"
---
# <span data-ttu-id="eb35d-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eb35d-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="eb35d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb35d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb35d-103">建立路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="eb35d-103">Creates a route filter.</span></span>

## <span data-ttu-id="eb35d-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb35d-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb35d-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb35d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb35d-106">New-AzRouteFilter Cmdlet 會建立 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="eb35d-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="eb35d-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb35d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb35d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb35d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="eb35d-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="eb35d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="eb35d-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb35d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb35d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb35d-111">-AsJob</span></span>
<span data-ttu-id="eb35d-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb35d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb35d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb35d-113">-DefaultProfile</span></span>
<span data-ttu-id="eb35d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb35d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb35d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eb35d-115">-Force</span></span>
<span data-ttu-id="eb35d-116">表示此 Cmdlet 會建立路由資料表，即使已存在具有相同名稱的路由篩選器也一樣。</span><span class="sxs-lookup"><span data-stu-id="eb35d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="eb35d-117">-位置</span><span class="sxs-lookup"><span data-stu-id="eb35d-117">-Location</span></span>
<span data-ttu-id="eb35d-118">指定此 Cmdlet 建立路由篩選器的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="eb35d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="eb35d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb35d-119">-Name</span></span>
<span data-ttu-id="eb35d-120">指定路由篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb35d-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="eb35d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb35d-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb35d-122">指定此 Cmdlet 用來建立路由篩選器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb35d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="eb35d-123">-規則</span><span class="sxs-lookup"><span data-stu-id="eb35d-123">-Rule</span></span>
<span data-ttu-id="eb35d-124">指定路由篩選規則物件的陣列，以與路由篩選器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="eb35d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="eb35d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb35d-125">-Tag</span></span>
<span data-ttu-id="eb35d-126">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="eb35d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eb35d-127">例如：</span><span class="sxs-lookup"><span data-stu-id="eb35d-127">For example:</span></span>

<span data-ttu-id="eb35d-128">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eb35d-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eb35d-129">-確認</span><span class="sxs-lookup"><span data-stu-id="eb35d-129">-Confirm</span></span>
<span data-ttu-id="eb35d-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb35d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb35d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb35d-131">-WhatIf</span></span>
<span data-ttu-id="eb35d-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb35d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb35d-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb35d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb35d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb35d-134">CommonParameters</span></span>
<span data-ttu-id="eb35d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb35d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb35d-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb35d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb35d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="eb35d-137">INPUTS</span></span>

## <span data-ttu-id="eb35d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="eb35d-138">OUTPUTS</span></span>

### <span data-ttu-id="eb35d-139">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eb35d-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="eb35d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="eb35d-140">NOTES</span></span>
<span data-ttu-id="eb35d-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="eb35d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eb35d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb35d-142">RELATED LINKS</span></span>

[<span data-ttu-id="eb35d-143">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eb35d-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="eb35d-144">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eb35d-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="eb35d-145">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eb35d-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="eb35d-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eb35d-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
