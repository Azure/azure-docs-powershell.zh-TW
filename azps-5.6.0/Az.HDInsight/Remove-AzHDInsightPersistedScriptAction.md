---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905394"
---
# <span data-ttu-id="bf9ae-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bf9ae-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="bf9ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ae-103">從 HDInsight 集區移除持續腳本動作。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="bf9ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf9ae-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf9ae-105">描述</span><span class="sxs-lookup"><span data-stu-id="bf9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9ae-106">**Remove-AzHDInsightPersistedScriptAction** Cmdlet 會從指定的 Azure HDInsight 集區持續腳本動作清單中移除持續腳本動作。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="bf9ae-107">當已移除的腳本縮放時，系統將不再執行該腳本。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="bf9ae-108">例子</span><span class="sxs-lookup"><span data-stu-id="bf9ae-108">EXAMPLES</span></span>

### <span data-ttu-id="bf9ae-109">範例 1：從組集中的保留腳本動作清單中移除腳本動作</span><span class="sxs-lookup"><span data-stu-id="bf9ae-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="bf9ae-110">此命令會從指定組上的持續腳本動作清單中，移除名為 Scriptaction 的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="bf9ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="bf9ae-111">PARAMETERS</span></span>

### <span data-ttu-id="bf9ae-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bf9ae-112">-ClusterName</span></span>
<span data-ttu-id="bf9ae-113">指定組名。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bf9ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ae-114">-DefaultProfile</span></span>
<span data-ttu-id="bf9ae-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bf9ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf9ae-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf9ae-116">-Name</span></span>
<span data-ttu-id="bf9ae-117">指定要移除的保留腳本動作名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="bf9ae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ae-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf9ae-119">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bf9ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ae-120">CommonParameters</span></span>
<span data-ttu-id="bf9ae-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf9ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ae-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf9ae-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ae-123">輸入</span><span class="sxs-lookup"><span data-stu-id="bf9ae-123">INPUTS</span></span>

### <span data-ttu-id="bf9ae-124">沒有</span><span class="sxs-lookup"><span data-stu-id="bf9ae-124">None</span></span>

## <span data-ttu-id="bf9ae-125">輸出</span><span class="sxs-lookup"><span data-stu-id="bf9ae-125">OUTPUTS</span></span>

### <span data-ttu-id="bf9ae-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="bf9ae-126">System.Void</span></span>

## <span data-ttu-id="bf9ae-127">筆記</span><span class="sxs-lookup"><span data-stu-id="bf9ae-127">NOTES</span></span>

## <span data-ttu-id="bf9ae-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf9ae-128">RELATED LINKS</span></span>

[<span data-ttu-id="bf9ae-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bf9ae-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="bf9ae-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bf9ae-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


