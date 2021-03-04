---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 3e60546992957a027dd5bbb94281e19e74e42274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908094"
---
# <span data-ttu-id="307d9-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="307d9-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="307d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="307d9-102">SYNOPSIS</span></span>
<span data-ttu-id="307d9-103">建立新 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="307d9-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="307d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="307d9-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="307d9-105">描述</span><span class="sxs-lookup"><span data-stu-id="307d9-105">DESCRIPTION</span></span>
<span data-ttu-id="307d9-106">**New-AzFirewallPolicy** Cmdlet 會建立 Azure 防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="307d9-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="307d9-107">例子</span><span class="sxs-lookup"><span data-stu-id="307d9-107">EXAMPLES</span></span>

### <span data-ttu-id="307d9-108">範例 1：1。</span><span class="sxs-lookup"><span data-stu-id="307d9-108">Example 1: 1.</span></span> <span data-ttu-id="307d9-109">建立空白策略</span><span class="sxs-lookup"><span data-stu-id="307d9-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="307d9-110">此範例會建立 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="307d9-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="307d9-111">範例 2：2。</span><span class="sxs-lookup"><span data-stu-id="307d9-111">Example 2: 2.</span></span> <span data-ttu-id="307d9-112">使用 ThreatIntel 模式建立空白策略</span><span class="sxs-lookup"><span data-stu-id="307d9-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="307d9-113">此範例會使用威脅 Intel 模式建立 Azure 防火牆策略</span><span class="sxs-lookup"><span data-stu-id="307d9-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="307d9-114">範例 3：3。</span><span class="sxs-lookup"><span data-stu-id="307d9-114">Example 3: 3.</span></span> <span data-ttu-id="307d9-115">使用 ThreatIntel Whitelist 建立空白政策</span><span class="sxs-lookup"><span data-stu-id="307d9-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="307d9-116">此範例會使用威脅 intel Whitelist 建立 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="307d9-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="307d9-117">範例 4：4。</span><span class="sxs-lookup"><span data-stu-id="307d9-117">Example 4: 4.</span></span> <span data-ttu-id="307d9-118">使用入侵偵測、身分識別與傳輸安全性建立策略</span><span class="sxs-lookup"><span data-stu-id="307d9-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="307d9-119">此範例會建立 Azure 防火牆策略，以模式警示、使用者指派的身分識別與傳輸安全性進行入侵偵測</span><span class="sxs-lookup"><span data-stu-id="307d9-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="307d9-120">參數</span><span class="sxs-lookup"><span data-stu-id="307d9-120">PARAMETERS</span></span>

### <span data-ttu-id="307d9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="307d9-121">-AsJob</span></span>
<span data-ttu-id="307d9-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="307d9-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="307d9-123">-BasePolicy</span></span>
<span data-ttu-id="307d9-124">繼承基礎策略</span><span class="sxs-lookup"><span data-stu-id="307d9-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307d9-125">-DefaultProfile</span></span>
<span data-ttu-id="307d9-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="307d9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="307d9-127">-DnsSetting</span></span>
<span data-ttu-id="307d9-128">DNS 設定</span><span class="sxs-lookup"><span data-stu-id="307d9-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-129">-強制</span><span class="sxs-lookup"><span data-stu-id="307d9-129">-Force</span></span>
<span data-ttu-id="307d9-130">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="307d9-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-131">-身分識別</span><span class="sxs-lookup"><span data-stu-id="307d9-131">-Identity</span></span>
<span data-ttu-id="307d9-132">要指派給防火牆策略的防火牆策略身分識別。</span><span class="sxs-lookup"><span data-stu-id="307d9-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-133">-入侵Detection</span><span class="sxs-lookup"><span data-stu-id="307d9-133">-IntrusionDetection</span></span>
<span data-ttu-id="307d9-134">入侵偵測設定</span><span class="sxs-lookup"><span data-stu-id="307d9-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-135">-位置</span><span class="sxs-lookup"><span data-stu-id="307d9-135">-Location</span></span>
<span data-ttu-id="307d9-136">位置。</span><span class="sxs-lookup"><span data-stu-id="307d9-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="307d9-137">-Name</span></span>
<span data-ttu-id="307d9-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="307d9-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307d9-139">-ResourceGroupName</span></span>
<span data-ttu-id="307d9-140">資源組名。</span><span class="sxs-lookup"><span data-stu-id="307d9-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="307d9-141">-SkuTier</span></span>
<span data-ttu-id="307d9-142">防火牆策略 SKU 層級</span><span class="sxs-lookup"><span data-stu-id="307d9-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-143">-標記</span><span class="sxs-lookup"><span data-stu-id="307d9-143">-Tag</span></span>
<span data-ttu-id="307d9-144">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="307d9-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="307d9-145">-ThreatIntelMode</span></span>
<span data-ttu-id="307d9-146">威脅情報的作業模式。</span><span class="sxs-lookup"><span data-stu-id="307d9-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="307d9-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="307d9-148">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="307d9-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="307d9-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="307d9-150">儲存在 KeyVault (之 (64 編碼未加密的 pfx) "機密"或 "憑證" 物件之機密識別碼</span><span class="sxs-lookup"><span data-stu-id="307d9-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="307d9-151">-TransportSecurityName</span></span>
<span data-ttu-id="307d9-152">傳輸安全性名稱</span><span class="sxs-lookup"><span data-stu-id="307d9-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="307d9-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="307d9-154">指派身分識別給使用者的 ResourceId，指派給防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="307d9-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-155">-確認</span><span class="sxs-lookup"><span data-stu-id="307d9-155">-Confirm</span></span>
<span data-ttu-id="307d9-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="307d9-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="307d9-157">-WhatIf</span></span>
<span data-ttu-id="307d9-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="307d9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="307d9-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="307d9-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307d9-160">CommonParameters</span></span>
<span data-ttu-id="307d9-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="307d9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307d9-162">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="307d9-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307d9-163">輸入</span><span class="sxs-lookup"><span data-stu-id="307d9-163">INPUTS</span></span>

### <span data-ttu-id="307d9-164">System.String</span><span class="sxs-lookup"><span data-stu-id="307d9-164">System.String</span></span>

### <span data-ttu-id="307d9-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="307d9-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="307d9-166">輸出</span><span class="sxs-lookup"><span data-stu-id="307d9-166">OUTPUTS</span></span>

### <span data-ttu-id="307d9-167">Microsoft.Azure.Commands.Network.models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="307d9-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="307d9-168">筆記</span><span class="sxs-lookup"><span data-stu-id="307d9-168">NOTES</span></span>

## <span data-ttu-id="307d9-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="307d9-169">RELATED LINKS</span></span>
