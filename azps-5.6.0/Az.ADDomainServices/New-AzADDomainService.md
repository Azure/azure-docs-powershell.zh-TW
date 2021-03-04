---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910573"
---
# <span data-ttu-id="758eb-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="758eb-101">New-AzADDomainService</span></span>

## <span data-ttu-id="758eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="758eb-102">SYNOPSIS</span></span>
<span data-ttu-id="758eb-103">建立網域服務作業會建立具有指定參數的新網域服務。</span><span class="sxs-lookup"><span data-stu-id="758eb-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="758eb-104">如果特定服務已存在，則任何可修補的屬性都會更新，而且任何可更新的屬性都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="758eb-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="758eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="758eb-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="758eb-106">描述</span><span class="sxs-lookup"><span data-stu-id="758eb-106">DESCRIPTION</span></span>
<span data-ttu-id="758eb-107">建立網域服務作業會建立具有指定參數的新網域服務。</span><span class="sxs-lookup"><span data-stu-id="758eb-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="758eb-108">如果特定服務已存在，則任何可修補的屬性都會更新，而且任何可更新的屬性都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="758eb-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="758eb-109">例子</span><span class="sxs-lookup"><span data-stu-id="758eb-109">EXAMPLES</span></span>

### <span data-ttu-id="758eb-110">範例 1：建立新 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="758eb-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="758eb-111">建立新 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="758eb-111">Create new ADDomainService</span></span>

## <span data-ttu-id="758eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="758eb-112">PARAMETERS</span></span>

### <span data-ttu-id="758eb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="758eb-113">-AsJob</span></span>
<span data-ttu-id="758eb-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="758eb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="758eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758eb-115">-DefaultProfile</span></span>
<span data-ttu-id="758eb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="758eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="758eb-117">-DomainConfigurationType</span></span>
<span data-ttu-id="758eb-118">網域組配置類型</span><span class="sxs-lookup"><span data-stu-id="758eb-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="758eb-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="758eb-119">-DomainName</span></span>
<span data-ttu-id="758eb-120">使用者要部署網域服務的 Azure 網功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="758eb-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="758eb-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="758eb-122">一個旗標，判斷 NtlmV1 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="758eb-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="758eb-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="758eb-124">一個旗標，判斷 SyncKerberosPasswords 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="758eb-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="758eb-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="758eb-126">一個旗標，判斷是否已啟用或停用 SyncNtlmPasswords。</span><span class="sxs-lookup"><span data-stu-id="758eb-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="758eb-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="758eb-128">一個旗標，判斷是否已啟用或停用 SyncOnPremPasswords。</span><span class="sxs-lookup"><span data-stu-id="758eb-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="758eb-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="758eb-130">判斷 TlsV1 是否已啟用或停用的標標。</span><span class="sxs-lookup"><span data-stu-id="758eb-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="758eb-131">-FilteredSync</span></span>
<span data-ttu-id="758eb-132">啟用或停用旗標以開啟群組式篩選同步</span><span class="sxs-lookup"><span data-stu-id="758eb-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="758eb-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="758eb-133">-ForestTrust</span></span>
<span data-ttu-id="758eb-134">Resource Forest To construct 的設定清單，請參閱 FORESTTRUST 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="758eb-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="758eb-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="758eb-136">判斷是否已啟用或停用網際網路上安全 LDAP 存取的標標。</span><span class="sxs-lookup"><span data-stu-id="758eb-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="758eb-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="758eb-138">判斷是否已啟用或停用 Secure LDAP 的標標。</span><span class="sxs-lookup"><span data-stu-id="758eb-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="758eb-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="758eb-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="758eb-140">設定 Secure LDAP 所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="758eb-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="758eb-141">此處傳遞的參數應該是憑證 pfx 檔案的 base64encoded 表示。</span><span class="sxs-lookup"><span data-stu-id="758eb-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="758eb-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="758eb-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="758eb-143">解密所提供的 Secure LDAP 憑證 pfx 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="758eb-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="758eb-144">-Name</span></span>
<span data-ttu-id="758eb-145">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="758eb-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="758eb-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="758eb-147">其他收件者的清單</span><span class="sxs-lookup"><span data-stu-id="758eb-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="758eb-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="758eb-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="758eb-149">應該通知網域控制站管理員</span><span class="sxs-lookup"><span data-stu-id="758eb-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="758eb-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="758eb-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="758eb-151">全域系統管理員應該收到通知</span><span class="sxs-lookup"><span data-stu-id="758eb-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="758eb-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="758eb-152">-NoWait</span></span>
<span data-ttu-id="758eb-153">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="758eb-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="758eb-154">-複本集</span><span class="sxs-lookup"><span data-stu-id="758eb-154">-ReplicaSet</span></span>
<span data-ttu-id="758eb-155">要建構的複本集清單，請參閱有關複本集屬性的記事區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="758eb-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="758eb-156">-ResourceForest</span></span>
<span data-ttu-id="758eb-157">資源樹目錄</span><span class="sxs-lookup"><span data-stu-id="758eb-157">Resource Forest</span></span>

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

### <span data-ttu-id="758eb-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758eb-158">-ResourceGroupName</span></span>
<span data-ttu-id="758eb-159">使用者訂閱中資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="758eb-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="758eb-160">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="758eb-160">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="758eb-161">-Sku</span></span>
<span data-ttu-id="758eb-162">SKU 類型</span><span class="sxs-lookup"><span data-stu-id="758eb-162">Sku Type</span></span>

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

### <span data-ttu-id="758eb-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="758eb-163">-SubscriptionId</span></span>
<span data-ttu-id="758eb-164">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="758eb-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="758eb-165">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="758eb-165">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-166">-標記</span><span class="sxs-lookup"><span data-stu-id="758eb-166">-Tag</span></span>
<span data-ttu-id="758eb-167">資源標記</span><span class="sxs-lookup"><span data-stu-id="758eb-167">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-168">-確認</span><span class="sxs-lookup"><span data-stu-id="758eb-168">-Confirm</span></span>
<span data-ttu-id="758eb-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="758eb-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758eb-170">-WhatIf</span></span>
<span data-ttu-id="758eb-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="758eb-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758eb-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="758eb-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758eb-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758eb-173">CommonParameters</span></span>
<span data-ttu-id="758eb-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="758eb-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758eb-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="758eb-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758eb-176">輸入</span><span class="sxs-lookup"><span data-stu-id="758eb-176">INPUTS</span></span>

## <span data-ttu-id="758eb-177">輸出</span><span class="sxs-lookup"><span data-stu-id="758eb-177">OUTPUTS</span></span>

### <span data-ttu-id="758eb-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="758eb-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="758eb-179">筆記</span><span class="sxs-lookup"><span data-stu-id="758eb-179">NOTES</span></span>

<span data-ttu-id="758eb-180">別名</span><span class="sxs-lookup"><span data-stu-id="758eb-180">ALIASES</span></span>

<span data-ttu-id="758eb-181">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="758eb-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="758eb-182">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="758eb-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="758eb-183">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="758eb-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="758eb-184">FORESTTRUST <IForestTrust[]>：資源樹目錄的設定清單</span><span class="sxs-lookup"><span data-stu-id="758eb-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="758eb-185">`[FriendlyName <String>]`：好用名稱</span><span class="sxs-lookup"><span data-stu-id="758eb-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="758eb-186">`[RemoteDnsIP <String>]`：遠端 Dns ips</span><span class="sxs-lookup"><span data-stu-id="758eb-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="758eb-187">`[TrustDirection <String>]`：信任方向</span><span class="sxs-lookup"><span data-stu-id="758eb-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="758eb-188">`[TrustPassword <String>]`：信任密碼</span><span class="sxs-lookup"><span data-stu-id="758eb-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="758eb-189">`[TrustedDomainFqdn <String>]`：信任的網域 FQDN</span><span class="sxs-lookup"><span data-stu-id="758eb-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="758eb-190">複製<複本集[]>：複本集清單</span><span class="sxs-lookup"><span data-stu-id="758eb-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="758eb-191">`[Location <String>]`：虛擬網路位置</span><span class="sxs-lookup"><span data-stu-id="758eb-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="758eb-192">`[SubnetId <String>]`：網域服務將部署在的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="758eb-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="758eb-193">網域服務將部署之子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="758eb-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="758eb-194">/virtualNetwork/vnetName/子網/子網名稱。</span><span class="sxs-lookup"><span data-stu-id="758eb-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="758eb-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="758eb-195">RELATED LINKS</span></span>

