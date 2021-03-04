---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901782"
---
# <span data-ttu-id="b7c34-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c34-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b7c34-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7c34-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c34-103">更新現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b7c34-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="b7c34-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7c34-104">SYNTAX</span></span>

### <span data-ttu-id="b7c34-105">By VpnServerConfigurationName (預設) </span><span class="sxs-lookup"><span data-stu-id="b7c34-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7c34-106">By VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b7c34-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7c34-107">By VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c34-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7c34-108">描述</span><span class="sxs-lookup"><span data-stu-id="b7c34-108">DESCRIPTION</span></span>
<span data-ttu-id="b7c34-109">**Update-Az VpnServerConfiguration** Cmdlet 可讓您使用不同的 VpnProtocols、VpnAuthenticationTypes、IpsecPolicies 來更新現有的 VpnServerConfiguration，並針對客戶對點至網站連接的需求，設定選取的 vpn 驗證類型相關參數。</span><span class="sxs-lookup"><span data-stu-id="b7c34-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="b7c34-110">例子</span><span class="sxs-lookup"><span data-stu-id="b7c34-110">EXAMPLES</span></span>

### <span data-ttu-id="b7c34-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b7c34-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="b7c34-112">上述命令將更新現有的 VpnServerConfiguration 與 VpnProtocol as IkeV2。</span><span class="sxs-lookup"><span data-stu-id="b7c34-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="b7c34-113">參數</span><span class="sxs-lookup"><span data-stu-id="b7c34-113">PARAMETERS</span></span>

### <span data-ttu-id="b7c34-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="b7c34-114">-AadAudience</span></span>
<span data-ttu-id="b7c34-115">P2S AAD 驗證的 AAD 物件。</span><span class="sxs-lookup"><span data-stu-id="b7c34-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="b7c34-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="b7c34-116">-AadIssuer</span></span>
<span data-ttu-id="b7c34-117">P2S AAD 驗證的 AAD 發行者。</span><span class="sxs-lookup"><span data-stu-id="b7c34-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="b7c34-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="b7c34-118">-AadTenant</span></span>
<span data-ttu-id="b7c34-119">P2S AAD 驗證的 AAD 租使用者。</span><span class="sxs-lookup"><span data-stu-id="b7c34-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="b7c34-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7c34-120">-AsJob</span></span>
<span data-ttu-id="b7c34-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7c34-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7c34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c34-122">-DefaultProfile</span></span>
<span data-ttu-id="b7c34-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7c34-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c34-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7c34-124">-InputObject</span></span>
<span data-ttu-id="b7c34-125">要修改的 vpn 伺服器組定物件</span><span class="sxs-lookup"><span data-stu-id="b7c34-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7c34-126">-Name</span></span>
<span data-ttu-id="b7c34-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b7c34-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7c34-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="b7c34-129">方格ClientRootCertificate 檔案路徑清單</span><span class="sxs-lookup"><span data-stu-id="b7c34-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="b7c34-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b7c34-130">-RadiusServerAddress</span></span>
<span data-ttu-id="b7c34-131">P2S 外部範圍伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="b7c34-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="b7c34-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="b7c34-132">-RadiusServerList</span></span>
<span data-ttu-id="b7c34-133">P2S 外部多個弧線伺服器。</span><span class="sxs-lookup"><span data-stu-id="b7c34-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7c34-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="b7c34-135">方格ClientRootCertificate 檔案路徑清單</span><span class="sxs-lookup"><span data-stu-id="b7c34-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="b7c34-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b7c34-136">-RadiusServerSecret</span></span>
<span data-ttu-id="b7c34-137">P2S 外部弧線伺服器機密。</span><span class="sxs-lookup"><span data-stu-id="b7c34-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="b7c34-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c34-138">-ResourceGroupName</span></span>
<span data-ttu-id="b7c34-139">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b7c34-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c34-140">-ResourceId</span></span>
<span data-ttu-id="b7c34-141">Vpn 伺服器配置的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7c34-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-142">-標記</span><span class="sxs-lookup"><span data-stu-id="b7c34-142">-Tag</span></span>
<span data-ttu-id="b7c34-143">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b7c34-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b7c34-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b7c34-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="b7c34-145">P2S VPN 用戶端路由通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="b7c34-145">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b7c34-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b7c34-147">VpnServerConfiguration 的 IPSec 政策清單。</span><span class="sxs-lookup"><span data-stu-id="b7c34-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7c34-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="b7c34-149">要撤銷檔案路徑的 VpnClientCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="b7c34-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="b7c34-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7c34-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="b7c34-151">要新增檔案路徑的 VpnClientRootCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="b7c34-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="b7c34-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="b7c34-152">-VpnProtocol</span></span>
<span data-ttu-id="b7c34-153">P2S VPN 用戶端路由通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="b7c34-153">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c34-154">-確認</span><span class="sxs-lookup"><span data-stu-id="b7c34-154">-Confirm</span></span>
<span data-ttu-id="b7c34-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7c34-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c34-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c34-156">-WhatIf</span></span>
<span data-ttu-id="b7c34-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7c34-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c34-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7c34-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c34-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c34-159">CommonParameters</span></span>
<span data-ttu-id="b7c34-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7c34-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c34-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7c34-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c34-162">輸入</span><span class="sxs-lookup"><span data-stu-id="b7c34-162">INPUTS</span></span>

### <span data-ttu-id="b7c34-163">Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c34-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="b7c34-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b7c34-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="b7c34-165">輸出</span><span class="sxs-lookup"><span data-stu-id="b7c34-165">OUTPUTS</span></span>

### <span data-ttu-id="b7c34-166">Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c34-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b7c34-167">筆記</span><span class="sxs-lookup"><span data-stu-id="b7c34-167">NOTES</span></span>

## <span data-ttu-id="b7c34-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7c34-168">RELATED LINKS</span></span>
