---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142316"
---
# <span data-ttu-id="249a3-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="249a3-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="249a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="249a3-102">SYNOPSIS</span></span>
<span data-ttu-id="249a3-103">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="249a3-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="249a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="249a3-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="249a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="249a3-105">DESCRIPTION</span></span>
<span data-ttu-id="249a3-106">**AzHDInsightPersistedScriptAction** Cmdlet 會取得 Azure HDInsight 群集的持久化腳本動作，並依時間順序列出這些作業，或取得指定的永久性腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="249a3-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="249a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="249a3-107">EXAMPLES</span></span>

### <span data-ttu-id="249a3-108">範例1：在群集上取得持久化腳本動作</span><span class="sxs-lookup"><span data-stu-id="249a3-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="249a3-109">這個命令會在名為 [hadoop-001] 的群集上取得持續執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="249a3-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="249a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="249a3-110">PARAMETERS</span></span>

### <span data-ttu-id="249a3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="249a3-111">-ClusterName</span></span>
<span data-ttu-id="249a3-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="249a3-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="249a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249a3-113">-DefaultProfile</span></span>
<span data-ttu-id="249a3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="249a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="249a3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="249a3-115">-Name</span></span>
<span data-ttu-id="249a3-116">指定持久化腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="249a3-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="249a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="249a3-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="249a3-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="249a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249a3-119">CommonParameters</span></span>
<span data-ttu-id="249a3-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="249a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249a3-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="249a3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249a3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="249a3-122">INPUTS</span></span>

### <span data-ttu-id="249a3-123">所有</span><span class="sxs-lookup"><span data-stu-id="249a3-123">None</span></span>

## <span data-ttu-id="249a3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="249a3-124">OUTPUTS</span></span>

### <span data-ttu-id="249a3-125">AzureHDInsightRuntimeScriptAction 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="249a3-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="249a3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="249a3-126">NOTES</span></span>

## <span data-ttu-id="249a3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="249a3-127">RELATED LINKS</span></span>

[<span data-ttu-id="249a3-128">移除-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="249a3-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="249a3-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="249a3-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


