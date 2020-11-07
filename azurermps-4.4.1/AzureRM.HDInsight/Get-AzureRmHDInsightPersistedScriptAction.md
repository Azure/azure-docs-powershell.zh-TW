---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626294"
---
# <span data-ttu-id="43a34-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43a34-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="43a34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43a34-102">SYNOPSIS</span></span>
<span data-ttu-id="43a34-103">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="43a34-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a34-104">句法</span><span class="sxs-lookup"><span data-stu-id="43a34-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a34-105">說明</span><span class="sxs-lookup"><span data-stu-id="43a34-105">DESCRIPTION</span></span>
<span data-ttu-id="43a34-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet 會取得 Azure HDInsight 群集的持久化腳本動作，並依時間順序列出這些作業，或取得指定的永久性腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="43a34-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="43a34-107">示例</span><span class="sxs-lookup"><span data-stu-id="43a34-107">EXAMPLES</span></span>

### <span data-ttu-id="43a34-108">範例1：在群集上取得持久化腳本動作</span><span class="sxs-lookup"><span data-stu-id="43a34-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="43a34-109">這個命令會在名為 [hadoop-001] 的群集上取得持續執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="43a34-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="43a34-110">參數</span><span class="sxs-lookup"><span data-stu-id="43a34-110">PARAMETERS</span></span>

### <span data-ttu-id="43a34-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="43a34-111">-ClusterName</span></span>
<span data-ttu-id="43a34-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="43a34-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="43a34-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="43a34-113">-Name</span></span>
<span data-ttu-id="43a34-114">指定持久化腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="43a34-114">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="43a34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a34-115">-ResourceGroupName</span></span>
<span data-ttu-id="43a34-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43a34-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="43a34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a34-117">-DefaultProfile</span></span>
<span data-ttu-id="43a34-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43a34-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a34-119">CommonParameters</span></span>
<span data-ttu-id="43a34-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43a34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a34-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43a34-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a34-122">輸入</span><span class="sxs-lookup"><span data-stu-id="43a34-122">INPUTS</span></span>

## <span data-ttu-id="43a34-123">輸出</span><span class="sxs-lookup"><span data-stu-id="43a34-123">OUTPUTS</span></span>

### <span data-ttu-id="43a34-124">System.object IList ' 1 [AzureHDInsightRuntimeScriptAction] （即 Azure. 命令..]</span><span class="sxs-lookup"><span data-stu-id="43a34-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="43a34-125">筆記</span><span class="sxs-lookup"><span data-stu-id="43a34-125">NOTES</span></span>

## <span data-ttu-id="43a34-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="43a34-126">RELATED LINKS</span></span>

[<span data-ttu-id="43a34-127">移除-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43a34-127">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="43a34-128">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43a34-128">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


