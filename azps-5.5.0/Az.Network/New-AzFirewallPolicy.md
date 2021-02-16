---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 0e3a9b99a23715b63eb42c83ba112776272969ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128866"
---
# <span data-ttu-id="102f8-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="102f8-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="102f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="102f8-102">SYNOPSIS</span></span>
<span data-ttu-id="102f8-103">建立新的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="102f8-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="102f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="102f8-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="102f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="102f8-105">DESCRIPTION</span></span>
<span data-ttu-id="102f8-106">**新的-AzFirewallPolicy** Cmdlet 會建立 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="102f8-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="102f8-107">示例</span><span class="sxs-lookup"><span data-stu-id="102f8-107">EXAMPLES</span></span>

### <span data-ttu-id="102f8-108">範例 1: 1。</span><span class="sxs-lookup"><span data-stu-id="102f8-108">Example 1: 1.</span></span> <span data-ttu-id="102f8-109">建立空白原則</span><span class="sxs-lookup"><span data-stu-id="102f8-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="102f8-110">這個範例會建立 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="102f8-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="102f8-111">範例 2: 2。</span><span class="sxs-lookup"><span data-stu-id="102f8-111">Example 2: 2.</span></span> <span data-ttu-id="102f8-112">使用 ThreatIntel 模式建立空原則</span><span class="sxs-lookup"><span data-stu-id="102f8-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="102f8-113">這個範例會建立含威脅英特爾模式的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="102f8-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="102f8-114">範例 3: 3。</span><span class="sxs-lookup"><span data-stu-id="102f8-114">Example 3: 3.</span></span> <span data-ttu-id="102f8-115">使用 ThreatIntel 白名單建立空白原則</span><span class="sxs-lookup"><span data-stu-id="102f8-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="102f8-116">這個範例會建立一個含有威脅英特爾白名單的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="102f8-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="102f8-117">範例 4: 4。</span><span class="sxs-lookup"><span data-stu-id="102f8-117">Example 4: 4.</span></span> <span data-ttu-id="102f8-118">使用入侵偵測、身分識別和傳輸安全性建立原則</span><span class="sxs-lookup"><span data-stu-id="102f8-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="102f8-119">這個範例會以模式警示、使用者指派身分識別和傳輸安全性來建立 azure 防火牆原則與入侵偵測</span><span class="sxs-lookup"><span data-stu-id="102f8-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="102f8-120">參數</span><span class="sxs-lookup"><span data-stu-id="102f8-120">PARAMETERS</span></span>

### <span data-ttu-id="102f8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="102f8-121">-AsJob</span></span>
<span data-ttu-id="102f8-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="102f8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="102f8-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="102f8-123">-BasePolicy</span></span>
<span data-ttu-id="102f8-124">要從其繼承的基本原則</span><span class="sxs-lookup"><span data-stu-id="102f8-124">The base policy to inherit from</span></span>

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

### <span data-ttu-id="102f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102f8-125">-DefaultProfile</span></span>
<span data-ttu-id="102f8-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="102f8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102f8-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="102f8-127">-DnsSetting</span></span>
<span data-ttu-id="102f8-128">DNS 設定</span><span class="sxs-lookup"><span data-stu-id="102f8-128">The DNS Setting</span></span>

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

### <span data-ttu-id="102f8-129">-Force</span><span class="sxs-lookup"><span data-stu-id="102f8-129">-Force</span></span>
<span data-ttu-id="102f8-130">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="102f8-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="102f8-131">身分識別</span><span class="sxs-lookup"><span data-stu-id="102f8-131">-Identity</span></span>
<span data-ttu-id="102f8-132">要指派給防火牆原則的防火牆原則身分識別。</span><span class="sxs-lookup"><span data-stu-id="102f8-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

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

### <span data-ttu-id="102f8-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="102f8-133">-IntrusionDetection</span></span>
<span data-ttu-id="102f8-134">入侵偵測設定</span><span class="sxs-lookup"><span data-stu-id="102f8-134">The Intrusion Detection Setting</span></span>

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

### <span data-ttu-id="102f8-135">-位置</span><span class="sxs-lookup"><span data-stu-id="102f8-135">-Location</span></span>
<span data-ttu-id="102f8-136">位於.</span><span class="sxs-lookup"><span data-stu-id="102f8-136">location.</span></span>

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

### <span data-ttu-id="102f8-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="102f8-137">-Name</span></span>
<span data-ttu-id="102f8-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="102f8-138">The resource name.</span></span>

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

### <span data-ttu-id="102f8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102f8-139">-ResourceGroupName</span></span>
<span data-ttu-id="102f8-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="102f8-140">The resource group name.</span></span>

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

### <span data-ttu-id="102f8-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="102f8-141">-SkuTier</span></span>
<span data-ttu-id="102f8-142">防火牆原則 sku 層級</span><span class="sxs-lookup"><span data-stu-id="102f8-142">Firewall policy sku tier</span></span>

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

### <span data-ttu-id="102f8-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="102f8-143">-Tag</span></span>
<span data-ttu-id="102f8-144">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="102f8-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="102f8-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="102f8-145">-ThreatIntelMode</span></span>
<span data-ttu-id="102f8-146">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="102f8-146">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="102f8-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="102f8-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="102f8-148">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="102f8-148">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="102f8-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="102f8-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="102f8-150">儲存在 KeyVault 中的) "Secret" 或 "Certificate" 物件 (以64編碼的未加密 pfx 的秘密識別碼</span><span class="sxs-lookup"><span data-stu-id="102f8-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

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

### <span data-ttu-id="102f8-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="102f8-151">-TransportSecurityName</span></span>
<span data-ttu-id="102f8-152">傳輸安全名稱</span><span class="sxs-lookup"><span data-stu-id="102f8-152">Transport security name</span></span>

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

### <span data-ttu-id="102f8-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="102f8-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="102f8-154">指派給防火牆原則的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="102f8-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

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

### <span data-ttu-id="102f8-155">-確認</span><span class="sxs-lookup"><span data-stu-id="102f8-155">-Confirm</span></span>
<span data-ttu-id="102f8-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="102f8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="102f8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="102f8-157">-WhatIf</span></span>
<span data-ttu-id="102f8-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="102f8-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="102f8-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="102f8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="102f8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102f8-160">CommonParameters</span></span>
<span data-ttu-id="102f8-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="102f8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102f8-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="102f8-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102f8-163">輸入</span><span class="sxs-lookup"><span data-stu-id="102f8-163">INPUTS</span></span>

### <span data-ttu-id="102f8-164">System.object</span><span class="sxs-lookup"><span data-stu-id="102f8-164">System.String</span></span>

### <span data-ttu-id="102f8-165">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="102f8-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="102f8-166">輸出</span><span class="sxs-lookup"><span data-stu-id="102f8-166">OUTPUTS</span></span>

### <span data-ttu-id="102f8-167">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="102f8-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="102f8-168">筆記</span><span class="sxs-lookup"><span data-stu-id="102f8-168">NOTES</span></span>

## <span data-ttu-id="102f8-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="102f8-169">RELATED LINKS</span></span>
