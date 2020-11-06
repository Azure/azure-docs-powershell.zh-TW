---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 7e24fac68efa4392944179d4a0618c0ad487c03f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455347"
---
# <span data-ttu-id="935bf-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="935bf-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="935bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="935bf-102">SYNOPSIS</span></span>
<span data-ttu-id="935bf-103">從 HDInsight 群集移除持久的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="935bf-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="935bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="935bf-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="935bf-105">DESCRIPTION</span></span>
<span data-ttu-id="935bf-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet 會從指定的 Azure HDInsight 群集的永久性腳本動作清單中，移除持久化腳本動作。</span><span class="sxs-lookup"><span data-stu-id="935bf-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="935bf-107">當群集放大時，移除的腳本就不會再執行。</span><span class="sxs-lookup"><span data-stu-id="935bf-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="935bf-108">示例</span><span class="sxs-lookup"><span data-stu-id="935bf-108">EXAMPLES</span></span>

### <span data-ttu-id="935bf-109">範例1：在群集上從永久性腳本動作清單中移除腳本動作</span><span class="sxs-lookup"><span data-stu-id="935bf-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="935bf-110">這個命令會從指定的群集中，從持久化腳本動作清單中移除名為 Scriptaction 的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="935bf-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="935bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="935bf-111">PARAMETERS</span></span>

### <span data-ttu-id="935bf-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="935bf-112">-ClusterName</span></span>
<span data-ttu-id="935bf-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="935bf-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="935bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935bf-114">-DefaultProfile</span></span>
<span data-ttu-id="935bf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="935bf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935bf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="935bf-116">-Name</span></span>
<span data-ttu-id="935bf-117">指定要移除的持久化腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="935bf-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="935bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="935bf-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="935bf-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="935bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935bf-120">CommonParameters</span></span>
<span data-ttu-id="935bf-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="935bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935bf-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="935bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935bf-123">輸入</span><span class="sxs-lookup"><span data-stu-id="935bf-123">INPUTS</span></span>

### <span data-ttu-id="935bf-124">所有</span><span class="sxs-lookup"><span data-stu-id="935bf-124">None</span></span>

## <span data-ttu-id="935bf-125">輸出</span><span class="sxs-lookup"><span data-stu-id="935bf-125">OUTPUTS</span></span>

### <span data-ttu-id="935bf-126">System.void</span><span class="sxs-lookup"><span data-stu-id="935bf-126">System.Void</span></span>

## <span data-ttu-id="935bf-127">筆記</span><span class="sxs-lookup"><span data-stu-id="935bf-127">NOTES</span></span>

## <span data-ttu-id="935bf-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="935bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="935bf-129">AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="935bf-129">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="935bf-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="935bf-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


