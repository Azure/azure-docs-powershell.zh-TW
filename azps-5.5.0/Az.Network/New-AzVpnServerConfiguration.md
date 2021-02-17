---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140314"
---
# <span data-ttu-id="a491c-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491c-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a491c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a491c-102">SYNOPSIS</span></span>
<span data-ttu-id="a491c-103">建立新的 VpnServerConfiguration，以指向網站連線。</span><span class="sxs-lookup"><span data-stu-id="a491c-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="a491c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a491c-104">SYNTAX</span></span>

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

## <span data-ttu-id="a491c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a491c-105">DESCRIPTION</span></span>
<span data-ttu-id="a491c-106">**新的-AzVpnServerConfiguration** Cmdlet 可讓您使用不同的 VpnProtocols、VpnAuthenticationTypes、IpsecPolicies 建立新的 VpnServerConfiguration，並根據客戶對網站連線的需求，設定選取的 vpn 驗證類型相關參數。</span><span class="sxs-lookup"><span data-stu-id="a491c-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a491c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a491c-107">EXAMPLES</span></span>

### <span data-ttu-id="a491c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a491c-108">Example 1</span></span>
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

<span data-ttu-id="a491c-109">上述命令會建立新的 VpnServerConfiguration，並以 VpnAuthenticationType 作為憑證。</span><span class="sxs-lookup"><span data-stu-id="a491c-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="a491c-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a491c-110">Example 2</span></span>

<span data-ttu-id="a491c-111">建立新的 VpnServerConfiguration，以指向網站連線。</span><span class="sxs-lookup"><span data-stu-id="a491c-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="a491c-112"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="a491c-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="a491c-113">參數</span><span class="sxs-lookup"><span data-stu-id="a491c-113">PARAMETERS</span></span>

### <span data-ttu-id="a491c-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a491c-114">-AadAudience</span></span>
<span data-ttu-id="a491c-115">用於 P2S AAD 驗證的 AAD 物件。</span><span class="sxs-lookup"><span data-stu-id="a491c-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a491c-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a491c-116">-AadIssuer</span></span>
<span data-ttu-id="a491c-117">AAD 頒發者以進行 P2S AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="a491c-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a491c-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a491c-118">-AadTenant</span></span>
<span data-ttu-id="a491c-119">用於 P2S AAD 驗證的 AAD 租使用者。</span><span class="sxs-lookup"><span data-stu-id="a491c-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a491c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a491c-120">-AsJob</span></span>
<span data-ttu-id="a491c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a491c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a491c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a491c-122">-DefaultProfile</span></span>
<span data-ttu-id="a491c-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a491c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a491c-124">-位置</span><span class="sxs-lookup"><span data-stu-id="a491c-124">-Location</span></span>
<span data-ttu-id="a491c-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="a491c-125">The resource location.</span></span>

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

### <span data-ttu-id="a491c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a491c-126">-Name</span></span>
<span data-ttu-id="a491c-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a491c-127">The resource name.</span></span>

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

### <span data-ttu-id="a491c-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a491c-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a491c-129">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="a491c-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="a491c-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a491c-130">-RadiusServerAddress</span></span>
<span data-ttu-id="a491c-131">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="a491c-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="a491c-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="a491c-132">-RadiusServerList</span></span>
<span data-ttu-id="a491c-133">P2S 外部多個 radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a491c-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="a491c-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a491c-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a491c-135">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="a491c-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="a491c-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a491c-136">-RadiusServerSecret</span></span>
<span data-ttu-id="a491c-137">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="a491c-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="a491c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a491c-138">-ResourceGroupName</span></span>
<span data-ttu-id="a491c-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a491c-139">The resource group name.</span></span>

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

### <span data-ttu-id="a491c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="a491c-140">-Tag</span></span>
<span data-ttu-id="a491c-141">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="a491c-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a491c-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a491c-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="a491c-143">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="a491c-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a491c-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a491c-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a491c-145">VpnServerConfiguration 的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="a491c-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="a491c-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a491c-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a491c-147">要廢除檔案路徑的 VpnClientCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="a491c-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="a491c-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a491c-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a491c-149">要新增檔路徑的 VpnClientRootCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="a491c-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="a491c-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a491c-150">-VpnProtocol</span></span>
<span data-ttu-id="a491c-151">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="a491c-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a491c-152">-確認</span><span class="sxs-lookup"><span data-stu-id="a491c-152">-Confirm</span></span>
<span data-ttu-id="a491c-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a491c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a491c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a491c-154">-WhatIf</span></span>
<span data-ttu-id="a491c-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a491c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a491c-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a491c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a491c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a491c-157">CommonParameters</span></span>
<span data-ttu-id="a491c-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a491c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a491c-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a491c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a491c-160">輸入</span><span class="sxs-lookup"><span data-stu-id="a491c-160">INPUTS</span></span>

### <span data-ttu-id="a491c-161">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a491c-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a491c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="a491c-162">OUTPUTS</span></span>

### <span data-ttu-id="a491c-163">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a491c-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a491c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="a491c-164">NOTES</span></span>

## <span data-ttu-id="a491c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="a491c-165">RELATED LINKS</span></span>
