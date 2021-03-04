---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916564"
---
# <span data-ttu-id="da5eb-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="da5eb-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="da5eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="da5eb-103">為一個組獲取持續執行腳本動作，並按時間順序列出這些動作，或獲得指定的持續腳本動作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="da5eb-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="da5eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="da5eb-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da5eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="da5eb-105">DESCRIPTION</span></span>
<span data-ttu-id="da5eb-106">**Get-AzHDInsightPersistedScriptAction** Cmdlet 會取得 Azure HDInsight 集區之持續腳本動作，並按時間順序列出這些動作，或取得指定持續腳本動作的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="da5eb-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="da5eb-107">例子</span><span class="sxs-lookup"><span data-stu-id="da5eb-107">EXAMPLES</span></span>

### <span data-ttu-id="da5eb-108">範例 1：取得在組集中的保留腳本動作</span><span class="sxs-lookup"><span data-stu-id="da5eb-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="da5eb-109">此命令會持續在名為 your-hadoop-001 的組上執行腳本動作。</span><span class="sxs-lookup"><span data-stu-id="da5eb-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="da5eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="da5eb-110">PARAMETERS</span></span>

### <span data-ttu-id="da5eb-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="da5eb-111">-ClusterName</span></span>
<span data-ttu-id="da5eb-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="da5eb-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5eb-113">-DefaultProfile</span></span>
<span data-ttu-id="da5eb-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="da5eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da5eb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="da5eb-115">-Name</span></span>
<span data-ttu-id="da5eb-116">指定保留腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="da5eb-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="da5eb-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="da5eb-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5eb-119">CommonParameters</span></span>
<span data-ttu-id="da5eb-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da5eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5eb-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da5eb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5eb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="da5eb-122">INPUTS</span></span>

### <span data-ttu-id="da5eb-123">沒有</span><span class="sxs-lookup"><span data-stu-id="da5eb-123">None</span></span>

## <span data-ttu-id="da5eb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="da5eb-124">OUTPUTS</span></span>

### <span data-ttu-id="da5eb-125">Microsoft.Azure.Commands.HDInsight.models.management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="da5eb-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="da5eb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="da5eb-126">NOTES</span></span>

## <span data-ttu-id="da5eb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="da5eb-127">RELATED LINKS</span></span>

[<span data-ttu-id="da5eb-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="da5eb-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="da5eb-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="da5eb-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


