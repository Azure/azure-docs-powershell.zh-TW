---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450707"
---
# <span data-ttu-id="fa5cc-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa5cc-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="fa5cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5cc-103">取得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa5cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa5cc-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa5cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5cc-106">**AzureRmCognitiveServicesAccountKey** Cmdlet 會取得已預配的認知服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="fa5cc-107">認知服務帳戶有兩個 API 金鑰： Key1 和 Key2。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="fa5cc-108">金鑰可讓您與認知服務帳戶端點互動。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="fa5cc-109">使用 New-AzureRmCognitiveServicesAccountKey 重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="fa5cc-110">示例</span><span class="sxs-lookup"><span data-stu-id="fa5cc-110">EXAMPLES</span></span>

## <span data-ttu-id="fa5cc-111">參數</span><span class="sxs-lookup"><span data-stu-id="fa5cc-111">PARAMETERS</span></span>

### <span data-ttu-id="fa5cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5cc-112">-DefaultProfile</span></span>
<span data-ttu-id="fa5cc-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa5cc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa5cc-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa5cc-114">-Name</span></span>
<span data-ttu-id="fa5cc-115">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-115">Specifies the name of the account.</span></span>
<span data-ttu-id="fa5cc-116">這個 Cmdlet 會取得這個帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-116">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="fa5cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa5cc-118">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-118">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="fa5cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5cc-119">CommonParameters</span></span>
<span data-ttu-id="fa5cc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5cc-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5cc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fa5cc-122">INPUTS</span></span>

### <span data-ttu-id="fa5cc-123">所有</span><span class="sxs-lookup"><span data-stu-id="fa5cc-123">None</span></span>
<span data-ttu-id="fa5cc-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa5cc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="fa5cc-125">OUTPUTS</span></span>

### <span data-ttu-id="fa5cc-126">PSCognitiveServicesAccountKeys （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="fa5cc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fa5cc-127">NOTES</span></span>

## <span data-ttu-id="fa5cc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa5cc-128">RELATED LINKS</span></span>

[<span data-ttu-id="fa5cc-129">新-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa5cc-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


