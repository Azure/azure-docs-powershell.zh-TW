---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446415"
---
# <span data-ttu-id="9f032-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="9f032-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="9f032-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f032-102">SYNOPSIS</span></span>
<span data-ttu-id="9f032-103">取得帳戶可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="9f032-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f032-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f032-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f032-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f032-105">DESCRIPTION</span></span>
<span data-ttu-id="9f032-106">**AzureRmCognitiveServicesAccountSkus** Cmdlet 會針對認知服務帳戶取得可用的 sku。</span><span class="sxs-lookup"><span data-stu-id="9f032-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="9f032-107">[SKU] 是帳戶的層級方案。</span><span class="sxs-lookup"><span data-stu-id="9f032-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="9f032-108">它會定義該帳戶的價格、通話限制及工資率。</span><span class="sxs-lookup"><span data-stu-id="9f032-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="9f032-109">F0 SKU 是免費的層級。</span><span class="sxs-lookup"><span data-stu-id="9f032-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="9f032-110">支付的層級包括 S0、S1、S2 等。</span><span class="sxs-lookup"><span data-stu-id="9f032-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="9f032-111">示例</span><span class="sxs-lookup"><span data-stu-id="9f032-111">EXAMPLES</span></span>

## <span data-ttu-id="9f032-112">參數</span><span class="sxs-lookup"><span data-stu-id="9f032-112">PARAMETERS</span></span>

### <span data-ttu-id="9f032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f032-113">-DefaultProfile</span></span>
<span data-ttu-id="9f032-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9f032-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f032-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f032-115">-Name</span></span>
<span data-ttu-id="9f032-116">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f032-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f032-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f032-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f032-118">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f032-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f032-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f032-119">CommonParameters</span></span>
<span data-ttu-id="9f032-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f032-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f032-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f032-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f032-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9f032-122">INPUTS</span></span>

### <span data-ttu-id="9f032-123">所有</span><span class="sxs-lookup"><span data-stu-id="9f032-123">None</span></span>
<span data-ttu-id="9f032-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9f032-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f032-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9f032-125">OUTPUTS</span></span>

### <span data-ttu-id="9f032-126">PSCognitiveServicesSkus （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="9f032-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="9f032-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9f032-127">NOTES</span></span>

## <span data-ttu-id="9f032-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f032-128">RELATED LINKS</span></span>

