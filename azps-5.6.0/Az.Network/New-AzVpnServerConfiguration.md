---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: f093a9f3a30ce1e46c08790d355689fdd9399c79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910010"
---
# <span data-ttu-id="cbdc6-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbdc6-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="cbdc6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdc6-103">為指向網站連線性建立新 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="cbdc6-104">語法</span><span class="sxs-lookup"><span data-stu-id="cbdc6-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdc6-105">描述</span><span class="sxs-lookup"><span data-stu-id="cbdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdc6-106">**New-Az VpnServerConfiguration** Cmdlet 可讓您使用不同的 VpnProtocols、VpnAuthenticationTypes、IpsecPolicies 來建立新的 VpnServerConfiguration，並針對客戶對點到網站連接的需求，設定選取的 vpn 驗證類型相關參數。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="cbdc6-107">例子</span><span class="sxs-lookup"><span data-stu-id="cbdc6-107">EXAMPLES</span></span>

### <span data-ttu-id="cbdc6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cbdc6-108">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="cbdc6-109">上述命令會使用 VpnAuthenticationType 作為憑證來建立新 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="cbdc6-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="cbdc6-110">Example 2</span></span>

<span data-ttu-id="cbdc6-111">為指向網站連線性建立新 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="cbdc6-112"> (自動) </span><span class="sxs-lookup"><span data-stu-id="cbdc6-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="cbdc6-113">參數</span><span class="sxs-lookup"><span data-stu-id="cbdc6-113">PARAMETERS</span></span>

### <span data-ttu-id="cbdc6-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="cbdc6-114">-AadAudience</span></span>
<span data-ttu-id="cbdc6-115">P2S AAD 驗證的 AAD 物件。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="cbdc6-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="cbdc6-116">-AadIssuer</span></span>
<span data-ttu-id="cbdc6-117">P2S AAD 驗證的 AAD 發行者。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="cbdc6-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="cbdc6-118">-AadTenant</span></span>
<span data-ttu-id="cbdc6-119">P2S AAD 驗證的 AAD 租使用者。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="cbdc6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbdc6-120">-AsJob</span></span>
<span data-ttu-id="cbdc6-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbdc6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbdc6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdc6-122">-DefaultProfile</span></span>
<span data-ttu-id="cbdc6-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdc6-124">-位置</span><span class="sxs-lookup"><span data-stu-id="cbdc6-124">-Location</span></span>
<span data-ttu-id="cbdc6-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-125">The resource location.</span></span>

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

### <span data-ttu-id="cbdc6-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbdc6-126">-Name</span></span>
<span data-ttu-id="cbdc6-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc6-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cbdc6-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="cbdc6-129">方格ClientRootCertificate 檔案路徑清單</span><span class="sxs-lookup"><span data-stu-id="cbdc6-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="cbdc6-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="cbdc6-130">-RadiusServerAddress</span></span>
<span data-ttu-id="cbdc6-131">P2S 外部範圍伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="cbdc6-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="cbdc6-132">-RadiusServerList</span></span>
<span data-ttu-id="cbdc6-133">P2S 外部多個弧線伺服器。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="cbdc6-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cbdc6-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="cbdc6-135">方格ClientRootCertificate 檔案路徑清單</span><span class="sxs-lookup"><span data-stu-id="cbdc6-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="cbdc6-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="cbdc6-136">-RadiusServerSecret</span></span>
<span data-ttu-id="cbdc6-137">P2S 外部弧線伺服器機密。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="cbdc6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdc6-138">-ResourceGroupName</span></span>
<span data-ttu-id="cbdc6-139">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-139">The resource group name.</span></span>

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

### <span data-ttu-id="cbdc6-140">-標記</span><span class="sxs-lookup"><span data-stu-id="cbdc6-140">-Tag</span></span>
<span data-ttu-id="cbdc6-141">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cbdc6-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="cbdc6-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="cbdc6-143">P2S VPN 用戶端路由通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="cbdc6-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdc6-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="cbdc6-145">VpnServerConfiguration 的 IPSec 政策清單。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc6-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cbdc6-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="cbdc6-147">要撤銷檔案路徑的 VpnClientCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="cbdc6-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="cbdc6-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cbdc6-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="cbdc6-149">要新增檔案路徑的 VpnClientRootCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="cbdc6-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="cbdc6-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="cbdc6-150">-VpnProtocol</span></span>
<span data-ttu-id="cbdc6-151">P2S VPN 用戶端路由通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="cbdc6-152">-確認</span><span class="sxs-lookup"><span data-stu-id="cbdc6-152">-Confirm</span></span>
<span data-ttu-id="cbdc6-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdc6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdc6-154">-WhatIf</span></span>
<span data-ttu-id="cbdc6-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdc6-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdc6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdc6-157">CommonParameters</span></span>
<span data-ttu-id="cbdc6-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbdc6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdc6-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbdc6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdc6-160">輸入</span><span class="sxs-lookup"><span data-stu-id="cbdc6-160">INPUTS</span></span>

### <span data-ttu-id="cbdc6-161">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="cbdc6-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="cbdc6-162">輸出</span><span class="sxs-lookup"><span data-stu-id="cbdc6-162">OUTPUTS</span></span>

### <span data-ttu-id="cbdc6-163">Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbdc6-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="cbdc6-164">筆記</span><span class="sxs-lookup"><span data-stu-id="cbdc6-164">NOTES</span></span>

## <span data-ttu-id="cbdc6-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbdc6-165">RELATED LINKS</span></span>
