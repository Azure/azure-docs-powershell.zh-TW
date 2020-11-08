---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128703"
---
# <span data-ttu-id="e612f-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e612f-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="e612f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e612f-102">SYNOPSIS</span></span>
<span data-ttu-id="e612f-103">在 HDInsight 群集中啟用監視，並將相關的記錄傳送到 [啟用期間] 指定的監視工作區。</span><span class="sxs-lookup"><span data-stu-id="e612f-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="e612f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e612f-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e612f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e612f-105">DESCRIPTION</span></span>
<span data-ttu-id="e612f-106">**Enable-AzHDInsightMonitoring** Cmdlet 可在 Azure HDInsight 群集中啟用監視。</span><span class="sxs-lookup"><span data-stu-id="e612f-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e612f-107">示例</span><span class="sxs-lookup"><span data-stu-id="e612f-107">EXAMPLES</span></span>

### <span data-ttu-id="e612f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e612f-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e612f-109">系統會在 HDInsight 群集上啟用 [監視]，並將相關的記錄傳送到 [監視] 工作區（含 id 1d364e89-bb71-4503-aa3d-a23535aea7bd）。</span><span class="sxs-lookup"><span data-stu-id="e612f-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="e612f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e612f-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e612f-111">系統會在 HDInsight 群集上啟用 [監視]，並將相關的記錄傳送到 [監視] 工作區（含 id 1d364e89-bb71-4503-aa3d-a23535aea7bd）。</span><span class="sxs-lookup"><span data-stu-id="e612f-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="e612f-112">參數</span><span class="sxs-lookup"><span data-stu-id="e612f-112">PARAMETERS</span></span>

### <span data-ttu-id="e612f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e612f-113">-DefaultProfile</span></span>
<span data-ttu-id="e612f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e612f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e612f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e612f-115">-Name</span></span>
<span data-ttu-id="e612f-116">要啟用監視的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="e612f-116">The name of the cluster to enable monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e612f-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e612f-117">-PrimaryKey</span></span>
<span data-ttu-id="e612f-118">監控工作區的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="e612f-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e612f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e612f-119">-ResourceGroupName</span></span>
<span data-ttu-id="e612f-120">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e612f-120">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e612f-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e612f-121">-WorkspaceId</span></span>
<span data-ttu-id="e612f-122">監視工作區的 id。</span><span class="sxs-lookup"><span data-stu-id="e612f-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e612f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e612f-123">-Confirm</span></span>
<span data-ttu-id="e612f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e612f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e612f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e612f-125">-WhatIf</span></span>
<span data-ttu-id="e612f-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e612f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e612f-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e612f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e612f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e612f-128">CommonParameters</span></span>
<span data-ttu-id="e612f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e612f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e612f-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e612f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e612f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e612f-131">INPUTS</span></span>

### <span data-ttu-id="e612f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e612f-132">System.String</span></span>

## <span data-ttu-id="e612f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e612f-133">OUTPUTS</span></span>

### <span data-ttu-id="e612f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e612f-134">System.Boolean</span></span>

## <span data-ttu-id="e612f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e612f-135">NOTES</span></span>

## <span data-ttu-id="e612f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e612f-136">RELATED LINKS</span></span>