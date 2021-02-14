---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 977621a3f92a8239925494102aed8c672509b222
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127315"
---
# <span data-ttu-id="6fbd8-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="6fbd8-101">New-AzADDomainService</span></span>

## <span data-ttu-id="6fbd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbd8-103">[建立網域服務] 作業會建立具有指定參數的新網域服務。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="6fbd8-104">如果特定服務已存在，則任何 patchable 屬性都會更新，而且任何不可變的屬性都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="6fbd8-105">句法</span><span class="sxs-lookup"><span data-stu-id="6fbd8-105">SYNTAX</span></span>

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

## <span data-ttu-id="6fbd8-106">說明</span><span class="sxs-lookup"><span data-stu-id="6fbd8-106">DESCRIPTION</span></span>
<span data-ttu-id="6fbd8-107">[建立網域服務] 作業會建立具有指定參數的新網域服務。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="6fbd8-108">如果特定服務已存在，則任何 patchable 屬性都會更新，而且任何不可變的屬性都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="6fbd8-109">示例</span><span class="sxs-lookup"><span data-stu-id="6fbd8-109">EXAMPLES</span></span>

### <span data-ttu-id="6fbd8-110">範例1：建立新的 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="6fbd8-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="6fbd8-111">建立新 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="6fbd8-111">Create new ADDomainService</span></span>

## <span data-ttu-id="6fbd8-112">參數</span><span class="sxs-lookup"><span data-stu-id="6fbd8-112">PARAMETERS</span></span>

### <span data-ttu-id="6fbd8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fbd8-113">-AsJob</span></span>
<span data-ttu-id="6fbd8-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6fbd8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6fbd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbd8-115">-DefaultProfile</span></span>
<span data-ttu-id="6fbd8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbd8-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="6fbd8-117">-DomainConfigurationType</span></span>
<span data-ttu-id="6fbd8-118">網域配置類型</span><span class="sxs-lookup"><span data-stu-id="6fbd8-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="6fbd8-119">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="6fbd8-119">-DomainName</span></span>
<span data-ttu-id="6fbd8-120">使用者想要將網域服務部署到哪個 Azure 網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="6fbd8-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="6fbd8-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="6fbd8-122">判斷是否已啟用或停用 NtlmV1 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="6fbd8-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="6fbd8-124">判斷是否已啟用或停用 SyncKerberosPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="6fbd8-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="6fbd8-126">判斷是否已啟用或停用 SyncNtlmPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="6fbd8-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="6fbd8-128">判斷是否已啟用或停用 SyncOnPremPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="6fbd8-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="6fbd8-130">判斷是否已啟用或停用 TlsV1 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="6fbd8-131">-FilteredSync</span></span>
<span data-ttu-id="6fbd8-132">啟用或停用標誌以開啟群組式篩選同步處理</span><span class="sxs-lookup"><span data-stu-id="6fbd8-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="6fbd8-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="6fbd8-133">-ForestTrust</span></span>
<span data-ttu-id="6fbd8-134">要構造之資原始目錄林的設定清單，請參閱 FORESTTRUST 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="6fbd8-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="6fbd8-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="6fbd8-136">[標誌] 可判斷是否已啟用或停用網際網路的安全 LDAP 存取。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="6fbd8-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="6fbd8-138">用於判斷是否已啟用或停用 [安全 LDAP] 的標誌。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="6fbd8-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="6fbd8-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="6fbd8-140">要設定安全 LDAP 所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="6fbd8-141">在此傳遞的參數應該是憑證 pfx 檔案的 base64encoded 標記法。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="6fbd8-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6fbd8-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="6fbd8-143">解密提供的安全 LDAP 憑證 pfx 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="6fbd8-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fbd8-144">-Name</span></span>
<span data-ttu-id="6fbd8-145">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-145">The name of the domain service.</span></span>

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

### <span data-ttu-id="6fbd8-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="6fbd8-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="6fbd8-147">其他收件者清單</span><span class="sxs-lookup"><span data-stu-id="6fbd8-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="6fbd8-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="6fbd8-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="6fbd8-149">是否應該通知網網域控制站管理員</span><span class="sxs-lookup"><span data-stu-id="6fbd8-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="6fbd8-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="6fbd8-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="6fbd8-151">系統應通知全域管理員</span><span class="sxs-lookup"><span data-stu-id="6fbd8-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="6fbd8-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6fbd8-152">-NoWait</span></span>
<span data-ttu-id="6fbd8-153">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6fbd8-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6fbd8-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="6fbd8-154">-ReplicaSet</span></span>
<span data-ttu-id="6fbd8-155">要構造的 ReplicaSets 清單，請參閱 REPLICASET 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

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

### <span data-ttu-id="6fbd8-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="6fbd8-156">-ResourceForest</span></span>
<span data-ttu-id="6fbd8-157">資原始目錄林</span><span class="sxs-lookup"><span data-stu-id="6fbd8-157">Resource Forest</span></span>

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

### <span data-ttu-id="6fbd8-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbd8-158">-ResourceGroupName</span></span>
<span data-ttu-id="6fbd8-159">使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="6fbd8-160">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6fbd8-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="6fbd8-161">-Sku</span></span>
<span data-ttu-id="6fbd8-162">Sku 類型</span><span class="sxs-lookup"><span data-stu-id="6fbd8-162">Sku Type</span></span>

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

### <span data-ttu-id="6fbd8-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fbd8-163">-SubscriptionId</span></span>
<span data-ttu-id="6fbd8-164">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6fbd8-165">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6fbd8-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fbd8-166">-Tag</span></span>
<span data-ttu-id="6fbd8-167">資源標記</span><span class="sxs-lookup"><span data-stu-id="6fbd8-167">Resource tags</span></span>

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

### <span data-ttu-id="6fbd8-168">-確認</span><span class="sxs-lookup"><span data-stu-id="6fbd8-168">-Confirm</span></span>
<span data-ttu-id="6fbd8-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbd8-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbd8-170">-WhatIf</span></span>
<span data-ttu-id="6fbd8-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbd8-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbd8-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbd8-173">CommonParameters</span></span>
<span data-ttu-id="6fbd8-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbd8-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbd8-176">輸入</span><span class="sxs-lookup"><span data-stu-id="6fbd8-176">INPUTS</span></span>

## <span data-ttu-id="6fbd8-177">輸出</span><span class="sxs-lookup"><span data-stu-id="6fbd8-177">OUTPUTS</span></span>

### <span data-ttu-id="6fbd8-178">IDomainService （ADDomainServices）。 Api202001。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="6fbd8-179">筆記</span><span class="sxs-lookup"><span data-stu-id="6fbd8-179">NOTES</span></span>

<span data-ttu-id="6fbd8-180">別名</span><span class="sxs-lookup"><span data-stu-id="6fbd8-180">ALIASES</span></span>

<span data-ttu-id="6fbd8-181">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6fbd8-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6fbd8-182">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6fbd8-183">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6fbd8-184">FORESTTRUST <IForestTrust [] >：資原始目錄林的設定清單</span><span class="sxs-lookup"><span data-stu-id="6fbd8-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="6fbd8-185">`[FriendlyName <String>]`：易記的名稱</span><span class="sxs-lookup"><span data-stu-id="6fbd8-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="6fbd8-186">`[RemoteDnsIP <String>]`：遠端 Dns ip</span><span class="sxs-lookup"><span data-stu-id="6fbd8-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="6fbd8-187">`[TrustDirection <String>]`：信任方向</span><span class="sxs-lookup"><span data-stu-id="6fbd8-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="6fbd8-188">`[TrustPassword <String>]`：信任密碼</span><span class="sxs-lookup"><span data-stu-id="6fbd8-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="6fbd8-189">`[TrustedDomainFqdn <String>]`：受信任的網域 FQDN</span><span class="sxs-lookup"><span data-stu-id="6fbd8-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="6fbd8-190">REPLICASET <IReplicaSet [] >： ReplicaSets 清單</span><span class="sxs-lookup"><span data-stu-id="6fbd8-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="6fbd8-191">`[Location <String>]`：虛擬網路位置</span><span class="sxs-lookup"><span data-stu-id="6fbd8-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="6fbd8-192">`[SubnetId <String>]`：將在其上部署網域服務的虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="6fbd8-193">要在其上部署網域服務的子網之 id。</span><span class="sxs-lookup"><span data-stu-id="6fbd8-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="6fbd8-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="6fbd8-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="6fbd8-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fbd8-195">RELATED LINKS</span></span>

