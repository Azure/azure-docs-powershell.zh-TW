---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: e6ed6669c98a54a037bcbdc579e08459cdff568e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909222"
---
# <span data-ttu-id="198b4-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="198b4-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="198b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="198b4-102">SYNOPSIS</span></span>
<span data-ttu-id="198b4-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="198b4-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="198b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="198b4-104">SYNTAX</span></span>

### <span data-ttu-id="198b4-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="198b4-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="198b4-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="198b4-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="198b4-107">描述</span><span class="sxs-lookup"><span data-stu-id="198b4-107">DESCRIPTION</span></span>
<span data-ttu-id="198b4-108">**New-AzCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="198b4-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="198b4-109">例子</span><span class="sxs-lookup"><span data-stu-id="198b4-109">EXAMPLES</span></span>

### <span data-ttu-id="198b4-110">1:</span><span class="sxs-lookup"><span data-stu-id="198b4-110">1:</span></span>
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

## <span data-ttu-id="198b4-111">參數</span><span class="sxs-lookup"><span data-stu-id="198b4-111">PARAMETERS</span></span>

### <span data-ttu-id="198b4-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="198b4-112">-ApiProperty</span></span>
<span data-ttu-id="198b4-113">認知服務帳戶的 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="198b4-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="198b4-114">這是特定帳戶類型所要求。</span><span class="sxs-lookup"><span data-stu-id="198b4-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="198b4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="198b4-115">-AssignIdentity</span></span>
<span data-ttu-id="198b4-116">為此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="198b4-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="198b4-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="198b4-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="198b4-118">是否要將認知服務帳戶加密金鑰Source 設定為 Microsoft.CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="198b4-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="198b4-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="198b4-119">-CustomSubdomainName</span></span>
<span data-ttu-id="198b4-120">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="198b4-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="198b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198b4-121">-DefaultProfile</span></span>
<span data-ttu-id="198b4-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="198b4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="198b4-123">-強制</span><span class="sxs-lookup"><span data-stu-id="198b4-123">-Force</span></span>
<span data-ttu-id="198b4-124">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="198b4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="198b4-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="198b4-125">-KeyName</span></span>
<span data-ttu-id="198b4-126">認知服務帳戶加密金鑰Source KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="198b4-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="198b4-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="198b4-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="198b4-128">是否要將認知服務帳戶加密金鑰Source 設定為 Microsoft.KeyVault。</span><span class="sxs-lookup"><span data-stu-id="198b4-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="198b4-129">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，則認知服務帳戶加密金鑰Source 也會設定為 Microsoft.KeyVault 天氣此參數為設定或不設定。</span><span class="sxs-lookup"><span data-stu-id="198b4-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="198b4-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="198b4-130">-KeyVaultUri</span></span>
<span data-ttu-id="198b4-131">認知服務帳戶加密金鑰Source KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="198b4-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="198b4-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="198b4-132">-KeyVersion</span></span>
<span data-ttu-id="198b4-133">認知服務帳戶加密金鑰Source KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="198b4-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="198b4-134">-位置</span><span class="sxs-lookup"><span data-stu-id="198b4-134">-Location</span></span>
<span data-ttu-id="198b4-135">指定建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="198b4-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="198b4-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="198b4-136">-Name</span></span>
<span data-ttu-id="198b4-137">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="198b4-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="198b4-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="198b4-138">-NetworkRuleSet</span></span>
<span data-ttu-id="198b4-139">NetworkRuleSet 可用來定義一組防火牆和虛擬網路的組組設定規則，以及設定網路屬性值，例如如何處理與任何已定義規則不相符的要求</span><span class="sxs-lookup"><span data-stu-id="198b4-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="198b4-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="198b4-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="198b4-141">認知服務帳戶的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="198b4-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="198b4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198b4-142">-ResourceGroupName</span></span>
<span data-ttu-id="198b4-143">指定要指派帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="198b4-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="198b4-144">資源群組必須已存在。</span><span class="sxs-lookup"><span data-stu-id="198b4-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="198b4-145">-SKUName</span><span class="sxs-lookup"><span data-stu-id="198b4-145">-SkuName</span></span>
<span data-ttu-id="198b4-146">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="198b4-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="198b4-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="198b4-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="198b4-148">F0 (免費層級) </span><span class="sxs-lookup"><span data-stu-id="198b4-148">F0 (free tier)</span></span>
- <span data-ttu-id="198b4-149">S0</span><span class="sxs-lookup"><span data-stu-id="198b4-149">S0</span></span>
- <span data-ttu-id="198b4-150">S1</span><span class="sxs-lookup"><span data-stu-id="198b4-150">S1</span></span>
- <span data-ttu-id="198b4-151">S2</span><span class="sxs-lookup"><span data-stu-id="198b4-151">S2</span></span>
- <span data-ttu-id="198b4-152">S3</span><span class="sxs-lookup"><span data-stu-id="198b4-152">S3</span></span>
- <span data-ttu-id="198b4-153">S4 如要詳細資訊，請參閱[認知服務 API。](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="198b4-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="198b4-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="198b4-154">-StorageAccountId</span></span>
<span data-ttu-id="198b4-155">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="198b4-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="198b4-156">-標記</span><span class="sxs-lookup"><span data-stu-id="198b4-156">-Tag</span></span>
<span data-ttu-id="198b4-157">將標記指定為名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="198b4-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="198b4-158">-類型</span><span class="sxs-lookup"><span data-stu-id="198b4-158">-Type</span></span>
<span data-ttu-id="198b4-159">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="198b4-159">Specifies the type of account to create.</span></span> <span data-ttu-id="198b4-160">使用 `Get-AzCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="198b4-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="198b4-161">-確認</span><span class="sxs-lookup"><span data-stu-id="198b4-161">-Confirm</span></span>
<span data-ttu-id="198b4-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="198b4-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="198b4-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198b4-163">-WhatIf</span></span>
<span data-ttu-id="198b4-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="198b4-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198b4-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="198b4-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="198b4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198b4-166">CommonParameters</span></span>
<span data-ttu-id="198b4-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="198b4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198b4-168">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="198b4-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198b4-169">輸入</span><span class="sxs-lookup"><span data-stu-id="198b4-169">INPUTS</span></span>

### <span data-ttu-id="198b4-170">System.String</span><span class="sxs-lookup"><span data-stu-id="198b4-170">System.String</span></span>

## <span data-ttu-id="198b4-171">輸出</span><span class="sxs-lookup"><span data-stu-id="198b4-171">OUTPUTS</span></span>

### <span data-ttu-id="198b4-172">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="198b4-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="198b4-173">筆記</span><span class="sxs-lookup"><span data-stu-id="198b4-173">NOTES</span></span>

## <span data-ttu-id="198b4-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="198b4-174">RELATED LINKS</span></span>

[<span data-ttu-id="198b4-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="198b4-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="198b4-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="198b4-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="198b4-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="198b4-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
