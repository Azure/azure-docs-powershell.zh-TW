---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956242"
---
# <span data-ttu-id="e19a1-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e19a1-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="e19a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e19a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e19a1-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="e19a1-103">Modifies an account.</span></span>

## <span data-ttu-id="e19a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e19a1-104">SYNTAX</span></span>

### <span data-ttu-id="e19a1-105">CognitiveServicesEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="e19a1-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e19a1-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e19a1-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e19a1-107">說明</span><span class="sxs-lookup"><span data-stu-id="e19a1-107">DESCRIPTION</span></span>
<span data-ttu-id="e19a1-108">**AzCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="e19a1-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="e19a1-109">示例</span><span class="sxs-lookup"><span data-stu-id="e19a1-109">EXAMPLES</span></span>

### <span data-ttu-id="e19a1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e19a1-110">Example 1</span></span>
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

## <span data-ttu-id="e19a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="e19a1-111">PARAMETERS</span></span>

### <span data-ttu-id="e19a1-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e19a1-112">-AssignIdentity</span></span>
<span data-ttu-id="e19a1-113">針對此儲存空間帳戶產生並指派新的認知服務帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="e19a1-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e19a1-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="e19a1-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="e19a1-115">是否將認知服務帳戶加密 KeySource 設定為 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="e19a1-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="e19a1-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="e19a1-116">-CustomSubdomainName</span></span>
<span data-ttu-id="e19a1-117">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="e19a1-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="e19a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19a1-118">-DefaultProfile</span></span>
<span data-ttu-id="e19a1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e19a1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e19a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e19a1-120">-Force</span></span>
<span data-ttu-id="e19a1-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e19a1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e19a1-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e19a1-122">-IdentityType</span></span>
<span data-ttu-id="e19a1-123">受管理的服務身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="e19a1-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="e19a1-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e19a1-124">-KeyName</span></span>
<span data-ttu-id="e19a1-125">認知服務帳戶加密 keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="e19a1-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="e19a1-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e19a1-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="e19a1-127">是否將認知服務帳戶加密 keySource 設定為 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e19a1-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="e19a1-128">如果您指定 KeyName、KeyVersion 和 KeyVaultUri，認知服務帳戶加密 KeySource 也會設定為 Microsoft。 KeyVault 天氣此參數已設定。</span><span class="sxs-lookup"><span data-stu-id="e19a1-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="e19a1-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e19a1-129">-KeyVaultUri</span></span>
<span data-ttu-id="e19a1-130">認知服務帳戶加密 keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e19a1-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="e19a1-131">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e19a1-131">-KeyVersion</span></span>
<span data-ttu-id="e19a1-132">認知服務帳戶加密 keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e19a1-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="e19a1-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="e19a1-133">-Name</span></span>
<span data-ttu-id="e19a1-134">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e19a1-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="e19a1-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e19a1-135">-NetworkRuleSet</span></span>
<span data-ttu-id="e19a1-136">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如如何處理不符合任何已定義規則的要求</span><span class="sxs-lookup"><span data-stu-id="e19a1-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="e19a1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19a1-137">-ResourceGroupName</span></span>
<span data-ttu-id="e19a1-138">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e19a1-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e19a1-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e19a1-139">-SkuName</span></span>
<span data-ttu-id="e19a1-140">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="e19a1-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="e19a1-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e19a1-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e19a1-142">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="e19a1-142">F0 (free tier)</span></span>
- <span data-ttu-id="e19a1-143">S0</span><span class="sxs-lookup"><span data-stu-id="e19a1-143">S0</span></span>
- <span data-ttu-id="e19a1-144">S1</span><span class="sxs-lookup"><span data-stu-id="e19a1-144">S1</span></span>
- <span data-ttu-id="e19a1-145">S2</span><span class="sxs-lookup"><span data-stu-id="e19a1-145">S2</span></span>
- <span data-ttu-id="e19a1-146">S3</span><span class="sxs-lookup"><span data-stu-id="e19a1-146">S3</span></span>
- <span data-ttu-id="e19a1-147">喚醒</span><span class="sxs-lookup"><span data-stu-id="e19a1-147">S4</span></span>

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

### <span data-ttu-id="e19a1-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e19a1-148">-StorageAccountId</span></span>
<span data-ttu-id="e19a1-149">使用者擁有的儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="e19a1-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="e19a1-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="e19a1-150">-Tag</span></span>
<span data-ttu-id="e19a1-151">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="e19a1-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="e19a1-152">-確認</span><span class="sxs-lookup"><span data-stu-id="e19a1-152">-Confirm</span></span>
<span data-ttu-id="e19a1-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e19a1-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e19a1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19a1-154">-WhatIf</span></span>
<span data-ttu-id="e19a1-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e19a1-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e19a1-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e19a1-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e19a1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19a1-157">CommonParameters</span></span>
<span data-ttu-id="e19a1-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e19a1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19a1-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e19a1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19a1-160">輸入</span><span class="sxs-lookup"><span data-stu-id="e19a1-160">INPUTS</span></span>

### <span data-ttu-id="e19a1-161">System.object</span><span class="sxs-lookup"><span data-stu-id="e19a1-161">System.String</span></span>

### <span data-ttu-id="e19a1-162">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="e19a1-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="e19a1-163">輸出</span><span class="sxs-lookup"><span data-stu-id="e19a1-163">OUTPUTS</span></span>

### <span data-ttu-id="e19a1-164">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="e19a1-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e19a1-165">筆記</span><span class="sxs-lookup"><span data-stu-id="e19a1-165">NOTES</span></span>

## <span data-ttu-id="e19a1-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="e19a1-166">RELATED LINKS</span></span>

[<span data-ttu-id="e19a1-167">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e19a1-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e19a1-168">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e19a1-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e19a1-169">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e19a1-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
