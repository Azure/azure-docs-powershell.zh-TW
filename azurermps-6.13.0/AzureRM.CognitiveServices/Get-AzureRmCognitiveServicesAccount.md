---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 3f139d4164c092f6ef57ad29d5ab9ad3eac59b56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452828"
---
# <span data-ttu-id="dd801-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd801-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="dd801-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd801-102">SYNOPSIS</span></span>
<span data-ttu-id="dd801-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd801-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd801-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd801-104">SYNTAX</span></span>

### <span data-ttu-id="dd801-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd801-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd801-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd801-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd801-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd801-107">DESCRIPTION</span></span>
<span data-ttu-id="dd801-108">**AzureRmCognitiveServicesAccount** Cmdlet 會取得 *ResoureGroupName* 參數所指定之資源群組中已預配的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd801-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>
<span data-ttu-id="dd801-109">如果您沒有指定 *ResoureGroupName* 參數，此 Cmdlet 會取得目前訂閱的所有認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd801-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="dd801-110">示例</span><span class="sxs-lookup"><span data-stu-id="dd801-110">EXAMPLES</span></span>

### <span data-ttu-id="dd801-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dd801-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
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

## <span data-ttu-id="dd801-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd801-112">PARAMETERS</span></span>

### <span data-ttu-id="dd801-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd801-113">-DefaultProfile</span></span>
<span data-ttu-id="dd801-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dd801-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd801-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd801-115">-Name</span></span>
<span data-ttu-id="dd801-116">指定要取得之認知服務帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd801-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="dd801-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd801-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd801-118">指定將 [認知服務] 帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd801-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="dd801-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd801-119">CommonParameters</span></span>
<span data-ttu-id="dd801-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd801-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd801-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd801-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd801-122">輸入</span><span class="sxs-lookup"><span data-stu-id="dd801-122">INPUTS</span></span>

### <span data-ttu-id="dd801-123">System.object</span><span class="sxs-lookup"><span data-stu-id="dd801-123">System.String</span></span>

## <span data-ttu-id="dd801-124">輸出</span><span class="sxs-lookup"><span data-stu-id="dd801-124">OUTPUTS</span></span>

### <span data-ttu-id="dd801-125">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="dd801-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="dd801-126">筆記</span><span class="sxs-lookup"><span data-stu-id="dd801-126">NOTES</span></span>

## <span data-ttu-id="dd801-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd801-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd801-128">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd801-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dd801-129">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd801-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dd801-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd801-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


