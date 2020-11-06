---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 7d197cdb7ee8fbfa63d8a3b36da5f038a5a0b8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613482"
---
# <span data-ttu-id="655f8-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="655f8-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="655f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="655f8-102">SYNOPSIS</span></span>
<span data-ttu-id="655f8-103">取得認知服務帳戶的目前使用方式。</span><span class="sxs-lookup"><span data-stu-id="655f8-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="655f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="655f8-104">SYNTAX</span></span>

### <span data-ttu-id="655f8-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="655f8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="655f8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="655f8-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="655f8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="655f8-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="655f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="655f8-108">DESCRIPTION</span></span>
<span data-ttu-id="655f8-109">**AzCognitiveServicesAccountUsage** Cmdlet 會取得有關認知服務帳戶的目前用途。</span><span class="sxs-lookup"><span data-stu-id="655f8-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="655f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="655f8-110">EXAMPLES</span></span>

### <span data-ttu-id="655f8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="655f8-111">Example 1</span></span>
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

### <span data-ttu-id="655f8-112">範例2</span><span class="sxs-lookup"><span data-stu-id="655f8-112">Example 2</span></span>
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

### <span data-ttu-id="655f8-113">範例3</span><span class="sxs-lookup"><span data-stu-id="655f8-113">Example 3</span></span>
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

## <span data-ttu-id="655f8-114">參數</span><span class="sxs-lookup"><span data-stu-id="655f8-114">PARAMETERS</span></span>

### <span data-ttu-id="655f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655f8-115">-DefaultProfile</span></span>
<span data-ttu-id="655f8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="655f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="655f8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="655f8-117">-InputObject</span></span>
<span data-ttu-id="655f8-118">認知服務帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="655f8-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="655f8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="655f8-119">-Name</span></span>
<span data-ttu-id="655f8-120">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="655f8-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="655f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="655f8-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="655f8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="655f8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="655f8-123">-ResourceId</span></span>
<span data-ttu-id="655f8-124">認知服務帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="655f8-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="655f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655f8-125">CommonParameters</span></span>
<span data-ttu-id="655f8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="655f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655f8-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="655f8-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655f8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="655f8-128">INPUTS</span></span>

### <span data-ttu-id="655f8-129">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="655f8-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="655f8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="655f8-130">System.String</span></span>

## <span data-ttu-id="655f8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="655f8-131">OUTPUTS</span></span>

### <span data-ttu-id="655f8-132">PSCognitiveServicesUsage （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="655f8-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="655f8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="655f8-133">NOTES</span></span>

## <span data-ttu-id="655f8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="655f8-134">RELATED LINKS</span></span>
