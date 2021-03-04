---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 46da28f86cac8aed68724683aaa69fde8ea64a50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916237"
---
# <span data-ttu-id="e6da8-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6da8-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e6da8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6da8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6da8-103">獲得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e6da8-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="e6da8-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6da8-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6da8-105">描述</span><span class="sxs-lookup"><span data-stu-id="e6da8-105">DESCRIPTION</span></span>
<span data-ttu-id="e6da8-106">**Get-AzCognitiveServicesAccountKey** Cmdlet 會取得已提供認知服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e6da8-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="e6da8-107">認知服務帳戶有兩個 API 金鑰：Key1 和 Key2。</span><span class="sxs-lookup"><span data-stu-id="e6da8-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="e6da8-108">這些按鍵可啟用與認知服務帳戶端點的互動。</span><span class="sxs-lookup"><span data-stu-id="e6da8-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="e6da8-109">使用New-AzCognitiveServicesAccountKey重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="e6da8-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="e6da8-110">例子</span><span class="sxs-lookup"><span data-stu-id="e6da8-110">EXAMPLES</span></span>

### <span data-ttu-id="e6da8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e6da8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="e6da8-112">參數</span><span class="sxs-lookup"><span data-stu-id="e6da8-112">PARAMETERS</span></span>

### <span data-ttu-id="e6da8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6da8-113">-DefaultProfile</span></span>
<span data-ttu-id="e6da8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e6da8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6da8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6da8-115">-Name</span></span>
<span data-ttu-id="e6da8-116">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6da8-116">Specifies the name of the account.</span></span>
<span data-ttu-id="e6da8-117">此 Cmdlet 會獲得此帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e6da8-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6da8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6da8-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6da8-119">指定帳戶指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e6da8-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6da8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6da8-120">CommonParameters</span></span>
<span data-ttu-id="e6da8-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6da8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6da8-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6da8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6da8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e6da8-123">INPUTS</span></span>

### <span data-ttu-id="e6da8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e6da8-124">System.String</span></span>

## <span data-ttu-id="e6da8-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e6da8-125">OUTPUTS</span></span>

### <span data-ttu-id="e6da8-126">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6da8-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e6da8-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e6da8-127">NOTES</span></span>

## <span data-ttu-id="e6da8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6da8-128">RELATED LINKS</span></span>

[<span data-ttu-id="e6da8-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6da8-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


