---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 4504eaf26331fa4e881d6a86f284a74b7f249565
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912134"
---
# <span data-ttu-id="96399-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="96399-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="96399-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96399-102">SYNOPSIS</span></span>
<span data-ttu-id="96399-103">Update 網域服務作業可用來更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="96399-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="96399-104">更新呼叫僅支援修補程式內內容中列出的屬性。</span><span class="sxs-lookup"><span data-stu-id="96399-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="96399-105">語法</span><span class="sxs-lookup"><span data-stu-id="96399-105">SYNTAX</span></span>

### <span data-ttu-id="96399-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="96399-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96399-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="96399-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96399-108">描述</span><span class="sxs-lookup"><span data-stu-id="96399-108">DESCRIPTION</span></span>
<span data-ttu-id="96399-109">Update 網域服務作業可用來更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="96399-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="96399-110">更新呼叫僅支援修補程式內內容中列出的屬性。</span><span class="sxs-lookup"><span data-stu-id="96399-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="96399-111">例子</span><span class="sxs-lookup"><span data-stu-id="96399-111">EXAMPLES</span></span>

### <span data-ttu-id="96399-112">範例 1：更新 AzADDomainService By ResourceGroupName 和 Name</span><span class="sxs-lookup"><span data-stu-id="96399-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="96399-113">更新 AzADDomainService By ResourceGroupName 和 Name</span><span class="sxs-lookup"><span data-stu-id="96399-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="96399-114">範例 2：Update AzADDomainService By Inputobject</span><span class="sxs-lookup"><span data-stu-id="96399-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="96399-115">更新 AzADDomainService By Inputobject</span><span class="sxs-lookup"><span data-stu-id="96399-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="96399-116">參數</span><span class="sxs-lookup"><span data-stu-id="96399-116">PARAMETERS</span></span>

### <span data-ttu-id="96399-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96399-117">-AsJob</span></span>
<span data-ttu-id="96399-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="96399-118">Run the command as a job</span></span>

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

### <span data-ttu-id="96399-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96399-119">-DefaultProfile</span></span>
<span data-ttu-id="96399-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96399-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96399-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="96399-121">-DomainConfigurationType</span></span>
<span data-ttu-id="96399-122">網域組配置類型</span><span class="sxs-lookup"><span data-stu-id="96399-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="96399-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="96399-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="96399-124">一個旗標，判斷 NtlmV1 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="96399-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="96399-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="96399-126">一個旗標，判斷 SyncKerberosPasswords 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="96399-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="96399-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="96399-128">一個旗標，判斷是否已啟用或停用 SyncNtlmPasswords。</span><span class="sxs-lookup"><span data-stu-id="96399-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="96399-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="96399-130">一個旗標，判斷是否已啟用或停用 SyncOnPremPasswords。</span><span class="sxs-lookup"><span data-stu-id="96399-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="96399-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="96399-132">判斷 TlsV1 是否已啟用或停用的標標。</span><span class="sxs-lookup"><span data-stu-id="96399-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="96399-133">-FilteredSync</span></span>
<span data-ttu-id="96399-134">啟用或停用旗標以開啟群組式篩選同步</span><span class="sxs-lookup"><span data-stu-id="96399-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="96399-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="96399-135">-ForestTrust</span></span>
<span data-ttu-id="96399-136">Resource Forest To construct 的設定清單，請參閱 FORESTTRUST 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96399-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="96399-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96399-137">-InputObject</span></span>
<span data-ttu-id="96399-138">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96399-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96399-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="96399-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="96399-140">判斷是否已啟用或停用網際網路上安全 LDAP 存取的標標。</span><span class="sxs-lookup"><span data-stu-id="96399-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="96399-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="96399-142">判斷是否已啟用或停用 Secure LDAP 的標標。</span><span class="sxs-lookup"><span data-stu-id="96399-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="96399-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="96399-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="96399-144">設定 Secure LDAP 所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="96399-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="96399-145">此處傳遞的參數應該是憑證 pfx 檔案的 base64encoded 表示。</span><span class="sxs-lookup"><span data-stu-id="96399-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="96399-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="96399-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="96399-147">解密所提供的 Secure LDAP 憑證 pfx 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="96399-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="96399-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="96399-148">-Name</span></span>
<span data-ttu-id="96399-149">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="96399-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96399-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="96399-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="96399-151">其他收件者的清單</span><span class="sxs-lookup"><span data-stu-id="96399-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="96399-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="96399-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="96399-153">應該通知網域控制站管理員</span><span class="sxs-lookup"><span data-stu-id="96399-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="96399-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="96399-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="96399-155">全域系統管理員應該收到通知</span><span class="sxs-lookup"><span data-stu-id="96399-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="96399-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="96399-156">-NoWait</span></span>
<span data-ttu-id="96399-157">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="96399-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96399-158">-複本集</span><span class="sxs-lookup"><span data-stu-id="96399-158">-ReplicaSet</span></span>
<span data-ttu-id="96399-159">要建構的複本集清單，請參閱有關複本集屬性的記事區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96399-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96399-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="96399-160">-ResourceForest</span></span>
<span data-ttu-id="96399-161">資源樹目錄</span><span class="sxs-lookup"><span data-stu-id="96399-161">Resource Forest</span></span>

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

### <span data-ttu-id="96399-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96399-162">-ResourceGroupName</span></span>
<span data-ttu-id="96399-163">使用者訂閱中資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96399-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="96399-164">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96399-164">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96399-165">-SKU</span><span class="sxs-lookup"><span data-stu-id="96399-165">-Sku</span></span>
<span data-ttu-id="96399-166">SKU 類型</span><span class="sxs-lookup"><span data-stu-id="96399-166">Sku Type</span></span>

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

### <span data-ttu-id="96399-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96399-167">-SubscriptionId</span></span>
<span data-ttu-id="96399-168">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="96399-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96399-169">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="96399-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96399-170">-標記</span><span class="sxs-lookup"><span data-stu-id="96399-170">-Tag</span></span>
<span data-ttu-id="96399-171">資源標記</span><span class="sxs-lookup"><span data-stu-id="96399-171">Resource tags</span></span>

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

### <span data-ttu-id="96399-172">-確認</span><span class="sxs-lookup"><span data-stu-id="96399-172">-Confirm</span></span>
<span data-ttu-id="96399-173">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96399-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96399-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96399-174">-WhatIf</span></span>
<span data-ttu-id="96399-175">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96399-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96399-176">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96399-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96399-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96399-177">CommonParameters</span></span>
<span data-ttu-id="96399-178">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96399-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96399-179">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96399-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96399-180">輸入</span><span class="sxs-lookup"><span data-stu-id="96399-180">INPUTS</span></span>

### <span data-ttu-id="96399-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="96399-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="96399-182">輸出</span><span class="sxs-lookup"><span data-stu-id="96399-182">OUTPUTS</span></span>

### <span data-ttu-id="96399-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="96399-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="96399-184">筆記</span><span class="sxs-lookup"><span data-stu-id="96399-184">NOTES</span></span>

<span data-ttu-id="96399-185">別名</span><span class="sxs-lookup"><span data-stu-id="96399-185">ALIASES</span></span>

<span data-ttu-id="96399-186">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="96399-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96399-187">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96399-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96399-188">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="96399-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96399-189">FORESTTRUST <IForestTrust[]>：資源樹目錄的設定清單</span><span class="sxs-lookup"><span data-stu-id="96399-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="96399-190">`[FriendlyName <String>]`：好用名稱</span><span class="sxs-lookup"><span data-stu-id="96399-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="96399-191">`[RemoteDnsIP <String>]`：遠端 Dns ips</span><span class="sxs-lookup"><span data-stu-id="96399-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="96399-192">`[TrustDirection <String>]`：信任方向</span><span class="sxs-lookup"><span data-stu-id="96399-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="96399-193">`[TrustPassword <String>]`：信任密碼</span><span class="sxs-lookup"><span data-stu-id="96399-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="96399-194">`[TrustedDomainFqdn <String>]`：信任的網域 FQDN</span><span class="sxs-lookup"><span data-stu-id="96399-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="96399-195">INPUTOBJECT： <IAdDomainServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="96399-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96399-196">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="96399-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="96399-197">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="96399-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96399-198">`[ResourceGroupName <String>]`：使用者訂閱中的資源組名。</span><span class="sxs-lookup"><span data-stu-id="96399-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="96399-199">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96399-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="96399-200">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="96399-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="96399-201">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="96399-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="96399-202">複製<複本集[]>：複本集清單</span><span class="sxs-lookup"><span data-stu-id="96399-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="96399-203">`[Location <String>]`：虛擬網路位置</span><span class="sxs-lookup"><span data-stu-id="96399-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="96399-204">`[SubnetId <String>]`：網域服務將部署在的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="96399-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="96399-205">網域服務將部署之子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96399-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="96399-206">/virtualNetwork/vnetName/子網/子網名稱。</span><span class="sxs-lookup"><span data-stu-id="96399-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="96399-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="96399-207">RELATED LINKS</span></span>

