---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141375"
---
# <span data-ttu-id="9d8bd-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="9d8bd-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="9d8bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8bd-103">取得認知服務帳戶的目前使用方式。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="9d8bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d8bd-104">SYNTAX</span></span>

### <span data-ttu-id="9d8bd-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d8bd-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d8bd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8bd-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d8bd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8bd-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d8bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d8bd-108">DESCRIPTION</span></span>
<span data-ttu-id="9d8bd-109">**AzCognitiveServicesAccountUsage** Cmdlet 會取得有關認知服務帳戶的目前用途。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="9d8bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d8bd-110">EXAMPLES</span></span>

### <span data-ttu-id="9d8bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9d8bd-111">Example 1</span></span>
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

### <span data-ttu-id="9d8bd-112">範例2</span><span class="sxs-lookup"><span data-stu-id="9d8bd-112">Example 2</span></span>
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

### <span data-ttu-id="9d8bd-113">範例3</span><span class="sxs-lookup"><span data-stu-id="9d8bd-113">Example 3</span></span>
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

## <span data-ttu-id="9d8bd-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d8bd-114">PARAMETERS</span></span>

### <span data-ttu-id="9d8bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8bd-115">-DefaultProfile</span></span>
<span data-ttu-id="9d8bd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d8bd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d8bd-117">-InputObject</span></span>
<span data-ttu-id="9d8bd-118">認知服務帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="9d8bd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d8bd-119">-Name</span></span>
<span data-ttu-id="9d8bd-120">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="9d8bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d8bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d8bd-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d8bd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d8bd-123">-ResourceId</span></span>
<span data-ttu-id="9d8bd-124">認知服務帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="9d8bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8bd-125">CommonParameters</span></span>
<span data-ttu-id="9d8bd-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8bd-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8bd-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9d8bd-128">INPUTS</span></span>

### <span data-ttu-id="9d8bd-129">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="9d8bd-130">System.object</span><span class="sxs-lookup"><span data-stu-id="9d8bd-130">System.String</span></span>

## <span data-ttu-id="9d8bd-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9d8bd-131">OUTPUTS</span></span>

### <span data-ttu-id="9d8bd-132">PSCognitiveServicesUsage （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="9d8bd-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="9d8bd-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9d8bd-133">NOTES</span></span>

## <span data-ttu-id="9d8bd-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d8bd-134">RELATED LINKS</span></span>
