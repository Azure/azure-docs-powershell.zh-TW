---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: f701d0c5e0ea2d8f4ce5ded850d131c6c066e9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449159"
---
# <span data-ttu-id="2e1eb-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="2e1eb-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="2e1eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1eb-103">在 HDInsight 群集中停用作業管理套件 (OMS) ，而相關的記錄將停止流入在啟用期間指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e1eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e1eb-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e1eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1eb-106">**Disable AzureRmHDInsightOperationsManagementSuite** Cmdlet 會停用 Azure HDInsight 群集中 (OMS) 的 Operations Management Suite。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2e1eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="2e1eb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2e1eb-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="2e1eb-109">將會在 HDInsight 群集上停用作業管理套件 (OMS) ，而相關記錄將停止流動至 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="2e1eb-110">範例2</span><span class="sxs-lookup"><span data-stu-id="2e1eb-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="2e1eb-111">將會在 HDInsight 群集上停用作業管理套件 (OMS) ，而相關記錄將停止流動至 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="2e1eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="2e1eb-112">PARAMETERS</span></span>

### <span data-ttu-id="2e1eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1eb-113">-DefaultProfile</span></span>
<span data-ttu-id="2e1eb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e1eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e1eb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e1eb-115">-Name</span></span>
<span data-ttu-id="2e1eb-116">要停用作業管理套件 (OMS) 的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="2e1eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e1eb-118">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="2e1eb-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2e1eb-119">-Confirm</span></span>
<span data-ttu-id="2e1eb-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e1eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e1eb-121">-WhatIf</span></span>
<span data-ttu-id="2e1eb-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e1eb-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e1eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1eb-124">CommonParameters</span></span>
<span data-ttu-id="2e1eb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1eb-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e1eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1eb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2e1eb-127">INPUTS</span></span>

### <span data-ttu-id="2e1eb-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2e1eb-128">System.String</span></span>

## <span data-ttu-id="2e1eb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2e1eb-129">OUTPUTS</span></span>

### <span data-ttu-id="2e1eb-130">OperationResource 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="2e1eb-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="2e1eb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2e1eb-131">NOTES</span></span>

## <span data-ttu-id="2e1eb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e1eb-132">RELATED LINKS</span></span>
