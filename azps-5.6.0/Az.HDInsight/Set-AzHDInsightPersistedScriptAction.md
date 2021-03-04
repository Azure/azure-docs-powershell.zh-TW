---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910082"
---
# <span data-ttu-id="ee241-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ee241-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="ee241-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee241-102">SYNOPSIS</span></span>
<span data-ttu-id="ee241-103">將先前執行的腳本動作設定為可保存的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="ee241-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="ee241-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee241-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee241-105">描述</span><span class="sxs-lookup"><span data-stu-id="ee241-105">DESCRIPTION</span></span>
<span data-ttu-id="ee241-106">**Set-AzHDInsightPersistedScriptAction** Cmdlet 將先前執行的腳本動作設為可保存的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="ee241-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="ee241-107">指定的腳本動作必須先前成功。</span><span class="sxs-lookup"><span data-stu-id="ee241-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="ee241-108">腳本動作會每次調整 Azure HDInsight 集區時執行。</span><span class="sxs-lookup"><span data-stu-id="ee241-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="ee241-109">例子</span><span class="sxs-lookup"><span data-stu-id="ee241-109">EXAMPLES</span></span>

### <span data-ttu-id="ee241-110">範例 1：將先前成功的腳本動作設定為可持續執行，或在集區上執行放大</span><span class="sxs-lookup"><span data-stu-id="ee241-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="ee241-111">此命令將先前成功的腳本動作設定為可保存的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="ee241-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="ee241-112">參數</span><span class="sxs-lookup"><span data-stu-id="ee241-112">PARAMETERS</span></span>

### <span data-ttu-id="ee241-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ee241-113">-ClusterName</span></span>
<span data-ttu-id="ee241-114">指定組名。</span><span class="sxs-lookup"><span data-stu-id="ee241-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ee241-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee241-115">-DefaultProfile</span></span>
<span data-ttu-id="ee241-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ee241-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee241-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee241-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee241-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee241-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ee241-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="ee241-119">-ScriptExecutionId</span></span>
<span data-ttu-id="ee241-120">指定要升級為持續執行之腳本動作的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee241-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="ee241-121">此腳本動作必須已成功，才能升級。</span><span class="sxs-lookup"><span data-stu-id="ee241-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="ee241-122">您可以使用 Get-AzHDInsightScriptActionHistory 找到腳本動作執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee241-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee241-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee241-123">CommonParameters</span></span>
<span data-ttu-id="ee241-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee241-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee241-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee241-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee241-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ee241-126">INPUTS</span></span>

### <span data-ttu-id="ee241-127">沒有</span><span class="sxs-lookup"><span data-stu-id="ee241-127">None</span></span>

## <span data-ttu-id="ee241-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ee241-128">OUTPUTS</span></span>

### <span data-ttu-id="ee241-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee241-129">System.Void</span></span>

## <span data-ttu-id="ee241-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ee241-130">NOTES</span></span>

## <span data-ttu-id="ee241-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee241-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee241-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ee241-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="ee241-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ee241-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


