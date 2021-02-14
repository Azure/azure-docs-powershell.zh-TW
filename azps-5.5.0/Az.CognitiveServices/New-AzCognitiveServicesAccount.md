---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143443"
---
# <span data-ttu-id="36fa8-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="36fa8-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="36fa8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="36fa8-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="36fa8-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="36fa8-104">句法</span><span class="sxs-lookup"><span data-stu-id="36fa8-104">SYNTAX</span></span>

### <span data-ttu-id="36fa8-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="36fa8-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fa8-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="36fa8-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36fa8-107">說明</span><span class="sxs-lookup"><span data-stu-id="36fa8-107">DESCRIPTION</span></span>
<span data-ttu-id="36fa8-108">**新的-AzCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="36fa8-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="36fa8-109">示例</span><span class="sxs-lookup"><span data-stu-id="36fa8-109">EXAMPLES</span></span>

### <span data-ttu-id="36fa8-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="36fa8-110">1:</span></span>
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

## <span data-ttu-id="36fa8-111">參數</span><span class="sxs-lookup"><span data-stu-id="36fa8-111">PARAMETERS</span></span>

### <span data-ttu-id="36fa8-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="36fa8-112">-ApiProperty</span></span>
<span data-ttu-id="36fa8-113">認知服務帳戶的 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="36fa8-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="36fa8-114">特定帳戶類型所需。</span><span class="sxs-lookup"><span data-stu-id="36fa8-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fa8-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="36fa8-115">-AssignIdentity</span></span>
<span data-ttu-id="36fa8-116">針對此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="36fa8-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="36fa8-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="36fa8-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="36fa8-118">是否將認知服務帳戶加密 KeySource 設定為 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="36fa8-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="36fa8-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="36fa8-119">-CustomSubdomainName</span></span>
<span data-ttu-id="36fa8-120">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="36fa8-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="36fa8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fa8-121">-DefaultProfile</span></span>
<span data-ttu-id="36fa8-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36fa8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36fa8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="36fa8-123">-Force</span></span>
<span data-ttu-id="36fa8-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="36fa8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36fa8-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="36fa8-125">-KeyName</span></span>
<span data-ttu-id="36fa8-126">認知服務帳戶加密 keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="36fa8-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="36fa8-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="36fa8-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="36fa8-128">是否將認知服務帳戶加密 keySource 設定為 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="36fa8-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="36fa8-129">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，認知服務帳戶加密 KeySource 也會設定為 Microsoft。 KeyVault 天氣此參數已設定。</span><span class="sxs-lookup"><span data-stu-id="36fa8-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="36fa8-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="36fa8-130">-KeyVaultUri</span></span>
<span data-ttu-id="36fa8-131">認知服務帳戶加密 keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="36fa8-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="36fa8-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="36fa8-132">-KeyVersion</span></span>
<span data-ttu-id="36fa8-133">認知服務帳戶加密 keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="36fa8-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="36fa8-134">-位置</span><span class="sxs-lookup"><span data-stu-id="36fa8-134">-Location</span></span>
<span data-ttu-id="36fa8-135">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="36fa8-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="36fa8-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="36fa8-136">-Name</span></span>
<span data-ttu-id="36fa8-137">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="36fa8-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="36fa8-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="36fa8-138">-NetworkRuleSet</span></span>
<span data-ttu-id="36fa8-139">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="36fa8-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="36fa8-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="36fa8-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="36fa8-141">認知服務帳戶的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="36fa8-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fa8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fa8-142">-ResourceGroupName</span></span>
<span data-ttu-id="36fa8-143">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36fa8-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="36fa8-144">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="36fa8-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="36fa8-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36fa8-145">-SkuName</span></span>
<span data-ttu-id="36fa8-146">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="36fa8-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="36fa8-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="36fa8-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36fa8-148">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="36fa8-148">F0 (free tier)</span></span>
- <span data-ttu-id="36fa8-149">S0</span><span class="sxs-lookup"><span data-stu-id="36fa8-149">S0</span></span>
- <span data-ttu-id="36fa8-150">S1</span><span class="sxs-lookup"><span data-stu-id="36fa8-150">S1</span></span>
- <span data-ttu-id="36fa8-151">S2</span><span class="sxs-lookup"><span data-stu-id="36fa8-151">S2</span></span>
- <span data-ttu-id="36fa8-152">S3</span><span class="sxs-lookup"><span data-stu-id="36fa8-152">S3</span></span>
- <span data-ttu-id="36fa8-153">S4 如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="36fa8-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="36fa8-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="36fa8-154">-StorageAccountId</span></span>
<span data-ttu-id="36fa8-155">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="36fa8-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="36fa8-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="36fa8-156">-Tag</span></span>
<span data-ttu-id="36fa8-157">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="36fa8-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="36fa8-158">-類型</span><span class="sxs-lookup"><span data-stu-id="36fa8-158">-Type</span></span>
<span data-ttu-id="36fa8-159">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="36fa8-159">Specifies the type of account to create.</span></span> <span data-ttu-id="36fa8-160">使用 `Get-AzCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="36fa8-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="36fa8-161">-確認</span><span class="sxs-lookup"><span data-stu-id="36fa8-161">-Confirm</span></span>
<span data-ttu-id="36fa8-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36fa8-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fa8-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fa8-163">-WhatIf</span></span>
<span data-ttu-id="36fa8-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36fa8-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36fa8-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36fa8-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fa8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fa8-166">CommonParameters</span></span>
<span data-ttu-id="36fa8-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36fa8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fa8-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36fa8-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fa8-169">輸入</span><span class="sxs-lookup"><span data-stu-id="36fa8-169">INPUTS</span></span>

### <span data-ttu-id="36fa8-170">System.object</span><span class="sxs-lookup"><span data-stu-id="36fa8-170">System.String</span></span>

## <span data-ttu-id="36fa8-171">輸出</span><span class="sxs-lookup"><span data-stu-id="36fa8-171">OUTPUTS</span></span>

### <span data-ttu-id="36fa8-172">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="36fa8-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="36fa8-173">筆記</span><span class="sxs-lookup"><span data-stu-id="36fa8-173">NOTES</span></span>

## <span data-ttu-id="36fa8-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="36fa8-174">RELATED LINKS</span></span>

[<span data-ttu-id="36fa8-175">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="36fa8-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="36fa8-176">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="36fa8-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="36fa8-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="36fa8-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
