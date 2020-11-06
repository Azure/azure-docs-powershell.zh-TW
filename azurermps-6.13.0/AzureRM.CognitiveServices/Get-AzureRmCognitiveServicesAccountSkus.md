---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451907"
---
# <span data-ttu-id="3c231-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="3c231-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="3c231-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c231-102">SYNOPSIS</span></span>
<span data-ttu-id="3c231-103">取得帳戶可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="3c231-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c231-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c231-104">SYNTAX</span></span>

### <span data-ttu-id="3c231-105">GetSkusWithAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="3c231-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c231-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="3c231-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c231-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c231-107">DESCRIPTION</span></span>
<span data-ttu-id="3c231-108">**AzureRmCognitiveServicesAccountSkus** Cmdlet 會針對認知服務帳戶取得可用的 sku。</span><span class="sxs-lookup"><span data-stu-id="3c231-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="3c231-109">[SKU] 是帳戶的層級方案。</span><span class="sxs-lookup"><span data-stu-id="3c231-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="3c231-110">它會定義該帳戶的價格、通話限制及工資率。</span><span class="sxs-lookup"><span data-stu-id="3c231-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="3c231-111">F0 SKU 是免費的層級。</span><span class="sxs-lookup"><span data-stu-id="3c231-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="3c231-112">支付的層級包括 S0、S1、S2 等。</span><span class="sxs-lookup"><span data-stu-id="3c231-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="3c231-113">示例</span><span class="sxs-lookup"><span data-stu-id="3c231-113">EXAMPLES</span></span>

### <span data-ttu-id="3c231-114">範例1</span><span class="sxs-lookup"><span data-stu-id="3c231-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="3c231-115">參數</span><span class="sxs-lookup"><span data-stu-id="3c231-115">PARAMETERS</span></span>

### <span data-ttu-id="3c231-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c231-116">-DefaultProfile</span></span>
<span data-ttu-id="3c231-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3c231-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c231-118">-位置</span><span class="sxs-lookup"><span data-stu-id="3c231-118">-Location</span></span>
<span data-ttu-id="3c231-119">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="3c231-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c231-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c231-120">-Name</span></span>
<span data-ttu-id="3c231-121">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c231-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c231-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c231-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c231-123">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c231-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c231-124">-類型</span><span class="sxs-lookup"><span data-stu-id="3c231-124">-Type</span></span>
<span data-ttu-id="3c231-125">認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="3c231-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c231-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c231-126">CommonParameters</span></span>
<span data-ttu-id="3c231-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c231-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c231-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c231-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c231-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3c231-129">INPUTS</span></span>

### <span data-ttu-id="3c231-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3c231-130">System.String</span></span>

## <span data-ttu-id="3c231-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3c231-131">OUTPUTS</span></span>

### <span data-ttu-id="3c231-132">PSCognitiveServicesSkus （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="3c231-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="3c231-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3c231-133">NOTES</span></span>

## <span data-ttu-id="3c231-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c231-134">RELATED LINKS</span></span>
