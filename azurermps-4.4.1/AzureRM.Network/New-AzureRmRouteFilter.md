---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448133"
---
# <span data-ttu-id="9d601-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d601-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9d601-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d601-102">SYNOPSIS</span></span>
<span data-ttu-id="9d601-103">建立路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="9d601-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d601-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d601-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d601-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d601-105">DESCRIPTION</span></span>
<span data-ttu-id="9d601-106">New-AzureRmRouteFilter Cmdlet 會建立 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="9d601-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="9d601-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d601-107">EXAMPLES</span></span>

### <span data-ttu-id="9d601-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9d601-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="9d601-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="9d601-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9d601-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d601-110">PARAMETERS</span></span>

### <span data-ttu-id="9d601-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9d601-111">-Force</span></span>
<span data-ttu-id="9d601-112">表示此 Cmdlet 會建立路由資料表，即使已存在具有相同名稱的路由篩選器也一樣。</span><span class="sxs-lookup"><span data-stu-id="9d601-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="9d601-113">-位置</span><span class="sxs-lookup"><span data-stu-id="9d601-113">-Location</span></span>
<span data-ttu-id="9d601-114">指定此 Cmdlet 建立路由篩選器的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="9d601-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="9d601-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d601-115">-Name</span></span>
<span data-ttu-id="9d601-116">指定路由篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d601-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="9d601-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d601-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d601-118">指定此 Cmdlet 用來建立路由篩選器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d601-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="9d601-119">-規則</span><span class="sxs-lookup"><span data-stu-id="9d601-119">-Rule</span></span>
<span data-ttu-id="9d601-120">指定路由篩選規則物件的陣列，以與路由篩選器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="9d601-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="9d601-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d601-121">-Tag</span></span>
<span data-ttu-id="9d601-122">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="9d601-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9d601-123">例如：</span><span class="sxs-lookup"><span data-stu-id="9d601-123">For example:</span></span>

<span data-ttu-id="9d601-124">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9d601-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9d601-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9d601-125">-Confirm</span></span>
<span data-ttu-id="9d601-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d601-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d601-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d601-127">-WhatIf</span></span>
<span data-ttu-id="9d601-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d601-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d601-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d601-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d601-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d601-130">-DefaultProfile</span></span>
<span data-ttu-id="9d601-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d601-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d601-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d601-132">CommonParameters</span></span>
<span data-ttu-id="9d601-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d601-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d601-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d601-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d601-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9d601-135">INPUTS</span></span>

## <span data-ttu-id="9d601-136">輸出</span><span class="sxs-lookup"><span data-stu-id="9d601-136">OUTPUTS</span></span>

### <span data-ttu-id="9d601-137">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d601-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9d601-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9d601-138">NOTES</span></span>
<span data-ttu-id="9d601-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="9d601-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9d601-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d601-140">RELATED LINKS</span></span>

[<span data-ttu-id="9d601-141">AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d601-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="9d601-142">新-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d601-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="9d601-143">移除-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d601-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="9d601-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d601-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
