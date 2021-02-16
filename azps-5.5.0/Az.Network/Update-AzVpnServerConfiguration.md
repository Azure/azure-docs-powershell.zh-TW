---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 552a6a317524de6d0f1db86a9a69a2733826d3f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132411"
---
# <span data-ttu-id="e4c2b-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4c2b-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="e4c2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c2b-103">更新現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="e4c2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4c2b-104">SYNTAX</span></span>

### <span data-ttu-id="e4c2b-105">ByVpnServerConfigurationName (預設) </span><span class="sxs-lookup"><span data-stu-id="e4c2b-105">ByVpnServerConfigurationName (Default)</span></span>
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

### <span data-ttu-id="e4c2b-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e4c2b-106">ByVpnServerConfigurationObject</span></span>
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

### <span data-ttu-id="e4c2b-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="e4c2b-107">ByVpnServerConfigurationResourceId</span></span>
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

## <span data-ttu-id="e4c2b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e4c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="e4c2b-109">**AzVpnServerConfiguration** Cmdlet 可讓您使用不同的 VpnProtocols、VpnAuthenticationTypes、IpsecPolicies 來更新現有的 VpnServerConfiguration，並根據客戶對於指向網站連線的需求，設定選取的 vpn 驗證類型相關參數。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="e4c2b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e4c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c2b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e4c2b-111">Example 1</span></span>
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

<span data-ttu-id="e4c2b-112">上述命令會使用 VpnProtocol 作為 IkeV2 來更新現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="e4c2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="e4c2b-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c2b-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="e4c2b-114">-AadAudience</span></span>
<span data-ttu-id="e4c2b-115">用於 P2S AAD 驗證的 AAD 物件。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="e4c2b-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="e4c2b-116">-AadIssuer</span></span>
<span data-ttu-id="e4c2b-117">AAD 頒發者以進行 P2S AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="e4c2b-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="e4c2b-118">-AadTenant</span></span>
<span data-ttu-id="e4c2b-119">用於 P2S AAD 驗證的 AAD 租使用者。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="e4c2b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4c2b-120">-AsJob</span></span>
<span data-ttu-id="e4c2b-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e4c2b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4c2b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c2b-122">-DefaultProfile</span></span>
<span data-ttu-id="e4c2b-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c2b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c2b-124">-InputObject</span></span>
<span data-ttu-id="e4c2b-125">要修改的 vpn 伺服器設定物件</span><span class="sxs-lookup"><span data-stu-id="e4c2b-125">The vpn server configuration object to be modified</span></span>

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

### <span data-ttu-id="e4c2b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4c2b-126">-Name</span></span>
<span data-ttu-id="e4c2b-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-127">The resource name.</span></span>

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

### <span data-ttu-id="e4c2b-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="e4c2b-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="e4c2b-129">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="e4c2b-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="e4c2b-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="e4c2b-130">-RadiusServerAddress</span></span>
<span data-ttu-id="e4c2b-131">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="e4c2b-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="e4c2b-132">-RadiusServerList</span></span>
<span data-ttu-id="e4c2b-133">P2S 外部多個 radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="e4c2b-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="e4c2b-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="e4c2b-135">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="e4c2b-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="e4c2b-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="e4c2b-136">-RadiusServerSecret</span></span>
<span data-ttu-id="e4c2b-137">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="e4c2b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c2b-138">-ResourceGroupName</span></span>
<span data-ttu-id="e4c2b-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-139">The resource group name.</span></span>

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

### <span data-ttu-id="e4c2b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4c2b-140">-ResourceId</span></span>
<span data-ttu-id="e4c2b-141">Vpn 伺服器配置的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-141">The Azure resource ID for the vpn server configuration.</span></span>

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

### <span data-ttu-id="e4c2b-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4c2b-142">-Tag</span></span>
<span data-ttu-id="e4c2b-143">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e4c2b-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e4c2b-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="e4c2b-145">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="e4c2b-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="e4c2b-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="e4c2b-147">VpnServerConfiguration 的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="e4c2b-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="e4c2b-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="e4c2b-149">要廢除檔案路徑的 VpnClientCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="e4c2b-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="e4c2b-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="e4c2b-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="e4c2b-151">要新增檔路徑的 VpnClientRootCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="e4c2b-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="e4c2b-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="e4c2b-152">-VpnProtocol</span></span>
<span data-ttu-id="e4c2b-153">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="e4c2b-154">-確認</span><span class="sxs-lookup"><span data-stu-id="e4c2b-154">-Confirm</span></span>
<span data-ttu-id="e4c2b-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c2b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c2b-156">-WhatIf</span></span>
<span data-ttu-id="e4c2b-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c2b-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c2b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c2b-159">CommonParameters</span></span>
<span data-ttu-id="e4c2b-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c2b-161">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c2b-162">輸入</span><span class="sxs-lookup"><span data-stu-id="e4c2b-162">INPUTS</span></span>

### <span data-ttu-id="e4c2b-163">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4c2b-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="e4c2b-164">PSIpsecPolicy [] 的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="e4c2b-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="e4c2b-165">輸出</span><span class="sxs-lookup"><span data-stu-id="e4c2b-165">OUTPUTS</span></span>

### <span data-ttu-id="e4c2b-166">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4c2b-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="e4c2b-167">筆記</span><span class="sxs-lookup"><span data-stu-id="e4c2b-167">NOTES</span></span>

## <span data-ttu-id="e4c2b-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4c2b-168">RELATED LINKS</span></span>
