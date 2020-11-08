---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956255"
---
# <span data-ttu-id="a48d3-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a48d3-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="a48d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a48d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a48d3-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="a48d3-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="a48d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="a48d3-104">SYNTAX</span></span>

### <span data-ttu-id="a48d3-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="a48d3-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a48d3-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a48d3-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a48d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="a48d3-107">DESCRIPTION</span></span>
<span data-ttu-id="a48d3-108">**新的-AzCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="a48d3-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="a48d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="a48d3-109">EXAMPLES</span></span>

### <span data-ttu-id="a48d3-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="a48d3-110">1:</span></span>
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

## <span data-ttu-id="a48d3-111">參數</span><span class="sxs-lookup"><span data-stu-id="a48d3-111">PARAMETERS</span></span>

### <span data-ttu-id="a48d3-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a48d3-112">-AssignIdentity</span></span>
<span data-ttu-id="a48d3-113">針對此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="a48d3-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a48d3-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="a48d3-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="a48d3-115">是否將認知服務帳戶加密 KeySource 設定為 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="a48d3-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="a48d3-116">-CustomSubdomainName</span></span>
<span data-ttu-id="a48d3-117">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a48d3-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="a48d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48d3-118">-DefaultProfile</span></span>
<span data-ttu-id="a48d3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a48d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a48d3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a48d3-120">-Force</span></span>
<span data-ttu-id="a48d3-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a48d3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a48d3-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a48d3-122">-KeyName</span></span>
<span data-ttu-id="a48d3-123">認知服務帳戶加密 keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="a48d3-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a48d3-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="a48d3-125">是否將認知服務帳戶加密 keySource 設定為 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a48d3-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="a48d3-126">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，認知服務帳戶加密 KeySource 也會設定為 Microsoft。 KeyVault 天氣此參數已設定。</span><span class="sxs-lookup"><span data-stu-id="a48d3-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a48d3-127">-KeyVaultUri</span></span>
<span data-ttu-id="a48d3-128">認知服務帳戶加密 keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a48d3-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="a48d3-129">-KeyVersion</span></span>
<span data-ttu-id="a48d3-130">認知服務帳戶加密 keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="a48d3-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-131">-位置</span><span class="sxs-lookup"><span data-stu-id="a48d3-131">-Location</span></span>
<span data-ttu-id="a48d3-132">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="a48d3-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="a48d3-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="a48d3-133">-Name</span></span>
<span data-ttu-id="a48d3-134">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a48d3-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="a48d3-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a48d3-135">-NetworkRuleSet</span></span>
<span data-ttu-id="a48d3-136">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="a48d3-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="a48d3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48d3-137">-ResourceGroupName</span></span>
<span data-ttu-id="a48d3-138">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a48d3-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="a48d3-139">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="a48d3-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="a48d3-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a48d3-140">-SkuName</span></span>
<span data-ttu-id="a48d3-141">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="a48d3-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a48d3-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a48d3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a48d3-143">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="a48d3-143">F0 (free tier)</span></span>
- <span data-ttu-id="a48d3-144">S0</span><span class="sxs-lookup"><span data-stu-id="a48d3-144">S0</span></span>
- <span data-ttu-id="a48d3-145">S1</span><span class="sxs-lookup"><span data-stu-id="a48d3-145">S1</span></span>
- <span data-ttu-id="a48d3-146">S2</span><span class="sxs-lookup"><span data-stu-id="a48d3-146">S2</span></span>
- <span data-ttu-id="a48d3-147">S3</span><span class="sxs-lookup"><span data-stu-id="a48d3-147">S3</span></span>
- <span data-ttu-id="a48d3-148">S4 如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="a48d3-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="a48d3-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a48d3-149">-StorageAccountId</span></span>
<span data-ttu-id="a48d3-150">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="a48d3-150">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48d3-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="a48d3-151">-Tag</span></span>
<span data-ttu-id="a48d3-152">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="a48d3-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="a48d3-153">-類型</span><span class="sxs-lookup"><span data-stu-id="a48d3-153">-Type</span></span>
<span data-ttu-id="a48d3-154">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a48d3-154">Specifies the type of account to create.</span></span> <span data-ttu-id="a48d3-155">使用 `Get-AzCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="a48d3-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="a48d3-156">-確認</span><span class="sxs-lookup"><span data-stu-id="a48d3-156">-Confirm</span></span>
<span data-ttu-id="a48d3-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a48d3-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a48d3-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a48d3-158">-WhatIf</span></span>
<span data-ttu-id="a48d3-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a48d3-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a48d3-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a48d3-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a48d3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48d3-161">CommonParameters</span></span>
<span data-ttu-id="a48d3-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a48d3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48d3-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a48d3-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48d3-164">輸入</span><span class="sxs-lookup"><span data-stu-id="a48d3-164">INPUTS</span></span>

### <span data-ttu-id="a48d3-165">System.object</span><span class="sxs-lookup"><span data-stu-id="a48d3-165">System.String</span></span>

## <span data-ttu-id="a48d3-166">輸出</span><span class="sxs-lookup"><span data-stu-id="a48d3-166">OUTPUTS</span></span>

### <span data-ttu-id="a48d3-167">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="a48d3-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a48d3-168">筆記</span><span class="sxs-lookup"><span data-stu-id="a48d3-168">NOTES</span></span>

## <span data-ttu-id="a48d3-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="a48d3-169">RELATED LINKS</span></span>

[<span data-ttu-id="a48d3-170">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a48d3-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a48d3-171">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a48d3-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a48d3-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a48d3-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)