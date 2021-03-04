---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: ccbba2c5fb6c417284ae025cf1410d68bb3c8add
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916245"
---
# <span data-ttu-id="0e127-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e127-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="0e127-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e127-102">SYNOPSIS</span></span>
<span data-ttu-id="0e127-103">獲得帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e127-103">Gets an account.</span></span>

## <span data-ttu-id="0e127-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e127-104">SYNTAX</span></span>

### <span data-ttu-id="0e127-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e127-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e127-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e127-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e127-107">描述</span><span class="sxs-lookup"><span data-stu-id="0e127-107">DESCRIPTION</span></span>
<span data-ttu-id="0e127-108">**Get-AzCognitiveServicesAccount** Cmdlet 會取得 *ResourceGroupName* 參數指定之資源群組中的已部署認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e127-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="0e127-109">如果您未指定 *ResourceGroupName* 參數，此 Cmdlet 會獲得目前訂閱的所有認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e127-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="0e127-110">例子</span><span class="sxs-lookup"><span data-stu-id="0e127-110">EXAMPLES</span></span>

### <span data-ttu-id="0e127-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0e127-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="0e127-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e127-112">PARAMETERS</span></span>

### <span data-ttu-id="0e127-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e127-113">-DefaultProfile</span></span>
<span data-ttu-id="0e127-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0e127-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e127-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e127-115">-Name</span></span>
<span data-ttu-id="0e127-116">指定要取得認知服務帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e127-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e127-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e127-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e127-118">指定指派給認知服務帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0e127-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e127-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e127-119">CommonParameters</span></span>
<span data-ttu-id="0e127-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e127-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e127-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e127-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e127-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0e127-122">INPUTS</span></span>

### <span data-ttu-id="0e127-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0e127-123">System.String</span></span>

## <span data-ttu-id="0e127-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0e127-124">OUTPUTS</span></span>

### <span data-ttu-id="0e127-125">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e127-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0e127-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0e127-126">NOTES</span></span>

## <span data-ttu-id="0e127-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e127-127">RELATED LINKS</span></span>

[<span data-ttu-id="0e127-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e127-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0e127-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e127-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0e127-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e127-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


