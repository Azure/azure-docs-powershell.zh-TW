---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 85c69786c75ea809fa5ffaea754ae444479673dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905041"
---
# <span data-ttu-id="28813-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="28813-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="28813-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28813-102">SYNOPSIS</span></span>
<span data-ttu-id="28813-103">會返回可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="28813-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="28813-104">語法</span><span class="sxs-lookup"><span data-stu-id="28813-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28813-105">描述</span><span class="sxs-lookup"><span data-stu-id="28813-105">DESCRIPTION</span></span>
<span data-ttu-id="28813-106">會返回可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="28813-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="28813-107">例子</span><span class="sxs-lookup"><span data-stu-id="28813-107">EXAMPLES</span></span>

### <span data-ttu-id="28813-108">範例 1：列出該組組的所有語言延伸模組</span><span class="sxs-lookup"><span data-stu-id="28813-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="28813-109">上述命令會返回可在 KQL 查詢內執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="28813-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="28813-110">參數</span><span class="sxs-lookup"><span data-stu-id="28813-110">PARAMETERS</span></span>

### <span data-ttu-id="28813-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="28813-111">-ClusterName</span></span>
<span data-ttu-id="28813-112">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="28813-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="28813-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28813-113">-DefaultProfile</span></span>
<span data-ttu-id="28813-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28813-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28813-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28813-115">-ResourceGroupName</span></span>
<span data-ttu-id="28813-116">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="28813-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="28813-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28813-117">-SubscriptionId</span></span>
<span data-ttu-id="28813-118">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="28813-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="28813-119">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="28813-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28813-120">-確認</span><span class="sxs-lookup"><span data-stu-id="28813-120">-Confirm</span></span>
<span data-ttu-id="28813-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28813-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28813-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28813-122">-WhatIf</span></span>
<span data-ttu-id="28813-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28813-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28813-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28813-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28813-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28813-125">CommonParameters</span></span>
<span data-ttu-id="28813-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28813-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28813-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28813-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28813-128">輸入</span><span class="sxs-lookup"><span data-stu-id="28813-128">INPUTS</span></span>

## <span data-ttu-id="28813-129">輸出</span><span class="sxs-lookup"><span data-stu-id="28813-129">OUTPUTS</span></span>

### <span data-ttu-id="28813-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="28813-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="28813-131">筆記</span><span class="sxs-lookup"><span data-stu-id="28813-131">NOTES</span></span>

<span data-ttu-id="28813-132">別名</span><span class="sxs-lookup"><span data-stu-id="28813-132">ALIASES</span></span>

## <span data-ttu-id="28813-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="28813-133">RELATED LINKS</span></span>

