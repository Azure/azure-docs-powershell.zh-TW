---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 7acebe247009c95f9d504dc09b2729eeb5aabbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127307"
---
# <span data-ttu-id="9ef5a-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9ef5a-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="9ef5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ef5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef5a-103">更新網域服務操作可用來更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="9ef5a-104">更新呼叫只支援修補程式本文中所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="9ef5a-105">句法</span><span class="sxs-lookup"><span data-stu-id="9ef5a-105">SYNTAX</span></span>

### <span data-ttu-id="9ef5a-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9ef5a-106">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="9ef5a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9ef5a-107">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="9ef5a-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ef5a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ef5a-109">更新網域服務操作可用來更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="9ef5a-110">更新呼叫只支援修補程式本文中所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="9ef5a-111">示例</span><span class="sxs-lookup"><span data-stu-id="9ef5a-111">EXAMPLES</span></span>

### <span data-ttu-id="9ef5a-112">範例1：依 ResourceGroupName 和 Name 更新 AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9ef5a-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="9ef5a-113">依 ResourceGroupName 和 Name 更新 AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9ef5a-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="9ef5a-114">範例2：由 Inputobject 更新 AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9ef5a-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="9ef5a-115">以 Inputobject 更新 AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9ef5a-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="9ef5a-116">參數</span><span class="sxs-lookup"><span data-stu-id="9ef5a-116">PARAMETERS</span></span>

### <span data-ttu-id="9ef5a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ef5a-117">-AsJob</span></span>
<span data-ttu-id="9ef5a-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9ef5a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9ef5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef5a-119">-DefaultProfile</span></span>
<span data-ttu-id="9ef5a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef5a-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="9ef5a-121">-DomainConfigurationType</span></span>
<span data-ttu-id="9ef5a-122">網域配置類型</span><span class="sxs-lookup"><span data-stu-id="9ef5a-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="9ef5a-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="9ef5a-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="9ef5a-124">判斷是否已啟用或停用 NtlmV1 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="9ef5a-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="9ef5a-126">判斷是否已啟用或停用 SyncKerberosPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="9ef5a-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="9ef5a-128">判斷是否已啟用或停用 SyncNtlmPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="9ef5a-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="9ef5a-130">判斷是否已啟用或停用 SyncOnPremPasswords 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="9ef5a-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="9ef5a-132">判斷是否已啟用或停用 TlsV1 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="9ef5a-133">-FilteredSync</span></span>
<span data-ttu-id="9ef5a-134">啟用或停用標誌以開啟群組式篩選同步處理</span><span class="sxs-lookup"><span data-stu-id="9ef5a-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="9ef5a-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="9ef5a-135">-ForestTrust</span></span>
<span data-ttu-id="9ef5a-136">要構造之資原始目錄林的設定清單，請參閱 FORESTTRUST 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ef5a-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef5a-137">-InputObject</span></span>
<span data-ttu-id="9ef5a-138">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ef5a-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="9ef5a-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="9ef5a-140">[標誌] 可判斷是否已啟用或停用網際網路的安全 LDAP 存取。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="9ef5a-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="9ef5a-142">用於判斷是否已啟用或停用 [安全 LDAP] 的標誌。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="9ef5a-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="9ef5a-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="9ef5a-144">要設定安全 LDAP 所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="9ef5a-145">在此傳遞的參數應該是憑證 pfx 檔案的 base64encoded 標記法。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="9ef5a-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9ef5a-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="9ef5a-147">解密提供的安全 LDAP 憑證 pfx 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="9ef5a-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ef5a-148">-Name</span></span>
<span data-ttu-id="9ef5a-149">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-149">The name of the domain service.</span></span>

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

### <span data-ttu-id="9ef5a-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="9ef5a-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="9ef5a-151">其他收件者清單</span><span class="sxs-lookup"><span data-stu-id="9ef5a-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="9ef5a-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="9ef5a-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="9ef5a-153">是否應該通知網網域控制站管理員</span><span class="sxs-lookup"><span data-stu-id="9ef5a-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="9ef5a-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="9ef5a-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="9ef5a-155">系統應通知全域管理員</span><span class="sxs-lookup"><span data-stu-id="9ef5a-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="9ef5a-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9ef5a-156">-NoWait</span></span>
<span data-ttu-id="9ef5a-157">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9ef5a-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9ef5a-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="9ef5a-158">-ReplicaSet</span></span>
<span data-ttu-id="9ef5a-159">要構造的 ReplicaSets 清單，請參閱 REPLICASET 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ef5a-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="9ef5a-160">-ResourceForest</span></span>
<span data-ttu-id="9ef5a-161">資原始目錄林</span><span class="sxs-lookup"><span data-stu-id="9ef5a-161">Resource Forest</span></span>

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

### <span data-ttu-id="9ef5a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef5a-162">-ResourceGroupName</span></span>
<span data-ttu-id="9ef5a-163">使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="9ef5a-164">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-164">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9ef5a-165">-Sku</span><span class="sxs-lookup"><span data-stu-id="9ef5a-165">-Sku</span></span>
<span data-ttu-id="9ef5a-166">Sku 類型</span><span class="sxs-lookup"><span data-stu-id="9ef5a-166">Sku Type</span></span>

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

### <span data-ttu-id="9ef5a-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ef5a-167">-SubscriptionId</span></span>
<span data-ttu-id="9ef5a-168">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ef5a-169">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9ef5a-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ef5a-170">-Tag</span></span>
<span data-ttu-id="9ef5a-171">資源標記</span><span class="sxs-lookup"><span data-stu-id="9ef5a-171">Resource tags</span></span>

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

### <span data-ttu-id="9ef5a-172">-確認</span><span class="sxs-lookup"><span data-stu-id="9ef5a-172">-Confirm</span></span>
<span data-ttu-id="9ef5a-173">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef5a-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef5a-174">-WhatIf</span></span>
<span data-ttu-id="9ef5a-175">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef5a-176">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef5a-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef5a-177">CommonParameters</span></span>
<span data-ttu-id="9ef5a-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef5a-179">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef5a-180">輸入</span><span class="sxs-lookup"><span data-stu-id="9ef5a-180">INPUTS</span></span>

### <span data-ttu-id="9ef5a-181">IAdDomainServicesIdentity （ADDomainServices）的</span><span class="sxs-lookup"><span data-stu-id="9ef5a-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="9ef5a-182">輸出</span><span class="sxs-lookup"><span data-stu-id="9ef5a-182">OUTPUTS</span></span>

### <span data-ttu-id="9ef5a-183">IDomainService （ADDomainServices）。 Api202001。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="9ef5a-184">筆記</span><span class="sxs-lookup"><span data-stu-id="9ef5a-184">NOTES</span></span>

<span data-ttu-id="9ef5a-185">別名</span><span class="sxs-lookup"><span data-stu-id="9ef5a-185">ALIASES</span></span>

<span data-ttu-id="9ef5a-186">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9ef5a-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ef5a-187">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ef5a-188">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ef5a-189">FORESTTRUST <IForestTrust [] >：資原始目錄林的設定清單</span><span class="sxs-lookup"><span data-stu-id="9ef5a-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="9ef5a-190">`[FriendlyName <String>]`：易記的名稱</span><span class="sxs-lookup"><span data-stu-id="9ef5a-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="9ef5a-191">`[RemoteDnsIP <String>]`：遠端 Dns ip</span><span class="sxs-lookup"><span data-stu-id="9ef5a-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="9ef5a-192">`[TrustDirection <String>]`：信任方向</span><span class="sxs-lookup"><span data-stu-id="9ef5a-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="9ef5a-193">`[TrustPassword <String>]`：信任密碼</span><span class="sxs-lookup"><span data-stu-id="9ef5a-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="9ef5a-194">`[TrustedDomainFqdn <String>]`：受信任的網域 FQDN</span><span class="sxs-lookup"><span data-stu-id="9ef5a-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="9ef5a-195">INPUTOBJECT <IAdDomainServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9ef5a-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ef5a-196">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="9ef5a-197">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9ef5a-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ef5a-198">`[ResourceGroupName <String>]`：使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="9ef5a-199">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="9ef5a-200">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9ef5a-201">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9ef5a-202">REPLICASET <IReplicaSet [] >： ReplicaSets 清單</span><span class="sxs-lookup"><span data-stu-id="9ef5a-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="9ef5a-203">`[Location <String>]`：虛擬網路位置</span><span class="sxs-lookup"><span data-stu-id="9ef5a-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="9ef5a-204">`[SubnetId <String>]`：將在其上部署網域服務的虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="9ef5a-205">要在其上部署網域服務的子網之 id。</span><span class="sxs-lookup"><span data-stu-id="9ef5a-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="9ef5a-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="9ef5a-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="9ef5a-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ef5a-207">RELATED LINKS</span></span>

