---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: fbb45450352a99edc5a89d24ac8eb6bc4bcbf383
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910809"
---
# <span data-ttu-id="36f21-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="36f21-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="36f21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36f21-102">SYNOPSIS</span></span>
<span data-ttu-id="36f21-103">更新專用雲端</span><span class="sxs-lookup"><span data-stu-id="36f21-103">Update a private cloud</span></span>

## <span data-ttu-id="36f21-104">語法</span><span class="sxs-lookup"><span data-stu-id="36f21-104">SYNTAX</span></span>

### <span data-ttu-id="36f21-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="36f21-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36f21-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36f21-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36f21-107">描述</span><span class="sxs-lookup"><span data-stu-id="36f21-107">DESCRIPTION</span></span>
<span data-ttu-id="36f21-108">更新專用雲端</span><span class="sxs-lookup"><span data-stu-id="36f21-108">Update a private cloud</span></span>

## <span data-ttu-id="36f21-109">例子</span><span class="sxs-lookup"><span data-stu-id="36f21-109">EXAMPLES</span></span>

### <span data-ttu-id="36f21-110">範例 1：根據名稱更新專用雲端的大小</span><span class="sxs-lookup"><span data-stu-id="36f21-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="36f21-111">根據名稱更新專用雲端的大小</span><span class="sxs-lookup"><span data-stu-id="36f21-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="36f21-112">範例 2：根據輸入物件更新專用雲端的大小</span><span class="sxs-lookup"><span data-stu-id="36f21-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="36f21-113">按輸入物件更新專用雲端的大小</span><span class="sxs-lookup"><span data-stu-id="36f21-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="36f21-114">參數</span><span class="sxs-lookup"><span data-stu-id="36f21-114">PARAMETERS</span></span>

### <span data-ttu-id="36f21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36f21-115">-AsJob</span></span>
<span data-ttu-id="36f21-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="36f21-116">Run the command as a job</span></span>

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

### <span data-ttu-id="36f21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f21-117">-DefaultProfile</span></span>
<span data-ttu-id="36f21-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36f21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f21-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="36f21-119">-IdentitySource</span></span>
<span data-ttu-id="36f21-120">vCenter單一登入身分識別來源若要建構，請參閱 IDENTITYSOURCE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="36f21-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f21-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36f21-121">-InputObject</span></span>
<span data-ttu-id="36f21-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="36f21-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36f21-123">-網際網路</span><span class="sxs-lookup"><span data-stu-id="36f21-123">-Internet</span></span>
<span data-ttu-id="36f21-124">啟用或停用網際網路連接</span><span class="sxs-lookup"><span data-stu-id="36f21-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f21-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="36f21-125">-ManagementClusterSize</span></span>
<span data-ttu-id="36f21-126">組大小</span><span class="sxs-lookup"><span data-stu-id="36f21-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f21-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-127">-Name</span></span>
<span data-ttu-id="36f21-128">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f21-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="36f21-129">-NoWait</span></span>
<span data-ttu-id="36f21-130">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="36f21-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36f21-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f21-131">-ResourceGroupName</span></span>
<span data-ttu-id="36f21-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36f21-132">The name of the resource group.</span></span>
<span data-ttu-id="36f21-133">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="36f21-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36f21-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36f21-134">-SubscriptionId</span></span>
<span data-ttu-id="36f21-135">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36f21-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36f21-136">-標記</span><span class="sxs-lookup"><span data-stu-id="36f21-136">-Tag</span></span>
<span data-ttu-id="36f21-137">資源標記。</span><span class="sxs-lookup"><span data-stu-id="36f21-137">Resource tags.</span></span>

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

### <span data-ttu-id="36f21-138">-確認</span><span class="sxs-lookup"><span data-stu-id="36f21-138">-Confirm</span></span>
<span data-ttu-id="36f21-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36f21-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f21-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f21-140">-WhatIf</span></span>
<span data-ttu-id="36f21-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36f21-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f21-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36f21-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f21-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f21-143">CommonParameters</span></span>
<span data-ttu-id="36f21-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36f21-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f21-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36f21-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f21-146">輸入</span><span class="sxs-lookup"><span data-stu-id="36f21-146">INPUTS</span></span>

### <span data-ttu-id="36f21-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="36f21-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="36f21-148">輸出</span><span class="sxs-lookup"><span data-stu-id="36f21-148">OUTPUTS</span></span>

### <span data-ttu-id="36f21-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="36f21-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="36f21-150">筆記</span><span class="sxs-lookup"><span data-stu-id="36f21-150">NOTES</span></span>

<span data-ttu-id="36f21-151">別名</span><span class="sxs-lookup"><span data-stu-id="36f21-151">ALIASES</span></span>

<span data-ttu-id="36f21-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="36f21-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36f21-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="36f21-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36f21-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="36f21-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36f21-155">IDENTITYSOURCE <IIdentitySource[]>：vCenter單一登入身分識別來源</span><span class="sxs-lookup"><span data-stu-id="36f21-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="36f21-156">`[Alias <String>]`：網域的 NetBIOS 名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="36f21-157">`[BaseGroupDn <String>]`：群組的基底區別名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="36f21-158">`[BaseUserDn <String>]`：使用者的基本區別名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="36f21-159">`[Domain <String>]`：網域的 dns 名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="36f21-160">`[Name <String>]`：身分識別來源的名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="36f21-161">`[Password <String>]`：Active Directory 使用者的密碼，使用者和群組至少具有基本 DN 的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="36f21-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="36f21-162">`[PrimaryServer <String>]`：主伺服器 URL</span><span class="sxs-lookup"><span data-stu-id="36f21-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="36f21-163">`[SecondaryServer <String>]`：次要伺服器 URL</span><span class="sxs-lookup"><span data-stu-id="36f21-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="36f21-164">`[Ssl <SslEnum?>]`：使用 SSL 憑證保護 LDAP 通訊 (LDAPS) </span><span class="sxs-lookup"><span data-stu-id="36f21-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="36f21-165">`[Username <String>]`：具有使用者和群組基本 DN 唯讀存取權最低之 Active Directory 使用者的識別碼</span><span class="sxs-lookup"><span data-stu-id="36f21-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="36f21-166">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="36f21-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36f21-167">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="36f21-168">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="36f21-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="36f21-169">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="36f21-170">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="36f21-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36f21-171">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="36f21-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="36f21-172">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="36f21-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="36f21-173">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36f21-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36f21-174">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="36f21-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="36f21-175">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36f21-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="36f21-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="36f21-176">RELATED LINKS</span></span>

