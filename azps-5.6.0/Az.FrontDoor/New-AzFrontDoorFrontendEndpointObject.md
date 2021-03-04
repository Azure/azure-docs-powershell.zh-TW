---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: a106295a883cc6729ddf7c5d4235a87ff036f066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906690"
---
# <span data-ttu-id="6beb3-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6beb3-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="6beb3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6beb3-102">SYNOPSIS</span></span>
<span data-ttu-id="6beb3-103">建立 PSFrontendEndpoint 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="6beb3-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="6beb3-104">語法</span><span class="sxs-lookup"><span data-stu-id="6beb3-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beb3-105">描述</span><span class="sxs-lookup"><span data-stu-id="6beb3-105">DESCRIPTION</span></span>
<span data-ttu-id="6beb3-106">建立 PSFrontendEndpoint 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="6beb3-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="6beb3-107">例子</span><span class="sxs-lookup"><span data-stu-id="6beb3-107">EXAMPLES</span></span>

### <span data-ttu-id="6beb3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6beb3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="6beb3-109">建立 PSFrontendEndpoint 物件以用於建立前門。</span><span class="sxs-lookup"><span data-stu-id="6beb3-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="6beb3-110">參數</span><span class="sxs-lookup"><span data-stu-id="6beb3-110">PARAMETERS</span></span>

### <span data-ttu-id="6beb3-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="6beb3-111">-CertificateSource</span></span>
<span data-ttu-id="6beb3-112">SSL 憑證的來源</span><span class="sxs-lookup"><span data-stu-id="6beb3-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="6beb3-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="6beb3-113">-CertificateType</span></span>
<span data-ttu-id="6beb3-114">用於安全連至 frontendEndpoint 之憑證的類型</span><span class="sxs-lookup"><span data-stu-id="6beb3-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="6beb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb3-115">-DefaultProfile</span></span>
<span data-ttu-id="6beb3-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6beb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beb3-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="6beb3-117">-HostName</span></span>
<span data-ttu-id="6beb3-118">frontendEndpoint 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6beb3-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="6beb3-119">必須是功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="6beb3-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="6beb3-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6beb3-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="6beb3-121">用戶端建立與前門的 SSL 交握所需的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="6beb3-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="6beb3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6beb3-122">-Name</span></span>
<span data-ttu-id="6beb3-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="6beb3-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="6beb3-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="6beb3-124">-ProtocolType</span></span>
<span data-ttu-id="6beb3-125">用於安全傳遞的 TLS 擴充通訊協定</span><span class="sxs-lookup"><span data-stu-id="6beb3-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="6beb3-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="6beb3-126">-SecretName</span></span>
<span data-ttu-id="6beb3-127">代表完整憑證 PFX 之金鑰庫密碼的名稱</span><span class="sxs-lookup"><span data-stu-id="6beb3-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="6beb3-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="6beb3-128">-SecretVersion</span></span>
<span data-ttu-id="6beb3-129">代表完整憑證 PFX 之金鑰庫密碼的版本</span><span class="sxs-lookup"><span data-stu-id="6beb3-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="6beb3-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="6beb3-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="6beb3-131">是否要允許此主機上的會話關聯。</span><span class="sxs-lookup"><span data-stu-id="6beb3-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="6beb3-132">預設值已停用</span><span class="sxs-lookup"><span data-stu-id="6beb3-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6beb3-133">-SessionAffinityTtlIn用</span><span class="sxs-lookup"><span data-stu-id="6beb3-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="6beb3-134">在數秒鐘內用於會話關聯性之 TTL ，如果適用。</span><span class="sxs-lookup"><span data-stu-id="6beb3-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="6beb3-135">預設值為 0</span><span class="sxs-lookup"><span data-stu-id="6beb3-135">Default value is 0</span></span>

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

### <span data-ttu-id="6beb3-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="6beb3-136">-Vault</span></span>
<span data-ttu-id="6beb3-137">包含 SSL 憑證的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="6beb3-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="6beb3-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="6beb3-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="6beb3-139">每個主機適用的 Web 應用程式防火牆 (資源識別碼) </span><span class="sxs-lookup"><span data-stu-id="6beb3-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="6beb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb3-140">CommonParameters</span></span>
<span data-ttu-id="6beb3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6beb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb3-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6beb3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6beb3-143">INPUTS</span></span>

### <span data-ttu-id="6beb3-144">沒有</span><span class="sxs-lookup"><span data-stu-id="6beb3-144">None</span></span>
## <span data-ttu-id="6beb3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6beb3-145">OUTPUTS</span></span>

### <span data-ttu-id="6beb3-146">Microsoft.Azure.Commands.FrontDoor.models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="6beb3-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="6beb3-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6beb3-147">NOTES</span></span>

## <span data-ttu-id="6beb3-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6beb3-148">RELATED LINKS</span></span>

<span data-ttu-id="6beb3-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6beb3-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
