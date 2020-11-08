---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127144"
---
# <span data-ttu-id="8e1d3-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e1d3-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8e1d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1d3-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-103">Modifies an account.</span></span>

## <span data-ttu-id="8e1d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e1d3-104">SYNTAX</span></span>

### <span data-ttu-id="8e1d3-105">CognitiveServicesEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="8e1d3-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1d3-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="8e1d3-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e1d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e1d3-107">DESCRIPTION</span></span>
<span data-ttu-id="8e1d3-108">**AzCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8e1d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e1d3-109">EXAMPLES</span></span>

### <span data-ttu-id="8e1d3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8e1d3-110">Example 1</span></span>
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

## <span data-ttu-id="8e1d3-111">參數</span><span class="sxs-lookup"><span data-stu-id="8e1d3-111">PARAMETERS</span></span>

### <span data-ttu-id="8e1d3-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="8e1d3-112">-ApiProperty</span></span>
<span data-ttu-id="8e1d3-113">認知服務帳戶的 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="8e1d3-114">特定帳戶類型所需。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="8e1d3-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8e1d3-115">-AssignIdentity</span></span>
<span data-ttu-id="8e1d3-116">針對此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8e1d3-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="8e1d3-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="8e1d3-118">是否將認知服務帳戶加密 KeySource 設定為 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="8e1d3-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="8e1d3-119">-CustomSubdomainName</span></span>
<span data-ttu-id="8e1d3-120">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="8e1d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1d3-121">-DefaultProfile</span></span>
<span data-ttu-id="8e1d3-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8e1d3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e1d3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8e1d3-123">-Force</span></span>
<span data-ttu-id="8e1d3-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e1d3-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8e1d3-125">-IdentityType</span></span>
<span data-ttu-id="8e1d3-126">受管理的服務身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e1d3-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8e1d3-127">-KeyName</span></span>
<span data-ttu-id="8e1d3-128">認知服務帳戶加密 keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="8e1d3-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="8e1d3-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="8e1d3-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="8e1d3-130">是否將認知服務帳戶加密 keySource 設定為 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="8e1d3-131">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，認知服務帳戶加密 KeySource 也會設定為 Microsoft。 KeyVault 天氣此參數已設定。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="8e1d3-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8e1d3-132">-KeyVaultUri</span></span>
<span data-ttu-id="8e1d3-133">認知服務帳戶加密 keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8e1d3-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="8e1d3-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8e1d3-134">-KeyVersion</span></span>
<span data-ttu-id="8e1d3-135">認知服務帳戶加密 keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8e1d3-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="8e1d3-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e1d3-136">-Name</span></span>
<span data-ttu-id="8e1d3-137">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="8e1d3-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e1d3-138">-NetworkRuleSet</span></span>
<span data-ttu-id="8e1d3-139">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="8e1d3-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="8e1d3-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8e1d3-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="8e1d3-141">認知服務帳戶的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="8e1d3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1d3-142">-ResourceGroupName</span></span>
<span data-ttu-id="8e1d3-143">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8e1d3-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8e1d3-144">-SkuName</span></span>
<span data-ttu-id="8e1d3-145">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8e1d3-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8e1d3-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e1d3-147">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="8e1d3-147">F0 (free tier)</span></span>
- <span data-ttu-id="8e1d3-148">S0</span><span class="sxs-lookup"><span data-stu-id="8e1d3-148">S0</span></span>
- <span data-ttu-id="8e1d3-149">S1</span><span class="sxs-lookup"><span data-stu-id="8e1d3-149">S1</span></span>
- <span data-ttu-id="8e1d3-150">S2</span><span class="sxs-lookup"><span data-stu-id="8e1d3-150">S2</span></span>
- <span data-ttu-id="8e1d3-151">S3</span><span class="sxs-lookup"><span data-stu-id="8e1d3-151">S3</span></span>
- <span data-ttu-id="8e1d3-152">喚醒</span><span class="sxs-lookup"><span data-stu-id="8e1d3-152">S4</span></span>

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

### <span data-ttu-id="8e1d3-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e1d3-153">-StorageAccountId</span></span>
<span data-ttu-id="8e1d3-154">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="8e1d3-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e1d3-155">-Tag</span></span>
<span data-ttu-id="8e1d3-156">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="8e1d3-157">-確認</span><span class="sxs-lookup"><span data-stu-id="8e1d3-157">-Confirm</span></span>
<span data-ttu-id="8e1d3-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1d3-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1d3-159">-WhatIf</span></span>
<span data-ttu-id="8e1d3-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e1d3-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e1d3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1d3-162">CommonParameters</span></span>
<span data-ttu-id="8e1d3-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1d3-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1d3-165">輸入</span><span class="sxs-lookup"><span data-stu-id="8e1d3-165">INPUTS</span></span>

### <span data-ttu-id="8e1d3-166">System.object</span><span class="sxs-lookup"><span data-stu-id="8e1d3-166">System.String</span></span>

### <span data-ttu-id="8e1d3-167">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="8e1d3-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8e1d3-168">輸出</span><span class="sxs-lookup"><span data-stu-id="8e1d3-168">OUTPUTS</span></span>

### <span data-ttu-id="8e1d3-169">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="8e1d3-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8e1d3-170">筆記</span><span class="sxs-lookup"><span data-stu-id="8e1d3-170">NOTES</span></span>

## <span data-ttu-id="8e1d3-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e1d3-171">RELATED LINKS</span></span>

[<span data-ttu-id="8e1d3-172">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e1d3-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8e1d3-173">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e1d3-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8e1d3-174">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e1d3-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
