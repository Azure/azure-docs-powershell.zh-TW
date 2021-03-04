---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912105"
---
# <span data-ttu-id="48cc4-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48cc4-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="48cc4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="48cc4-103">修改帳戶。</span><span class="sxs-lookup"><span data-stu-id="48cc4-103">Modifies an account.</span></span>

## <span data-ttu-id="48cc4-104">語法</span><span class="sxs-lookup"><span data-stu-id="48cc4-104">SYNTAX</span></span>

### <span data-ttu-id="48cc4-105">CognitiveServicesEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="48cc4-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48cc4-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="48cc4-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48cc4-107">描述</span><span class="sxs-lookup"><span data-stu-id="48cc4-107">DESCRIPTION</span></span>
<span data-ttu-id="48cc4-108">**Set-AzCognitiveServicesAccount** Cmdlet 會修改指定認知服務帳戶的 SKU 或標籤。</span><span class="sxs-lookup"><span data-stu-id="48cc4-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="48cc4-109">例子</span><span class="sxs-lookup"><span data-stu-id="48cc4-109">EXAMPLES</span></span>

### <span data-ttu-id="48cc4-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="48cc4-110">Example 1</span></span>
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

## <span data-ttu-id="48cc4-111">參數</span><span class="sxs-lookup"><span data-stu-id="48cc4-111">PARAMETERS</span></span>

### <span data-ttu-id="48cc4-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="48cc4-112">-ApiProperty</span></span>
<span data-ttu-id="48cc4-113">認知服務帳戶的 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="48cc4-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="48cc4-114">這是特定帳戶類型所要求。</span><span class="sxs-lookup"><span data-stu-id="48cc4-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="48cc4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="48cc4-115">-AssignIdentity</span></span>
<span data-ttu-id="48cc4-116">為此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="48cc4-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="48cc4-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="48cc4-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="48cc4-118">是否要將認知服務帳戶加密金鑰Source 設定為 Microsoft.CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="48cc4-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="48cc4-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="48cc4-119">-CustomSubdomainName</span></span>
<span data-ttu-id="48cc4-120">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="48cc4-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="48cc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cc4-121">-DefaultProfile</span></span>
<span data-ttu-id="48cc4-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="48cc4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48cc4-123">-強制</span><span class="sxs-lookup"><span data-stu-id="48cc4-123">-Force</span></span>
<span data-ttu-id="48cc4-124">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="48cc4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48cc4-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="48cc4-125">-IdentityType</span></span>
<span data-ttu-id="48cc4-126">受管理服務身分識別的類型。</span><span class="sxs-lookup"><span data-stu-id="48cc4-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="48cc4-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="48cc4-127">-KeyName</span></span>
<span data-ttu-id="48cc4-128">認知服務帳戶加密金鑰Source KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="48cc4-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="48cc4-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="48cc4-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="48cc4-130">是否要將認知服務帳戶加密金鑰Source 設定為 Microsoft.KeyVault。</span><span class="sxs-lookup"><span data-stu-id="48cc4-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="48cc4-131">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，則認知服務帳戶加密金鑰Source 也會設定為 Microsoft.KeyVault 天氣此參數為設定或不設定。</span><span class="sxs-lookup"><span data-stu-id="48cc4-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="48cc4-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="48cc4-132">-KeyVaultUri</span></span>
<span data-ttu-id="48cc4-133">認知服務帳戶加密金鑰Source KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="48cc4-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="48cc4-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="48cc4-134">-KeyVersion</span></span>
<span data-ttu-id="48cc4-135">認知服務帳戶加密金鑰Source KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="48cc4-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="48cc4-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="48cc4-136">-Name</span></span>
<span data-ttu-id="48cc4-137">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="48cc4-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="48cc4-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="48cc4-138">-NetworkRuleSet</span></span>
<span data-ttu-id="48cc4-139">NetworkRuleSet 可用來定義一組防火牆和虛擬網路的組組設定規則，以及設定網路屬性值，例如如何處理與任何已定義規則不相符的要求</span><span class="sxs-lookup"><span data-stu-id="48cc4-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="48cc4-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="48cc4-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="48cc4-141">認知服務帳戶的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="48cc4-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="48cc4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cc4-142">-ResourceGroupName</span></span>
<span data-ttu-id="48cc4-143">指定帳戶指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="48cc4-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="48cc4-144">-SKUName</span><span class="sxs-lookup"><span data-stu-id="48cc4-144">-SkuName</span></span>
<span data-ttu-id="48cc4-145">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="48cc4-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="48cc4-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="48cc4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48cc4-147">F0 (免費層級) </span><span class="sxs-lookup"><span data-stu-id="48cc4-147">F0 (free tier)</span></span>
- <span data-ttu-id="48cc4-148">S0</span><span class="sxs-lookup"><span data-stu-id="48cc4-148">S0</span></span>
- <span data-ttu-id="48cc4-149">S1</span><span class="sxs-lookup"><span data-stu-id="48cc4-149">S1</span></span>
- <span data-ttu-id="48cc4-150">S2</span><span class="sxs-lookup"><span data-stu-id="48cc4-150">S2</span></span>
- <span data-ttu-id="48cc4-151">S3</span><span class="sxs-lookup"><span data-stu-id="48cc4-151">S3</span></span>
- <span data-ttu-id="48cc4-152">S4</span><span class="sxs-lookup"><span data-stu-id="48cc4-152">S4</span></span>

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

### <span data-ttu-id="48cc4-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="48cc4-153">-StorageAccountId</span></span>
<span data-ttu-id="48cc4-154">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="48cc4-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="48cc4-155">-標記</span><span class="sxs-lookup"><span data-stu-id="48cc4-155">-Tag</span></span>
<span data-ttu-id="48cc4-156">將標記指定為名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="48cc4-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="48cc4-157">-確認</span><span class="sxs-lookup"><span data-stu-id="48cc4-157">-Confirm</span></span>
<span data-ttu-id="48cc4-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48cc4-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cc4-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48cc4-159">-WhatIf</span></span>
<span data-ttu-id="48cc4-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48cc4-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48cc4-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48cc4-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cc4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cc4-162">CommonParameters</span></span>
<span data-ttu-id="48cc4-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48cc4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cc4-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48cc4-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cc4-165">輸入</span><span class="sxs-lookup"><span data-stu-id="48cc4-165">INPUTS</span></span>

### <span data-ttu-id="48cc4-166">System.String</span><span class="sxs-lookup"><span data-stu-id="48cc4-166">System.String</span></span>

### <span data-ttu-id="48cc4-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="48cc4-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="48cc4-168">輸出</span><span class="sxs-lookup"><span data-stu-id="48cc4-168">OUTPUTS</span></span>

### <span data-ttu-id="48cc4-169">Microsoft.Azure.Commands.management.CognitiveServices.models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48cc4-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="48cc4-170">筆記</span><span class="sxs-lookup"><span data-stu-id="48cc4-170">NOTES</span></span>

## <span data-ttu-id="48cc4-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="48cc4-171">RELATED LINKS</span></span>

[<span data-ttu-id="48cc4-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48cc4-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="48cc4-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48cc4-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="48cc4-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48cc4-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
