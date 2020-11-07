---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 3d1e5db009cc88cf4647586c4234d63ae42f0575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787698"
---
# <span data-ttu-id="8b80c-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="8b80c-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="8b80c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b80c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b80c-103">取得 HDInsight 服務的相關屬性，例如可用的位置和容量。</span><span class="sxs-lookup"><span data-stu-id="8b80c-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="8b80c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b80c-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b80c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b80c-105">DESCRIPTION</span></span>
<span data-ttu-id="8b80c-106">**AzHDInsightProperty** Cmdlet 會取得 Azure HDInsight 專用的屬性，例如可用位置的清單、HDInsight 群集版本，以及可用的計算容量。</span><span class="sxs-lookup"><span data-stu-id="8b80c-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="8b80c-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b80c-107">EXAMPLES</span></span>

### <span data-ttu-id="8b80c-108">範例1：取得 Azure HDInsight 群集的屬性</span><span class="sxs-lookup"><span data-stu-id="8b80c-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="8b80c-109">這個命令會從來自美國地區2的 HDInsight 服務取得屬性。</span><span class="sxs-lookup"><span data-stu-id="8b80c-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="8b80c-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b80c-110">PARAMETERS</span></span>

### <span data-ttu-id="8b80c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b80c-111">-DefaultProfile</span></span>
<span data-ttu-id="8b80c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8b80c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b80c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="8b80c-113">-Location</span></span>
<span data-ttu-id="8b80c-114">指定要提取 HDInsight 屬性的位置。</span><span class="sxs-lookup"><span data-stu-id="8b80c-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="8b80c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b80c-115">CommonParameters</span></span>
<span data-ttu-id="8b80c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b80c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b80c-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b80c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b80c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8b80c-118">INPUTS</span></span>

### <span data-ttu-id="8b80c-119">所有</span><span class="sxs-lookup"><span data-stu-id="8b80c-119">None</span></span>

## <span data-ttu-id="8b80c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="8b80c-120">OUTPUTS</span></span>

### <span data-ttu-id="8b80c-121">CapabilitiesResponse 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="8b80c-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="8b80c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="8b80c-122">NOTES</span></span>

## <span data-ttu-id="8b80c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b80c-123">RELATED LINKS</span></span>
