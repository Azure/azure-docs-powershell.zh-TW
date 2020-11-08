---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136393"
---
# <span data-ttu-id="bde2e-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="bde2e-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="bde2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bde2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bde2e-103">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="bde2e-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="bde2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bde2e-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bde2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="bde2e-105">DESCRIPTION</span></span>
<span data-ttu-id="bde2e-106">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="bde2e-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="bde2e-107">示例</span><span class="sxs-lookup"><span data-stu-id="bde2e-107">EXAMPLES</span></span>

### <span data-ttu-id="bde2e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bde2e-108">Example 1</span></span>
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

<span data-ttu-id="bde2e-109">建立用來建立前門的 PSFrontendEndpoint 物件。</span><span class="sxs-lookup"><span data-stu-id="bde2e-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="bde2e-110">參數</span><span class="sxs-lookup"><span data-stu-id="bde2e-110">PARAMETERS</span></span>

### <span data-ttu-id="bde2e-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="bde2e-111">-CertificateSource</span></span>
<span data-ttu-id="bde2e-112">SSL 憑證的來源</span><span class="sxs-lookup"><span data-stu-id="bde2e-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="bde2e-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="bde2e-113">-CertificateType</span></span>
<span data-ttu-id="bde2e-114">用於安全連線至 frontendEndpoint 的憑證類型</span><span class="sxs-lookup"><span data-stu-id="bde2e-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="bde2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde2e-115">-DefaultProfile</span></span>
<span data-ttu-id="bde2e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bde2e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bde2e-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="bde2e-117">-HostName</span></span>
<span data-ttu-id="bde2e-118">FrontendEndpoint 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="bde2e-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="bde2e-119">必須是功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="bde2e-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="bde2e-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bde2e-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="bde2e-121">用戶端所需的最低 TLS 版本，以使用前門建立 SSL 握手。</span><span class="sxs-lookup"><span data-stu-id="bde2e-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="bde2e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bde2e-122">-Name</span></span>
<span data-ttu-id="bde2e-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="bde2e-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="bde2e-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="bde2e-124">-ProtocolType</span></span>
<span data-ttu-id="bde2e-125">用於安全傳遞的 TLS 延伸通訊協定</span><span class="sxs-lookup"><span data-stu-id="bde2e-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="bde2e-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="bde2e-126">-SecretName</span></span>
<span data-ttu-id="bde2e-127">代表完整證書 PFX 的主要保存庫密碼名稱</span><span class="sxs-lookup"><span data-stu-id="bde2e-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="bde2e-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="bde2e-128">-SecretVersion</span></span>
<span data-ttu-id="bde2e-129">代表完整證書 PFX 的主要保存庫密碼版本</span><span class="sxs-lookup"><span data-stu-id="bde2e-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="bde2e-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="bde2e-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="bde2e-131">是否允許在這個主機上進行會話關聯。</span><span class="sxs-lookup"><span data-stu-id="bde2e-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="bde2e-132">已停用預設值</span><span class="sxs-lookup"><span data-stu-id="bde2e-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="bde2e-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="bde2e-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="bde2e-134">要在會話關聯的秒數中使用的 TTL （如果適用的話）。</span><span class="sxs-lookup"><span data-stu-id="bde2e-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="bde2e-135">預設值為0</span><span class="sxs-lookup"><span data-stu-id="bde2e-135">Default value is 0</span></span>

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

### <span data-ttu-id="bde2e-136">-保存庫</span><span class="sxs-lookup"><span data-stu-id="bde2e-136">-Vault</span></span>
<span data-ttu-id="bde2e-137">包含 SSL 憑證的主要保存庫</span><span class="sxs-lookup"><span data-stu-id="bde2e-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="bde2e-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="bde2e-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="bde2e-139">每個主機的 Web 應用程式防火牆原則的資源識別碼（如果適用的話） () </span><span class="sxs-lookup"><span data-stu-id="bde2e-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="bde2e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde2e-140">CommonParameters</span></span>
<span data-ttu-id="bde2e-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bde2e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde2e-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bde2e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde2e-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bde2e-143">INPUTS</span></span>

### <span data-ttu-id="bde2e-144">所有</span><span class="sxs-lookup"><span data-stu-id="bde2e-144">None</span></span>
## <span data-ttu-id="bde2e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="bde2e-145">OUTPUTS</span></span>

### <span data-ttu-id="bde2e-146">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="bde2e-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="bde2e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="bde2e-147">NOTES</span></span>

## <span data-ttu-id="bde2e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="bde2e-148">RELATED LINKS</span></span>

<span data-ttu-id="bde2e-149">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="bde2e-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
