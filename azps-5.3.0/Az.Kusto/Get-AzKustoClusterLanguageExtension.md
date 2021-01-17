---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435364"
---
# <span data-ttu-id="bf277-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="bf277-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="bf277-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf277-102">SYNOPSIS</span></span>
<span data-ttu-id="bf277-103">傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="bf277-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bf277-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf277-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf277-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf277-105">DESCRIPTION</span></span>
<span data-ttu-id="bf277-106">傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="bf277-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bf277-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf277-107">EXAMPLES</span></span>

### <span data-ttu-id="bf277-108">範例1：列出為群集設定的所有語言擴充功能</span><span class="sxs-lookup"><span data-stu-id="bf277-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="bf277-109">上述命令會傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="bf277-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bf277-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf277-110">PARAMETERS</span></span>

### <span data-ttu-id="bf277-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bf277-111">-ClusterName</span></span>
<span data-ttu-id="bf277-112">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf277-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="bf277-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf277-113">-DefaultProfile</span></span>
<span data-ttu-id="bf277-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf277-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf277-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf277-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf277-116">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf277-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="bf277-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf277-117">-SubscriptionId</span></span>
<span data-ttu-id="bf277-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="bf277-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf277-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bf277-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bf277-120">-確認</span><span class="sxs-lookup"><span data-stu-id="bf277-120">-Confirm</span></span>
<span data-ttu-id="bf277-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf277-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf277-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf277-122">-WhatIf</span></span>
<span data-ttu-id="bf277-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf277-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf277-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf277-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf277-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf277-125">CommonParameters</span></span>
<span data-ttu-id="bf277-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf277-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf277-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf277-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf277-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bf277-128">INPUTS</span></span>

## <span data-ttu-id="bf277-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bf277-129">OUTPUTS</span></span>

### <span data-ttu-id="bf277-130">ILanguageExtension （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="bf277-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="bf277-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bf277-131">NOTES</span></span>

<span data-ttu-id="bf277-132">別名</span><span class="sxs-lookup"><span data-stu-id="bf277-132">ALIASES</span></span>

## <span data-ttu-id="bf277-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf277-133">RELATED LINKS</span></span>

