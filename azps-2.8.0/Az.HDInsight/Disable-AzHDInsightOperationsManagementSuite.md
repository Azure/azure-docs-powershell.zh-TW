---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 4f4508d38e4401198359fc816d1a94875f70940a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612317"
---
# <span data-ttu-id="42680-101">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="42680-101">Disable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="42680-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42680-102">SYNOPSIS</span></span>
<span data-ttu-id="42680-103">在 HDInsight 群集中停用作業管理套件 (OMS) ，而相關的記錄將停止流入在啟用期間指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="42680-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="42680-104">句法</span><span class="sxs-lookup"><span data-stu-id="42680-104">SYNTAX</span></span>

```
Disable-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42680-105">說明</span><span class="sxs-lookup"><span data-stu-id="42680-105">DESCRIPTION</span></span>
<span data-ttu-id="42680-106">**Disable AzHDInsightOperationsManagementSuite** Cmdlet 會停用 Azure HDInsight 群集中 (OMS) 的 Operations Management Suite。</span><span class="sxs-lookup"><span data-stu-id="42680-106">The **Disable-AzHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="42680-107">示例</span><span class="sxs-lookup"><span data-stu-id="42680-107">EXAMPLES</span></span>

### <span data-ttu-id="42680-108">範例1</span><span class="sxs-lookup"><span data-stu-id="42680-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="42680-109">將會在 HDInsight 群集上停用作業管理套件 (OMS) ，而相關記錄將停止流動至 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="42680-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="42680-110">範例2</span><span class="sxs-lookup"><span data-stu-id="42680-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="42680-111">將會在 HDInsight 群集上停用作業管理套件 (OMS) ，而相關記錄將停止流動至 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="42680-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="42680-112">參數</span><span class="sxs-lookup"><span data-stu-id="42680-112">PARAMETERS</span></span>

### <span data-ttu-id="42680-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42680-113">-DefaultProfile</span></span>
<span data-ttu-id="42680-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42680-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42680-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="42680-115">-Name</span></span>
<span data-ttu-id="42680-116">要停用作業管理套件 (OMS) 的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="42680-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42680-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42680-117">-ResourceGroupName</span></span>
<span data-ttu-id="42680-118">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="42680-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="42680-119">-確認</span><span class="sxs-lookup"><span data-stu-id="42680-119">-Confirm</span></span>
<span data-ttu-id="42680-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42680-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42680-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42680-121">-WhatIf</span></span>
<span data-ttu-id="42680-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42680-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42680-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42680-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42680-124">CommonParameters</span></span>
<span data-ttu-id="42680-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42680-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42680-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42680-127">輸入</span><span class="sxs-lookup"><span data-stu-id="42680-127">INPUTS</span></span>

### <span data-ttu-id="42680-128">System.object</span><span class="sxs-lookup"><span data-stu-id="42680-128">System.String</span></span>

## <span data-ttu-id="42680-129">輸出</span><span class="sxs-lookup"><span data-stu-id="42680-129">OUTPUTS</span></span>

### <span data-ttu-id="42680-130">OperationResource 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="42680-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="42680-131">筆記</span><span class="sxs-lookup"><span data-stu-id="42680-131">NOTES</span></span>

## <span data-ttu-id="42680-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="42680-132">RELATED LINKS</span></span>
