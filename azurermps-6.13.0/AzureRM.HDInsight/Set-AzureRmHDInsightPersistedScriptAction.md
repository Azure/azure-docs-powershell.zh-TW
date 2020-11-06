---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446997"
---
# <span data-ttu-id="9c09b-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9c09b-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="9c09b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c09b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c09b-103">將先前執行的腳本動作設為持久化的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9c09b-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c09b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c09b-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c09b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c09b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c09b-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet 會將先前執行的腳本動作設定為持久化的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9c09b-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="9c09b-107">指定的腳本動作必須先前已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9c09b-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="9c09b-108">每當 Azure HDInsight 群集放大時，腳本動作就會執行。</span><span class="sxs-lookup"><span data-stu-id="9c09b-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="9c09b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c09b-109">EXAMPLES</span></span>

### <span data-ttu-id="9c09b-110">範例1：設定先前成功的腳本動作，以保留，或在群集上執行升級</span><span class="sxs-lookup"><span data-stu-id="9c09b-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="9c09b-111">這個命令會將先前成功的腳本動作設成持久的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9c09b-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="9c09b-112">參數</span><span class="sxs-lookup"><span data-stu-id="9c09b-112">PARAMETERS</span></span>

### <span data-ttu-id="9c09b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9c09b-113">-ClusterName</span></span>
<span data-ttu-id="9c09b-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c09b-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9c09b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c09b-115">-DefaultProfile</span></span>
<span data-ttu-id="9c09b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9c09b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c09b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c09b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c09b-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c09b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9c09b-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="9c09b-119">-ScriptExecutionId</span></span>
<span data-ttu-id="9c09b-120">指定要升級以保留的腳本動作的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c09b-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="9c09b-121">此腳本動作必須已成功才能升級。</span><span class="sxs-lookup"><span data-stu-id="9c09b-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="9c09b-122">您可以使用 AzureRmHDInsightScriptActionHistory 來尋找腳本動作執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c09b-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="9c09b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c09b-123">CommonParameters</span></span>
<span data-ttu-id="9c09b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c09b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c09b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c09b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c09b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9c09b-126">INPUTS</span></span>

### <span data-ttu-id="9c09b-127">所有</span><span class="sxs-lookup"><span data-stu-id="9c09b-127">None</span></span>

## <span data-ttu-id="9c09b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9c09b-128">OUTPUTS</span></span>

### <span data-ttu-id="9c09b-129">System.void</span><span class="sxs-lookup"><span data-stu-id="9c09b-129">System.Void</span></span>

## <span data-ttu-id="9c09b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9c09b-130">NOTES</span></span>

## <span data-ttu-id="9c09b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c09b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9c09b-132">AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9c09b-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="9c09b-133">移除-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9c09b-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

