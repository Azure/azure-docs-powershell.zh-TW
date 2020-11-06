---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: d19c22ffd0be5b6ea935b832d847bb74661e3106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613484"
---
# <span data-ttu-id="abc7a-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abc7a-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="abc7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="abc7a-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="abc7a-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="abc7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="abc7a-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abc7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="abc7a-105">DESCRIPTION</span></span>
<span data-ttu-id="abc7a-106">**新的-AzCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="abc7a-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="abc7a-107">示例</span><span class="sxs-lookup"><span data-stu-id="abc7a-107">EXAMPLES</span></span>

### <span data-ttu-id="abc7a-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="abc7a-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="abc7a-109">參數</span><span class="sxs-lookup"><span data-stu-id="abc7a-109">PARAMETERS</span></span>

### <span data-ttu-id="abc7a-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="abc7a-110">-CustomSubdomainName</span></span>
<span data-ttu-id="abc7a-111">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="abc7a-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc7a-112">-DefaultProfile</span></span>
<span data-ttu-id="abc7a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="abc7a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abc7a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="abc7a-114">-Force</span></span>
<span data-ttu-id="abc7a-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="abc7a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abc7a-116">-位置</span><span class="sxs-lookup"><span data-stu-id="abc7a-116">-Location</span></span>
<span data-ttu-id="abc7a-117">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="abc7a-117">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="abc7a-118">-Name</span></span>
<span data-ttu-id="abc7a-119">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="abc7a-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="abc7a-120">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="abc7a-120">-NetworkRuleSet</span></span>
<span data-ttu-id="abc7a-121">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="abc7a-121">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc7a-122">-ResourceGroupName</span></span>
<span data-ttu-id="abc7a-123">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="abc7a-123">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="abc7a-124">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="abc7a-124">The resource group must already exist.</span></span>

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

### <span data-ttu-id="abc7a-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="abc7a-125">-SkuName</span></span>
<span data-ttu-id="abc7a-126">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="abc7a-126">Specifies the SKU for the account.</span></span>
<span data-ttu-id="abc7a-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="abc7a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abc7a-128">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="abc7a-128">F0 (free tier)</span></span>
- <span data-ttu-id="abc7a-129">S0</span><span class="sxs-lookup"><span data-stu-id="abc7a-129">S0</span></span>
- <span data-ttu-id="abc7a-130">S1</span><span class="sxs-lookup"><span data-stu-id="abc7a-130">S1</span></span>
- <span data-ttu-id="abc7a-131">S2</span><span class="sxs-lookup"><span data-stu-id="abc7a-131">S2</span></span>
- <span data-ttu-id="abc7a-132">S3</span><span class="sxs-lookup"><span data-stu-id="abc7a-132">S3</span></span>
- <span data-ttu-id="abc7a-133">S4 如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="abc7a-133">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="abc7a-134">-Tag</span></span>
<span data-ttu-id="abc7a-135">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="abc7a-135">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-136">-類型</span><span class="sxs-lookup"><span data-stu-id="abc7a-136">-Type</span></span>
<span data-ttu-id="abc7a-137">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="abc7a-137">Specifies the type of account to create.</span></span> <span data-ttu-id="abc7a-138">使用 `Get-AzCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="abc7a-138">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc7a-139">-確認</span><span class="sxs-lookup"><span data-stu-id="abc7a-139">-Confirm</span></span>
<span data-ttu-id="abc7a-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abc7a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc7a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc7a-141">-WhatIf</span></span>
<span data-ttu-id="abc7a-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abc7a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc7a-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abc7a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc7a-144">CommonParameters</span></span>
<span data-ttu-id="abc7a-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abc7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc7a-146">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="abc7a-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc7a-147">輸入</span><span class="sxs-lookup"><span data-stu-id="abc7a-147">INPUTS</span></span>

### <span data-ttu-id="abc7a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="abc7a-148">System.String</span></span>

## <span data-ttu-id="abc7a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="abc7a-149">OUTPUTS</span></span>

### <span data-ttu-id="abc7a-150">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="abc7a-150">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="abc7a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="abc7a-151">NOTES</span></span>

## <span data-ttu-id="abc7a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="abc7a-152">RELATED LINKS</span></span>

[<span data-ttu-id="abc7a-153">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abc7a-153">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="abc7a-154">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abc7a-154">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="abc7a-155">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abc7a-155">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
