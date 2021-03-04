---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 2fc4e536ed3f97b1d0e31ccea382d4dc55d59083
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909225"
---
# <span data-ttu-id="bd321-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="bd321-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="bd321-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd321-102">SYNOPSIS</span></span>
<span data-ttu-id="bd321-103">取得認知服務帳戶的目前使用狀況。</span><span class="sxs-lookup"><span data-stu-id="bd321-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="bd321-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd321-104">SYNTAX</span></span>

### <span data-ttu-id="bd321-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd321-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd321-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd321-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd321-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd321-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd321-108">描述</span><span class="sxs-lookup"><span data-stu-id="bd321-108">DESCRIPTION</span></span>
<span data-ttu-id="bd321-109">**Get-AzCognitiveServicesAccountUsage Cmdlet** 會取得認知服務帳戶的目前使用方式。</span><span class="sxs-lookup"><span data-stu-id="bd321-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="bd321-110">例子</span><span class="sxs-lookup"><span data-stu-id="bd321-110">EXAMPLES</span></span>

### <span data-ttu-id="bd321-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd321-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="bd321-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="bd321-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="bd321-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="bd321-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="bd321-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd321-114">PARAMETERS</span></span>

### <span data-ttu-id="bd321-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd321-115">-DefaultProfile</span></span>
<span data-ttu-id="bd321-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd321-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd321-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd321-117">-InputObject</span></span>
<span data-ttu-id="bd321-118">認知服務帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="bd321-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd321-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd321-119">-Name</span></span>
<span data-ttu-id="bd321-120">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bd321-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd321-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd321-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd321-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bd321-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd321-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd321-123">-ResourceId</span></span>
<span data-ttu-id="bd321-124">認知服務帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd321-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd321-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd321-125">CommonParameters</span></span>
<span data-ttu-id="bd321-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd321-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd321-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd321-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd321-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bd321-128">INPUTS</span></span>

### <span data-ttu-id="bd321-129">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bd321-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="bd321-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bd321-130">System.String</span></span>

## <span data-ttu-id="bd321-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bd321-131">OUTPUTS</span></span>

### <span data-ttu-id="bd321-132">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="bd321-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="bd321-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bd321-133">NOTES</span></span>

## <span data-ttu-id="bd321-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd321-134">RELATED LINKS</span></span>
