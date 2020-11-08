---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959153"
---
# <span data-ttu-id="a7362-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7362-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a7362-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7362-102">SYNOPSIS</span></span>
<span data-ttu-id="a7362-103">更新現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="a7362-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="a7362-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7362-104">SYNTAX</span></span>

### <span data-ttu-id="a7362-105">ByVpnServerConfigurationNameByCertificateAuthentication (預設) </span><span class="sxs-lookup"><span data-stu-id="a7362-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7362-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7362-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7362-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7362-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7362-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7362-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7362-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7362-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7362-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7362-114">說明</span><span class="sxs-lookup"><span data-stu-id="a7362-114">DESCRIPTION</span></span>
<span data-ttu-id="a7362-115">**AzVpnServerConfiguration** Cmdlet 可讓您使用不同的 VpnProtocols、VpnAuthenticationTypes、IpsecPolicies 來更新現有的 VpnServerConfiguration，並根據客戶對於指向網站連線的需求，設定選取的 vpn 驗證類型相關參數。</span><span class="sxs-lookup"><span data-stu-id="a7362-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a7362-116">示例</span><span class="sxs-lookup"><span data-stu-id="a7362-116">EXAMPLES</span></span>

### <span data-ttu-id="a7362-117">範例1</span><span class="sxs-lookup"><span data-stu-id="a7362-117">Example 1</span></span>
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

<span data-ttu-id="a7362-118">上述命令會使用 VpnProtocol 作為 IkeV2 來更新現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="a7362-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="a7362-119">參數</span><span class="sxs-lookup"><span data-stu-id="a7362-119">PARAMETERS</span></span>

### <span data-ttu-id="a7362-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a7362-120">-AadAudience</span></span>
<span data-ttu-id="a7362-121">用於 P2S AAD 驗證的 AAD 物件。</span><span class="sxs-lookup"><span data-stu-id="a7362-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a7362-122">-AadIssuer</span></span>
<span data-ttu-id="a7362-123">AAD 頒發者以進行 P2S AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="a7362-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a7362-124">-AadTenant</span></span>
<span data-ttu-id="a7362-125">用於 P2S AAD 驗證的 AAD 租使用者。</span><span class="sxs-lookup"><span data-stu-id="a7362-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7362-126">-AsJob</span></span>
<span data-ttu-id="a7362-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a7362-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7362-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7362-128">-DefaultProfile</span></span>
<span data-ttu-id="a7362-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7362-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7362-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7362-130">-InputObject</span></span>
<span data-ttu-id="a7362-131">要修改的 vpn 伺服器設定物件</span><span class="sxs-lookup"><span data-stu-id="a7362-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7362-132">-Name</span></span>
<span data-ttu-id="a7362-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a7362-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a7362-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a7362-135">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="a7362-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a7362-136">-RadiusServerAddress</span></span>
<span data-ttu-id="a7362-137">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="a7362-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a7362-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a7362-139">RadiusClientRootCertificate 檔路徑的清單</span><span class="sxs-lookup"><span data-stu-id="a7362-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a7362-140">-RadiusServerSecret</span></span>
<span data-ttu-id="a7362-141">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="a7362-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7362-142">-ResourceGroupName</span></span>
<span data-ttu-id="a7362-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7362-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7362-144">-ResourceId</span></span>
<span data-ttu-id="a7362-145">Vpn 伺服器配置的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7362-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7362-146">-Tag</span></span>
<span data-ttu-id="a7362-147">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="a7362-147">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a7362-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="a7362-149">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="a7362-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a7362-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a7362-151">VpnServerConfiguration 的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="a7362-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a7362-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a7362-153">要廢除檔案路徑的 VpnClientCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="a7362-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a7362-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a7362-155">要新增檔路徑的 VpnClientRootCertificates 清單</span><span class="sxs-lookup"><span data-stu-id="a7362-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a7362-156">-VpnProtocol</span></span>
<span data-ttu-id="a7362-157">P2S VPN 用戶端隧道通訊協定的清單。</span><span class="sxs-lookup"><span data-stu-id="a7362-157">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7362-158">-確認</span><span class="sxs-lookup"><span data-stu-id="a7362-158">-Confirm</span></span>
<span data-ttu-id="a7362-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7362-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7362-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7362-160">-WhatIf</span></span>
<span data-ttu-id="a7362-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7362-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7362-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7362-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7362-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7362-163">CommonParameters</span></span>
<span data-ttu-id="a7362-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7362-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7362-165">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7362-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7362-166">輸入</span><span class="sxs-lookup"><span data-stu-id="a7362-166">INPUTS</span></span>

### <span data-ttu-id="a7362-167">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7362-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="a7362-168">PSIpsecPolicy [] 的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="a7362-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a7362-169">輸出</span><span class="sxs-lookup"><span data-stu-id="a7362-169">OUTPUTS</span></span>

### <span data-ttu-id="a7362-170">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7362-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a7362-171">筆記</span><span class="sxs-lookup"><span data-stu-id="a7362-171">NOTES</span></span>

## <span data-ttu-id="a7362-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7362-172">RELATED LINKS</span></span>