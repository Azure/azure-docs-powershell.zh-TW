---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278862"
---
# <span data-ttu-id="4aa48-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4aa48-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="4aa48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4aa48-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa48-103">傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="4aa48-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4aa48-104">句法</span><span class="sxs-lookup"><span data-stu-id="4aa48-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4aa48-105">說明</span><span class="sxs-lookup"><span data-stu-id="4aa48-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa48-106">傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="4aa48-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4aa48-107">示例</span><span class="sxs-lookup"><span data-stu-id="4aa48-107">EXAMPLES</span></span>

### <span data-ttu-id="4aa48-108">範例1：列出為群集設定的所有語言擴充功能</span><span class="sxs-lookup"><span data-stu-id="4aa48-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="4aa48-109">上述命令會傳回可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="4aa48-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4aa48-110">參數</span><span class="sxs-lookup"><span data-stu-id="4aa48-110">PARAMETERS</span></span>

### <span data-ttu-id="4aa48-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4aa48-111">-ClusterName</span></span>
<span data-ttu-id="4aa48-112">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aa48-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4aa48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa48-113">-DefaultProfile</span></span>
<span data-ttu-id="4aa48-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4aa48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa48-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa48-115">-ResourceGroupName</span></span>
<span data-ttu-id="4aa48-116">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aa48-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4aa48-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aa48-117">-SubscriptionId</span></span>
<span data-ttu-id="4aa48-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4aa48-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4aa48-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4aa48-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4aa48-120">-確認</span><span class="sxs-lookup"><span data-stu-id="4aa48-120">-Confirm</span></span>
<span data-ttu-id="4aa48-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4aa48-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa48-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa48-122">-WhatIf</span></span>
<span data-ttu-id="4aa48-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4aa48-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa48-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4aa48-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa48-125">CommonParameters</span></span>
<span data-ttu-id="4aa48-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4aa48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa48-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4aa48-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa48-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4aa48-128">INPUTS</span></span>

## <span data-ttu-id="4aa48-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4aa48-129">OUTPUTS</span></span>

### <span data-ttu-id="4aa48-130">ILanguageExtension （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="4aa48-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="4aa48-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4aa48-131">NOTES</span></span>

<span data-ttu-id="4aa48-132">別名</span><span class="sxs-lookup"><span data-stu-id="4aa48-132">ALIASES</span></span>

## <span data-ttu-id="4aa48-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4aa48-133">RELATED LINKS</span></span>

