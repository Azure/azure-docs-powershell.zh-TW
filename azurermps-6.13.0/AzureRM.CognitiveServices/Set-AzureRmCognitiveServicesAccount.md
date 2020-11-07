---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624248"
---
# <span data-ttu-id="eb40c-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eb40c-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="eb40c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb40c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb40c-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="eb40c-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb40c-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb40c-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb40c-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb40c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb40c-106">**AzureRmCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="eb40c-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="eb40c-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb40c-107">EXAMPLES</span></span>

### <span data-ttu-id="eb40c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb40c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="eb40c-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb40c-109">PARAMETERS</span></span>

### <span data-ttu-id="eb40c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb40c-110">-DefaultProfile</span></span>
<span data-ttu-id="eb40c-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eb40c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb40c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="eb40c-112">-Force</span></span>
<span data-ttu-id="eb40c-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="eb40c-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb40c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb40c-114">-Name</span></span>
<span data-ttu-id="eb40c-115">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="eb40c-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="eb40c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb40c-116">-ResourceGroupName</span></span>
<span data-ttu-id="eb40c-117">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb40c-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="eb40c-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eb40c-118">-SkuName</span></span>
<span data-ttu-id="eb40c-119">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="eb40c-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="eb40c-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="eb40c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb40c-121">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="eb40c-121">F0 (free tier)</span></span>
- <span data-ttu-id="eb40c-122">S0</span><span class="sxs-lookup"><span data-stu-id="eb40c-122">S0</span></span>
- <span data-ttu-id="eb40c-123">S1</span><span class="sxs-lookup"><span data-stu-id="eb40c-123">S1</span></span>
- <span data-ttu-id="eb40c-124">S2</span><span class="sxs-lookup"><span data-stu-id="eb40c-124">S2</span></span>
- <span data-ttu-id="eb40c-125">S3</span><span class="sxs-lookup"><span data-stu-id="eb40c-125">S3</span></span>
- <span data-ttu-id="eb40c-126">喚醒</span><span class="sxs-lookup"><span data-stu-id="eb40c-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb40c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb40c-127">-Tag</span></span>
<span data-ttu-id="eb40c-128">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="eb40c-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb40c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="eb40c-129">-Confirm</span></span>
<span data-ttu-id="eb40c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb40c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb40c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb40c-131">-WhatIf</span></span>
<span data-ttu-id="eb40c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb40c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb40c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb40c-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb40c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb40c-134">CommonParameters</span></span>
<span data-ttu-id="eb40c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb40c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb40c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb40c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb40c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="eb40c-137">INPUTS</span></span>

### <span data-ttu-id="eb40c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="eb40c-138">System.String</span></span>

### <span data-ttu-id="eb40c-139">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="eb40c-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="eb40c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="eb40c-140">OUTPUTS</span></span>

### <span data-ttu-id="eb40c-141">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="eb40c-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="eb40c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="eb40c-142">NOTES</span></span>

## <span data-ttu-id="eb40c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb40c-143">RELATED LINKS</span></span>

[<span data-ttu-id="eb40c-144">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eb40c-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="eb40c-145">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eb40c-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="eb40c-146">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eb40c-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
