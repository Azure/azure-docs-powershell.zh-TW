---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457171"
---
# <span data-ttu-id="fbeec-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fbeec-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="fbeec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbeec-102">SYNOPSIS</span></span>
<span data-ttu-id="fbeec-103">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fbeec-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbeec-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbeec-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbeec-105">說明</span><span class="sxs-lookup"><span data-stu-id="fbeec-105">DESCRIPTION</span></span>
<span data-ttu-id="fbeec-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet 會取得 Azure HDInsight 群集的持久化腳本動作，並依時間順序列出這些作業，或取得指定的永久性腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fbeec-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="fbeec-107">示例</span><span class="sxs-lookup"><span data-stu-id="fbeec-107">EXAMPLES</span></span>

### <span data-ttu-id="fbeec-108">範例1：在群集上取得持久化腳本動作</span><span class="sxs-lookup"><span data-stu-id="fbeec-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="fbeec-109">這個命令會在名為 [hadoop-001] 的群集上取得持續執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="fbeec-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fbeec-110">參數</span><span class="sxs-lookup"><span data-stu-id="fbeec-110">PARAMETERS</span></span>

### <span data-ttu-id="fbeec-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fbeec-111">-ClusterName</span></span>
<span data-ttu-id="fbeec-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbeec-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbeec-113">-DefaultProfile</span></span>
<span data-ttu-id="fbeec-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fbeec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeec-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="fbeec-115">-Name</span></span>
<span data-ttu-id="fbeec-116">指定持久化腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbeec-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbeec-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbeec-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbeec-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbeec-119">CommonParameters</span></span>
<span data-ttu-id="fbeec-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbeec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbeec-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbeec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbeec-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fbeec-122">INPUTS</span></span>

### <span data-ttu-id="fbeec-123">所有</span><span class="sxs-lookup"><span data-stu-id="fbeec-123">None</span></span>
<span data-ttu-id="fbeec-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fbeec-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbeec-125">輸出</span><span class="sxs-lookup"><span data-stu-id="fbeec-125">OUTPUTS</span></span>

### <span data-ttu-id="fbeec-126">System.object IList ' 1 [AzureHDInsightRuntimeScriptAction] （即 Azure. 命令..]</span><span class="sxs-lookup"><span data-stu-id="fbeec-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="fbeec-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fbeec-127">NOTES</span></span>

## <span data-ttu-id="fbeec-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbeec-128">RELATED LINKS</span></span>

[<span data-ttu-id="fbeec-129">移除-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fbeec-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="fbeec-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fbeec-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


