---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444763"
---
# <span data-ttu-id="e8cbb-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="e8cbb-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="e8cbb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cbb-103">取得認知服務帳戶的目前使用方式。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8cbb-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8cbb-104">SYNTAX</span></span>

### <span data-ttu-id="e8cbb-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cbb-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cbb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cbb-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8cbb-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cbb-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8cbb-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8cbb-108">DESCRIPTION</span></span>
<span data-ttu-id="e8cbb-109">**AzureRmCognitiveServicesAccountUsage** Cmdlet 會取得有關認知服務帳戶的目前用途。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="e8cbb-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8cbb-110">EXAMPLES</span></span>

### <span data-ttu-id="e8cbb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8cbb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="e8cbb-112">範例2</span><span class="sxs-lookup"><span data-stu-id="e8cbb-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="e8cbb-113">範例3</span><span class="sxs-lookup"><span data-stu-id="e8cbb-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="e8cbb-114">參數</span><span class="sxs-lookup"><span data-stu-id="e8cbb-114">PARAMETERS</span></span>

### <span data-ttu-id="e8cbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cbb-115">-DefaultProfile</span></span>
<span data-ttu-id="e8cbb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8cbb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8cbb-117">-InputObject</span></span>
<span data-ttu-id="e8cbb-118">認知服務帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cbb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8cbb-119">-Name</span></span>
<span data-ttu-id="e8cbb-120">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cbb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cbb-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8cbb-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cbb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8cbb-123">-ResourceId</span></span>
<span data-ttu-id="e8cbb-124">認知服務帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cbb-125">CommonParameters</span></span>
<span data-ttu-id="e8cbb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cbb-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cbb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e8cbb-128">INPUTS</span></span>

### <span data-ttu-id="e8cbb-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e8cbb-129">System.String</span></span>

## <span data-ttu-id="e8cbb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e8cbb-130">OUTPUTS</span></span>

### <span data-ttu-id="e8cbb-131">PSCognitiveServicesUsage （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="e8cbb-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="e8cbb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e8cbb-132">NOTES</span></span>

## <span data-ttu-id="e8cbb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8cbb-133">RELATED LINKS</span></span>