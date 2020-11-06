---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613475"
---
# <span data-ttu-id="b1278-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1278-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="b1278-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1278-102">SYNOPSIS</span></span>
<span data-ttu-id="b1278-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="b1278-103">Modifies an account.</span></span>

## <span data-ttu-id="b1278-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1278-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1278-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1278-105">DESCRIPTION</span></span>
<span data-ttu-id="b1278-106">**AzCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="b1278-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b1278-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1278-107">EXAMPLES</span></span>

### <span data-ttu-id="b1278-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b1278-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="b1278-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1278-109">PARAMETERS</span></span>

### <span data-ttu-id="b1278-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="b1278-110">-CustomSubdomainName</span></span>
<span data-ttu-id="b1278-111">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b1278-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="b1278-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1278-112">-DefaultProfile</span></span>
<span data-ttu-id="b1278-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b1278-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1278-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b1278-114">-Force</span></span>
<span data-ttu-id="b1278-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b1278-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1278-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1278-116">-Name</span></span>
<span data-ttu-id="b1278-117">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b1278-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="b1278-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1278-118">-NetworkRuleSet</span></span>
<span data-ttu-id="b1278-119">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="b1278-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="b1278-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1278-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1278-121">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1278-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="b1278-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b1278-122">-SkuName</span></span>
<span data-ttu-id="b1278-123">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="b1278-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b1278-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b1278-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1278-125">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="b1278-125">F0 (free tier)</span></span>
- <span data-ttu-id="b1278-126">S0</span><span class="sxs-lookup"><span data-stu-id="b1278-126">S0</span></span>
- <span data-ttu-id="b1278-127">S1</span><span class="sxs-lookup"><span data-stu-id="b1278-127">S1</span></span>
- <span data-ttu-id="b1278-128">S2</span><span class="sxs-lookup"><span data-stu-id="b1278-128">S2</span></span>
- <span data-ttu-id="b1278-129">S3</span><span class="sxs-lookup"><span data-stu-id="b1278-129">S3</span></span>
- <span data-ttu-id="b1278-130">喚醒</span><span class="sxs-lookup"><span data-stu-id="b1278-130">S4</span></span>

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

### <span data-ttu-id="b1278-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1278-131">-Tag</span></span>
<span data-ttu-id="b1278-132">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="b1278-132">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="b1278-133">-確認</span><span class="sxs-lookup"><span data-stu-id="b1278-133">-Confirm</span></span>
<span data-ttu-id="b1278-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1278-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1278-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1278-135">-WhatIf</span></span>
<span data-ttu-id="b1278-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1278-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1278-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1278-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1278-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1278-138">CommonParameters</span></span>
<span data-ttu-id="b1278-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1278-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1278-140">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1278-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1278-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b1278-141">INPUTS</span></span>

### <span data-ttu-id="b1278-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b1278-142">System.String</span></span>

### <span data-ttu-id="b1278-143">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="b1278-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="b1278-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b1278-144">OUTPUTS</span></span>

### <span data-ttu-id="b1278-145">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="b1278-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b1278-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b1278-146">NOTES</span></span>

## <span data-ttu-id="b1278-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1278-147">RELATED LINKS</span></span>

[<span data-ttu-id="b1278-148">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1278-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b1278-149">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1278-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b1278-150">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1278-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
