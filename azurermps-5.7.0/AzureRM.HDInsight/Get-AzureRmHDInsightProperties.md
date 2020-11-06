---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 4b3437f9df1be7e458aaa528769de406d755a071
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452260"
---
# <span data-ttu-id="bbff2-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="bbff2-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="bbff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbff2-102">SYNOPSIS</span></span>
<span data-ttu-id="bbff2-103">取得 HDInsight 服務的相關屬性，例如可用的位置和容量。</span><span class="sxs-lookup"><span data-stu-id="bbff2-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbff2-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbff2-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbff2-105">DESCRIPTION</span></span>
<span data-ttu-id="bbff2-106">**AzureRmHDInsightProperties** Cmdlet 會取得 Azure HDInsight 專用的屬性，例如可用位置的清單、HDInsight 群集版本，以及可用的計算容量。</span><span class="sxs-lookup"><span data-stu-id="bbff2-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="bbff2-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbff2-107">EXAMPLES</span></span>

### <span data-ttu-id="bbff2-108">範例1：取得 Azure HDInsight 群集的屬性</span><span class="sxs-lookup"><span data-stu-id="bbff2-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="bbff2-109">這個命令會從來自美國地區2的 HDInsight 服務取得屬性。</span><span class="sxs-lookup"><span data-stu-id="bbff2-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="bbff2-110">參數</span><span class="sxs-lookup"><span data-stu-id="bbff2-110">PARAMETERS</span></span>

### <span data-ttu-id="bbff2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbff2-111">-DefaultProfile</span></span>
<span data-ttu-id="bbff2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bbff2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbff2-113">-位置</span><span class="sxs-lookup"><span data-stu-id="bbff2-113">-Location</span></span>
<span data-ttu-id="bbff2-114">指定要提取 HDInsight 屬性的位置。</span><span class="sxs-lookup"><span data-stu-id="bbff2-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="bbff2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbff2-115">CommonParameters</span></span>
<span data-ttu-id="bbff2-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbff2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbff2-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbff2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbff2-118">輸入</span><span class="sxs-lookup"><span data-stu-id="bbff2-118">INPUTS</span></span>

### <span data-ttu-id="bbff2-119">所有</span><span class="sxs-lookup"><span data-stu-id="bbff2-119">None</span></span>
<span data-ttu-id="bbff2-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bbff2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbff2-121">輸出</span><span class="sxs-lookup"><span data-stu-id="bbff2-121">OUTPUTS</span></span>

### <span data-ttu-id="bbff2-122">CapabilitiesResponse 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="bbff2-122">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="bbff2-123">筆記</span><span class="sxs-lookup"><span data-stu-id="bbff2-123">NOTES</span></span>

## <span data-ttu-id="bbff2-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbff2-124">RELATED LINKS</span></span>
