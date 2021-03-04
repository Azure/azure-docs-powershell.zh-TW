---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916562"
---
# <span data-ttu-id="89358-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="89358-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="89358-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89358-102">SYNOPSIS</span></span>
<span data-ttu-id="89358-103">獲得 HDInsight 服務的屬性，例如可用位置和容量。</span><span class="sxs-lookup"><span data-stu-id="89358-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="89358-104">語法</span><span class="sxs-lookup"><span data-stu-id="89358-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89358-105">描述</span><span class="sxs-lookup"><span data-stu-id="89358-105">DESCRIPTION</span></span>
<span data-ttu-id="89358-106">**Get-AzHDInsightProperty Cmdlet** 會取得 Azure HDInsight 特有的屬性，例如可用位置清單、HDInsight 集區版本，以及可用的計算容量。</span><span class="sxs-lookup"><span data-stu-id="89358-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="89358-107">例子</span><span class="sxs-lookup"><span data-stu-id="89358-107">EXAMPLES</span></span>

### <span data-ttu-id="89358-108">範例 1：取得 Azure HDInsight 集區的屬性</span><span class="sxs-lookup"><span data-stu-id="89358-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="89358-109">此命令會從 HDInsight 服務從位置 EAST US 2 獲得屬性。</span><span class="sxs-lookup"><span data-stu-id="89358-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="89358-110">參數</span><span class="sxs-lookup"><span data-stu-id="89358-110">PARAMETERS</span></span>

### <span data-ttu-id="89358-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89358-111">-DefaultProfile</span></span>
<span data-ttu-id="89358-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="89358-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89358-113">-位置</span><span class="sxs-lookup"><span data-stu-id="89358-113">-Location</span></span>
<span data-ttu-id="89358-114">指定要抓取 HDInsight 屬性的位置。</span><span class="sxs-lookup"><span data-stu-id="89358-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="89358-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89358-115">CommonParameters</span></span>
<span data-ttu-id="89358-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89358-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89358-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89358-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89358-118">輸入</span><span class="sxs-lookup"><span data-stu-id="89358-118">INPUTS</span></span>

### <span data-ttu-id="89358-119">沒有</span><span class="sxs-lookup"><span data-stu-id="89358-119">None</span></span>
## <span data-ttu-id="89358-120">輸出</span><span class="sxs-lookup"><span data-stu-id="89358-120">OUTPUTS</span></span>

### <span data-ttu-id="89358-121">Microsoft.Azure.management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="89358-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="89358-122">筆記</span><span class="sxs-lookup"><span data-stu-id="89358-122">NOTES</span></span>

## <span data-ttu-id="89358-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="89358-123">RELATED LINKS</span></span>
