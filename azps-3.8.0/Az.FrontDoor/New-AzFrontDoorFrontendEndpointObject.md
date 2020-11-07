---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797150"
---
# <span data-ttu-id="0a6ec-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0a6ec-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="0a6ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6ec-103">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="0a6ec-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0a6ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a6ec-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6ec-106">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="0a6ec-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0a6ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a6ec-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6ec-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0a6ec-108">Example 1</span></span>
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

<span data-ttu-id="0a6ec-109">建立用來建立前門的 PSFrontendEndpoint 物件。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="0a6ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a6ec-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6ec-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="0a6ec-111">-CertificateSource</span></span>
<span data-ttu-id="0a6ec-112">SSL 憑證的來源</span><span class="sxs-lookup"><span data-stu-id="0a6ec-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="0a6ec-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="0a6ec-113">-CertificateType</span></span>
<span data-ttu-id="0a6ec-114">用於安全連線至 frontendEndpoint 的憑證類型</span><span class="sxs-lookup"><span data-stu-id="0a6ec-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="0a6ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6ec-115">-DefaultProfile</span></span>
<span data-ttu-id="0a6ec-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6ec-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="0a6ec-117">-HostName</span></span>
<span data-ttu-id="0a6ec-118">FrontendEndpoint 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="0a6ec-119">必須是功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="0a6ec-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0a6ec-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="0a6ec-121">用戶端所需的最低 TLS 版本，以使用前門建立 SSL 握手。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="0a6ec-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a6ec-122">-Name</span></span>
<span data-ttu-id="0a6ec-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="0a6ec-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="0a6ec-124">-ProtocolType</span></span>
<span data-ttu-id="0a6ec-125">用於安全傳遞的 TLS 延伸通訊協定</span><span class="sxs-lookup"><span data-stu-id="0a6ec-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="0a6ec-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="0a6ec-126">-SecretName</span></span>
<span data-ttu-id="0a6ec-127">代表完整證書 PFX 的主要保存庫密碼名稱</span><span class="sxs-lookup"><span data-stu-id="0a6ec-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0a6ec-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="0a6ec-128">-SecretVersion</span></span>
<span data-ttu-id="0a6ec-129">代表完整證書 PFX 的主要保存庫密碼版本</span><span class="sxs-lookup"><span data-stu-id="0a6ec-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0a6ec-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="0a6ec-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="0a6ec-131">是否允許在這個主機上進行會話關聯。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="0a6ec-132">已停用預設值</span><span class="sxs-lookup"><span data-stu-id="0a6ec-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="0a6ec-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0a6ec-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="0a6ec-134">要在會話關聯的秒數中使用的 TTL （如果適用的話）。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="0a6ec-135">預設值為0</span><span class="sxs-lookup"><span data-stu-id="0a6ec-135">Default value is 0</span></span>

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

### <span data-ttu-id="0a6ec-136">-保存庫</span><span class="sxs-lookup"><span data-stu-id="0a6ec-136">-Vault</span></span>
<span data-ttu-id="0a6ec-137">包含 SSL 憑證的主要保存庫</span><span class="sxs-lookup"><span data-stu-id="0a6ec-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="0a6ec-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="0a6ec-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="0a6ec-139">每個主機的 Web 應用程式防火牆原則的資源識別碼（如果適用的話） () </span><span class="sxs-lookup"><span data-stu-id="0a6ec-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="0a6ec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6ec-140">CommonParameters</span></span>
<span data-ttu-id="0a6ec-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6ec-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6ec-143">輸入</span><span class="sxs-lookup"><span data-stu-id="0a6ec-143">INPUTS</span></span>

### <span data-ttu-id="0a6ec-144">所有</span><span class="sxs-lookup"><span data-stu-id="0a6ec-144">None</span></span>
## <span data-ttu-id="0a6ec-145">輸出</span><span class="sxs-lookup"><span data-stu-id="0a6ec-145">OUTPUTS</span></span>

### <span data-ttu-id="0a6ec-146">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="0a6ec-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="0a6ec-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0a6ec-147">NOTES</span></span>

## <span data-ttu-id="0a6ec-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a6ec-148">RELATED LINKS</span></span>

<span data-ttu-id="0a6ec-149">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0a6ec-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
