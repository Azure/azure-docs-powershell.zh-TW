---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138353"
---
# <span data-ttu-id="4cb2a-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cb2a-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="4cb2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb2a-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-103">Gets an account.</span></span>

## <span data-ttu-id="4cb2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cb2a-104">SYNTAX</span></span>

### <span data-ttu-id="4cb2a-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb2a-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cb2a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb2a-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cb2a-107">說明</span><span class="sxs-lookup"><span data-stu-id="4cb2a-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb2a-108">**AzCognitiveServicesAccount** Cmdlet 會取得 *ResourceGroupName* 參數所指定之資源群組中已預配的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4cb2a-109">如果您沒有指定 *ResourceGroupName* 參數，此 Cmdlet 會取得目前訂閱的所有認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="4cb2a-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cb2a-110">EXAMPLES</span></span>

### <span data-ttu-id="4cb2a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4cb2a-111">Example 1</span></span>
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

## <span data-ttu-id="4cb2a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4cb2a-112">PARAMETERS</span></span>

### <span data-ttu-id="4cb2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb2a-113">-DefaultProfile</span></span>
<span data-ttu-id="4cb2a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4cb2a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cb2a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cb2a-115">-Name</span></span>
<span data-ttu-id="4cb2a-116">指定要取得之認知服務帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="4cb2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4cb2a-118">指定將 [認知服務] 帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="4cb2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb2a-119">CommonParameters</span></span>
<span data-ttu-id="4cb2a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb2a-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb2a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4cb2a-122">INPUTS</span></span>

### <span data-ttu-id="4cb2a-123">System.object</span><span class="sxs-lookup"><span data-stu-id="4cb2a-123">System.String</span></span>

## <span data-ttu-id="4cb2a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4cb2a-124">OUTPUTS</span></span>

### <span data-ttu-id="4cb2a-125">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="4cb2a-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4cb2a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4cb2a-126">NOTES</span></span>

## <span data-ttu-id="4cb2a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cb2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4cb2a-128">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cb2a-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="4cb2a-129">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cb2a-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="4cb2a-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cb2a-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

